# 🟣 Kotlin Tip #004 — Use `when` Instead of `switch`

Kotlin uses `when`.

```kotlin
val number = 2

when (number) {
    1 -> println("One")
    2 -> println("Two")
    else -> println("Other")
}
```

## Why It's Useful

More powerful than switch.
