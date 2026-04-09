# 📱 Android Tip #006 — Use `Room Database`

Local storage made easy.

```kotlin id="rm6616"
@Dao
interface UserDao {
    @Query("SELECT * FROM user")
    fun getAll(): List<User>
}
```

## Why It's Useful

Simplifies SQLite usage.
