## Iguana ##

### [![Iguana][]][Iguana 1] ###

 *  Iguana ([download][])
 *  Main website: [iguana-parser.github.io][Iguana 1]
 *  Works with Rascal, [Java][], [Scala][]
 *  Parsing algorithms: [GLL][], [data dependency][]
 *  Example from [@iguana-parser/examples][iguana-parser_examples]:
    
    > ``````````
    > Start ::= Element
    > 
    > Element ::= s=STag Content ETag(s)
    > STag    ::= '<' n:Name Attribute* '>' {n.yield}
    > ETag(s) ::= '</' n:Name [n.yield == s] '>'
    > 
    > Attribute ::= Name "=" String
    > Content ::= Element* | Text
    > 
    > @Layout
    > L ::= Whitespaces
    > 
    > regex
    > {
    > 	Name ::= [a-zA-Z][a-zA-Z0-9]*
    > 	Text ::= [a-zA-Z0-9]+
    > 	String ::= '\"' [a-zA-Z0-9]+ '\"'
    > 	Whitespaces ::= [\n\r\t\f\ ]*
    > }
    > ``````````
 *  More examples: [@iguana-parser/examples][iguana-parser_examples 1]
 *  Maintained by Ali Afroozeh and Anastasia Izmaylova


[Iguana]: 
[Iguana 1]: http://iguana-parser.github.io/
[download]: https://github.com/iguana-parser/iguana
[Java]: http://101companies.org/wiki/Language:Java
[Scala]: https://en.wikipedia.org/wiki/Scala_%28programming_language%29
[GLL]: http://dotat.at/tmp/gll.pdf
[data dependency]: http://iguana-parser.github.io/documentation.html#data-dependent-grammars
[iguana-parser_examples]: https://github.com/iguana-parser/examples/blob/master/src/resources/grammars/XML.iggy
[iguana-parser_examples 1]: https://github.com/iguana-parser/examples/tree/master/src/resources/grammars