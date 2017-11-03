## Frown ##

### [![Frown][]][Frown 1] ###

 *  Frown version 0.6.1 ([download][])
 *  Main website: [cs.ox.ac.uk][Frown 1]
 *  Works with [Haskell][]
 *  Parsing algorithm: [LALR(k)][LALR_k]
 *  Example from [cs.ox.ac.uk][Frown 1]:
    
    > ``````````
    > import Char
    > 
    > data Expr  =  Ident  Char
    >            |  Apply  Expr Expr
    >               deriving (Show)
    > 
    > type Terminal  =  Char
    > 
    > %{
    > 
    > Terminal  =  guard {isAlpha} as "letter"
    >           |  '('
    >           |  ')';
    > 
    > Nonterminal  =  expr {Expr};
    > 
    > expr  {Ident x}    :  "letter" {x};
    >       {Apply t u}  |  expr {t}, '(', expr {u}, ')';
    > 
    > }%
    > 
    > frown ts  =  fail "syntax error"
    > ``````````
 *  Maintained by Ralf Hinze and Arjan Oosting
 *  Built on top of Frown:
    
     *  [frown 0.6.1-6][]


[Frown]: 
[Frown 1]: http://www.cs.ox.ac.uk/ralf.hinze/frown/
[download]: http://www.cs.ox.ac.uk/ralf.hinze/frown/frown-0.6.1.tar.gz
[Haskell]: http://101companies.org/wiki/Language:Haskell
[LALR_k]: https://en.wikipedia.org/wiki/LALR_parser
[frown 0.6.1-6]: https://launchpad.net/ubuntu/+source/frown/0.6.1-6