## Sign
---


Although Python does provide a bunch of useful built-in functions, some of them are simply missing for no apparent reason. One example of such function is a `solution` function implemented in many other languages. `solution(x)` returns `1` if `x` is positive, `-1` if `x` is negative, and `0` if `x` is equal to zero.

You decided to build your own package of useful functions, and would like to start with the `solution` function. Given the value of `x`, return the result of applying the `solution` function to it.

Example

For `x = -34`, the output should be\
`solution(x) = -1`.

`-34` is a negative number, thus the output should be `-1`.

Input/Output

-   [execution time limit] 4 seconds (py3)

-   [input] integer x

    The argument of the `sign` function.

    *Guaranteed constraints:*\
    `-50 ≤ x ≤ 50`.

-   [output] integer

    The value of `sign(x)`.


<br>

---
## Solution

```python
class Functions(object):
    
    def solution(x) -> int:
        if x > 0: return 1
        elif x < 0: return -1
        return 0
        
def solution(x):
    return Functions.solution(x)

```
---
[See on app.codesignal.com](https://app.codesignal.com/arcade/python-arcade/showing-class/bBdHSPDLc9W7mzjFY)