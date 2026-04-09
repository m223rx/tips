# 📱 Android Tip #003 — Use `ViewModel`

Separate UI logic from data.

```kotlin id="vm3311"
class MyViewModel : ViewModel() {
    val text = MutableLiveData<String>()
}
```

## Why It's Useful

Survives configuration changes.
