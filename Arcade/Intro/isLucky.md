## Is Lucky
---
Ticket numbers usually consist of an even number of digits. A ticket number is considered lucky if the sum of the first half of the digits is equal to the sum of the second half.

Given a ticket number n, determine if it's lucky or not.

Example

For n = 1230, the output should be
solution(n) = true;
For n = 239017, the output should be
solution(n) = false.
Input/Output

[execution time limit] 4 seconds (py3)

[input] integer n

A ticket number represented as a positive integer with an even number of digits.

Guaranteed constraints:
10 ≤ n < 106.

[output] boolean

true if n is a lucky ticket number, false otherwise.

<br>

---
## Solution

```python
def string_sum(s):
    res = 0
    for c in s:
        res += int(c)        
    return res

def solution(n):
    s = str(n)
    sum1 = string_sum(s[:len(s)//2])
    sum2 = string_sum(s[len(s)//2:])
    return sum1 == sum2
```

---
[See on app.codesignal.com](https://app.codesignal.com/arcade/intro/level-3/3AdBC97QNuhF6RwsQ)



<br>
---
## Solution

```python

```
---
[See on app.codesignal.com]()