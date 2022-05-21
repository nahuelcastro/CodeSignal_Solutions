## Check Palindrome
---

Given a year, return the century it is in. The first century spans from the year 1 up to and including the year 100, the second - from the year 101 up to and including the year 200, etc.

Example

-   For `year = 1905`, the output should be\
    `solution(year) = 20`;
-   For `year = 1700`, the output should bGiven the string, check if it is a [palindrome](keyword://palindrome).

Example

-   For `inputString = "aabaa"`, the output should be\
    `solution(inputString) = true`;
-   For `inputString = "abac"`, the output should be\
    `solution(inputString) = false`;
-   For `inputString = "a"`, the output should be\
    `solution(inputString) = true`.

Input/Output

-   [execution time limit] 4 seconds (py3)

-   [input] string inputString

    A non-empty string consisting of lowercase characters.

    *Guaranteed constraints:*\
    `1 ≤ inputString.length ≤ 10^5^`.

-   [output] boolean

    `true` if `inputString` is a palindrome, `false` otherwise.

-e\
    `solution(year) = 17`.

Input/Output

-   [execution time limit] 4 seconds (py3)

-   [input] integer year

    A positive integer, designating the year.

    *Guaranteed constraints:*\
    `1 ≤ year ≤ 2005`.

-   [output] integer

    The number of the century the year is in.

<br>

---
## Solution

```python
def solution(inputString):
    return inputString == inputString[::-1]
```

---
[See on app.codesignal.com](https://app.codesignal.com/arcade/intro/level-1/s5PbmwxfECC52PWyQ)
