# 🌶️ Flask Tip #007 — Redirect

Redirect users.

```python
from flask import redirect, url_for

@app.route("/home")
def home():
    return redirect(url_for("dashboard"))
```

## Why It's Useful

Control navigation flow.
