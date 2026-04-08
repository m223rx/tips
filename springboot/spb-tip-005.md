# 🌱 Spring Boot Tip #005 — Use `@Repository`

Create database repositories.

```java
@Repository
public interface UserRepository extends JpaRepository<User, Long> {
}
```

## Why It's Useful

Simplifies database access.
