---
description: Endpoints the Hi-Fi frontend calls on the backend API.
icon: code
---

# API Reference

All requests go to the base URL set in `API_URL`. See [Configuration](configuration.md).

{% hint style="info" %}
Every request needs an `Authorization: Bearer <token>` header.
{% endhint %}

## List projects

`GET /projects`

{% tabs %}
{% tab title="Request" %}
```bash
curl -H "Authorization: Bearer $TOKEN" \
  "$API_URL/projects"
```
{% endtab %}

{% tab title="Response 200" %}
```json
[
  { "id": "p_1", "name": "Website redesign" },
  { "id": "p_2", "name": "Mobile app" }
]
```
{% endtab %}
{% endtabs %}

## Create a project

`POST /projects`

| Field  | Type   | Required | Description         |
| ------ | ------ | -------- | ------------------- |
| `name` | string | Yes      | Project display name |

{% code title="Request" %}
```bash
curl -X POST -H "Authorization: Bearer $TOKEN" \
  -H "Content-Type: application/json" \
  -d '{"name":"New project"}' \
  "$API_URL/projects"
```
{% endcode %}

## Error codes

| Status | Meaning                          |
| ------ | -------------------------------- |
| `400`  | The request body is invalid      |
| `401`  | The token is missing or expired  |
| `404`  | The resource doesn't exist       |
| `500`  | Something went wrong on the server |
