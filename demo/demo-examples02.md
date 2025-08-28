## 💉 SQL Injection Demo (Mobile App)

- Vulnerable Code

```java
Cursor c = db.rawQuery("SELECT * FROM users WHERE username = '" + input + "'", null);
```

- Exploit

Input:

```bash
' OR '1'='1
```

## Result

- Query returns all users instead of just one.

- Sensitive info (emails, passwords) leaked.

## Defense

- Use parameterized queries:

```java
Cursor c = db.rawQuery("SELECT * FROM users WHERE username = ?", new String[]{ input });
```
