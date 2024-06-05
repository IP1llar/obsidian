An **expression** is any valid OCaml program. OCaml  **evaluates** expressions, yielding **values**.
Each expression (and value) has a **type**.

Integers are of type `int`

### Mathematical Operators
| Operator  | Description                                 |
| :-------: | ------------------------------------------- |
|  `a + b`  | addition                                    |
|  `a - b`  | subtract `b` from `a`                       |
|  `a * b`  | multiplication                              |
|  `a / b`  | divide `a` by `b`, returning the whole part |
| `a mod b` | divide `a` by `b`, returning the remainder  |
The mod, `*` , and `/` operators have higher precedence than the `+` and `-` operators.

## Comparison Operators
| Operator | Description                              |
| -------- | ---------------------------------------- |
| `a = b`  | true if `a` and `b` are equal            |
| `a < b`  | true if `a` is less than `b`             |
| `a <= b` | true if `a` is less than or equal to `b` |
| `a > b`  | true if `a` is more than `b`             |
| `a >= b` | true if `a` is more than or equal `b`    |
| `a <> b` | true if `a` is not equal to `b`          |

Boolean types (`bool`) can either be `true` or `false`. The comparison operators yield `bool` types.

If we try to use operators with types for which they are not intended, OCaml will not accept the program at all, showing us where our mistake is by underlining it.

``` OCaml
# 1 + true;;
Error: This expression has type bool but an expression was expected of type int
```

## Boolean Operators
| Operator | Description |
| `&&` | true only if `a` and `b` are both true |
| `||` | true if `a` is true, `b` is true, or both are true |

`&&` is of higher precedence than `||`

### Char
`char` types hold a single *character*, such as `a` or `?`. We use single quotation marks:

``` OCaml
# 'c';;
- : char = 'c'
```

### if ... then ... else

``` OCaml
# if 100 > 99 then 0 else 1;;
- : int = 0
```

- The expression between `if` and `then` must have type `bool`.
- The types of expression for the `true` and `false` cases must be the same type.
- The whole expression evaluates to the same type as the `true` and `false` cases.


## Questions
1. What are the types of the following expressions and what do they evaluate to, and why?
	- `17` -> `int` because it is an integer
	-  `1 + 2 * 3 + 4` -> `int = 11` because of order of operations `1 + (2 * 3) + 4 = 1 + 6 + 4 = 11` 
	- `800 / 80 / 8` -> `int = 1` because of order of operations `(800 / 80) / 8 = 10 / 8 = 1(.25) = 1` 
	- `400 > 200` -> `bool = true` because `400` is greater than `200` so the expression evaluates to the `bool`: `true`.
	- `1 <> 1` -> `bool = false` because `1` is equal to `1` 
	- `true || false` -> `bool = true` because with `||` only one case needs to be true
	- `true && false` -> `bool = false` because with `&&` both cases need to be true
	- `if true then false else true` -> `bool = false` because the expression between `if` and `then` is `true` so we evaluate the expression after `then`, which evaluates to `false`.
	- `'%'` -> `char = '%'` because it is a single character
	- `'a' + 'b'` -> `Error` because the `+` operator expects type `int` instead of type `char`
2. Consider the evaluations of the expressions `1 + 2 mod 3`, `(1 + 2) mod 3`, and `1 + (2 mod 3)`. What can you conclude about the `+` and `mod` operators.
	- `1 + 2 mod 3 = 3` -> the `mid`
	- `(1 + 2) mod 3 = 0`
	- 