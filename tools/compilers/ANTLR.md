## ANTLR ##

### [![ANTLR][]][ANTLR 1] ###

 *  ANTLR version 4 ([download][])
 *  Main website: [antlr.org][ANTLR 1]
 *  Works with [Java][], [C\#][C], [JavaScript][], [Python2][], [Python3][]
 *  Wikipedia: ([English][]) ([Dutch][]) ([French][]) ([German][]) ([Russian][])
 *  Parsing algorithm: [ALL(\*)][ALL]
 *  Example from [antlr.org][ANTLR 1]:
    
    > ``````````
    > grammar Expr;
    > prog: (expr NEWLINE)* ;
    > expr: expr ('*'|'/') expr
    >     | expr ('+'|'-') expr
    >     | INT
    >     | '(' expr ')'
    >     ;
    > NEWLINE : [\r\n]+ ;
    > INT     : [0-9]+ ;
    > ``````````
 *  More examples: [pragprog.com][]
 *  Maintained by Terence Parr
 *  Built on top of ANTLR:
    
     *  [EMFText][]
     *  [Xtext][]


[ANTLR]: 
[ANTLR 1]: http://www.antlr.org/
[download]: http://www.antlr.org/download.html
[Java]: http://101companies.org/wiki/Language:Java
[C]: http://101companies.org/wiki/Language:CSharp
[JavaScript]: http://101companies.org/wiki/Language:JavaScript
[Python2]: https://docs.python.org/2/
[Python3]: https://docs.python.org/3/
[English]: https://en.wikipedia.org/wiki/ANTLR
[Dutch]: https://nl.wikipedia.org/wiki/ANTLR
[French]: https://fr.wikipedia.org/wiki/ANTLR
[German]: https://de.wikipedia.org/wiki/ANTLR
[Russian]: https://ru.wikipedia.org/wiki/ANTLR
[ALL]: http://www.antlr.org/papers/allstar-techreport.pdf
[pragprog.com]: https://pragprog.com/titles/tpantlr2/source_code
[EMFText]: http://www.emftext.org/index.php/EMFText
[Xtext]: http://www.eclipse.org/Xtext/