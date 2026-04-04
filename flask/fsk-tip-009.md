# 🌶️ Flask Tip #009 — Environment Variables

Use environment variables.

```python
import os

secret = os.getenv("SECRET_KEY")
```

## Why It's Useful

Secure sensitive data.
