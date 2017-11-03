## PetitParser ##

### [![PetitParser][]][PetitParser 1] ###

 *  Helvetia / Pharo version 5.0 ([download][]) ([download][])
 *  Main website: [scg.unibe.ch][PetitParser 1]
 *  Works with [Smalltalk][]
 *  Parsing algorithms: [scannerless][], [monadic][], [Packrat][], [contexts][]
 *  Example from [lukas-renggli.ch][]:
    
    > ``````````
    > identifier := (#letter asParser , (#letter asParser / #digit asParser) star) flatten.
    > number :=  #digit asParser plus token trim ==> [ :token | token value asNumber ].
    > 
    > term := PPUnresolvedParser new.
    > prod := PPUnresolvedParser new.
    > prim := PPUnresolvedParser new.
    > 
    > term def: (prod , $+ asParser trim , term ==> [ :nodes | nodes first + nodes last ])
    >    / prod.
    > prod def: (prim , $* asParser trim , prod ==> [ :nodes | nodes first * nodes last ])
    >    / prim.
    > prim def: ($( asParser trim , term , $) asParser trim ==> [ :nodes | nodes second ])
    >    / number.
    > 
    > start := term end.
    > ``````````
 *  Maintained by Tudor Gîrba, Jan Kurš
 *  Built on top of Helvetia / Pharo:
    
     *  [PetitParser for Dart][]
     *  [PetitParser for Java][]
     *  [PetitParser for PHP][]
     *  [PetitParser for Smalltalk/X][PetitParser for Smalltalk_X]
     *  [PetitParser for TypeScript][]


[PetitParser]: 
[PetitParser 1]: http://scg.unibe.ch/research/helvetia/petitparser
[download]: https://cocodo.github.io/['http://pharo.org/',%20'http://source.lukas-renggli.ch/built/oneclick/Helvetia-OneClick.zip']
[Smalltalk]: https://en.wikipedia.org/wiki/Smalltalk
[scannerless]: https://en.wikipedia.org/wiki/Scannerless_parsing
[monadic]: http://www.cs.nott.ac.uk/~pszgmh/monparsing.pdf
[Packrat]: http://bford.info/packrat/
[contexts]: http://www.slideshare.net/esug/parsing-contexts-for-petitparser
[lukas-renggli.ch]: https://www.lukas-renggli.ch/blog/petitparser-1
[PetitParser for Dart]: https://github.com/petitparser/dart-petitparser
[PetitParser for Java]: https://github.com/petitparser/java-petitparser
[PetitParser for PHP]: https://github.com/mindplay-dk/petitparserphp
[PetitParser for Smalltalk_X]: https://bitbucket.org/janvrany/stx-goodies-petitparser/overview
[PetitParser for TypeScript]: https://github.com/mindplay-dk/petitparser-ts