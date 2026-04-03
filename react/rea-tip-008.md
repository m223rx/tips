# ⚛️ React Tip #008 — Use Fragments

Wrap multiple elements without extra nodes.

```javascript id="rx008"
import { Fragment } from "react";

function Example() {
  return (
    <Fragment>
      <p>Hello</p>
      <p>m223rx</p>
    </Fragment>
  );
}
```

## Why It's Useful

Avoids unnecessary divs and keeps DOM clean.
