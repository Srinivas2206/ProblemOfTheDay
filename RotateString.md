# 796. Rotate String

## Problem
Given two strings s and goal, return true if and only if s can become goal after some number of shifts on s.

A shift on s consists of moving the leftmost character of s to the rightmost position.

For example, if s = "abcde", then it will be "bcdea" after one shift.

## Example 1:
Input: s = "abcde", goal = "cdeab"
Output: true
## Example 2:

Input: s = "abcde", goal = "abced"
Output: false

## Constraints:

1 <= s.length, goal.length <= 100
s and goal consist of lowercase English letters.

## My Approach

- I have taken a simple for loop to iterate n times over the string s, where n is the length of the string s.
- In each iteration, I have taken if statement to check if s is same as goal string and it will return true if the condition satisfies.
- Then under the else statement i shifted the leftmost character to the rightmost position using string slicing.
- After all iterations completed, then it will return false as "s" cannot become "goal".

```Python3
def rotateString(s, goal):
    n = len(s)
    for i in range(n):
        if s == goal:
            return True
        else:
            s = s[1:]+s[0]
    return False
s ="abcde"
goal = "cdeab"
print(rotateString(s,goal))
```

