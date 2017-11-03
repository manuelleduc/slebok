## GDK ##

### Grammar Deployment Kit ###

 *  GDK version 1.4.4 ([download][])
 *  Main website: [gdk.sourceforge.net][]
 *  Works with [C][]
 *  Parsing algorithm: [LL][]
 *  Example from [@slebok/zoo][slebok_zoo]:
    
    > ``````````
    > specification : rule+;
    > rule          : ident ":" disjunction ";";
    > disjunction   : {conjunction "|"};
    > conjunction   : term+;
    > term          : basis repetition?;
    > basis         : ident
    >               | literal
    >               | "%epsilon"
    >               | alternation
    >               | group
    >               ;
    > repetition    : "+" | "*" | "?";
    > alternation   : "{" basis basis "}" repetition;
    > group : "(" disjunction ")" ;
    > ``````````
 *  More examples: [gdk.sourceforge.net][gdk.sourceforge.net 1]
 *  Maintained by Jan Kort


[download]: http://gdk.sourceforge.net/gdk-1.4.4.tar.gz
[gdk.sourceforge.net]: http://gdk.sourceforge.net/
[C]: http://101companies.org/wiki/Language:C
[LL]: https://en.wikipedia.org/wiki/LL_parser
[slebok_zoo]: https://github.com/slebok/zoo/blob/master/zoo/%C2%A7wip/metasyntax/lll-kort/fetched/src.gdkref.txt
[gdk.sourceforge.net 1]: http://gdk.sourceforge.net/gdkref.pdf