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
	- `1 + 2 mod 3 = 3` -> the `mod` operator is higher priority than the `+` operator so this expression is evaluated as `1 + (2 mod 3) = 1 + 2 = 3`.
	- `(1 + 2) mod 3 = 0` -> the brackets override the higher priority of the `mod` operator so it evaluates as `(1 + 2) mod 3 = 3 mod 3 = 0`.
	- `1 + (2 mod 3) = 3` -> the brackets don't have an effect as the `mod` operator is already higher priority than the `+` operator.
3. A programmer writes `1+2 * 3+4`. What does this evaluate to? What advice would you give him?
	- `1+2 * 3+4 = 1 + (2 * 3) + 4 = 11`
	- The advice would be that space do not work to change priority of operators. As a result they should be used to evenly space expressions like this for readability.
4. The range of numbers available is limited. There are two special numbers: `min_int` and `max_int`. What are their values on your computer?
	- `max_int = 4611686018427387903`
	- `min_int = -4611686018427387904`
	What happens when you evaluate the expressions `max_int + 1` and `min_int - 1`?
	- `min_int - 1 = 4611686018427387903 = max_int`
	- `max_int + 1 = -4611686018427387904 = min_int`
	There is integer rollover
5. What happens when you try to evaluate the expression `1/0`? Why?
	- `1/0` -> `Exception: Division_by_zero`
	- Division by `0` is nonsensical so an Exception is thrown
6. Can you discover what the `mod` operator does when one or both operands are negative? 
	- `-4 mod 3 = -1` 
	- `4 mod -3 = 1
	- `-4 mod -3 = -1`
	- OCaml uses truncated division (rounding towards 0)
	What about if the first operand is zero?
	- `0 mod 3 = 0`
	What about if the second operand is zero?
	- `3 mod 0` -> `Exception: Division_by_zero`
7. Why not just use, for example, the integer `0` to represent false and the integer `1` for true? Why have a separate `bool` type at all?
	- While not strictly necessary, having a `bool` type promotes type safety and could use less memory than needing space for an integer type
8. What is the effect of the comparison operators like `<` and `>` on alphabetic values of type `char`?
	- `'p' < 'q'` -> `true`
	- `'q' < 'p'` -> `false`
		These are evaluated in terms 