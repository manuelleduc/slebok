## Beaver ##

### [![Beaver][]][Beaver 1] ###

 *  Beaver version 0.9.11 ([download][])
 *  Main website: [beaver.sourceforge.net][Beaver 1]
 *  Works with [Java][]
 *  Parsing algorithm: [LALR(1)][LALR_1]
 *  Example from [beaver.sourceforge.net][]:
    
    > ``````````
    > %%
    > 
    > %left RPAREN;
    > %left MULT, DIV;
    > %left PLUS, MINUS;
    > 
    > %typeof NUMBER = "Number";
    > %typeof expr = "Expr";
    > 
    > %%
    > 
    > expr = expr.a MULT  expr.b   {: return new Expr(a.value * b.value); :}
    >      | expr.a DIV   expr.b   {: return new Expr(a.value / b.value); :}
    >      | expr.a PLUS  expr.b   {: return new Expr(a.value + b.value); :}
    >      | expr.a MINUS expr.b   {: return new Expr(a.value - b.value); :}
    >      | NUMBER.n              {: return new Expr(n.doubleValue());   :}
    >      | LPAREN expr.e RPAREN  {: return e; :}
    >      ;
    > ``````````
 *  More examples: [beaver.sourceforge.net][Beaver 1]
 *  Used with:
    
     *  [JLex][]
     *  [JFlex][]


[Beaver]: 
[Beaver 1]: http://beaver.sourceforge.net/
[download]: https://sourceforge.net/projects/beaver/files/
[Java]: http://101companies.org/wiki/Language:Java
[LALR_1]: https://en.wikipedia.org/wiki/LALR_parser
[beaver.sourceforge.net]: http://beaver.sourceforge.net/spec.html
[JLex]: https://www.cs.princeton.edu/~appel/modern/java/JLex/
[JFlex]: http://www.jflex.de/