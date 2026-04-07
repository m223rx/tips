# ☕ Java Tip #004 — Use `Optional`

Avoid NullPointerException.

```java
Optional<String> name = Optional.of("m223rx");

name.ifPresent(System.out::println);
```

## Why It's Useful

Safer null handling.
