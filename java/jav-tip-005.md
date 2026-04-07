# ☕ Java Tip #005 — Use Streams

Process collections easily.

```java
List<String> names = List.of("m223rx", "alex", "john");

names.stream()
     .filter(n -> n.startsWith("m"))
     .forEach(System.out::println);
```

## Why It's Useful

Cleaner and functional code.
