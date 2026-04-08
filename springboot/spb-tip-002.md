# 🌱 Spring Boot Tip #002 — Use `@RestController`

Create REST APIs quickly.

```java
@RestController
public class HelloController {

    @GetMapping("/")
    public String hello() {
        return "Hello m223rx";
    }
}
```

## Why It's Useful

Automatically returns JSON or text.
