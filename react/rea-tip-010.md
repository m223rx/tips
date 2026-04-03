# ⚛️ React Tip #010 — Lift State Up

Share state between components by lifting it to a common parent.

```javascript id="rx010"
function Parent() {
  const [name, setName] = useState("");

  return (
    <>
      <Input name={name} setName={setName} />
      <Display name={name} />
    </>
  );
}

function Input({ name, setName }) {
  return <input value={name} onChange={e => setName(e.target.value)} />;
}

function Display({ name }) {
  return <p>Hello, {name}</p>;
}
```

## Why It's Useful

Synchronizes state across multiple components.
