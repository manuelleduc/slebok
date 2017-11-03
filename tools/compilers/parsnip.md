## parsnip ##

### parsnip ###

 *  parsnip version 0.23 ([download][])
 *  Main website: [parsnip-parser.sourceforge.net][]
 *  Works with [C++][C]
 *  Parsing algorithm: [Packrat][]
 *  Example from [spikebucket.blogspot.be][]:
    
    > ``````````
    > double multiply(double x, double y) { return x*y; }
    > double add(double x, double y) { return x+y; }
    > double subtract(double x, double y) { return x-y; }
    > double divide(double x, double y) { return x/y; }
    > 
    > typedef Parser<string, double>::type NumParser;
    > 
    > NumParser ops = op_table(real)
    >                  ->infix_left("+", 10, add)
    >                  ->infix_left("-", 10, subtract)
    >                  ->infix_left("*", 20, multiply)
    >                  ->infix_left("/", 20, divide);
    > 
    > ParseResult<double> result;
    > 
    > result = parse("3+4*2", ops);
    > 
    > if (result.parse_finished())
    > {
    >   std::cout << parse.data();
    > }
    > ``````````
 *  Maintained by Alex Rubinsteyn


[download]: https://sourceforge.net/projects/parsnip-parser/files/
[parsnip-parser.sourceforge.net]: http://parsnip-parser.sourceforge.net/
[C]: http://101companies.org/wiki/Language:CPlusPlus
[Packrat]: http://bford.info/packrat/
[spikebucket.blogspot.be]: http://spikebucket.blogspot.be/2007/10/simple-calculator.html