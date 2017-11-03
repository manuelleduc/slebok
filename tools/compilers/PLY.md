## PLY ##

### Python Lex-Yacc ###

 *  PLY version 3.9 ([download][])
 *  Main website: [dabeaz.com][]
 *  Works with [Python2][], [Python3][]
 *  Parsing algorithm: [LR][]
 *  Example from [dabeaz.com][dabeaz.com 1]:
    
    > ``````````
    > names = { }
    > 
    > def p_statement_assign(t):
    >     'statement : NAME EQUALS expression'
    >     names[t[1]] = t[3]
    > 
    > def p_statement_expr(t):
    >      'statement : expression'
    >     print(t[1])
    > 
    > def p_expression_binop(t):
    >     '''expression : expression PLUS expression
    >                   | expression MINUS expression
    >                   | expression TIMES expression
    >                   | expression DIVIDE expression'''
    >     if t[2] == '+'  : t[0] = t[1] + t[3]
    >     elif t[2] == '-': t[0] = t[1] - t[3]
    >     elif t[2] == '*': t[0] = t[1] * t[3]
    >     elif t[2] == '/': t[0] = t[1] / t[3]
    > 
    > def p_expression_uminus(t):
    >     'expression : MINUS expression %prec UMINUS'
    >     t[0] = -t[2]
    > 
    > def p_expression_group(t):
    >     'expression : LPAREN expression RPAREN'
    >     t[0] = t[2]
    > 
    > def p_expression_number(t):
    >     'expression : NUMBER'
    >     t[0] = t[1]
    > 
    > def p_expression_name(t):
    >     'expression : NAME'
    >     try:
    >         t[0] = names[t[1]]
    >     except LookupError:
    >         print("Undefined name '%s'" % t[1])
    >         t[0] = 0
    > ``````````
 *  More examples: [dabeaz.com][dabeaz.com 2]
 *  Maintained by David Beazley


[download]: http://www.dabeaz.com/ply/ply-3.9.tar.gz
[dabeaz.com]: http://www.dabeaz.com/ply/
[Python2]: https://docs.python.org/2/
[Python3]: https://docs.python.org/3/
[LR]: https://en.wikipedia.org/wiki/LR_parser
[dabeaz.com 1]: http://www.dabeaz.com/ply/example.html
[dabeaz.com 2]: http://www.dabeaz.com/ply/ply.html