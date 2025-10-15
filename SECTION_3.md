# Q5: Debugging & Reasoning

- The problem: Modifying the list while iterating causes skipped items.

- The wrong output: [1, 2, 4]

- Here is my fix: (in python)

```
numbers = [1, 2, 3, 4, 5]
numbers = [n for n in numbers if n % 2 != 0]
print(numbers)
```
