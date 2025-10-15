# Logic & Problem Solving

## Q1: 

Here is mys solution in python:
```
def second_largest(nums):
    unique_nums = list(set(nums))
    unique_nums.sort()
    return unique_nums[-2]
```

### My explanation:
I first remove duplicates, then sort the list, and return second last item.

## Q2:
To optimize a page that takes time to load, I would look for obvious problems like:

- Too many large images: TI'd compress or use modern formats like WebP which is a bit lighter.
- Too many requests: I'd combine files, use lazy loading approach to keeep users engaged while waiing, and caching.
- Unoptimized scripts: Minifying scrips like JS/CSS to reduce compiling time and defer non-critical scripts.
