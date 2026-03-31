# 🗄️ SQL Tip #009 — Group Results

Group data using `GROUP BY`.

```sql
SELECT role, COUNT(*)
FROM users
GROUP BY role;
```

## Why It's Useful

Aggregate data by categories.
