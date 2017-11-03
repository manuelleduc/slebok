## Happy ##

### [![Happy][]][Happy 1] ###

 *  Happy version 1.18.5 ([download][])
 *  Main website: [haskell.org][Happy 1]
 *  Works with [Haskell][]
 *  Parsing algorithm: [GLR][]
 *  Example from [haskell.org][]:
    
    > ``````````
    > Exp   : let var '=' Exp in Exp  { Let $2 $4 $6 }
    >       | Exp1                    { Exp1 $1 }
    > 
    > Exp1  : Exp1 '+' Term           { Plus $1 $3 }
    >       | Exp1 '-' Term           { Minus $1 $3 }
    >       | Term                    { Term $1 }
    > 
    > Term  : Term '*' Factor         { Times $1 $3 }
    >       | Term '/' Factor         { Div $1 $3 }
    >       | Factor                  { Factor $1 }
    > 
    > Factor
    >       : int                     { Int $1 }
    >       | var                     { Var $1 }
    >       | '(' Exp ')'             { Brack $2 }
    > ``````````
 *  More examples: [haskell.org][haskell.org 1]
 *  Maintained by Andy Gill and Simon Marlow
 *  Used with:
    
     *  [Alex][]


[Happy]: 
[Happy 1]: https://www.haskell.org/happy/
[download]: https://www.haskell.org/happy/#download
[Haskell]: http://101companies.org/wiki/Language:Haskell
[GLR]: https://en.wikipedia.org/wiki/GLR_parser
[haskell.org]: https://www.haskell.org/happy/doc/html/sec-using.html
[haskell.org 1]: https://www.haskell.org/happy/doc/html/index.html
[Alex]: https://www.haskell.org/alex/