## Kiama ##

### [![Kiama][]][Kiama 1] ###

 *  Kiama version 2.0.0 ([download][])
 *  Main website: [@inkytonik/kiama][Kiama 1]
 *  Works with [Scala][]
 *  Parsing algorithms: [Packrat][], [AG][]
 *  Example from [@inkytonik/kiama][inkytonik_kiama]:
    
    > ``````````
    > class SyntaxAnalyser(positions : Positions) extends Parsers(positions)
    > {
    >     lazy val stmt : Parser[Stmt] =
    >         ";" ^^ (_ => Null()) | sequence | asgnStmt | whileStmt
    > 
    >     lazy val asgnStmt =
    >         variable ~ ("=" ~> exp) <~ ";" ^^ Asgn
    > 
    >     lazy val whileStmt =
    >         ("while" ~> "(" ~> exp <~ ")") ~ stmt ^^ While
    > 
    >     lazy val sequence =
    >         "{" ~> (stmt*) <~ "}" ^^ Seqn
    > 
    >     lazy val exp : PackratParser[Exp] =
    >         exp ~ ("+" ~> term) ^^ Add |
    >             exp ~ ("-" ~> term) ^^ Sub |
    >             term
    > 
    >     lazy val term : PackratParser[Exp] =
    >         term ~ ("*" ~> factor) ^^ Mul |
    >             term ~ ("/" ~> factor) ^^ Div |
    >             factor
    > 
    >     lazy val factor : Parser[Exp] =
    >         double | integer | variable | "-" ~> exp ^^ Neg | "(" ~> exp <~ ")"
    > 
    >     lazy val double =
    >         """[0-9]+\.[0-9]+""".r ^^ (s => Num(s.toDouble))
    > 
    >     lazy val integer =
    >         "[0-9]+".r ^^ (s => Num(s.toInt))
    > 
    >     lazy val variable =
    >         idn ^^ Var
    > 
    >     lazy val idn =
    >         not(keyword) ~> "[a-zA-Z][a-zA-Z0-9]*".r
    > 
    >     lazy val keyword =
    >         keywords("[^a-zA-Z0-9]".r, List("while"))
    > 
    > }
    > ``````````
 *  More examples: [@inkytonik/kiama][inkytonik_kiama 1]
 *  Maintained by Anthony Sloane


[Kiama]: 
[Kiama 1]: https://bitbucket.org/inkytonik/kiama
[download]: https://bitbucket.org/inkytonik/kiama/src
[Scala]: https://en.wikipedia.org/wiki/Scala_%28programming_language%29
[Packrat]: http://bford.info/packrat/
[AG]: https://en.wikipedia.org/wiki/Attribute_grammar
[inkytonik_kiama]: https://bitbucket.org/inkytonik/kiama/src/21ee36be99e8d9c6c697b80aca0a56e2eb4d2db3/library/src/test/scala/org/bitbucket/inkytonik/kiama/example/imperative/SyntaxAnalyser.scala
[inkytonik_kiama 1]: https://bitbucket.org/inkytonik/kiama/src/21ee36be99e8d9c6c697b80aca0a56e2eb4d2db3/library/src/test/scala/org/bitbucket/inkytonik/kiama/example/