## JavaCC ##

### [![JavaCC][]][JavaCC 1] ###

 *  JavaCC version 6.0.1 ([download][])
 *  Main website: [javacc.java.net][JavaCC 1]
 *  Works with [Java][], [C][], [C++][C 1]
 *  Wikipedia: ([English][]) ([French][]) ([German][]) ([Russian][])
 *  Parsing algorithm: [LL(k)][LL_k]
 *  Example from [engr.mun.ca][]:
    
    > ``````````
    > double Primary() throws NumberFormatException :
    > {
    > 	Token t ;
    > 	double d ;
    > }
    > {
    > 	t=<NUMBER>
    > 	{ return Double.parseDouble( t.image ) ; }
    > |
    > 	<PREVIOUS>
    > 	{ return previousValue ; }
    > |
    > 	<OPEN_PAR> d=Expression() <CLOSE_PAR>
    > 	{ return d ; }
    > |
    > 	<MINUS> d=Primary()
    > 	{ return -d ; }
    > }
    > ``````````
 *  More examples: [engr.mun.ca][engr.mun.ca 1], [javacc.org][]
 *  Maintained by Glassfish Kenai, Paul Cager, Tom Copeland and sreeni.


[JavaCC]: 
[JavaCC 1]: https://javacc.java.net/
[download]: https://java.net/projects/javacc/downloads
[Java]: http://101companies.org/wiki/Language:Java
[C]: http://101companies.org/wiki/Language:C
[C 1]: http://101companies.org/wiki/Language:CPlusPlus
[English]: https://en.wikipedia.org/wiki/JavaCC
[French]: https://fr.wikipedia.org/wiki/JavaCC
[German]: https://de.wikipedia.org/wiki/JavaCC
[Russian]: https://ru.wikipedia.org/wiki/JavaCC
[LL_k]: https://en.wikipedia.org/wiki/LL_parser
[engr.mun.ca]: http://www.engr.mun.ca/~theo/JavaCC-Tutorial/
[engr.mun.ca 1]: http://www.engr.mun.ca/~theo/JavaCC-FAQ/javacc-faq-moz.htm
[javacc.org]: http://javacc.org/