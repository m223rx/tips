# 🐦 Flutter Tip #005 — Use `ListView.builder`

Efficient list rendering.

```dart
ListView.builder(
  itemCount: 10,
  itemBuilder: (context, index) {
    return Text("Item $index");
  },
)
```

## Why It's Useful

Better performance for large lists.
