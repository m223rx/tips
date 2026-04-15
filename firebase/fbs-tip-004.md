# 🔥 Firebase Tip #004 — Get Documents

Fetch data from Firestore.

```javascript
import { getDocs, collection } from "firebase/firestore";

const querySnapshot = await getDocs(collection(db, "users"));
```

## Why It's Useful

Retrieve stored data.
