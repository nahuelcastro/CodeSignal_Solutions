## First Not Repeating Character
---
Given a string `s` consisting of small English letters, find and return the first instance of a non-repeating character in it. If there is no such character, return `'_'`.

Example

-   For `s = "abacabad"`, the output should be\
    `solution(s) = 'c'`.

    There are `2` non-repeating characters in the string: `'c'` and `'d'`. Return `c` since it appears in the string first.

-   For `s = "abacabaabacaba"`, the output should be\
    `solution(s) = '_'`.

    There are no characters in this string that do not repeat.

Input/Output

-   [execution time limit] 0.5 seconds (cpp)

-   [input] string s

    A string that contains only lowercase English letters.

    *Guaranteed constraints:*\
    `1 ≤ s.length ≤ 10^5^`.

-   [output] char

    The first non-repeating character in `s`, or `'_'` if there are no characters that do not repeat.

[C++] Syntax Tips

```
// Prints help message to the console
// Returns a string
string helloWorld(string name) {
    cout << "This prints to the console when you Run Tests" << endl;
    return "Hello, " + name;
}

```

<br>


---
## Solution

```c++
char solution(string s) {
    int counting[26] = {};
    for (int i = 0; i < s.size(); i++) {
        counting[int(s[i]) - 97] ++;
    }
    
    for (int i = 0; i < s.size(); i++) {
        if(counting[int(s[i]) - 97] == 1){
            return s[i];
        }
    }
    
    return '_';
}
```


---
[See on app.codesignal.com](https://app.codesignal.com/interview-practice/task/uX5iLwhc6L5ckSyNC/description)
