# ⚛️ React Tip #009 — Controlled Components

Control input values with state.

```javascript id="rx009"
import { useState } from "react";

function NameInput() {
  const [name, setName] = useState("");

  return (
    <input
      value={name}
      onChange={e => setName(e.target.value)}
      placeholder="Enter name"
    />
  );
}
```

## Why It's Useful

Enables validation and dynamic input handling.
