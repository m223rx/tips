# 🐍 Python Tip #009 — Zip Lists

Use `zip()` to iterate multiple lists.

## Example

```python
names = ["Ali", "John"]
ages = [20, 25]

for name, age in zip(names, ages):
    print(name, age)
```

## Output

```
Ali 20
John 25
```

## Why It's Useful

Cleaner multi-list iteration.
