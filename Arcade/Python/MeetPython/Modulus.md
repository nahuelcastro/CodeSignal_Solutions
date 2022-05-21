## Modulus
---
Implement the missing code, denoted by ellipses. You may not modify the pre-existing code.

Implement a function that, given an integer `n`, uses a specific method on it and returns the number of bits in its binary representation.

*Note: in this task and most of the following tasks you will be given a code snippet with some part of it replaced by the ellipsis (`...`). Only this part is allowed to be changed.*

Example

For `n = 50`, the output should be\
`solution(n) = 6`.

`50~10~ = 110010~2~`, a number that consists of `6` digits. Thus, the output should be `6`.

Input/Output

-   [execution time limit] 4 seconds (py3)

-   [input] integer n

    A positive integer.
Implement the missing code, denoted by ellipses. You may not modify the pre-existing code.

It frustrates you more than you'd like to admit that the solution operator in Python can be applied to non-integer values. When you write code, you expect the result of the solution operator to always be an integer, but thanks to Python this isn't always the case.

To fix this, you've decided to write your own solution operator as a function. Your task is to implement a function that, given a number `n`, returns `-1` if this number is not an integer and `n % 2` otherwise. It is guaranteed that if the number represents an integer, it will be written without a decimal point.

Example

-   For `n = 15`, the output should be\
    `solution(n) = 1`;

-   For `n = 23.12`, the output should be\
    `solution(n) = -1`.

Input/Output

-   [execution time limit] 4 seconds (py3)

-   [input] numeric n

    A non-negative number that can be an `int`, a `float`, or a `long`.

    *Guaranteed constraints:*\
    `0 ≤ n ≤ 1000`.

-   [output] integer

    Return `n % 2` if `n` is an integer, otherwise return `-1`.

-
    *Guaranteed constraints:*\
    `1 ≤ n ≤ 10^9^`.

-   [output] integer

    The number of bits in binary representation of `n`.

    <br>
---
## Solution

```python
def solution(n):
    if n % 1 == 0:
        return n % 2
    else:
        return -1

```
---
[See on app.codesignal.com](https://app.codesignal.com/arcade/python-arcade/meet-python/mygD2J9yDbRmtKW8T)