## Eli ##

### [![Eli][]][Eli 1] ###

 *  Eli version 4.8.1 ([download][])
 *  Main website: [eli-project.sourceforge.net][Eli 1]
 *  Parsing algorithm: [AG][]
 *  Example from [eli-project.sourceforge.net][]:
    
    > ``````````
    > ClassDeclaration:
    >   Modifiers 'class' Identifier Super Interfaces ClassBody .
    > 
    > Super:
    >   'extends' InhName / .
    > 
    > Interfaces:
    >   ['implements' InterfaceTypeList] .
    > 
    > InterfaceTypeList:
    >   InterfaceType /
    >   InterfaceTypeList ',' InterfaceType .
    > 
    > ClassBody:
    >   '{' ClassBodyDeclarations '}' .
    > 
    > ClassBodyDeclarations:
    >   / ClassBodyDeclarationList .
    > 
    > ClassBodyDeclarationList:
    >   ClassBodyDeclaration /
    >   ClassBodyDeclarationList ClassBodyDeclaration .
    > ``````````
 *  More examples: [eli-project.sourceforge.net][eli-project.sourceforge.net 1]


[Eli]: 
[Eli 1]: http://eli-project.sourceforge.net/
[download]: https://sourceforge.net/projects/eli-project/
[AG]: https://en.wikipedia.org/wiki/Attribute_grammar
[eli-project.sourceforge.net]: http://eli-project.sourceforge.net/Java/node29.html
[eli-project.sourceforge.net 1]: http://eli-project.sourceforge.net/EliExamples.html