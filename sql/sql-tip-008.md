# 🗄️ SQL Tip #008 — Use JOIN

Combine tables using JOIN.

```sql
SELECT users.name, posts.title
FROM users
JOIN posts ON users.id = posts.user_id;
```

## Why It's Useful

Retrieve related data from multiple tables.
