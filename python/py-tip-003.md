# 🐍 Python Tip #003 — Enumerate

Use `enumerate()` to get index and value together.

## Example

```python
names = ["Ali", "John", "Sara"]

for index, name in enumerate(names):
    print(index, name)
```

## Output

```
0 Ali
1 John
2 Sara
```

## Why It's Useful

Cleaner than manually managing index counters.
