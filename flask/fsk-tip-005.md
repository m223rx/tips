# 🌶️ Flask Tip #005 — Templates

Use HTML templates.

```python
from flask import render_template

@app.route("/")
def home():
    return render_template("index.html")
```

## Why It's Useful

Separate frontend and backend.
