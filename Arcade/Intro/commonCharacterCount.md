## Common Character Count
---
Given two strings, find the number of common characters between them.

Example

For `s1 = "aabcc"` and `s2 = "adcaa"`, the output should be\
`solution(s1, s2) = 3`.

Strings have `3` common characters - `2` "a"s and `1` "c".

Input/Output

-   [execution time limit] 4 seconds (py3)

-   [input] string s1

    A string consisting of lowercase English letters.

    *Guaranteed constraints:*\
    `1 ≤ s1.length < 15`.

-   [input] string s2

    A string consisting of lowercase English letters.

    *Guaranteed constraints:*\
    `1 ≤ s2.length < 15`.

-   [output] integer

<br>

---
## Solution

```python
def solution(s1, s2):
    s1_v = listofzeros = [0] * (255)
    s2_v = listofzeros = [0] * (255)

    for s in s1:
        s1_v[ord(s)] += 1
    for s in s2:
        s2_v[ord(s)] += 1

    count = 0
    for i in range(len(s1_v)):
        count = count + min(s1_v[i], s2_v[i])
    return count


```

---
[See on app.codesignal.com](https://app.codesignal.com/arcade/intro/level-3/JKKuHJknZNj4YGL32)