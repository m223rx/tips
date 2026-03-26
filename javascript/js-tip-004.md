# ⚡ JavaScript Tip #004 — Default Parameters

Set default values for function parameters.

```javascript id="js-default"
function greet(name = "Guest") {
  console.log(`Hello, ${name}`);
}

greet();
greet("Ali");
```

**Output:**

```
Hello, Guest
Hello, Ali
```
