## BiYacc ##

### [![BiYacc][]][BiYacc 1] ###

 *  BiYacc ([download][])
 *  Main website: [biyacc.yozora.moe][BiYacc 1]
 *  Works with [Haskell][]
 *  Parsing algorithm: [BX][]
 *  Example from [biyacc.yozora.moe][BiYacc 1]:
    
    > ``````````
    > Abstract
    > 
    > data Arith = Add Arith Arith
    >            | Sub Arith Arith
    >            | Mul Arith Arith
    >            | Div Arith Arith
    >            | Num Natural
    >            | Var String
    >   deriving (Show, Eq, Read)
    > 
    > Concrete
    > 
    > Expr   -> Expr '+' Term
    >         | Expr '-' Term
    >         | Term
    >         ;
    > 
    > Term   -> Term '*' Factor
    >         | Term '/' Factor
    >         | Factor
    >         ;
    > 
    > Factor -> '-' Factor
    >         | Int
    >         | Name
    >         | '(' Expr ')'
    >         ;
    > 
    > Actions
    > 
    > Arith +> Expr
    > Add x y +> (x +> Expr) '+' (y +> Term);
    > Sub x y +> (x +> Expr) '-' (y +> Term);
    > exp     +> (exp +> Term);
    > 
    > Arith +> Term
    > Mul x y +>  (x +> Term) '*' (y +> Factor);
    > Div x y +>  (x +> Term) '/' (y +> Factor);
    > exp     +>  (exp +> Factor);
    > 
    > Arith +> Factor
    > Sub (Num 0) y +> '-' (y +> Factor);
    > Num i         +> (i +> Int);
    > Var n         +> (n +> Name);
    > exp           +> '(' (exp +> Expr) ')';
    > ``````````
 *  More examples: [biyacc.yozora.moe][BiYacc 1]
 *  Maintained by Zirun Zhu, Yongzhe Zhang, Hsiang-Shang Ko, Pedro Martins, João Saraiva and Zhenjiang Hu


[BiYacc]: 
[BiYacc 1]: http://biyacc.yozora.moe/
[download]: http://biyacc.yozora.moe/src/biyacc_src.zip
[Haskell]: http://101companies.org/wiki/Language:Haskell
[BX]: http://www.prg.nii.ac.jp/project/bigul/