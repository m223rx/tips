# ⚡ JavaScript Tip #001 — Swap Variables

Swap variables without a temporary variable using array destructuring.

```javascript id="js-swap"
let a = 5;
let b = 10;

[a, b] = [b, a];
console.log(a, b);
```

**Output:**

```
10 5
```
