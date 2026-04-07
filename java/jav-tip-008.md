# ☕ Java Tip #008 — Use `switch` Expressions (Java 14+)

Cleaner switch statements.

```java
int day = 2;

String name = switch (day) {
    case 1 -> "Monday";
    case 2 -> "Tuesday";
    default -> "Other";
};
```

## Why It's Useful

Cleaner and modern Java.
