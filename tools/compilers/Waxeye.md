## Waxeye ##

### [![Waxeye][]][Waxeye 1] ###

 *  Waxeye version 0.8.0 ([download][])
 *  Main website: [waxeye.org][Waxeye 1]
 *  Works with [C][], [Java][], [JavaScript][], [Python2][], [Ruby][], [Scheme][]
 *  Parsing algorithm: [Packrat][]
 *  Example from [waxeye.org][]:
    
    > ``````````
    > calc  <- ws sum
    > 
    > sum   <- prod *([+-] ws prod)
    > 
    > prod  <- unary *([*/] ws unary)
    > 
    > unary <= '-' ws unary
    >        | :'(' ws sum :')' ws
    >        | num
    > 
    > num   <- +[0-9] ?('.' +[0-9]) ws
    > 
    > ws    <: *[ \t\n\r]
    > ``````````
 *  More examples: [@orlandohill/waxeye][orlandohill_waxeye]
 *  Maintained by Orlando Hill


[Waxeye]: 
[Waxeye 1]: http://waxeye.org/
[download]: http://sourceforge.net/project/platformdownload.php?group_id=210831
[C]: http://101companies.org/wiki/Language:C
[Java]: http://101companies.org/wiki/Language:Java
[JavaScript]: http://101companies.org/wiki/Language:JavaScript
[Python2]: https://docs.python.org/2/
[Ruby]: https://en.wikipedia.org/wiki/Ruby_%28programming_language%29
[Scheme]: https://en.wikipedia.org/wiki/Scheme_%28programming_language%29
[Packrat]: http://bford.info/packrat/
[waxeye.org]: http://waxeye.org/manual.html#_example_a_calculator
[orlandohill_waxeye]: https://github.com/orlandohill/waxeye