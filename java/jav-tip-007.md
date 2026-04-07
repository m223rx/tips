# ☕ Java Tip #007 — Use `StringBuilder`

Efficient string concatenation.

```java
StringBuilder sb = new StringBuilder();
sb.append("Hello ");
sb.append("m223rx");

System.out.println(sb.toString());
```

## Why It's Useful

Better performance than `+`.
