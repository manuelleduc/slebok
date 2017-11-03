## TXL ##

### [![TXL][]][TXL 1] ###

 *  TXL version 10.6d ([download][])
 *  Main website: [txl.ca][TXL 1]
 *  Works with TXL, [XML][]
 *  Wikipedia: ([English][])
 *  Parsing algorithms: [top-down][], [backtracking][]
 *  Example from [txl.ca][]:
    
    > ``````````
    > define program
    >         [compilation_unit]
    > end define
    > 
    > define compilation_unit
    >         [definition_module]
    >     |   [opt 'IMPLEMENTATION] [program_module]
    > end define
    > 
    > define definition_module
    >                                         [NL]
    >         DEFINITION MODULE [id] ;        [NL][NL]
    >                 [repeat import_]
    >                 [repeat definition]
    >         END [id] .                      [NL]
    > end define
    > 
    > define program_module
    >         MODULE [id] [opt priority] ;    [NL][NL]
    >                 [repeat import_]
    >                 [block] [id] .
    > end define
    > ``````````
 *  More examples: [txl.ca][txl.ca 1]
 *  Maintained by James Cordy


[TXL]: 
[TXL 1]: http://www.txl.ca/
[download]: http://www.txl.ca/ndownload.html
[XML]: https://en.wikipedia.org/wiki/XML
[English]: https://en.wikipedia.org/wiki/TXL_%28programming_language%29
[top-down]: https://en.wikipedia.org/wiki/Top-down_parsing
[backtracking]: https://en.wikipedia.org/wiki/Backtracking
[txl.ca]: http://www.txl.ca/examples/Standard/examples.zip
[txl.ca 1]: http://www.txl.ca/nresources.html