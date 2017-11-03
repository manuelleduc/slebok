## xtc ##

### eXTensible Compiler ###

 *  xtc version 2.4.0 ([download][])
 *  Main website: [cs.nyu.edu][]
 *  Works with [Java][]
 *  Parsing algorithm: [Packrat][]
 *  Example from [cs.nyu.edu][cs.nyu.edu 1]:
    
    > ``````````
    > Module        <- Spacing Intro Production* EOF
    > Intro         <- ModuleDecl Dependency* Header? Body? Footer? Option?
    > ModuleDecl    <- "module" FSpacing ModuleRef SEMICOLON
    > Dependency    <- Modification / Instantiation / Import
    > Modification  <- "modify" FSpacing ModuleRef ModuleTarget? SEMICOLON
    > Instantiation <- "instantiate" FSpacing ModuleRef ModuleTarget? SEMICOLON
    > Import        <- "import" FSpacing ModuleRef ModuleTarget? SEMICOLON
    > ModuleRef     <- QName ModuleParams?
    > ModuleParams  <- OPEN ( QName (COMMA QName)* )? CLOSE
    > ModuleTarget  <- "as" FSpacing QName
    > Header        <- "header" Spacing Action
    > Body          <- "body" Spacing Action
    > Footer        <- "footer" Spacing Action
    > Option        <- "option" FSpacing Attribute (COMMA Attribute)* SEMICOLON
    > Production    <- Full / Addition / Removal / Override
    > Full          <- PAttributes QName Identifier EQUAL Choice SEMICOLON
    > Addition      <- QName Identifier PLUSEQUAL
    >                  ( SName ELLIPSIS SLASH Choice SEMICOLON
    >                  / Choice SLASH SName ELLIPSIS SEMICOLON )
    > Removal       <- QName Identifier MINUSEQUAL
    >                  SName ( COMMA SName )* SEMICOLON
    > Override      <- QName Identifier COLONEQUAL Choice SEMICOLON
    >                  / QName Identifier COLONEQUAL ELLIPSIS SLASH Choice SEMICOLON
    >                  / QName Identifier COLONEQUAL Choice SLASH ELLIPSIS SEMICOLON
    >                  / PAttributes QName Identifier COLONEQUAL ELLIPSIS SEMICOLON
    > ``````````
 *  More examples: [cs.nyu.edu][cs.nyu.edu 2]
 *  Maintained by Robert Grimm


[download]: http://cs.nyu.edu/rgrimm/xtc/#distribution
[cs.nyu.edu]: http://cs.nyu.edu/rgrimm/xtc/
[Java]: http://101companies.org/wiki/Language:Java
[Packrat]: http://bford.info/packrat/
[cs.nyu.edu 1]: http://cs.nyu.edu/rgrimm/xtc/rats-intro.html
[cs.nyu.edu 2]: http://cs.nyu.edu/rgrimm/xtc/#documentation