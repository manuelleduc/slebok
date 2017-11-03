## Bison ##

### [![Bison][]][Bison 1] ###

 *  Bison version 3.0.4 ([download][])
 *  Main website: [gnu.org][Bison 1]
 *  Works with [C][], [C++][C 1], [Java][]
 *  Wikipedia: ([English][]) ([French][]) ([German][]) ([Russian][])
 *  Parsing algorithms: [LALR(1)][LALR_1], [GLR][]
 *  Example from [gnu.org][]:
    
    > ``````````
    > %token TYPE DOTDOT ID
    > 
    > %left '+' '-'
    > %left '*' '/'
    > 
    > %%
    > type_decl: TYPE ID '=' type ';' ;
    > 
    > type: '(' id_list ')'
    >     | expr DOTDOT expr;
    > id_list: ID
    >        | id_list ',' ID;
    > expr: '(' expr ')'
    >     | expr '+' expr
    >     | expr '-' expr
    >     | expr '*' expr
    >     | expr '/' expr
    >     | ID;
    > ``````````
 *  More examples: [gnu.org][]
 *  Maintained by Akim Demaille and Paul Eggert
 *  Used with:
    
     *  [flex][] ([English][English 1]) ([French][French 1]) ([Russian][Russian 1])


[Bison]: 
[Bison 1]: https://www.gnu.org/software/bison/
[download]: http://ftp.gnu.org/gnu/bison/
[C]: http://101companies.org/wiki/Language:C
[C 1]: http://101companies.org/wiki/Language:CPlusPlus
[Java]: http://101companies.org/wiki/Language:Java
[English]: https://en.wikipedia.org/wiki/GNU%20bison
[French]: https://fr.wikipedia.org/wiki/GNU%20Bison
[German]: https://de.wikipedia.org/wiki/GNU%20Bison
[Russian]: https://ru.wikipedia.org/wiki/GNU%20Bison
[LALR_1]: https://en.wikipedia.org/wiki/LALR_parser
[GLR]: https://en.wikipedia.org/wiki/GLR_parser
[gnu.org]: https://www.gnu.org/software/bison/manual/bison.html
[flex]: https://github.com/westes/flex
[English 1]: https://en.wikipedia.org/wiki/Flex_%28lexical_analyser_generator%29
[French 1]: https://fr.wikipedia.org/wiki/Flex_%28logiciel%29
[Russian 1]: https://ru.wikipedia.org/wiki/Flex_%28%D0%B3%D0%B5%D0%BD%D0%B5%D1%80%D0%B0%D1%82%D0%BE%D1%80_%D0%BB%D0%B5%D0%BA%D1%81%D0%B8%D1%87%D0%B5%D1%81%D0%BA%D0%B8%D1%85_%D0%B0%D0%BD%D0%B0%D0%BB%D0%B8%D0%B7%D0%B0%D1%82%D0%BE%D1%80%D0%BE%D0%B2%29