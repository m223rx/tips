# 🐍 Python Tip #001 — Swap Variables

You can swap variables without using a temporary variable.

## Example

```python
a = 5
b = 10

a, b = b, a

print(a, b)
```

## Output

```
10 5
```

## Why It's Useful

Cleaner and more Pythonic than using a temporary variable.
