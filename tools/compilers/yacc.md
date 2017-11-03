## yacc ##

### Yet Another Compiler-compiler ###

 *  yacc
 *  Main website: [dinosaur.compilertools.net][]
 *  Works with [C][]
 *  Wikipedia: ([English][]) ([Dutch][]) ([French][]) ([German][]) ([Russian][])
 *  Parsing algorithm: [LALR][]
 *  Example from [dinosaur.compilertools.net][dinosaur.compilertools.net 1]:
    
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
 *  Maintained by Stephen C. Johnson
 *  Used with:
    
     *  [lex][] ([English][English 1]) ([French][French 1]) ([Dutch][Dutch 1]) ([Russian][Russian 1])


[dinosaur.compilertools.net]: http://dinosaur.compilertools.net/#yacc
[C]: http://101companies.org/wiki/Language:C
[English]: https://en.wikipedia.org/wiki/Yacc
[Dutch]: https://nl.wikipedia.org/wiki/Yacc
[French]: https://fr.wikipedia.org/wiki/Yacc%20%28logiciel%29
[German]: https://de.wikipedia.org/wiki/Yacc
[Russian]: https://ru.wikipedia.org/wiki/Yacc
[LALR]: https://en.wikipedia.org/wiki/LALR_parser
[dinosaur.compilertools.net 1]: http://dinosaur.compilertools.net/yacc/index.html
[lex]: http://dinosaur.compilertools.net/#lex
[English 1]: https://en.wikipedia.org/wiki/Lex_%28software%29
[French 1]: https://fr.wikipedia.org/wiki/Lex_%28logiciel%29
[Dutch 1]: https://nl.wikipedia.org/wiki/Lex_%28computerprogramma%29
[Russian 1]: https://ru.wikipedia.org/wiki/Lex