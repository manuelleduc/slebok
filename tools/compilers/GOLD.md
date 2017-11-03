## GOLD ##

### [![GOLD Parsing System][]][GOLD Parsing System 1] GOLD Parsing System ###

 *  GOLD version 5 ([download][])
 *  Main website: [goldparser.org][GOLD Parsing System 1]
 *  Works with [Intel Asm][], [C][], [C\#][C 1], [D][], [Delphi][], [Java][], [Pascal][], [Python3][], [VB][], [VB.NET][], [C++][C 2]
 *  Wikipedia: ([English][]) ([German][])
 *  Parsing algorithms: [LALR][], [DFA][]
 *  Example from [goldparser.org][]:
    
    > ``````````
    > Id = {Letter}{AlphaNumeric}*
    > 
    > <Statement> ::= if Id then <Statement>
    >               | if Id then <Then Stm> else <Statement>
    >               | Id ':=' Id
    > 
    > <Then Stm>  ::= if Id then <Then Stm> else <Then Stm>
    >               | Id ':=' Id
    > ``````````
 *  More examples: [goldparser.org][], [goldparser.org][goldparser.org 1]
 *  Devin Cook [and others][]
 *  Built on top of GOLD:
    
     *  [C++ Gold Parser Engine][C_ Gold Parser Engine]
     *  [Calitha][]
     *  [PyGold][]
     *  [goldengine for Java][]


[GOLD Parsing System]: 
[GOLD Parsing System 1]: http://www.goldparser.org/
[download]: http://www.goldparser.org/engine/index.htm
[Intel Asm]: https://en.wikipedia.org/wiki/x86_assembly_language
[C]: http://101companies.org/wiki/Language:C
[C 1]: http://101companies.org/wiki/Language:CSharp
[D]: https://en.wikipedia.org/wiki/D_%28programming_language%29
[Delphi]: https://en.wikipedia.org/wiki/Delphi_%28programming_language%29
[Java]: http://101companies.org/wiki/Language:Java
[Pascal]: https://en.wikipedia.org/wiki/Pascal_%28programming_language%29
[Python3]: https://docs.python.org/3/
[VB]: https://en.wikipedia.org/wiki/Visual_Basic
[VB.NET]: https://en.wikipedia.org/wiki/Visual_Basic_.NET
[C 2]: http://101companies.org/wiki/Language:CPlusPlus
[English]: https://en.wikipedia.org/wiki/GOLD%20%28parser%29
[German]: https://de.wikipedia.org/wiki/GOLD%20Parsing%20System
[LALR]: https://en.wikipedia.org/wiki/LALR_parser
[DFA]: https://en.wikipedia.org/wiki/Deterministic_finite_automaton
[goldparser.org]: http://www.goldparser.org/doc/grammars/index.htm
[goldparser.org 1]: http://www.goldparser.org/grammars/index.htm
[and others]: http://goldparser.org/contributors/
[C_ Gold Parser Engine]: https://sourceforge.net/projects/cpp-gpengine/
[Calitha]: http://www.calitha.com/
[PyGold]: https://sourceforge.net/projects/pygold/
[goldengine for Java]: https://github.com/ridencww/goldengine