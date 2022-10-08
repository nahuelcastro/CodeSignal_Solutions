##

---

Implement the missing code, denoted by ellipses. You may not modify the pre-existing code.

You've been working on a numerical analysis when something went horribly wrong: your solution returned completely unexpected results. It looks like you apply a wrong function at some point of calculation. This part of the program was implemented by your colleague who didn't follow the PEP standards, so it's extremely difficult to comprehend.

To understand what function is applied to `x` instead of the one that should have been applied, you decided to go ahead and compare the result with results of all the functions you could come up with. Given the variable `x` and a list of `functions`, return a list of values `f(x)` for each `x` in `functions`.

Example

For `x = 1` and\
`functions = ["math.sin", "math.cos", "lambda x: x * 2", "lambda x: x ** 2"]`,\
the output should be\
`solution(x, functions) = [0.84147, 0.5403, 2, 1]`.

Input/Output

- [execution time limit] 4 seconds (py3)

- [input] float x

  The value to which the functions should be applied. It is guaranteed to have at most `1` digit after the decimal point.

  _Guaranteed constraints:_\
  `-1000 ≤ x ≤ 1000`.

- [input] array.string functions

  Array of functions. Each function is given as a string. It is guaranteed that the result of applying function `eval` to `functions[i]` produces a valid function for each `i`. It is also guaranteed that `eval(functions[i])` is defined in point `x` for each `i`.

  _Guaranteed constraints:_\
  `1 ≤ functions.length ≤ 10`.

- [output] array.float

  A list of the same length as `functions`, where the `i^th^` element is the result of applying the `i^th^` function to `x`. Your output will be considered correct if its absolute error does not exceed `10^-5^`.

<br>

---

## Solution

```python

def solution(x, functions):
    return [eval(f)(x) for f in functions]


```

---

[See on app.codesignal.com](https://app.codesignal.com/arcade/python-arcade/higher-order-thinking/2wXrvGPGwwEejLXq2)
