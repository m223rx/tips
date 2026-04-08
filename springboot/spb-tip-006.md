# 🌱 Spring Boot Tip #006 — Use `@RequestParam`

Handle query parameters.

```java
@GetMapping("/user")
public String user(@RequestParam String name) {
    return name;
}
```

Example:

```
/user?name=m223rx
```

## Why It's Useful

Easy request handling.
