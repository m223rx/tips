# Challenge: Custom HashMap Implementation in Java

## Difficulty
Medium

## Description
Design and implement your own version of a hash map (associative array) in Java without using any of the built‑in collection classes such as `java.util.HashMap`, `java.util.Hashtable`, or `java.util.concurrent.ConcurrentHashMap`.  

Your custom hash map should store key‑value pairs where keys are **non‑null** objects of any type that correctly implement `hashCode()` and `equals()`, and values can be any object (including `null`). The implementation must handle collisions using **separate chaining** (linked lists or dynamic arrays) and should dynamically resize (rehash) when the load factor exceeds a specified threshold.

The public API should closely resemble that of `java.util.Map<K,V>` for the subset of operations listed in the **Requirements** section.

## Requirements
- Create a generic class `CustomHashMap<K, V>` with the following public methods:
  - `int size()`: returns the number of key‑value pairs stored.
  - `boolean isEmpty()`: returns `true` if the map contains no entries.
  - `V get(Object key)`: returns the value associated with the given key, or `null` if the key is not present.
  - `V put(K key, V value)`: inserts the key‑value pair into the map. If the key already exists, replace its value and return the old value; otherwise, return `null`.
  - `V remove(Object key)`: removes the entry for the specified key and returns its associated value, or `null` if the key was not present.
  - `boolean containsKey(Object key)`: returns `true` if the map contains the given key.
  - `boolean containsValue(Object value)`: returns `true` if at least one entry maps to the given value.
  - `Set<K> keySet()`: returns a `Set` view of the keys contained in the map.
  - `Collection<V> values()`: returns a `Collection` view of the values contained in the map.
  - `Set<Map.Entry<K, V>> entrySet()`: returns a `Set` view of the key‑value mappings.
- Implement **separate chaining** for collision resolution. Each bucket should maintain a dynamic list of entries.
- The map must **automatically resize** (rehash) when the load factor (size / number of buckets) exceeds **0.75**. Upon resizing, the number of buckets should double.
- Throw an `IllegalArgumentException` if a `null` key is supplied to any method that requires a key.
- The `keySet()`, `values()`, and `entrySet()` collections must reflect live changes to the map (i.e., modifications to the map should be visible through these views and vice‑versa where applicable).
- The implementation must be **thread‑unsafe** (no synchronization required).

## Bonus
- Implement an efficient `Iterator` for the `entrySet()` that supports the optional `remove()` operation.
- Provide an overload of `put(K key, V value, boolean replaceIfExists)` where `replaceIfExists` controls whether an existing entry should be overwritten.
- Add a constructor that allows the initial capacity and load factor to be specified.
- Implement the `java.io.Serializable` interface for `CustomHashMap` and ensure proper serialization of its contents.
    


---
**Author:** m223rx
**Date:** 2026-03-28 13:41:07
---
    


    