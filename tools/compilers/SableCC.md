## SableCC ##

### [![SableCC][]][SableCC 1] ###

 *  SableCC version 3.7 ([download][])
 *  Main website: [sablecc.org][SableCC 1]
 *  Works with [Java][]
 *  Wikipedia: ([English][])
 *  Parsing algorithm: [LALR(1)][LALR_1]
 *  Example from [engr.mun.ca][]:
    
    > ``````````
    > Grammar expression;
    > 
    > Lexer
    > 
    >   num = digit+;
    >   digit = '0'..'9';
    >   blanks = (' ' | eol | tab)+;
    > 
    >   eol = cr | lf | cr lf;
    >   cr = #13;
    >   lf = #10;
    >   tab = #9;
    > 
    > Parser
    > 
    >   Ignored
    >     blanks;
    > 
    >   program =
    >     exp ';';
    > 
    >   exp =
    >     {mul:} exp [op:]'*' exp |
    >     {add:} exp [op:]'+' exp |
    >     {num:} num;
    > 
    >     Precedence
    >       Left mul;
    >       Left add;
    > ``````````
 *  More examples: [@SableCC/sablecc][SableCC_sablecc]
 *  Maintained by Etienne M. Gagnon, Patrick Pelletier, Jean Privat, Jérôme Dassonville and Lucas Satabin


[SableCC]: 
[SableCC 1]: http://www.sablecc.org/
[download]: http://www.sablecc.org/downloads
[Java]: http://101companies.org/wiki/Language:Java
[English]: https://en.wikipedia.org/wiki/SableCC
[LALR_1]: https://en.wikipedia.org/wiki/LALR_parser
[engr.mun.ca]: http://www.engr.mun.ca/~theo/JavaCC-Tutorial/
[SableCC_sablecc]: https://github.com/SableCC/sablecc