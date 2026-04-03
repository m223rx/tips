# ⚛️ React Tip #002 — Use useState Hook

Manage state in functional components.

```javascript id="rx002"
import { useState } from "react";

function Counter() {
  const [count, setCount] = useState(0);

  return (
    <button onClick={() => setCount(count + 1)}>
      Count: {count}
    </button>
  );
}
```

## Why It's Useful

Easily manage dynamic values.
