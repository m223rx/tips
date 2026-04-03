# ⚛️ React Tip #004 — Conditional Rendering

Render elements conditionally.

```javascript id="rx004"
function Status({ isOnline }) {
  return <p>{isOnline ? "Online" : "Offline"}</p>;
}
```

## Why It's Useful

Displays UI based on state or props.
