## SwiftParsec ##

### SwiftParsec ###

 *  SwiftParsec version 2.1 ([download][])
 *  Main website: [@davedufresne/SwiftParsec][davedufresne_SwiftParsec]
 *  Works with [Swift][]
 *  Parsing algorithms: [monadic][], [recursive descent][]
 *  Example from [@davedufresne/SwiftParsec][davedufresne_SwiftParsec 1]:
    
    > ``````````
    > let noneOf = StringParser.noneOf
    > 
    > let quotedChars = noneOf("\"") <|>
    >     StringParser.string("\"\"").attempt *>
    >     GenericParser(result: "\"")
    > 
    > let character = StringParser.character
    > 
    > let quote = character("\"")
    > let quotedField = quote *> quotedChars.many.stringValue <*
    >     (quote <?> "quote at end of field")
    > 
    > let field = quotedField <|> noneOf("\r\n,\n\r").many.stringValue
    > let record = field.separatedBy(character(","))
    > 
    > let endOfLine = StringParser.crlf.attempt <|>
    >     (character("\n") *> character("\r")).attempt <|>
    >     character("\n") <|>
    >     character("\r") <?> "end of line"
    > 
    > let csv = record.separatedBy(endOfLine)
    > ``````````
 *  More examples: [@davedufresne/SwiftParsec][davedufresne_SwiftParsec 2]
 *  Maintained by David Dufresne


[download]: https://github.com/davedufresne/SwiftParsec/archive/master.zip
[davedufresne_SwiftParsec]: https://github.com/davedufresne/SwiftParsec
[Swift]: https://en.wikipedia.org/wiki/Swift_%28programming_language%29
[monadic]: http://www.cs.nott.ac.uk/~pszgmh/monparsing.pdf
[recursive descent]: https://en.wikipedia.org/wiki/Recursive_descent_parser
[davedufresne_SwiftParsec 1]: https://github.com/davedufresne/SwiftParsec/wiki/2-First-Step:-CSV-Parser#csv-parsing
[davedufresne_SwiftParsec 2]: https://github.com/davedufresne/SwiftParsec/wiki