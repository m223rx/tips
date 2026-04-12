# 🐦 Flutter Tip #009 — Use `FutureBuilder`

Handle async data.

```dart
FutureBuilder(
  future: fetchData(),
  builder: (context, snapshot) {
    return Text("Loading...");
  },
)
```

## Why It's Useful

Async UI handling.
