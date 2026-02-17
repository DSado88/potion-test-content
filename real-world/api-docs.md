# API Reference

## Authentication

All endpoints require a Bearer token in the `Authorization` header.

```
Authorization: Bearer <your-api-token>
```

### POST /auth/login

**Request:**
```json
{
  "email": "user@example.com",
  "password": "secret123"
}
```

**Response (200):**
```json
{
  "token": "eyJhbGciOiJIUzI1NiIs...",
  "expires_at": "2026-02-18T16:00:00Z",
  "user": {
    "id": "usr_abc123",
    "email": "user@example.com",
    "name": "Test User"
  }
}
```

**Error (401):**
```json
{
  "error": "invalid_credentials",
  "message": "Email or password is incorrect"
}
```

---

## Users

### GET /users

List all users (paginated).

**Query Parameters:**

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| `page` | integer | 1 | Page number |
| `per_page` | integer | 20 | Items per page (max 100) |
| `sort` | string | `created_at` | Sort field |
| `order` | string | `desc` | Sort order (`asc` or `desc`) |
| `status` | string | - | Filter by status: `active`, `inactive`, `pending` |

**Response (200):**
```json
{
  "data": [
    {
      "id": "usr_abc123",
      "email": "alice@example.com",
      "name": "Alice Johnson",
      "status": "active",
      "created_at": "2025-01-15T10:30:00Z"
    }
  ],
  "pagination": {
    "page": 1,
    "per_page": 20,
    "total": 150,
    "total_pages": 8
  }
}
```

### GET /users/:id

Get a single user by ID.

### POST /users

Create a new user.

**Request:**
```json
{
  "email": "newuser@example.com",
  "name": "New User",
  "role": "member"
}
```

### PATCH /users/:id

Update a user.

### DELETE /users/:id

Delete a user. Returns `204 No Content` on success.

> [!WARNING]
> Deleting a user is **irreversible**. All associated data will be permanently removed.

---

## Rate Limits

| Endpoint | Limit | Window |
|----------|-------|--------|
| `/auth/*` | 10 req | 1 minute |
| `GET /*` | 1000 req | 1 hour |
| `POST /*` | 100 req | 1 hour |
| `DELETE /*` | 50 req | 1 hour |

Rate limit headers are included in every response:

```
X-RateLimit-Limit: 1000
X-RateLimit-Remaining: 998
X-RateLimit-Reset: 1708185600
```
