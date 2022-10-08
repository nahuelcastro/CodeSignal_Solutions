##

---

Implement the missing code, denoted by ellipses. You may not modify the pre-existing code.

You are working on a revolutionary video game. In this game the player will be able to collect several types of bonuses on each level, and his total score for the level is equal to the sum of the first `n` `bonuses` he collected. However, if he collects less than `n` bonuses, his score will be equal to `0`.

Given the `bonuses` the player got, your task is to return his final score for the level.

Example

- For `bonuses = [4, 2, 4, 5]` and `n = 3`,\
  the output should be\
  `solution(bonuses, n) = 10`.

  `4 + 2 + 4 = 10`.

- For `bonuses = [4, 2, 4, 5]` and `n = 5`,\
  the output should be\
  `solution(bonuses, n) = 0`.

  The player has collected only `4` bonuses, so his final score is `0`.

Input/Output

- [execution time limit] 4 seconds (py3)

- [input] array.integer bonuses

  A list of bonuses the player collected.

  _Guaranteed constraints:_\
  `0 ≤ bonuses.length ≤ 20`,\
  `0 ≤ bonuses[i] ≤ 50`.

- [input] integer n

  The number of bonuses that should be collected to obtain non-zero final score.

  _Guaranteed constraints:_\
  `1 ≤ n ≤ 20`.

- [output] integer

  Final score for the level.

<br>

---

## Solution

```python

def solution(bonuses, n):
    it = iter(bonuses)
    res = 0

    try:
        for _ in range(n):
            res += next(it)
    except StopIteration:
        res = 0

    return res



```

---

[See on app.codesignal.com](https://app.codesignal.com/arcade/python-arcade/yin-and-yang/4ReLEsLE6SDZkXDzK)
