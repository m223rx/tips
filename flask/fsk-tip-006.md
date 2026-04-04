# 🌶️ Flask Tip #006 — Static Files

Use static files.

Folder structure:

```
static/
  style.css
```

HTML:

```html
<link rel="stylesheet" href="{{ url_for('static', filename='style.css') }}">
```

## Why It's Useful

Serve CSS, JS, and images.
