## SPARK ##

### Scanning, Parsing, and Rewriting Kit ###

 *  SPARK version 0.6.1 ([download][])
 *  Main website: [pages.cpsc.ucalgary.ca][]
 *  Works with [Python2][]
 *  Parsing algorithm: ?
 *  Example from [pages.cpsc.ucalgary.ca][pages.cpsc.ucalgary.ca 1]:
    
    > ``````````
    > class ExprParser(GenericParser):
    > 	def __init__(self, start='expr'):
    > 		GenericParser.__init__(self, start)
    > 
    > 	def p_rules(self args):
    > 		'''
    > 			expr class="kw">::= expr + term
    > 			expr class="kw">::= term
    > 			term class="kw">::= term * factor
    > 			term class="kw">::= factor
    > 			factor class="kw">::= number
    > 			factor class="kw">::= float
    > 		'''
    > ``````````
 *  Maintained by John Aycock


[download]: http://pages.cpsc.ucalgary.ca/~aycock/spark/spark-0.6.1.tar.gz
[pages.cpsc.ucalgary.ca]: http://pages.cpsc.ucalgary.ca/~aycock/spark/
[Python2]: https://docs.python.org/2/
[pages.cpsc.ucalgary.ca 1]: http://pages.cpsc.ucalgary.ca/~aycock/spark/paper.pdf