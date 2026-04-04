# 🌶️ Flask Tip #004 — Request Data

Access request data.

```python
from flask import request

@app.route("/login", methods=["POST"])
def login():
    username = request.form.get("username")
    return username
```

## Why It's Useful

Handle form submissions.
