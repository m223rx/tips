# ☕ Java Tip #002 — Use Try-With-Resources

Automatically close resources.

```java
try (BufferedReader br = new BufferedReader(new FileReader("file.txt"))) {
    System.out.println(br.readLine());
}
```

## Why It's Useful

Prevents memory leaks.
