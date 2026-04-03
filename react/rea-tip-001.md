# ⚛️ React Tip #001 — Use Functional Components

Functional components are simpler and easier to read.

```javascript id="rx001"
function Greeting({ name }) {
  return <h1>Hello, {name}!</h1>;
}

// Usage
<Greeting name="m223rx" />
```

## Why It's Useful

Less boilerplate and easier to maintain.
