# 🟣 Kotlin Tip #007 — Extension Functions

Add functions to existing classes.

```kotlin
fun String.hello() {
    println("Hello $this")
}

"m223rx".hello()
```

## Why It's Useful

Cleaner utility functions.
