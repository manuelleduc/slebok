## SimpleParse ##

### SimpleParse ###

 *  SimpleParse version 2.1.0a1 ([download][])
 *  Main website: [simpleparse.sourceforge.net][]
 *  Works with [Python2][]
 *  Parsing algorithms: [top-down][], [one-pass][]
 *  Example from [simpleparse.sourceforge.net][simpleparse.sourceforge.net 1]:
    
    > ``````````
    > declaration = r'''# note use of raw string when embedding in python code...
    > file           :=  [ \t\n]*, section+
    > section        :=  '[', identifier!, ']'!, ts, '\n', body
    > body           :=  statement*
    > statement      :=  (ts, semicolon_comment) / equality / nullline
    > nullline       :=  ts, '\n'
    > comment        :=  -'\n'*
    > equality       :=  ts, identifier, ts, '=', ts, identified, ts, '\n'
    > identifier     :=  [a-zA-Z], [a-zA-Z0-9_]*
    > identified     :=  string / number / identifier
    > ts             :=  [ \t]*
    > '''
    > ``````````
 *  Maintained by Mike C. Fletcher


[download]: http://www.antlr.org/download.html
[simpleparse.sourceforge.net]: http://simpleparse.sourceforge.net/
[Python2]: https://docs.python.org/2/
[top-down]: https://en.wikipedia.org/wiki/Top-down_parsing
[one-pass]: https://en.wikipedia.org/wiki/One-pass_compiler
[simpleparse.sourceforge.net 1]: http://simpleparse.sourceforge.net/simpleparse_grammars.html