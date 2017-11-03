## Coco/R ##

### Coco/R ###

 *  Coco/R ([download][])
 *  Main website: [ssw.jku.at][download]
 *  Works with [C\#][C], [Java][], [C++][C 1], [F\#][F], [VB.NET][], [Swift][], [Oberon][]
 *  Wikipedia: ([English][]) ([German][]) ([Russian][])
 *  Parsing algorithms: [recursive descent][], [AG][], [LL(k)][LL_k]
 *  Example from [ssw.jku.at][]:
    
    > ``````````
    > COMPILER Sample
    > 
    > CHARACTERS
    >   digit = '0'..'9'.
    > TOKENS
    >   number = digit {digit}.
    > IGNORE '\r' + '\n'
    > 
    > PRODUCTIONS
    >   Sample                     (. int n; .)
    >   = {
    >       "calc"
    >       Expr<out n>            (. Console.WriteLine(n); .)
    >     }.
    > 
    >   Expr<out int n>            (. int n1; .)
    >   = Term<out n>
    >     {
    >       '+'
    >       Term<out n1>           (. n = n + n1; .)
    >     }.
    > 
    >   Term<out int n>
    >   = number                   (. n = Convert.Int32(t.val); .)
    >   .
    > END Sample.
    > ``````````
 *  More examples: [ssw.jku.at][ssw.jku.at 1]
 *  Maintained by Hanspeter Mössenböck, Markus Löberbauer and Albrecht Wöß
 *  Built on top of Coco/R:
    
     *  [Coco/Ruby][Coco_Ruby]
     *  [CocoPy][]
     *  [CocoXml][]
     *  [DCocoR][]
     *  [ParserBuilder][]
     *  [cocor\_ada][cocor_ada]


[download]: http://ssw.jku.at/Coco/
[C]: http://101companies.org/wiki/Language:CSharp
[Java]: http://101companies.org/wiki/Language:Java
[C 1]: http://101companies.org/wiki/Language:CPlusPlus
[F]: https://en.wikipedia.org/wiki/F_Sharp_%28programming_language%29
[VB.NET]: https://en.wikipedia.org/wiki/Visual_Basic_.NET
[Swift]: https://en.wikipedia.org/wiki/Swift_%28programming_language%29
[Oberon]: https://en.wikipedia.org/wiki/Oberon_%28programming_language%29
[English]: https://en.wikipedia.org/wiki/Coco/R
[German]: https://de.wikipedia.org/wiki/Coco/R
[Russian]: https://ru.wikipedia.org/wiki/Coco/R
[recursive descent]: https://en.wikipedia.org/wiki/Recursive_descent_parser
[AG]: https://en.wikipedia.org/wiki/Attribute_grammar
[LL_k]: https://en.wikipedia.org/wiki/LL_parser
[ssw.jku.at]: http://ssw.jku.at/Coco/Tutorial/
[ssw.jku.at 1]: http://ssw.jku.at/Coco/Cookbook/
[Coco_Ruby]: http://www.zenspider.com/projects/cocor.html
[CocoPy]: https://pypi.python.org/pypi/CocoPy/
[CocoXml]: https://code.google.com/archive/p/cocoxml/
[DCocoR]: https://github.com/VilleKrumlinde/dcocor
[ParserBuilder]: https://sourceforge.net/projects/parserbuilder/
[cocor_ada]: http://www.ada-ru.org/files/cocor_ada-1.53.1.tar.gz