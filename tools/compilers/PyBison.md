## PyBison ##

### PyBison ###

 *  PyBison version 0.1.8 ([download][])
 *  Main website: [freenet.mcnabhosting.com][]
 *  Works with [Python2][]
 *  Parsing algorithm: [LALR(1)][LALR_1]
 *  Example from [freenet.mcnabhosting.com][freenet.mcnabhosting.com 1]:
    
    > ``````````
    > def on_exp(self, target, option, names, values):
    >     """
    >     exp : NUMBER
    >         | exp PLUS exp
    >         | exp MINUS exp
    >         | exp TIMES exp
    >         | exp DIVIDE exp
    >         | MINUS exp %prec NEG
    >         | exp POW exp
    >         | LPAREN exp RPAREN
    >     """
    >     if option == 0:
    >         return float(values[0])
    >     elif option == 1:
    >         return values[0] + values[2]
    >     elif option == 2:
    >         return values[0] - values[2]
    >     elif option == 3:
    >         return values[0] * values[2]
    >     elif option == 4:
    >         return values[0] / values[2]
    >     elif option == 5:
    >         return - values[1]
    >     elif option == 6:
    >         return values[0] ** values[2]
    >     elif option == 7:
    >         return values[1]
    > ``````````
 *  More examples: [freenet.mcnabhosting.com][freenet.mcnabhosting.com 2]
 *  Maintained by David McNab
 *  Not to be confused with [PyBison by Scott Hassan][]!


[download]: http://www.freenet.org.nz/python/pybison/pybison-0.1.8.tar.gz
[freenet.mcnabhosting.com]: http://freenet.mcnabhosting.com/python/pybison/
[Python2]: https://docs.python.org/2/
[LALR_1]: https://en.wikipedia.org/wiki/LALR_parser
[freenet.mcnabhosting.com 1]: http://freenet.mcnabhosting.com/python/pybison/calc.py
[freenet.mcnabhosting.com 2]: http://freenet.mcnabhosting.com/python/pybison/walkthrough.html
[PyBison by Scott Hassan]: https://wiki.python.org/moin/PyBison