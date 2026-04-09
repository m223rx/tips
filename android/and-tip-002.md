# 📱 Android Tip #002 — Use `LiveData`

Observe data changes.

```kotlin id="l2vd21"
val data = MutableLiveData<String>()

data.observe(this) { value ->
    println(value)
}
```

## Why It's Useful

Automatically updates UI when data changes.
