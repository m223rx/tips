# 🌶️ Flask Tip #003 — JSON Response

Return JSON response.

```python
from flask import jsonify

@app.route("/api")
def api():
    return jsonify({"user": "m223rx"})
```

## Why It's Useful

Build APIs quickly.
