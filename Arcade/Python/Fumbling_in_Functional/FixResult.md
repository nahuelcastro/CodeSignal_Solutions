## Fix Result
---


Your teacher asked you to implement a function that calculates the Answer to the Ultimate Question of Life, the Universe, and Everything and returns it as an array of integers. After several hours of hardcore coding you managed to write such a function, and it produced a quite reasonable `result`. However, when you decided to compare your answer with results of your classmates, you discovered that the elements of your `result` are roughly `10` times greater than the ones your peers got.

You don't have time to investigate the problem, so you need to implement a function that will fix the given array for you. Given `result`, return an array of the same length, where the `i^th^` element is equal to the `i^th^` element of `result` with the last digit dropped.

Example

For `result = [42, 239, 365, 50]`, the output should be\
`solution(result) = [4, 23, 36, 5]`.

Input/Output

-   [execution time limit] 4 seconds (py3)

-   [input] array.integer result

    The result your function produced, where each element is greater than `9`.

    *Guaranteed constraints:*\
    `0 ≤ result.length ≤ 15`,\
    `10 ≤ result[i] ≤ 10^5^`.

-   [output] array.integer

    Array consisting of elements of `result` with last digits dropped.


<br>

---
## Solution

```python
def solution(result):
    def fix(x):
        return x // 10

    return list(map(fix, result))

```
---
[See on app.codesignal.com](https://app.codesignal.com/arcade/python-arcade/fumbling-in-functional/TjCNTwysvW6za5Qh4)