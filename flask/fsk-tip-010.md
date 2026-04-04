# 🌶️ Flask Tip #010 — Blueprints

Organize large applications.

```python
from flask import Blueprint

auth = Blueprint("auth", __name__)

@auth.route("/login")
def login():
    return "Login"
```

## Why It's Useful

Structure large Flask apps cleanly.
