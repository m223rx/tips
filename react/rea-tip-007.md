# ⚛️ React Tip #007 — Key Prop in Lists

Add a `key` when rendering lists.

```javascript id="rx007"
const users = ["m223rx", "Ali", "Sara"];

function UserList() {
  return (
    <ul>
      {users.map((user, index) => (
        <li key={index}>{user}</li>
      ))}
    </ul>
  );
}
```

## Why It's Useful

Helps React identify elements for efficient updates.
