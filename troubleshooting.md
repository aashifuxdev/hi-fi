---
description: Fixes for the most common problems when running Hi-Fi locally.
icon: wrench
---

# Troubleshooting

## `npm install` fails

{% hint style="danger" %}
Errors like `Unsupported engine` mean your Node.js version is too old.
{% endhint %}

Check your version and upgrade to Node.js 18 or later:

```bash
node -v
```

## Port 3000 is already in use

Another process is using the port. Either stop it, or change `PORT` in your `.env`:

```env
PORT=3001
```

## API requests return `401`

{% stepper %}
{% step %}
### Check the token

Make sure your token hasn't expired.
{% endstep %}

{% step %}
### Check `API_URL`

Confirm it points at the right environment. See [Configuration](configuration.md).
{% endstep %}

{% step %}
### Restart the dev server

Changes to `.env` only take effect after a restart.
{% endstep %}
{% endstepper %}

{% hint style="info" %}
Still stuck? Check the [FAQ](faq.md) or open an issue on GitHub.
{% endhint %}
