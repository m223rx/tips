# ⚛️ React Tip #006 — Pass Props

Pass data to child components.

```javascript id="rx006"
function Child({ name }) {
  return <p>Hello, {name}</p>;
}

function Parent() {
  return <Child name="m223rx" />;
}
```

## Why It's Useful

Enables reusable and dynamic components.
