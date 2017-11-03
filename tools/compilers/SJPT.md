## SJPT ##

### Simple Java Parsing Toolkit ###

 *  SJPT version 0.10 ([download][])
 *  Main website: [sjpt.sourceforge.net][]
 *  Works with [Java][]
 *  Parsing algorithms: [LL(1)][LL_1], [LR(0)][LR_0], [SLR(1)][SLR_1], [LR(1)][LR_0], [LALR(1)][LALR_1]
 *  Example from [prdownloads.sourceforge.net][]:
    
    > ``````````
    > import ro.infoiasi.donald.compiler.parser0.runtime.*;
    > 
    > terminal SEMI, PLUS, MINUS, TIMES, DIVIDE, LPAREN, RPAREN;
    > terminal Integer NUMBER, ID;
    > 
    > non terminal Object expr_list, expr_part;
    > non terminal Integer expr, factor, term;
    > 
    > expr_list ::= expr_list expr_part
    >             | expr_part;
    > 
    > expr_part ::= expr:e {: System.out.println(" = " + e); :} SEMI;
    > 
    > expr      ::= factor:f PLUS expr:e {: RESULT = new Integer(f.intValue() + e.intValue()); :}
    >             | factor:f MINUS expr:e {: RESULT = new Integer(f.intValue() - e.intValue()); :}
    >             | factor:f {: RESULT = new Integer(f.intValue()); :};
    > 
    > factor    ::= factor:f TIMES term:t {: RESULT = new Integer(f.intValue() * t.intValue()); :}
    >             | factor:f DIVIDE term:t {: RESULT = new Integer(f.intValue() / t.intValue()); :}
    >             | term:t {: RESULT = new Integer(t.intValue()); :};
    > 
    > 
    > term      ::= LPAREN expr:e RPAREN {: RESULT = e; :}
    >             | NUMBER:n {: RESULT = n; :}
    >             | ID:i {: RESULT = i; :};
    > ``````````
 *  Maintained by Catalin Hritcu


[download]: http://sjpt.sourceforge.net/download/index.html
[sjpt.sourceforge.net]: http://sjpt.sourceforge.net/
[Java]: http://101companies.org/wiki/Language:Java
[LL_1]: https://en.wikipedia.org/wiki/LL_parser
[LR_0]: https://en.wikipedia.org/wiki/LR_parser
[SLR_1]: https://en.wikipedia.org/wiki/Simple_LR_parser
[LALR_1]: https://en.wikipedia.org/wiki/LALR_parser
[prdownloads.sourceforge.net]: http://prdownloads.sourceforge.net/sjpt/sjpt-0.10.zip?download