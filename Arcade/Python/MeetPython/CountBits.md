## Count Bits
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

    *Guaranteed constraints:*\
    `1 ≤ n ≤ 10^9^`.

-   [output] integer

    The number of bits in binary representation of `n`.


<br>
---
## Solution

```python
def solution(n):
    return n.bit_length()

```
---
[See on app.codesignal.com](https://app.codesignal.com/arcade/python-arcade/meet-python/7bGkfoFf65CiqbX3s)