## Ensō ##

### [![Ensō][Ens]][Ens_Ens] ###

 *  Ensō ([download][])
 *  Main website: [@enso-lang/enso][Ens_Ens]
 *  Parsing algorithm: [GLL][]
 *  Example from [cs.utexas.edu][]:
    
    > ``````````
    > start G
    > G ::= [Grammar] "start" start:</rules[it]> rules:R*
    > R ::= [Rule] name:sym "::=" arg:A
    > A ::= [Alt] alts:C + @"|"
    > C ::= [Create] "[" name:sym "]" arg:S | S
    > S ::= [Sequence] elements:F*
    > F ::= [Field] name:sym  ":" arg:P | P
    > P ::= [Lit] value:str
    >     | [Value] kind:("int" | "str" | "real" | "sym")
    >     | [Ref] "<" path:Path  ">"
    >     | [Call] rule:</rules[it]>
    >     | [Code] "{" code:Expr "}"
    >     | [Regular] arg:P "*" Sep? { optional && many }
    >     | [Regular] arg:P "?" { optional }
    >     | "(" A ")"
    > Sep ::= "@"sep:P
    > ``````````
 *  More examples: [enso-lang.org][]
 *  Maintained by William R. Cook, Alex Loh and Tijs van der Storm


[Ens]: 
[Ens_Ens]: https://github.com/enso-lang/enso
[download]: https://github.com/enso-lang/enso/archive/master.zip
[GLL]: http://dotat.at/tmp/gll.pdf
[cs.utexas.edu]: http://www.cs.utexas.edu/~wcook/Drafts/2012/2012-07-13EnsoMSR.pdf
[enso-lang.org]: http://enso-lang.org/blog/