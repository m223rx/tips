# 🐳 Docker Tip #009 — Port Mapping

Expose container port.

```bash
docker run -p 8080:80 nginx
```

## Why It's Useful

Access container from host.

Example:

```
http://localhost:8080
```
