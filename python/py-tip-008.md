# 🐍 Python Tip #008 — Dictionary Get

Use `.get()` to avoid errors.

## Example

```python
user = {"name": "Mohamed"}

print(user.get("age", "Not Found"))
```

## Output

```
Not Found
```

## Why It's Useful

Prevents `KeyError`.
