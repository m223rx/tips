# 🌱 Spring Boot Tip #009 — Use `@Entity`

Create database models.

```java
@Entity
public class User {

    @Id
    @GeneratedValue
    private Long id;

    private String name;
}
```

## Why It's Useful

Map Java objects to database tables.
