## ML-Yacc ##

### ML-Yacc ###

 *  ML-Yacc version 2.4 ([download][])
 *  Main website: [smlnj.org][]
 *  Works with [ML][]
 *  Parsing algorithm: [LALR][]
 *  Example from [smlnj.org][smlnj.org 1]:
    
    > ``````````
    > fun lookup "bogus" = 10000
    >   | lookup s = 0
    > 
    > %%
    > 
    > %eop EOF SEMI
    > 
    > %pos int
    > 
    > %left SUB PLUS
    > %left TIMES DIV
    > %right CARAT
    > 
    > %term ID of string | NUM of int | PLUS | TIMES | PRINT |
    >       SEMI | EOF | CARAT | DIV | SUB
    > %nonterm EXP of int | START of int option
    > 
    > %name Calc
    > 
    > %subst PRINT for ID
    > %prefer PLUS TIMES DIV SUB
    > %keyword PRINT SEMI
    > 
    > %noshift EOF
    > %value ID ("bogus")
    > %nodefault
    > %verbose
    > %%
    > 
    > START : PRINT EXP (print EXP;
    >                    print "\n";
    >                    flush_out std_out; SOME EXP)
    >       | EXP (SOME EXP)
    >       | (NONE)
    > EXP : NUM             (NUM)
    >     | ID              (lookup ID)
    >     | EXP PLUS EXP    (EXP1+EXP2)
    >     | EXP TIMES EXP   (EXP1*EXP2)
    >     | EXP DIV EXP     (EXP1 div EXP2)
    >     | EXP SUB EXP     (EXP1-EXP2)
    >     | EXP CARAT EXP   (let fun e (m,0) = 1
    >                               | e (m,l) = m*e(m,l-1)
    >                        in e (EXP1,EXP2)
    >                        end)
    > ``````````
 *  More examples: [smlnj.org][smlnj.org 2]
 *  Maintained by David R. Tarditi and Andrew W. Appel


[download]: https://www.cs.princeton.edu/~appel/modern/ml/whichver.html
[smlnj.org]: http://www.smlnj.org/doc/ML-Yacc/index.html
[ML]: https://en.wikipedia.org/wiki/ML_%28programming_language%29
[LALR]: https://en.wikipedia.org/wiki/LALR_parser
[smlnj.org 1]: http://www.smlnj.org/doc/ML-Yacc/mlyacc007.html#toc14
[smlnj.org 2]: http://www.smlnj.org/doc/ML-Yacc/mlyacc002.html