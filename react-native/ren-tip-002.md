# 📱 React Native Tip #002 — Use `useState`

Manage state in functional components.

```javascript
import React, { useState } from "react";
import { Text, Button } from "react-native";

export default function App() {
  const [count, setCount] = useState(0);

  return (
    <>
      <Text>{count}</Text>
      <Button title="Add" onPress={() => setCount(count + 1)} />
    </>
  );
}
```

## Why It's Useful

Handles dynamic UI updates.
