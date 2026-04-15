# 🔥 Firebase Tip #003 — Add Document

Insert data into Firestore.

```javascript
import { addDoc, collection } from "firebase/firestore";

await addDoc(collection(db, "users"), {
  name: "m223rx"
});
```

## Why It's Useful

Add data quickly.
