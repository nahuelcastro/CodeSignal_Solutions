## The Hashtag Generator

The marketing team is spending way too much time typing in hashtags.\
Let's help them with our own Hashtag Generator!

Here's the deal:

-   It must start with a hashtag (`#`).
-   All words must have their first letter capitalized.
-   If the final result is longer than 140 chars it must return `false`.
-   If the input or the result is an empty string it must return `false`.

Examples
--------

```python
" Hello there thanks for trying my Kata"  =>  "#HelloThereThanksForTryingMyKata"
"    Hello     World   "                  =>  "#HelloWorld"
""                                        =>  false

```

`
`
---

### Given Code


```python
def generate_hashtag(s):
    pass
```

---

### Solution

```python
def generate_hashtag(s):
    if (s == '' or s == ' '):
        return False
    res = s.title()
    res = res.replace(" ", "")
    res = '#' + res
    if (len(res) > 140):
        return False
    return res
```


---


[See on CodeWars.com](https://www.codewars.com/kata/52449b062fb80683ec000024)