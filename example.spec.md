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

```js
z.object({
  message: z.literal(),
}).meta({
  message: "OK",
})
```

## Items

### Create Item

Create a new item.

> POST /items

#### Request

- Body

```js
z.object({
  name: z.string().min(1),
  description: z.string().optional(),
}).meta({
  name: "Sample Item",
  description: "This is a sample item.",
})
```

#### Responses

- 201 - Item created successfully.

```js
z.object({
  id: z.string().uuid(),
  name: z.string(),
  description: z.string().optional(),
  createdAt: z.string().datetime(),
  updatedAt: z.string().datetime(),
}).meta({
  id: "123e4567-e89b-12d3-a456-426614174000",
  name: "Sample Item",
  description: "This is a sample item.",
  createdAt: "2024-06-01T12:00:00.000Z",
  updatedAt: "2024-06-01T12:00:00.000Z",
})
```
