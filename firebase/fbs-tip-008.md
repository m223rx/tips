# 🔥 Firebase Tip #008 — Real-time Listener

Listen for data changes.

```javascript
import { onSnapshot, collection } from "firebase/firestore";

onSnapshot(collection(db, "users"), (snapshot) => {
  console.log(snapshot.docs);
});
```

## Why It's Useful

Real-time updates.
