## Rascal ##

### [![Rascal][]][Rascal 1] ###

 *  Rascal version 0.7.1 ([download][])
 *  Main website: [rascal-mpl.org][Rascal 1]
 *  Wikipedia: ([English][])
 *  Parsing algorithm: [GLL][]
 *  Example from [@usethesource/rascal][usethesource_rascal]:
    
    > ``````````
    > start syntax Program
    >   = program: "begin" Declarations decls {Statement  ";"}* body "end" ;
    > 
    > syntax Declarations
    >   = "declare" {IdType ","}* decls ";" ;
    > 
    > syntax IdType = idtype: Id id ":" Type t;
    > 
    > syntax Statement
    >   = assign: Id var ":="  Expression val
    >   | cond: "if" Expression cond "then" {Statement ";"}*  thenPart "else" {Statement ";"}* elsePart "fi"
    >   | cond: "if" Expression cond "then" {Statement ";"}*  thenPart "fi"
    >   | loop: "while" Expression cond "do" {Statement ";"}* body "od"
    >   ;
    > 
    > syntax Type
    >   = natural:"natural"
    >   | string :"string"
    >   | nil    :"nil-type"
    >   ;
    > 
    > syntax Expression
    >   = id: Id name
    >   | strcon: String string
    >   | natcon: Natural natcon
    >   | bracket "(" Expression e ")"
    >   > left concat: Expression lhs "||" Expression rhs
    >   > left ( add: Expression lhs "+" Expression rhs
    >          | min: Expression lhs "-" Expression rhs
    >          )
    >   ;
    > 
    > 
    > lexical Id  = [a-z][a-z0-9]* !>> [a-z0-9];
    > lexical Natural = [0-9]+ ;
    > lexical String = "\"" ![\"]*  "\"";
    > 
    > layout Layout = WhitespaceAndComment* !>> [\ \t\n\r%];
    > 
    > lexical WhitespaceAndComment
    >    = [\ \t\n\r]
    >    | @category="Comment" "%" ![%]+ "%"
    >    | @category="Comment" "%%" ![\n]* $
    >    ;
    > 
    > public start[Program] program(str s) {
    >   return parse(#start[Program], s);
    > }
    > 
    > public start[Program] program(str s, loc l) {
    >   return parse(#start[Program], s, l);
    > }
    > ``````````
 *  More examples: [tutor.rascal-mpl.org][]
 *  Maintained by Paul Klint, Jurgen Vinju and Tijs van der Storm


[Rascal]: 
[Rascal 1]: http://www.rascal-mpl.org/
[download]: http://www.rascal-mpl.org/start/
[English]: https://en.wikipedia.org/wiki/RascalMPL
[GLL]: http://dotat.at/tmp/gll.pdf
[usethesource_rascal]: https://github.com/usethesource/rascal/blob/master/src/org/rascalmpl/library/lang/pico/syntax/Main.rsc
[tutor.rascal-mpl.org]: http://tutor.rascal-mpl.org/