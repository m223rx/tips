# ☕ Java Tip #003 — Use `equals()` Not `==`

Compare strings properly.

```java
String name = "m223rx";

if (name.equals("m223rx")) {
    System.out.println("Match");
}
```

## Why It's Useful

`==` compares references, not values.
