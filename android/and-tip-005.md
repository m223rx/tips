# 📱 Android Tip #005 — Use `CoroutineScope`

Handle async tasks.

```kotlin id="co5515"
lifecycleScope.launch {
    val data = fetchData()
}
```

## Why It's Useful

Avoid blocking the main thread.
