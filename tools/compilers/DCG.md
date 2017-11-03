## DCG ##

### Definite Clause Grammars ###

 *  SWI Prolog version 7.2.3 ([download][])
 *  Main website: [swi-prolog.org][]
 *  Works with [Prolog][]
 *  Wikipedia: ([English][]) ([Russian][])
 *  Parsing algorithm: [DCG][]
 *  Example from [@grammarware/slps][grammarware_slps]:
    
    > ``````````
    > expr(E) --> lassoc(ops,atom,binary,E).
    > 
    > expr(apply(N,Es)) -->
    > 	name(N),
    > 	+(atom,Es).
    > 
    > expr(ifThenElse(E1,E2,E3)) -->
    > 	reserved("if"),
    > 	expr(E1),
    > 	reserved("then"),
    > 	expr(E2),
    > 	reserved("else"),
    > 	expr(E3).
    > ``````````
 *  More examples: [pathwayslms.com][]
 *  [DCG contributors][]


[download]: http://www.swi-prolog.org/download/stable
[swi-prolog.org]: http://www.swi-prolog.org/
[Prolog]: http://101companies.org/wiki/Language:Prolog
[English]: https://en.wikipedia.org/wiki/Definite%20clause%20grammar
[Russian]: https://ru.wikipedia.org/wiki/DC-%D0%B3%D1%80%D0%B0%D0%BC%D0%BC%D0%B0%D1%82%D0%B8%D0%BA%D0%B0
[DCG]: https://pdfs.semanticscholar.org/fbc0/4a1951003ba164303b2898fb7f3c6b4e9083.pdf
[grammarware_slps]: https://github.com/grammarware/slps/blob/master/topics/fl/prolog1/Parser.pro
[pathwayslms.com]: http://www.pathwayslms.com/swipltuts/dcg/
[DCG contributors]: http://www.swi-prolog.org/Contributors.html