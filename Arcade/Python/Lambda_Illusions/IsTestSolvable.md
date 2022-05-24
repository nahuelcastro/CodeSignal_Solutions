## Is Test Solvable
---


You've been preparing all night for the upcoming test and entered the class certain that you will ace it. Now that you received the test questions, you died inside a little: looks like you prepared for the test on a completely different topic.

You're not even sure if you should bother to answer the questions. You still have some hope though: it is known that there's a glitch in the test preparing system, so that if the sum of digits of question ids is divisible by `k`, the answer to each question has a `90%` probability to be an A.

Given the list of question `ids`, determine if the sum of their digits is divisible by `k` to see if it's worth trying to pass the test.

Example

For `ids = [529665, 909767, 644200]` and `k = 3`, the output should be\
`solution(ids, k) = true`.

The sum of digits is

```
(5 + 2 + 9 + 6 + 6 + 5) + (9 + 0 + 9 + 7 + 6 + 7) + (6 + 4 + 4 + 2 + 0 + 0) = 87

```

which is divisible by `3`. Today is your lucky day after all!

Input/Output

-   [execution time limit] 4 seconds (py3)

-   [input] array.integer ids

    Array of unique question ids.

    *Guaranteed constraints:*\
    `1 ≤ ids.length ≤ 50`,\
    `0 ≤ ids[i] ≤ 10^6^`.

-   [input] integer k

    The number that causes a glitch in the test preparing system.

    *Guaranteed constraints:*\
    `2 ≤ k ≤ 10`.

-   [output] boolean

    `true` if the total sum of digits in `ids` is divisible by `k`, `false` otherwise.


<br>

---
## Solution

```python
def solution(ids, k):
    digitSum = lambda q: sum( int(x) for x in str(q))

    sm = 0
    for questionId in ids:
        sm += digitSum(questionId)
    return sm % k == 0

```
---
[See on app.codesignal.com](https://app.codesignal.com/arcade/python-arcade/lambda-illusions/eP7hJDmLdZym2Kdo3)