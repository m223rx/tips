# ⚡ JavaScript Tip #006 — Short-Circuit Evaluation

Use `||` and `&&` for default values and conditions.

```javascript id="js-short"
const name = null;
console.log(name || "Guest");  // Outputs "Guest"

const isLoggedIn = true;
isLoggedIn && console.log("Welcome back!");
```
