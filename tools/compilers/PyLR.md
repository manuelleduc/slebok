## PyLR ##

### PyLR ###

 *  PyLR ([download][])
 *  Main website: [web.archive.org][]
 *  Works with [Python2][]
 *  Parsing algorithm: [LR][]
 *  Example from [web.archive.org][web.archive.org 1]:
    
    > ``````````
    > _class SimpleMathParser
    > _lex mathlex.mathlex()
    > _code from PyLR.Lexers import mathlex
    > """
    > expression: expression PLUS term (addfunc)
    >      |      term;
    > 
    > term: term TIMES factor (timesfunc)
    >   |   factor;
    > 
    > factor: LPAREN expression RPAREN (parenfunc)
    >    |    INT;
    > """
    > ``````````
 *  Maintained by Scott


[download]: http://web.archive.org/web/19991009130507/http://starship.skyport.net/crew/scott/PyLR.tgz
[web.archive.org]: http://web.archive.org/web/19991009130507/http://starship.skyport.net/crew/scott/PyLR.html
[Python2]: https://docs.python.org/2/
[LR]: https://en.wikipedia.org/wiki/LR_parser
[web.archive.org 1]: http://web.archive.org/web/19991012163829/http://starship.skyport.net/crew/scott/manual.html