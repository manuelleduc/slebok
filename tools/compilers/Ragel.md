## Ragel ##

### Ragel ###

 *  Ragel version 7.0.0.9 ([download][])
 *  Main website: [colm.net][]
 *  Works with [C][], [C++][C 1], [Intel Asm][], [Obj-C][], [D][], [Go][], [Ruby][], [Java][]
 *  Wikipedia: ([English][]) ([French][]) ([German][]) ([Russian][])
 *  Parsing algorithm: [FSM][]
 *  Example from [colm.net][]:
    
    > ``````````
    > action dgt      { printf("DGT: %c\n", fc); }
    > action dec      { printf("DEC: .\n"); }
    > action exp      { printf("EXP: %c\n", fc); }
    > action exp_sign { printf("SGN: %c\n", fc); }
    > action number   { /*NUMBER*/ }
    > 
    > number = (
    >     [0-9]+ $dgt ( '.' @dec [0-9]+ $dgt )?
    >     ( [eE] ( [+\-] $exp_sign )? [0-9]+ $exp )?
    > ) %number;
    > 
    > main := ( number '\n' )*;
    > ``````````
 *  Maintained by Adrian D. Thurston
 *  Built on top of Ragel:
    
     *  [Colm][]


[download]: http://www.colm.net/files/ragel/ragel-7.0.0.9.tar.gz
[colm.net]: http://www.colm.net/open-source/ragel/
[C]: http://101companies.org/wiki/Language:C
[C 1]: http://101companies.org/wiki/Language:CPlusPlus
[Intel Asm]: https://en.wikipedia.org/wiki/x86_assembly_language
[Obj-C]: https://en.wikipedia.org/wiki/Objective-C
[D]: https://en.wikipedia.org/wiki/D_%28programming_language%29
[Go]: https://en.wikipedia.org/wiki/Go_%28programming_language%29
[Ruby]: https://en.wikipedia.org/wiki/Ruby_%28programming_language%29
[Java]: http://101companies.org/wiki/Language:Java
[English]: https://en.wikipedia.org/wiki/Ragel
[French]: https://fr.wikipedia.org/wiki/Ragel
[German]: https://de.wikipedia.org/wiki/Ragel
[Russian]: https://ru.wikipedia.org/wiki/Ragel
[FSM]: https://en.wikipedia.org/wiki/Finite-state_machine
[Colm]: http://www.colm.net/open-source/colm/