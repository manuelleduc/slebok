## YAPPS ##

### Yet Another Python Parser System ###

 *  YAPPS version 2 ([download][])
 *  Main website: [web.archive.org][]
 *  Works with [Python1.5][]
 *  Parsing algorithm: [recursive descent][]
 *  Example from [web.archive.org][web.archive.org 1]:
    
    > ``````````
    > parser Calculator:
    >     option:    "context-insensitive-scanner"
    >     token END: "$"
    >     token NUM: "[0-9]+"
    > 
    >     rule goal:           expr END                         -> << expr        >>
    >     rule expr:           factor expr_tail<<factor>>       -> << expr_tail   >>
    >     rule expr_tail<<v>>:                                  -> << v           >>
    >                        | "+" factor expr_tail<<v+factor>> -> << expr_tail   >>
    >                        | "-" factor expr_tail<<v-factor>> -> << expr_tail   >>
    >     rule factor:         term factor_tail<<term>>         -> << factor_tail >>
    >     rule factor_tail<<v>>:                                -> << v           >>
    >                        | "*" term factor_tail<<v*term>>   -> << factor_tail >>
    >                        | "/" term factor_tail<<v/term>>   -> << factor_tail >>
    >     rule term:           NUM                              -> << atoi(NUM)   >>
    >                        | "(" expr ")"                     -> << expr        >>
    > ``````````
 *  Maintained by Amit Patel


[download]: http://web.archive.org/web/20161120233057/http://theory.stanford.edu/~amitp/yapps/yapps.py
[web.archive.org]: http://web.archive.org/web/20161120233057/http://theory.stanford.edu/~amitp/yapps/#yapps2
[Python1.5]: https://docs.python.org/release/1.5/
[recursive descent]: https://en.wikipedia.org/wiki/Recursive_descent_parser
[web.archive.org 1]: http://web.archive.org/web/20161217113346/http://theory.stanford.edu/%7Eamitp/yapps/expr.g