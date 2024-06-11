## Basics
Integers `min_int ... -3 -2 -1 0 1 2 3 ... max_int` of type **int**
Booleans `true` and `false` of type **bool**
Characters of type **char** like `'X'` and `'!'`

Mathematical operators `+ - * / mod` which take two integers and give another

Operators = < <= > >= <> which compare two values and evaluate to either `true` or `false`

The conditional **if** `expression1` **then** `expression2` **else** `expression3`, where `expression1` has type **bool** and `expression2` and `expression3` have the same type as one another

The boolean operators `&&` and `||` which allow us to build compound boolean expressions

## Names and Functions
Assigning a name to the result of evaluation an expression using the `let name = expression` construct. Building compound expressions using `let name1 = expression1 in let name2 = expression2 in ...`

Functions, introduced by `let name argument1 argument2 ... = expression`. These have type `a -> b, a -> b -> g` etc for some types `a, b, g` etc

Recursive functions, which are introduced in the same way, but using `let rec` instead of `let`.