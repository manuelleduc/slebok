## byacc ##

### Berkeley Yacc ###

 *  byacc version 1.9 ([download][])
 *  Main website: [invisible-island.net][]
 *  Works with [C][]
 *  Wikipedia: ([English][])
 *  Parsing algorithm: [LALR][]
 *  Example from [dinosaur.compilertools.net][]:
    
    > ``````````
    > %left  '+'  '-'
    > %left  '*'  '/'
    > 
    > %%
    > 
    > expr    :       expr  '+'  expr
    >         |       expr  '-'  expr
    >         |       expr  '*'  expr
    >         |       expr  '/'  expr
    >         |       '-'  expr      %prec  '*'
    >         |       NAME
    >         ;
    > ``````````
 *  Maintained by Robert Corbett
 *  Used with:
    
     *  [flex][] ([English][English 1]) ([French][]) ([Russian][])
     *  [lex][] ([English][English 2]) ([French][French 1]) ([Dutch][]) ([Russian][Russian 1])


[download]: ftp://ftp.cs.berkeley.edu/pub/4bsd/byacc.1.9.tar.Z
[invisible-island.net]: http://invisible-island.net/byacc/byacc.html
[C]: http://101companies.org/wiki/Language:C
[English]: https://en.wikipedia.org/wiki/Berkeley%20Yacc
[LALR]: https://en.wikipedia.org/wiki/LALR_parser
[dinosaur.compilertools.net]: http://dinosaur.compilertools.net/yacc/index.html
[flex]: https://github.com/westes/flex
[English 1]: https://en.wikipedia.org/wiki/Flex_%28lexical_analyser_generator%29
[French]: https://fr.wikipedia.org/wiki/Flex_%28logiciel%29
[Russian]: https://ru.wikipedia.org/wiki/Flex_%28%D0%B3%D0%B5%D0%BD%D0%B5%D1%80%D0%B0%D1%82%D0%BE%D1%80_%D0%BB%D0%B5%D0%BA%D1%81%D0%B8%D1%87%D0%B5%D1%81%D0%BA%D0%B8%D1%85_%D0%B0%D0%BD%D0%B0%D0%BB%D0%B8%D0%B7%D0%B0%D1%82%D0%BE%D1%80%D0%BE%D0%B2%29
[lex]: http://dinosaur.compilertools.net/#lex
[English 2]: https://en.wikipedia.org/wiki/Lex_%28software%29
[French 1]: https://fr.wikipedia.org/wiki/Lex_%28logiciel%29
[Dutch]: https://nl.wikipedia.org/wiki/Lex_%28computerprogramma%29
[Russian 1]: https://ru.wikipedia.org/wiki/Lex