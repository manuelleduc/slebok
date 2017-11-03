## RecDescent ##

### Parse::RecDescent ###

 *  RecDescent version 1.967013 ([download][])
 *  Main website: [metacpan.org][]
 *  Works with [Perl][]
 *  Parsing algorithm: [recursive descent][]
 *  Example from [metacpan.org][]:
    
    > ``````````
    > parser = Parse::RecDescent->new(q{
    > <autoaction: { [@item] } >
    > 
    > expression: and_expr '||' expression | and_expr
    > and_expr:   not_expr '&&' and_expr   | not_expr
    > not_expr:   '!' brack_expr       | brack_expr
    > brack_expr: '(' expression ')'       | identifier
    > identifier: /[a-z]+/i
    > });
    > ``````````
 *  Maintained by Jeremy T. Braun


[download]: https://cpan.metacpan.org/authors/id/J/JT/JTBRAUN/Parse-RecDescent-1.967013.tar.gz
[metacpan.org]: https://metacpan.org/pod/Parse::RecDescent
[Perl]: https://en.wikipedia.org/wiki/Perl
[recursive descent]: https://en.wikipedia.org/wiki/Recursive_descent_parser