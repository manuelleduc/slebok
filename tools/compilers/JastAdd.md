## JastAdd ##

### [![JastAdd][]][JastAdd 1] ###

 *  JastAdd version 2.2.2 ([download][])
 *  Main website: [jastadd.org][JastAdd 1]
 *  Parsing algorithm: [RAG][]
 *  Example from [@jastadd/examples][jastadd_examples]:
    
    > ``````````
    > Program ::= Block /PredefinedType:TypeDecl*/;
    > Block ::= BlockStmt*;
    > abstract BlockStmt;
    > abstract Stmt: BlockStmt;
    > abstract Decl: BlockStmt ::= <Name:String>;
    > abstract TypeDecl:Decl;
    > ClassDecl: TypeDecl ::= [Superclass:IdUse] Body:Block;
    > VarDecl: Decl ::= Type:Access;
    > AssignStmt: Stmt ::= Variable:Access Value:Exp;
    > WhileStmt: Stmt ::= Condition:Exp Body:Stmt;
    > abstract Exp;
    > abstract Access:Exp;
    > abstract IdUse: Access ::= <Name:String>;
    > Use: IdUse;
    > Dot:Access ::= ObjectReference:Access IdUse;
    > BooleanLiteral : Exp ::= <Value:String>;
    > ``````````
 *  More examples: [@jastadd/examples][jastadd_examples 1], [jastadd.org][]
 *  Maintained by Görel Hedin, Emma Söderberg, Emma Söderberg and Jesper Öqvist


[JastAdd]: 
[JastAdd 1]: http://jastadd.org/
[download]: http://jastadd.org/web/download.php
[RAG]: https://pdfs.semanticscholar.org/89f1/857e15d270c5c1f8417381368e4781c871e4.pdf
[jastadd_examples]: https://bitbucket.org/jastadd/examples/src/013a8f218469b994d221f3f5c24812be8fc3908c/PicoJava/spec/picojava.ast?at=master&fileviewer=file-view-default
[jastadd_examples 1]: https://bitbucket.org/jastadd/examples/src
[jastadd.org]: http://jastadd.org/web/documentation/