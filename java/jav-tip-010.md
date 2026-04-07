# ☕ Java Tip #010 — Use Lambda Expressions

Simplify anonymous classes.

```java
Runnable r = () -> System.out.println("Hello m223rx");

new Thread(r).start();
```

## Why It's Useful

Cleaner and modern Java code.
