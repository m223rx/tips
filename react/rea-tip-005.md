# ⚛️ React Tip #005 — Event Handling

Use event handlers in JSX.

```javascript id="rx005"
function ClickMe() {
  const handleClick = () => alert("Clicked!");
  return <button onClick={handleClick}>Click Me</button>;
}
```

## Why It's Useful

Adds interactivity to your components.
