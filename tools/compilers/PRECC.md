## PRECC ##

### [![PREttier Compiler-Compiler][]][PREttier Compiler-Compiler 1] PREttier Compiler-Compiler ###

 *  PRECC version 2.60 ([download][])
 *  Main website: [preccx.sourceforge.net][PREttier Compiler-Compiler 1]
 *  Works with [C][]
 *  Parsing algorithm: [LL(k)][LL_k]
 *  Example from [preccx.sourceforge.net][]:
    
    > ``````````
    > integer = [ <'+'>|<'-'> ]
    >           unsigned_int
    >           [ {<'E'>|<'e'>} [<'+'>] unsigned_int ]
    > 
    > unsigned_int = (isdigit)+
    > ``````````
 *  Maintained by Peter Breuer and Jonathan Bowen


[PREttier Compiler-Compiler]: 
[PREttier Compiler-Compiler 1]: http://preccx.sourceforge.net/
[download]: ftp://oboe.it.uc3m.es/pub/Programs/
[C]: http://101companies.org/wiki/Language:C
[LL_k]: https://en.wikipedia.org/wiki/LL_parser
[preccx.sourceforge.net]: http://preccx.sourceforge.net/archive/redo/precc/user-manual.html