# 🟣 Kotlin Tip #003 — Use Nullable Types

Avoid NullPointerException.

```kotlin
var name: String? = null
```

Safe call:

```kotlin
println(name?.length)
```

## Why It's Useful

Safer null handling.
