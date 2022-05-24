## College Courses
---


John has just entered a college, and should now pick several courses to take. He knows nothing, except that number x is a bad luck for him, which is why he won't even consider courses whose title consist of x letters.

Given a list of courses, remove the courses with titles consisting of x letters and return the result.

Example

For x = 7 and
courses = ["Art", "Finance", "Business", "Speech", "History", "Writing", "Statistics"],
the output should be
solution(x, courses) = ["Art", "Business", "Speech", "Statistics"].

Input/Output

[execution time limit] 4 seconds (py3)

[input] integer x

John's unlucky number.

Guaranteed constraints:
5 ≤ x ≤ 15.

[input] array.string courses

The list of courses.

Guaranteed constraints:
0 ≤ courses.length ≤ 50,
3 ≤ courses[i].length ≤ 25.

[output] array.string

The courses John should consider.


<br>

---
## Solution

```python
def solution(x, courses):
    def shouldConsider(course):
        return len(course) != x

    return list(filter(shouldConsider, courses))

```
---
[See on app.codesignal.com](https://app.codesignal.com/arcade/python-arcade/fumbling-in-functional/hJqXodrjeBDPZPZRn)