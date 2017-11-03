## BtYacc ##

### BtYacc ###

 *  BtYacc version 3.0 ([download][])
 *  Main website: [siber.com][download]
 *  Works with [C++][C]
 *  Parsing algorithms: [backtracking][], [bottom-up][]
 *  Example from [siber.com][]:
    
    > ``````````
    > %left LO '+' '-'
    > %left HI '*' '/' '%'
    > %nonassoc UNARY
    > 
    > %%
    > 
    > expr: expr op1 expr %prec LO
    >     | expr op2 expr %prec HI
    >     | unary expr %prec UNARY
    >     ;
    > 
    > op1 : '+'
    >     | '-'
    >     ;
    > 
    > op2 : '*'
    >     | '/'
    >     | '%'
    >     ;
    > 
    > unary : '+' | '-' | '*' | '&' ;
    > ``````````
 *  Maintained by Chris Dodd and Vadim Maslov


[download]: http://www.siber.com/btyacc/
[C]: http://101companies.org/wiki/Language:CPlusPlus
[backtracking]: https://en.wikipedia.org/wiki/Backtracking
[bottom-up]: https://en.wikipedia.org/wiki/Bottom-up_parsing
[siber.com]: http://www.siber.com/btyacc/btyacc-3-0.zip