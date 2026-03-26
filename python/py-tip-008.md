# 🐍 Python Tip #008 — Dictionary Get

Use `.get()` to avoid errors.

## Example

```python
user = {"name": "m223rx"}

print(user.get("age", "Not Found"))
```

## Output

```
Not Found
```

## Why It's Useful

Prevents `KeyError`.
