# 🌶️ Flask Tip #002 — Route Parameters

Use dynamic routes.

```python
@app.route("/user/<name>")
def user(name):
    return f"Hello, {name}"
```

Visit:

```
/user/m223rx
```

## Why It's Useful

Create dynamic URLs easily.
