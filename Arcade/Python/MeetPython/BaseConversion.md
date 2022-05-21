## Base Conversion
---
Implement the missing code, denoted by ellipses. You may not modify the pre-existing code.

Your university professor decided to have a little fun and asked the class to implement a function that, given a number `n` and a base `x`, converts the number from base `x` to base `16`. To make things more interesting, he announced that the first student to write the solution will have to answer fewer question than the rest of the class during the final exam.

Laughing devilishly, you asked if it was okay to use a language of your choice, and the unsuspecting professor answered "yes". It's settled then: Python is your language of choice!

Now you're bound to win. Implement a function that, given an integer number `n` and a base `x`, converts `n` from base `x` to base `16`.

Example

For `n = "1302"` and `x = 5`, the output should be\
`solution(n, x) = "ca"`.

Here's why:\
`1302~5~ = 202~10~ = ca~16~`.

Input/Output

-   [execution time limit] 4 seconds (py3)

-   [input] string n

    A valid non-negative integer in base `x`. The string is guaranteed to consist of digits and lowercase English letters.

    *Guaranteed constraints:*\
    `1 < n.length ≤ 10`.

-   [input] integer x

    The base of `n`.

    *Guaranteed constraints:*\
    `2 ≤ x ≤ 36`.

-   [output] string

    The value of `n` in base `16`. The string should contain only digits and lowercase English letters `'a' - 'f'`.
<br>
---
## Solution

```python
def solution(n, x):
    return hex(int(str(n),x))[2:]


```
---
[See on app.codesignal.com](https://app.codesignal.com/arcade/python-arcade/meet-python/u7FW6fpp8Mqxe6sjt)