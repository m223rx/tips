# 🐍 Python Tip #007 — Remove Duplicates

Use `set()` to remove duplicates.

## Example

```python
numbers = [1, 2, 2, 3, 4, 4]

unique = list(set(numbers))
print(unique)
```

## Output

```
[1, 2, 3, 4]
```

## Why It's Useful

Quick way to remove duplicate values.
