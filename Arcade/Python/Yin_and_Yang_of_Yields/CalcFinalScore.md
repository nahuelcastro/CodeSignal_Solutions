##

---

Implement the missing code, denoted by ellipses. You may not modify the pre-existing code.

You are working on a revolutionary video game. This game will consist of several levels, and on each level the player will be able to collect bonuses. For each passed level the player will thus get some score, determined by the number of collected bonuses.

Player's final score is decided by the number of completed levels and scores obtained on each of them. The final score is calculated as the sum of squares of `n` maximum scores obtained. If the number of completed levels is less than `n`, the score is calculated as the sum of squared scores for each level, and final result is divided by `5` as a penalty (the result is rounded down to the nearest integer).

Given the list of `scores` the player got for completed levels and the number `n` that determines the number of levels you have to pass to avoid being penalized, return the player's final game score.

Example

- For `scores = [4, 2, 4, 5]` and `n = 3`,\
  the output should be\
  `solution(scores, n) = 57`.

  `5^2^ + 4^2^ + 4^2^ = 57`.

- For `scores = [4, 2, 4, 5]` and `n = 5`,\
  the output should be\
  `solution(scores, n) = 12`.

  `(4^2^ + 2^2^ + 4^2^ + 5^2^) / 5 = 61 / 5 ≈ 12`.

Input/Output

- [execution time limit] 4 seconds (py3)

- [input] array.integer scores

  A list of scores the player obtained.

  _Guaranteed constraints:_\
  `0 ≤ scores.length ≤ 20`,\
  `0 ≤ scores[i] ≤ 50`.

- [input] integer n

  The number of levels that should be completed in order not to receive a penalty.

  _Guaranteed constraints:_\
  `1 ≤ n ≤ 20`.

- [output] integer

  The final score.

<br>

---

## Solution

```python

def solution(scores, n):
    gen = iter( x**2 for x in sorted(scores, reverse=True))

    res = 0
    try:
        for _ in range(n):
            res += next(gen)
    except StopIteration:
        res //= 5

    return res

```

---

[See on app.codesignal.com](https://app.codesignal.com/arcade/python-arcade/yin-and-yang/4ReLEsLE6SDZkXDzK)
