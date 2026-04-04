# 🌶️ Flask Tip #008 — Error Handling

Handle errors.

```python
@app.errorhandler(404)
def not_found(error):
    return "Page not found", 404
```

## Why It's Useful

Improve user experience.
