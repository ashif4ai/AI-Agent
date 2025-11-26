# API Design Document

## API Information
- **API Version:** [v1]
- **Base URL:** [https://api.example.com]
- **Protocol:** [REST / GraphQL / Both]
- **Authentication:** [JWT / OAuth2 / API Key / etc.]
- **Last Updated:** [YYYY-MM-DD]

---

## API Overview

### Purpose
[What this API does and why]

### Primary Use Cases
1. [Use case 1]
2. [Use case 2]
3. [Use case 3]

### Versioning Strategy
- **URL-based:** `/api/v1/...`
- **Supported Versions:** [v1, v2]
- **Deprecation Policy:** [Policy description]

---

## Authentication & Authorization

### Authentication Methods

#### JWT (JSON Web Token)
- **Header:** `Authorization: Bearer <token>`
- **Token Expiration:** [Duration]
- **Refresh Token:** [Yes/No]

#### OAuth 2.0
- **Grant Types:** [Authorization Code, Client Credentials]
- **Scopes:** [scope1, scope2]

#### API Key
- **Header:** `X-API-Key: <key>`
- **Rotation:** [Frequency]

### Authorization Model
- **Type:** [Role-based / Attribute-based]
- **Roles:** [admin, user, guest, etc.]

---

## Core Endpoints

### 1. Authentication Endpoints

#### POST /api/v1/auth/login
**Purpose:** User login

**Request:**
```json
{
  "email": "user@example.com",
  "password": "password123"
}
```

**Response (200):**
```json
{
  "token": "eyJhbGc...",
  "refreshToken": "eyJhbGc...",
  "expiresIn": 3600,
  "user": {
    "id": 1,
    "email": "user@example.com",
    "name": "User Name"
  }
}
```

**Error Responses:**
```json
{
  "401": {
    "code": "INVALID_CREDENTIALS",
    "message": "Invalid email or password"
  }
}
```

#### POST /api/v1/auth/logout
**Purpose:** User logout

**Request Headers:**
```
Authorization: Bearer <token>
```

**Response (200):**
```json
{
  "message": "Logged out successfully"
}
```

---

### 2. User Endpoints

#### GET /api/v1/users/:id
**Purpose:** Retrieve user profile

**Parameters:**
| Param | Type | Required | Description |
|-------|------|----------|-------------|
| id | integer | Yes | User ID |

**Response (200):**
```json
{
  "id": 1,
  "email": "user@example.com",
  "name": "User Name",
  "createdAt": "2024-01-01T00:00:00Z"
}
```

#### PUT /api/v1/users/:id
**Purpose:** Update user profile

**Request:**
```json
{
  "name": "New Name",
  "email": "newemail@example.com"
}
```

**Response (200):**
```json
{
  "id": 1,
  "email": "newemail@example.com",
  "name": "New Name",
  "updatedAt": "2024-01-01T00:00:00Z"
}
```

---

### 3. Resource Endpoints

#### GET /api/v1/resources
**Purpose:** List all resources

**Query Parameters:**
| Param | Type | Required | Default | Description |
|-------|------|----------|---------|-------------|
| page | integer | No | 1 | Page number |
| limit | integer | No | 10 | Items per page |
| sort | string | No | -createdAt | Sort field |
| search | string | No | - | Search query |

**Response (200):**
```json
{
  "data": [
    {
      "id": 1,
      "name": "Resource 1",
      "description": "Description",
      "createdAt": "2024-01-01T00:00:00Z"
    }
  ],
  "pagination": {
    "page": 1,
    "limit": 10,
    "total": 50,
    "pages": 5
  }
}
```

#### POST /api/v1/resources
**Purpose:** Create new resource

**Request:**
```json
{
  "name": "New Resource",
  "description": "Resource description",
  "type": "resource_type"
}
```

**Response (201):**
```json
{
  "id": 2,
  "name": "New Resource",
  "description": "Resource description",
  "type": "resource_type",
  "createdAt": "2024-01-01T00:00:00Z"
}
```

#### GET /api/v1/resources/:id
**Purpose:** Retrieve specific resource

**Response (200):**
```json
{
  "id": 1,
  "name": "Resource 1",
  "description": "Description",
  "createdAt": "2024-01-01T00:00:00Z"
}
```

#### PUT /api/v1/resources/:id
**Purpose:** Update resource

**Request:**
```json
{
  "name": "Updated Name",
  "description": "Updated description"
}
```

**Response (200):**
```json
{
  "id": 1,
  "name": "Updated Name",
  "description": "Updated description",
  "updatedAt": "2024-01-01T00:00:00Z"
}
```

#### DELETE /api/v1/resources/:id
**Purpose:** Delete resource

**Response (204):** No content

---

## Error Handling

### Error Response Format
```json
{
  "error": {
    "code": "ERROR_CODE",
    "message": "Human-readable error message",
    "details": {
      "field": "fieldName",
      "reason": "Detailed reason"
    }
  }
}
```

### HTTP Status Codes
| Code | Meaning | Scenarios |
|------|---------|-----------|
| 200 | OK | Successful GET, PUT |
| 201 | Created | Successful POST |
| 204 | No Content | Successful DELETE |
| 400 | Bad Request | Invalid input, validation errors |
| 401 | Unauthorized | Missing/invalid token |
| 403 | Forbidden | Insufficient permissions |
| 404 | Not Found | Resource doesn't exist |
| 409 | Conflict | Resource already exists |
| 429 | Too Many Requests | Rate limit exceeded |
| 500 | Server Error | Internal server error |

### Common Error Codes
| Code | HTTP Status | Description |
|------|-------------|-------------|
| INVALID_CREDENTIALS | 401 | Login failed |
| TOKEN_EXPIRED | 401 | Token expired |
| UNAUTHORIZED | 403 | No permission |
| NOT_FOUND | 404 | Resource doesn't exist |
| VALIDATION_ERROR | 400 | Input validation failed |
| DUPLICATE_ENTRY | 409 | Resource already exists |
| RATE_LIMIT_EXCEEDED | 429 | Too many requests |

---

## Rate Limiting

### Limits per User
- **Authenticated:** [X requests per minute]
- **Unauthenticated:** [Y requests per minute]

### Headers
```
X-RateLimit-Limit: 1000
X-RateLimit-Remaining: 999
X-RateLimit-Reset: 1640100000
```

---

## Pagination

### Standard Pagination
```json
{
  "data": [...],
  "pagination": {
    "page": 1,
    "limit": 10,
    "total": 100,
    "pages": 10
  }
}
```

### Cursor Pagination
```json
{
  "data": [...],
  "pagination": {
    "nextCursor": "abc123",
    "prevCursor": "xyz789",
    "hasMore": true
  }
}
```

---

## Filtering & Searching

### Query Parameters
```
GET /api/v1/resources?status=active&type=user&search=name
```

### Filter Operators
- `eq`: Equal
- `ne`: Not equal
- `gt`: Greater than
- `gte`: Greater than or equal
- `lt`: Less than
- `lte`: Less than or equal
- `in`: In array
- `contains`: Contains (for strings)

---

## Webhooks

### Event Types
- `resource.created`
- `resource.updated`
- `resource.deleted`
- `user.registered`

### Webhook Payload
```json
{
  "id": "evt_123",
  "event": "resource.created",
  "data": {
    "id": 1,
    "name": "Resource"
  },
  "timestamp": "2024-01-01T00:00:00Z"
}
```

### Retry Policy
- Retries: [X times]
- Backoff: [Exponential / Linear]

---

## API Examples & SDKs

### JavaScript/TypeScript
```typescript
import { APIClient } from '@example/sdk';

const client = new APIClient({
  apiKey: 'your-api-key'
});

const resource = await client.resources.get(1);
```

### Python
```python
from example_sdk import APIClient

client = APIClient(api_key='your-api-key')
resource = client.resources.get(1)
```

### cURL
```bash
curl -X GET https://api.example.com/api/v1/resources/1 \
  -H "Authorization: Bearer your-token"
```

---

## Best Practices

### Request/Response
- Always include timestamps in UTC
- Use snake_case for JSON fields
- Include API version in URL
- Support both JSON request/response

### Pagination
- Default limit: 10, max: 100
- Always include pagination metadata
- Use cursor pagination for large datasets

### Security
- Always use HTTPS
- Validate all inputs
- Implement rate limiting
- Log all access

### Documentation
- Keep API docs in sync with code
- Provide examples for each endpoint
- Document all error codes
- Include changelog

---

## Changelog

### v1.0 (YYYY-MM-DD)
- Initial API release
- Resources endpoint
- User authentication

### v1.1 (YYYY-MM-DD)
- Added webhooks support
- Implemented rate limiting
- [Other changes]

---

**API Owner:** [Name]
**Last Updated:** [YYYY-MM-DD]
**Next Review:** [YYYY-MM-DD]
