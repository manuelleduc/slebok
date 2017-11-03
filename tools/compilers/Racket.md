## Racket ##

### [![Racket][]][Racket 1] ###

 *  Racket version 6.7 ([download][])
 *  Main website: [racket-lang.org][Racket 1]
 *  Works with [Racket][Racket 2]
 *  Wikipedia: ([English][]) ([French][]) ([German][]) ( [Russian][])
 *  Parsing algorithm: [LALR(1)][LALR_1]
 *  Example from [gist.github.com][]:
    
    > ``````````
    > (define simple-math-lexer
    >   (lexer
    >    ("-" (token--))
    >    ("+" (token-+))
    >    ("let" (token-LET))
    >    ("in" (token-IN))
    >    ((re-+ number10) (token-NUM (string->number lexeme)))
    >    (identifier      (token-VAR lexeme))
    >    ;; recursively calls the lexer which effectively skips whitespace
    >    (whitespace (simple-math-lexer input-port))
    >    ((eof) (token-EOF))))
    > 
    > (define simple-math-parser
    >   (parser
    >    (start exp)
    >    (end EOF)
    >    (error void)
    >    (tokens a b)
    >    (precs (left - +))
    >    (grammar
    >     (exp ((LET VAR NUM IN exp)
    >           (make-let-exp $2 (num-exp $3) $5))
    >          ((NUM) (num-exp $1))
    >          ((VAR) (var-exp $1))
    >          ((exp + exp) (make-arith-exp + $1 $3))
    >          ((exp - exp) (make-arith-exp - $1 $3))))))
    > ``````````
 *  More examples: [matt.might.net][], [docs.racket-lang.org][], [docs.racket-lang.org][docs.racket-lang.org 1]


[Racket]: 
[Racket 1]: https://racket-lang.org/
[download]: https://download.racket-lang.org/
[Racket 2]: https://en.wikipedia.org/wiki/Racket_features
[English]: https://en.wikipedia.org/wiki/Racket%20%28programming%20language%29
[French]: https://fr.wikipedia.org/wiki/DrRacket
[German]: https://de.wikipedia.org/wiki/DrRacket
[Russian]: https://ru.wikipedia.org/wiki/Racket%20%28%D1%8F%D0%B7%D1%8B%D0%BA%20%D0%BF%D1%80%D0%BE%D0%B3%D1%80%D0%B0%D0%BC%D0%BC%D0%B8%D1%80%D0%BE%D0%B2%D0%B0%D0%BD%D0%B8%D1%8F%29
[LALR_1]: https://en.wikipedia.org/wiki/LALR_parser
[gist.github.com]: https://gist.github.com/danking/1068185
[matt.might.net]: http://matt.might.net/articles/parsing-bibtex/
[docs.racket-lang.org]: https://docs.racket-lang.org/syntax/stxparse.html
[docs.racket-lang.org 1]: http://docs.racket-lang.org/parser-tools/