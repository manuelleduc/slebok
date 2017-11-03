## Irony ##

### [![Irony][]][Irony 1] ###

 *  Irony version BETA ([download][])
 *  Main website: [irony.codeplex.com][Irony 1]
 *  Works with [C\#][C]
 *  Wikipedia: ([English][])
 *  Parsing algorithm: [LALR(1)][LALR_1]
 *  Example from [irony.codeplex.com][]:
    
    > ``````````
    > Expr.Rule = Term | UnExpr | BinExpr | PostFixExpr;
    > Term.Rule = number | ParExpr | identifier;
    > ParExpr.Rule = "(" + Expr + ")";
    > UnExpr.Rule = UnOp + Term;
    > UnOp.Rule = ToTerm("+") | "-" | "++" | "--";
    > BinExpr.Rule = Expr + BinOp + Expr;
    > BinOp.Rule = ToTerm("+") | "-" | "*" | "/" | "**";
    > PostFixExpr.Rule = Term + PostFixOp;
    > PostFixOp.Rule = ToTerm("++") | "--";
    > AssignmentStmt.Rule = identifier + AssignmentOp + Expr;
    > AssignmentOp.Rule = ToTerm("=") | "+=" | "-=" | "*=" | "/=";
    > Statement.Rule = AssignmentStmt | Expr | Empty;
    > ProgramLine.Rule = Statement + NewLine;
    > Program.Rule = MakeStarRule(Program, ProgramLine);
    > this.Root = Program;
    > ``````````
 *  [Irony contributors][]


[Irony]: 
[Irony 1]: https://irony.codeplex.com/
[download]: http://download-codeplex.sec.s-msft.com/Download/Release?ProjectName=irony&DownloadId=27478&FileTime=130313476309630000&Build=21031
[C]: http://101companies.org/wiki/Language:CSharp
[English]: https://en.wikipedia.org/wiki/Irony%20%28framework%29
[LALR_1]: https://en.wikipedia.org/wiki/LALR_parser
[irony.codeplex.com]: https://irony.codeplex.com/wikipage?title=Expression%20Grammar%20sample
[Irony contributors]: https://irony.codeplex.com/wikipage?title=Contributors