## jparsec ##

### jparsec ###

 *  jparsec version 3.0 ([download][])
 *  Main website: [@jparsec/jparsec][jparsec_jparsec]
 *  Works with [Java][]
 *  Parsing algorithm: [recursive descent][]
 *  Example from [@jparsec/jparsec][jparsec_jparsec 1]:
    
    > ``````````
    > Terminals operators = Terminals.operators(","); // only one operator supported so far
    > Parser<?> integerTokenizer = Terminals.IntegerLiteral.TOKENIZER;
    > Parser<String> integerSyntacticParser = Terminals.IntegerLiteral.PARSER;
    > Parser<?> ignored = Parsers.or(Scanners.JAVA_BLOCK_COMMENT, Scanners.WHITESPACES);
    > Parser<?> tokenizer = Parsers.or(operators.tokenizer(), integerTokenizer); // tokenizes the operators and integer
    > Parser<List<String>> integers = integerSyntacticParser.sepBy(operators.token(","))
    >     .from(tokenizer, ignored.skipMany());
    > assertEquals(Arrays.asList("1", "2", "3"), integers.parse("1, /*this is comment*/2, 3");
    > ``````````
 *  Maintained by Arnaud Bailly, Gregory Ssi-Yan-Kai, Ben Yu, Alex Michael Berry


[download]: https://github.com/jparsec/jparsec/archive/master.zip
[jparsec_jparsec]: https://github.com/jparsec/jparsec
[Java]: http://101companies.org/wiki/Language:Java
[recursive descent]: https://en.wikipedia.org/wiki/Recursive_descent_parser
[jparsec_jparsec 1]: https://github.com/jparsec/jparsec/wiki/Overview#step-1-terminals