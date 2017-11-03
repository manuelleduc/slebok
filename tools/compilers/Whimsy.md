## Whimsy ##

### [![Whimsy][]][Whimsy 1] ###

 *  Autumn ([download][])
 *  Main website: [@norswap/whimsy][Whimsy 1]
 *  Works with [Kotlin][]
 *  Parsing algorithms: PEG, [monadic][]
 *  Example from [@norswap/whimsy][norswap_whimsy]:
    
    > ``````````
    > import norswap.autumn.Grammar
    > import norswap.autumn.parsers.*
    > 
    > class RegexGrammar: Grammar()
    > {
    >      fun meta_char()
    >         = char_set("|*+?()\\")
    > 
    >     fun regular_char()
    >         = seq { not { meta_char() } && char_any() }
    > 
    >     fun quoted_char()
    >         = seq { string("\\") && char_any() }
    > 
    >     fun character()
    >         = choice { quoted_char() || regular_char() }
    > 
    >     fun paren_group(): Boolean
    >         = seq { string("(") && alternation() && string(")") }
    > 
    >     fun atom()
    >         = choice { paren_group() || character() }
    > 
    >     fun repetition_char()
    >         = char_set("*+?")
    > 
    >     fun repetition()
    >         = seq { atom() && repeat0 { repetition_char() } }
    > 
    >     fun concatenation()
    >         = repeat1 { repetition() }
    > 
    >     fun alternation()
    >         = around1 ({ concatenation() } , { string("|") })
    > 
    >     override fun root() =
    >         alternation()
    > }
    > ``````````
 *  Maintained by Nicolas Laurent


[Whimsy]: 
[Whimsy 1]: https://github.com/norswap/whimsy
[download]: https://github.com/norswap/whimsy/archive/master.zip
[Kotlin]: https://kotlinlang.org/
[monadic]: http://www.cs.nott.ac.uk/~pszgmh/monparsing.pdf
[norswap_whimsy]: https://github.com/norswap/whimsy/blob/master/doc/autumn/guide/first-grammar.md