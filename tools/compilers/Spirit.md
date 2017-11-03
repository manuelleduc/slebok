## Spirit ##

### [![Spirit][]][Spirit 1] ###

 *  Spirit version 3.0.0 ([download][])
 *  Main website: [boost-spirit.com][Spirit 1]
 *  Works with [C++][C]
 *  Wikipedia: ([English][]) ([German][])
 *  Parsing algorithms: [backtracking][], [LL(\*)][LL]
 *  Example from [English][English 1]:
    
    > ``````````
    > #include <string>
    > #include <iostream>
    > #include <boost/spirit/include/qi.hpp>
    > #include <boost/spirit/include/phoenix.hpp>
    > 
    > int main()
    > {
    >   namespace qi = boost::spirit::qi;
    > 
    >   std::string input;
    > 
    >   std::cout << "Input a line: \n";
    >   getline(std::cin, input);
    >   std::cout << "Got '" << input << "'.\n";
    > 
    >   unsigned count = 0;
    > 
    >   auto rule = *(qi::lit("cat") [ ++qi::_val ] | qi::omit[qi::char_]);
    >   qi::parse(input.begin(), input.end(), rule, count);
    > 
    >   std::cout << "The input contained " << count << " occurrences of 'cat'\n";
    > }
    > ``````````
 *  Maintained by Joel de Guzman, Hartmut Kaiser, Carl Barron, François Barel, Dan Nuffer, Ben Hanson, Martijn van der Lee, John David, Juan Carlos Arevalo-Baeza, Martin Wille, Peter Simons, Jeff Westfahl, João Abecasis, Dan Marsden, Nicola Musatti, Tobias Schwinger, Thomas Heller, Bryce Lelbach, Jeroen Habraken, Agustín Bergé, Kohei Takahashi


[Spirit]: 
[Spirit 1]: http://boost-spirit.com/home/
[download]: http://boost-spirit.com/home/download/
[C]: http://101companies.org/wiki/Language:CPlusPlus
[English]: https://en.wikipedia.org/wiki/Spirit%20Parser%20Framework
[German]: https://de.wikipedia.org/wiki/Spirit%20%28Parser%29
[backtracking]: https://en.wikipedia.org/wiki/Backtracking
[LL]: https://en.wikipedia.org/wiki/LL_parser
[English 1]: https://en.wikipedia.org/wiki/Spirit_Parser_Framework#Example