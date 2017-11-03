## Kleenex ##

### [![Kleenex][]][Kleenex 1] ###

 *  Kleenex ([download][])
 *  Main website: [kleenexlang.org][Kleenex 1]
 *  Works with [C][]
 *  Parsing algorithm: [FST][]
 *  Example from [@diku-kmc/kleenexlang][diku-kmc_kleenexlang]:
    
    > ``````````
    > main := (num /[^0-9]/ | other)*
    > num := digit{1,3} ("," digit{3})*
    > digit := /[0-9]/
    > other := /./
    > ``````````
 *  Maintained by Niels Bjørn Bugge Grathwohl, Fritz Henglein, Ulrik Terp Rasmussen, Kristoffer Aalund Søholm, Sebastian Paaske Tørholm


[Kleenex]: 
[Kleenex 1]: http://kleenexlang.org/
[download]: http://www.antlr.org/download.html
[C]: http://101companies.org/wiki/Language:C
[FST]: https://en.wikipedia.org/wiki/Finite-state_transducer
[diku-kmc_kleenexlang]: https://github.com/diku-kmc/kleenexlang