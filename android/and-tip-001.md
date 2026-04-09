# 📱 Android Tip #001 — Use `ViewBinding`

Avoid `findViewById`.

```kotlin id="a1vbd1"
val binding = ActivityMainBinding.inflate(layoutInflater)
setContentView(binding.root)

binding.textView.text = "Hello m223rx"
```

## Why It's Useful

Safer and cleaner UI access.
