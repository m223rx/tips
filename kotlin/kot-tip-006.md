# 🟣 Kotlin Tip #006 — Default Parameters

Set default values.

```kotlin
fun greet(name: String = "m223rx") {
    println("Hello $name")
}
```

Call:

```kotlin
greet()
```

## Why It's Useful

Avoid method overloading.
