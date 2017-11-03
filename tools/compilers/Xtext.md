## Xtext ##

### [![Xtext][]][Xtext 1] ###

 *  Xtext version 2.11.0 ([download][])
 *  Main website: [eclipse.org][Xtext 1]
 *  Works with [Java][]
 *  Wikipedia: ([English][]) ([German][]) ([Spanish][])
 *  Example from [eclipse.org][]:
    
    > ``````````
    > grammar org.example.domainmodel.Domainmodel
    > with org.eclipse.xtext.common.Terminals
    > 
    > generate domainmodel "http://www.example.org/domainmodel/Domainmodel"
    > 
    > Domainmodel :
    >     (elements+=Type)*;
    > 
    > Type:
    >     DataType | Entity;
    > 
    > DataType:
    >     'datatype' name=ID;
    > 
    > Entity:
    >     'entity' name=ID ('extends' superType=[Entity])? '{'
    >         (features+=Feature)*
    >     '}';
    > 
    > Feature:
    >     (many?='many')? name=ID ':' type=[Type];
    > ``````````
 *  More examples: [eclipse.org][eclipse.org 1]
 *  Used with:
    
     *  [ANTLR][]


[Xtext]: 
[Xtext 1]: http://www.eclipse.org/Xtext/
[download]: http://www.eclipse.org/Xtext/download.html
[Java]: http://101companies.org/wiki/Language:Java
[English]: https://en.wikipedia.org/wiki/Xtext
[German]: https://de.wikipedia.org/wiki/Xtext
[Spanish]: https://es.wikipedia.org/wiki/Xtext
[eclipse.org]: http://www.eclipse.org/Xtext/documentation/102_domainmodelwalkthrough.html
[eclipse.org 1]: http://www.eclipse.org/Xtext/documentation/103_domainmodelnextsteps.html
[ANTLR]: http://www.antlr.org/