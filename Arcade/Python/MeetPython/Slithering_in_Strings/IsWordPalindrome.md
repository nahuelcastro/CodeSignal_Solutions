## Is Word Palindrome?
---
Implement the missing code, denoted by ellipses. You may not modify the pre-existing code.

Given a `word`, check whether it is a *palindrome* or not. A string is considered to be a *palindrome* if it reads the same in both directions.

Example

-   For `word = "aibohphobia"`, the output should be\
    `solution(word) = true`;

-   For `word = "hehehehehe"`, the output should be\
    `solution(word) = false`.

Input/Output

-   [execution time limit] 4 seconds (py3)

-   [input] string word

    A string containing lowercase English letters.

    *Guaranteed constraints:*\
    `1 ≤ word.length ≤ 20`.

-   [output] boolean

    `true` if the given `word` is a *palindrome*, `false` otherwise.
<br>

---
## Solution

```python
def solution(word):
    return word == word[::-1]

```
---
[See on app.codesignal.com](https://app.codesignal.com/arcade/python-arcade/slithering-in-strings/r6xwnEjaw5kNgsyZD)