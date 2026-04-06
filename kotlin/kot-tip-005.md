# 🟣 Kotlin Tip #005 — Use Data Classes

Create models easily.

```kotlin
data class User(
    val name: String,
    val age: Int
)
```

## Why It's Useful

Auto generates:

* toString()
* equals()
* hashCode()
