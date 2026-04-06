# 🟣 Kotlin Tip #008 — Use `let`

Safe null handling.

```kotlin
val name: String? = "m223rx"

name?.let {
    println(it)
}
```

## Why It's Useful

Avoid null checks.
