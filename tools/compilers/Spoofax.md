## Spoofax ##

### [![Spoofax][]][Spoofax 1] ###

 *  Spoofax version 2.1.0 ([download][])
 *  Main website: [metaborg.org][Spoofax 1]
 *  Works with [SDF3][]
 *  Wikipedia: ([English][])
 *  Parsing algorithm: [SGLR][]
 *  Example from [metaborg.org][]:
    
    > ``````````
    > Exp.If = <
    >    if(<Exp>)
    >      <Exp>
    >    else
    >      <Exp>
    > > {case-insensitive}
    > ``````````
 *  More examples: [declare-your-language.metaborg.org][]
 *  Maintained by Eelco Visser et al
 *  Used with:
    
     *  [NaBL][]
     *  [Stratego][]
     *  [DynSem][]


[Spoofax]: 
[Spoofax 1]: http://metaborg.org/en/latest/
[download]: http://www.metaborg.org/en/latest/source/download.html
[SDF3]: https://en.wikipedia.org/wiki/Syntax_Definition_Formalism
[English]: https://en.wikipedia.org/wiki/Stratego/XT
[SGLR]: https://pdfs.semanticscholar.org/90f2/8a411455fb783da17ad4b4efdda4464606c4.pdf
[metaborg.org]: http://www.metaborg.org/en/latest/source/langdev/meta/lang/sdf3.html
[declare-your-language.metaborg.org]: http://declare-your-language.metaborg.org/
[NaBL]: http://www.metaborg.org/en/latest/source/langdev/meta/lang/nabl2/getting-started.html
[Stratego]: http://www.metaborg.org/en/latest/source/langdev/meta/lang/stratego/index.html
[DynSem]: http://www.metaborg.org/en/latest/source/langdev/meta/lang/dynsem/index.html