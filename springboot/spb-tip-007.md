# 🌱 Spring Boot Tip #007 — Use `@PathVariable`

Handle dynamic URLs.

```java
@GetMapping("/user/{id}")
public String user(@PathVariable int id) {
    return "User " + id;
}
```

## Why It's Useful

Create dynamic endpoints.
