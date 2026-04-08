# 🌱 Spring Boot Tip #001 — Use `@SpringBootApplication`

Start your Spring Boot app easily.

```java
@SpringBootApplication
public class App {
    public static void main(String[] args) {
        SpringApplication.run(App.class, args);
    }
}
```

## Why It's Useful

Combines:

* @Configuration
* @EnableAutoConfiguration
* @ComponentScan
