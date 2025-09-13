# Markdown to OpenAPI Specification

| Enviornment | URL                            |
| ----------- | ------------------------------ |
| development | http://localhost:3000/api/v1   |
| production  | https://api.example.com/api/v1 |

## System

### Health

Check the health of the system.

> GET /health

#### Responses

- 200 - System is healthy.

```json
{
  "message": "OK"
}
```
