# 🌶️ Flask Tip #001 — Basic Flask App

Create a simple Flask app.

```python
from flask import Flask

app = Flask(__name__)

@app.route("/")
def home():
    return "Hello, m223rx!"

if __name__ == "__main__":
    app.run(debug=True)
```

## Why It's Useful

Start building Flask apps quickly.
