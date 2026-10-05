---
description: Every environment variable and config option the Hi-Fi project supports.
icon: gear
---

# Configuration

Hi-Fi reads its settings from a `.env` file in the project root. Set it up first by following [Getting Started](sample.md).

## Environment variables

| Variable    | Required | Default       | Description                                      |
| ----------- | -------- | ------------- | ------------------------------------------------ |
| `API_URL`   | Yes      | —             | Base URL of the backend API                      |
| `PORT`      | No       | `3000`        | Port the local server listens on                 |
| `LOG_LEVEL` | No       | `info`        | One of `debug`, `info`, `warn`, `error`          |
| `NODE_ENV`  | No       | `development` | Set to `production` for optimised builds         |

{% hint style="warning" %}
Never commit your `.env` file to version control. Add it to `.gitignore`.
{% endhint %}

## Per-environment files

{% tabs %}
{% tab title="Development" %}
{% code title=".env.development" %}
```env
API_URL=http://localhost:8080
LOG_LEVEL=debug
```
{% endcode %}
{% endtab %}

{% tab title="Production" %}
{% code title=".env.production" %}
```env
API_URL=https://api.example.com
LOG_LEVEL=warn
NODE_ENV=production
```
{% endcode %}
{% endtab %}
{% endtabs %}

{% hint style="info" %}
Values in `.env` override the per-environment files.
{% endhint %}
