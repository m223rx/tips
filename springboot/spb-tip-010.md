# 🌱 Spring Boot Tip #010 — Use `@PostMapping`

Handle POST requests.

```java
@PostMapping("/user")
public String createUser(@RequestBody User user) {
    return user.getName();
}
```

## Why It's Useful

Create REST APIs easily.
