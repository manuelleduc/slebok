## ParseLib ##

### ParseLib ###

 *  ParseLib version 2015.1.1 ([download][])
 *  Main website: [hackage.haskell.org][]
 *  Works with [Haskell][]
 *  Parsing algorithm: [monadic][]
 *  Example from [haskell.org][]:
    
    > ``````````
    > exprparser :: Parser Expr
    > exprparser = buildExpressionParser table term <?> "expression"
    > table = [ [Prefix (m_reservedOp "~" >> return (Uno Not))]
    >         , [Infix (m_reservedOp "&" >> return (Duo And)) AssocLeft]
    >         , [Infix (m_reservedOp "=" >> return (Duo Iff)) AssocLeft]
    >         ]
    > term = m_parens exprparser
    >        <|> fmap Var m_identifier
    >        <|> (m_reserved "true" >> return (Con True))
    >        <|> (m_reserved "false" >> return (Con False))
    > ``````````
 *  Maintained by Jurriën Stutterheim and João Paulo Pizani Flor
 *  Built on top of ParseLib:
    
     *  [ParseLib in Frege/JVM][ParseLib in Frege_JVM]


[download]: http://hackage.haskell.org/package/uu-tc-2015.1.1/uu-tc-2015.1.1.tar.gz
[hackage.haskell.org]: http://hackage.haskell.org/package/uu-tc
[Haskell]: http://101companies.org/wiki/Language:Haskell
[monadic]: http://www.cs.nott.ac.uk/~pszgmh/monparsing.pdf
[haskell.org]: https://www.haskell.org/happy/doc/html/sec-using.html
[ParseLib in Frege_JVM]: https://github.com/pepijnkokke/ParseLib