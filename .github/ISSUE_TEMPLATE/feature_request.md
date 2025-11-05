---
name: Feature request
about: Feature (Internal – Virtual Fusion)
title: ''
labels: enhancement
assignees: ''

---

### Summary
Short description of what this ticket implements.

---

## API Endpoints

### Endpoint 1
- Method and path: `GET /api/v1/example`
- Purpose: one line
- Auth: None | Bearer JWT | API key
- Required headers: `Authorization: Bearer <token>` (if applicable), `Content-Type: application/json`

**Path parameters**
| Name | In   | Type   | Required | Description |
|------|------|--------|----------|-------------|
| id   | path | string | Yes/No   |             |

**Query parameters**
| Name       | In    | Type    | Required | Default | Description                 |
|------------|-------|---------|----------|---------|-----------------------------|
| page       | query | integer | No       | 1       | Page number                 |
| page_size  | query | integer | No       | 25      | Items per page              |
| search     | query | string  | No       |         | Optional search term        |
| sort       | query | string  | No       |         | Example: name,-created_at   |

**Request body example**
```json
{
  "name": "Example",
  "is_active": true
}
````

**cURL example (optional)**

```bash
curl -X GET "https://api.virtualsme.ai/api/v1/users?page=1&page_size=25" \
  -H "Authorization: Bearer <token>" \
  -H "Content-Type: application/json"
```

**Response example: 200 (list, paginated)**

```json
{
  "data": [
    /* items */
  ],
  "page": 1,
  "page_size": 25,
  "total_pages": 10,
  "total_items": 250
}
```

**Response example: 200 (single resource)**

```json
{
  "data": {
    "id": "12345",
    "name": "Example",
    "is_active": true,
    "created_at": "2025-11-05T10:00:00Z"
  }
}
```

**Error responses**

* 400 validation_error
* 401 unauthorized
* 403 forbidden
* 404 not_found
* 409 conflict
* 422 unprocessable_entity
* 500 server_error

---

### Endpoint N

* Method and path:
* Purpose:
* Auth:
* Required headers:

**Path parameters**

| Name | In | Type | Required | Description |
| ---- | -- | ---- | -------- | ----------- |

**Query parameters**

| Name | In | Type | Required | Default | Description |
| ---- | -- | ---- | -------- | ------- | ----------- |

**Request body example**

```json
{}
```

**cURL example (optional)**

```bash
curl -X <METHOD> "<URL>" -H "Authorization: Bearer <token>" -d '{}'
```

**Response example: 200**

```json
{
  "data": {}
}
```

**Error responses**

* 400
* 401
* 404
* 500

---

## Data Model Changes

* New tables or fields:
* Indexes:
* Migrations required: Yes or No
* Backfill required: Yes or No

## Dependencies

* Microservices touched:
* Queues or topics:
* External services:

## Breaking Changes

* Contract change: Yes or No
* Backward compatibility plan:

## Acceptance Checklist

* [ ] Unit tests added
* [ ] API docs updated
* [ ] Feature flag or config added if applicable
* [ ] Tested in Stage
* [ ] No breaking changes unless specified

## Notes

Anything else relevant for implementation.
