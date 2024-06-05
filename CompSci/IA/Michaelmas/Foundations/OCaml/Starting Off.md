An **expression** is any valid OCaml program. OCaml  **evaluates** expressions, yielding **values**.
Each expression (and value) has a **type**. 

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

If we try to use operators with types for which they are not intended, OCaml will not accept the program at all, showing us where our mistake is by underlining it.

``` OCaml
# 1 + true;;
Error: This expression has type bool but an expression was expected of type int
```
