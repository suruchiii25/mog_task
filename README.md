# Longest Valid Parentheses

## Problem Statement

Given a string containing only the characters `(` and `)`, determine the length of the longest valid (well-formed) parentheses substring.

### Example 1

**Input**

```text
(()
```

**Output**

```text
2
```

**Explanation**

The longest valid parentheses substring is `()`.

---

### Example 2

**Input**

```text
)()())
```

**Output**

```text
4
```

**Explanation**

The longest valid parentheses substring is `()()`.

---

### Example 3

**Input**

```text

```

**Output**

```text
0
```

---

## Approach

This solution uses a **stack** to store the indices of parentheses.

- Initialize the stack with `-1` to act as the base index.
- For every opening parenthesis `(`, push its index onto the stack.
- For every closing parenthesis `)`:
  - Pop the top element.
  - If the stack becomes empty, push the current index as the new base.
  - Otherwise, calculate the length of the current valid substring using the difference between the current index and the top of the stack.
- Keep track of the maximum valid substring length encountered.

---

## Algorithm

1. Push `-1` onto the stack.
2. Traverse the string from left to right.
3. If the current character is `(`, push its index.
4. Otherwise:
   - Pop the top index.
   - If the stack is empty, push the current index.
   - Else, update the maximum length.
5. Return the maximum length.

---

## Time Complexity

**O(n)**

where `n` is the length of the string.

---

## Space Complexity

**O(n)**

due to the stack used to store indices.

---

## How to Run

### Compile

```bash
g++ mogliccode.cpp -o mogliccode
```

### Execute

**Windows (PowerShell)**

```bash
.\mogliccode.exe
```

**Linux/macOS**

```bash
./mogliccode
```

---

## Language

- C++
