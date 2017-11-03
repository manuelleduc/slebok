## Copper ##

### Copper ###

 *  Copper version 0.7.2 ([download][])
 *  Main website: [melt.cs.umn.edu][]
 *  Works with [Silver][]
 *  Parsing algorithms: [context-aware][], [LALR(1)][LALR_1]
 *  Example from [@melt-umn/copper][melt-umn_copper]:
    
    > ``````````
    > %cf{
    >     non terminal stmt;
    >     non terminal Double stmts,expr;
    > 
    >     start with stmts;
    > 
    >     precedence left PLUS, BINARY_MINUS;
    >     precedence left TIMES, DIVIDE;
    >     precedence left UNARY_MINUS;
    > 
    >     stmts ::=
    >       stmts:hd stmt:tl   {: RESULT = (env.containsKey("RESULT") ? env.get("RESULT") : 0.0/0.0); :}
    >     | stmt:s             {: RESULT = (env.containsKey("RESULT") ? env.get("RESULT") : 0.0/0.0);  :}
    >     ;
    > 
    >     stmt ::=
    >       UNASSIGNED_ID:i ASSIGN expr:e SEMI      {: env.put(i,e); :}
    >     | expr:e SEMI                             {: env.put("_e" + (nextUnnamed++),e); :}
    >     ;
    > 
    >     expr ::=
    >       expr:l PLUS expr:r           {: RESULT = l + r;    :}
    >     | expr:l BINARY_MINUS expr:r   {: RESULT = l - r;    :}
    >     | expr:l TIMES expr:r          {: RESULT = l * r;    :}
    >     | expr:l DIVIDE expr:r         {: RESULT = l / r;    :}
    >     | UNARY_MINUS expr:e           {: RESULT = -1.0 * e; :}
    >         %layout ()
    >     | LPAREN expr:e RPAREN         {: RESULT = e;        :}
    >     | NUMBER:n                     {: RESULT = n;        :}
    >     | ASSIGNED_ID:i                {: RESULT = i;        :}
    >     | UNASSIGNED_ID:u
    >       {:
    >           error(_pos,"Undefined symbol '" + u + "'");
    >           RESULT = 0.0/0.0;
    >       :}
    >     ;
    > 
    > %cf}
    > ``````````
 *  More examples: [@melt-umn/copper][melt-umn_copper 1]
 *  Maintained by Eric Van Wyk


[download]: https://github.com/melt-umn/copper
[melt.cs.umn.edu]: http://melt.cs.umn.edu/copper/index.html
[Silver]: http://melt.cs.umn.edu/silver/
[context-aware]: http://www-users.cs.umn.edu/~evw/pubs/vanwyk07gpce/
[LALR_1]: https://en.wikipedia.org/wiki/LALR_parser
[melt-umn_copper]: https://github.com/melt-umn/copper/blob/develop/tests/grammars/CExprGrammar.x
[melt-umn_copper 1]: https://github.com/melt-umn/copper/tree/develop/tests/grammars