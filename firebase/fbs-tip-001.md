# 🔥 Firebase Tip #001 — Initialize Firebase

Initialize Firebase in your app.

```javascript
import { initializeApp } from "firebase/app";

const firebaseConfig = {
  apiKey: "YOUR_KEY",
};

const app = initializeApp(firebaseConfig);
```

## Why It's Useful

Required before using Firebase services.
