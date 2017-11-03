## Parsec ##

### [![Parsec][]][Parsec 1] ###

 *  Parsec version 3.1.11 ([download][])
 *  Main website: [wiki.haskell.org][Parsec 1]
 *  Works with [Haskell][], [F\#][F], [Java][], [JavaScript][], [Erlang][]
 *  Wikipedia: ([English][])
 *  Parsing algorithms: [monadic][], [recursive descent][]
 *  Example from [web.archive.org][]:
    
    > ``````````
    > import ParsecExpr
    > 
    > expr    :: Parser Integer
    > expr    = buildExpressionParser table factor
    >         <?> "expression"
    > 
    > table   = [[op "*" (*) AssocLeft, op "/" div AssocLeft]
    >           ,[op "+" (+) AssocLeft, op "-" (-) AssocLeft]
    >           ]
    >         where
    >           op s f assoc
    >              = Infix (do{ string s; return f}) assoc
    > 
    > factor  = do{ char '('
    >             ; x <- expr
    >             ; char ')'
    >             ; return x
    >             }
    >         <|> number
    >         <?> "simple expression"
    > 
    > number  :: Parser Integer
    > number  = do{ ds <- many1 digit
    >             ; return (read ds)
    >             }
    >         <?> "number"
    > ``````````
 *  Maintained by Antoine Latter
 *  Built on top of Parsec:
    
     *  [Bennu][]
     *  [FParsec][]
     *  [Parsec-Erlang][]
     *  [ParsecJ][]
     *  [XParsec][]
     *  [jsparsec][]


[Parsec]: 
[Parsec 1]: https://wiki.haskell.org/Parsec
[download]: http://hackage.haskell.org/package/parsec
[Haskell]: http://101companies.org/wiki/Language:Haskell
[F]: https://en.wikipedia.org/wiki/F_Sharp_%28programming_language%29
[Java]: http://101companies.org/wiki/Language:Java
[JavaScript]: http://101companies.org/wiki/Language:JavaScript
[Erlang]: https://en.wikipedia.org/wiki/Erlang_%28programming_language%29
[English]: https://en.wikipedia.org/wiki/Parsec%20%28parser%29
[monadic]: http://www.cs.nott.ac.uk/~pszgmh/monparsing.pdf
[recursive descent]: https://en.wikipedia.org/wiki/Recursive_descent_parser
[web.archive.org]: https://web.archive.org/web/20140529211116/http://legacy.cs.uu.nl/daan/download/parsec/parsec.html
[Bennu]: https://github.com/mattbierner/bennu/
[FParsec]: http://www.quanttec.com/fparsec/
[Parsec-Erlang]: https://bitbucket.org/dmercer/parsec-erlang/
[ParsecJ]: https://github.com/jon-hanson/parsecj/
[XParsec]: http://xparsec.corsis.tech/
[jsparsec]: https://github.com/balazs-endresz/jsparsec