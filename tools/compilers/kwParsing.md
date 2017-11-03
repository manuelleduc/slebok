## kwParsing ##

### kwParsing ###

 *  kwParsing ([download][])
 *  Main website: [web.archive.org][]
 *  Works with [Python2][]
 *  Parsing algorithm: ?
 *  Example from [web.archive.org][web.archive.org 1]:
    
    > ``````````
    > GRAMMARSTRING ="""
    >        Value ::  ## indicates Value is the root nonterminal for the grammar
    >          @R SetqRule :: Value >> ( setq var Value )
    >          @R ListRule :: Value >> ( ListTail
    >          @R TailFull :: ListTail >> Value ListTail
    >          @R TailEmpty :: ListTail >> )
    >          @R Varrule :: Value >> var
    >          @R Intrule :: Value >> int
    >          @R Strrule :: Value >> str
    >          @R PrintRule :: Value >> ( print Value )
    > """
    > ``````````
 *  Maintained by Aaron Watters


[download]: http://web.archive.org/web/19980422214116/http://starship.skyport.net/crew/aaron_watters/kwParsing/kwP.tar.gz
[web.archive.org]: http://web.archive.org/web/19980422214116/http://starship.skyport.net/crew/aaron_watters/kwParsing/
[Python2]: https://docs.python.org/2/
[web.archive.org 1]: http://web.archive.org/web/19980716070842/http://starship.skyport.net/crew/aaron_watters/kwParsing/kwParsing.html