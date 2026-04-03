# ⚛️ React Tip #003 — Use useEffect Hook

Perform side effects in functional components.

```javascript id="rx003"
import { useEffect } from "react";

useEffect(() => {
  console.log("Component mounted!");
}, []); // Empty dependency = run once
```

## Why It's Useful

Handle API calls, subscriptions, or events.
