## Silver ##

### Silver ###

 *  Silver version 0.4.0 ([download][])
 *  Main website: [melt.cs.umn.edu][]
 *  Works with [Silver][melt.cs.umn.edu]
 *  Parsing algorithms: [context-aware][], [LALR(1)][LALR_1], [AG][]
 *  Example from [melt.cs.umn.edu][melt.cs.umn.edu 1]:
    
    > ``````````
    > nonterminal Root_c ;
    > synthesized attribute pp :: String ;
    > synthesized attribute ast_Root :: Root;
    > attribute pp, ast_Root occurs on Root_c ;
    > 
    > concrete production root_c
    > r::Root_c ::= e::Expr_c
    > { r.pp = e.pp;
    >   r.ast_Root = root(e.ast_Expr);
    > }
    > 
    > synthesized attribute ast_Expr :: Expr ;
    > nonterminal Expr_c with pp, ast_Expr;
    > nonterminal Term_c with pp, ast_Expr;
    > nonterminal Factor_c with pp, ast_Expr;
    > 
    > concrete production add_c
    > sum::Expr_c ::= e::Expr_c ’+’ t::Term_c
    > { sum.pp = e.pp ++ " + " ++ t.pp ;
    >   sum.ast_Expr = add(e.ast_Expr, t.ast_Expr );
    > }
    > 
    > concrete production exprTerm_c
    > e::Expr_c ::= t::Term_c
    > { e.pp = t.pp ;
    >   e.ast_Expr = t.ast_Expr ;
    > }
    > 
    > concrete production mul_c
    > prd::Term_c ::= t::Term_c ’*’ f::Factor_c
    > { prd.pp = t.pp ++ " * " ++ f.pp ;
    >   prd.ast_Expr = mul(t.ast_Expr, f.ast_Expr);
    > }
    > 
    > concrete production termFactor_c
    > t::Term_c ::= f::Factor_c
    > { t.pp = f.pp ;
    >   t.ast_Expr = f.ast_Expr ;
    > }
    > 
    > concrete production integerConstant_c
    > ic::Factor_c ::= i::IntLit_t
    > { ic.pp = i.lexeme ;
    >   ic.ast_Expr = integerConstant(i);
    > }
    > ``````````
 *  More examples: [melt.cs.umn.edu][melt.cs.umn.edu 2]
 *  Maintained by Ted Kaminski and Eric Van Wyk


[download]: https://github.com/melt-umn/silver
[melt.cs.umn.edu]: http://melt.cs.umn.edu/silver/
[context-aware]: http://www-users.cs.umn.edu/~evw/pubs/vanwyk07gpce/
[LALR_1]: https://en.wikipedia.org/wiki/LALR_parser
[AG]: https://en.wikipedia.org/wiki/Attribute_grammar
[melt.cs.umn.edu 1]: http://melt.cs.umn.edu/silver/doc/tutorial/4_attribute_grammars/
[melt.cs.umn.edu 2]: http://melt.cs.umn.edu/silver/doc/tutorial