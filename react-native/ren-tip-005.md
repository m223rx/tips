# 📱 React Native Tip #005 — Use `FlatList`

Efficient list rendering.

```javascript
<FlatList
  data={[1,2,3]}
  renderItem={({ item }) => <Text>{item}</Text>}
/>
```

## Why It's Useful

Better performance than ScrollView for large lists.
