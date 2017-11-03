## pyparsing ##

### pyparsing ###

 *  pyparsing version 2.1.10 ([download][])
 *  Main website: [pyparsing.wikispaces.com][]
 *  Works with [Python2][], [Python3][]
 *  Parsing algorithms: [scannerless][], [recursive descent][]
 *  Example from [pyparsing.wikispaces.com][]:
    
    > ``````````
    > from pyparsing import Word, alphas
    > greet = Word( alphas ) + "," + Word( alphas ) + "!"
    > hello = "Hello, World!"
    > print (hello, "->", greet.parseString( hello ))
    > ``````````
 *  More examples: [pyparsing.wikispaces.com][pyparsing.wikispaces.com 1]
 *  Maintained by Paul McGuire


[download]: https://sourceforge.net/projects/pyparsing/
[pyparsing.wikispaces.com]: http://pyparsing.wikispaces.com/
[Python2]: https://docs.python.org/2/
[Python3]: https://docs.python.org/3/
[scannerless]: https://en.wikipedia.org/wiki/Scannerless_parsing
[recursive descent]: https://en.wikipedia.org/wiki/Recursive_descent_parser
[pyparsing.wikispaces.com 1]: http://pyparsing.wikispaces.com/Examples