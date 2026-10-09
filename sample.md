---
description: Install, configure, and run the Hi-Fi project for the first time.
icon: rocket
---

# Getting Started

introduced updates. Welcome to the Hi-Fi project. This guide walks you through installing, configuring, and running the project for the first time.

made changes in gitbook. updated in branch github.

Edited in branch(gitbook)

{% hint style="info" %}
You need **Node.js 18 or later** installed before you begin.
{% endhint %}

## Installation

{% stepper %}
{% step %}
### Clone the repository

{% code title="Terminal" %}
```bash
git clone https://github.com/aashifuxdev/hi-fi.git
cd hi-fi
```
{% endcode %}
{% endstep %}

{% step %}
### Install dependencies

```bash
npm install
```
{% endstep %}
{% endstepper %}

## Configuration

Create a `.env` file in the project root:

{% code title=".env" lineNumbers="true" %}
```env
API_URL=https://api.example.com
PORT=3000
```
{% endcode %}

| Variable  | Required | Description                 |
| --------- | -------- | --------------------------- |
| `API_URL` | Yes      | Base URL of the backend API |
| `PORT`    | No       | Local port (default `3000`) |

{% hint style="warning" %}
Never commit your `.env` file to version control.
{% endhint %}

## Running the project

{% tabs %}
{% tab title="Development" %}
```bash
npm run dev
```
{% endtab %}

{% tab title="Production" %}
```bash
npm run build && npm start
```
{% endtab %}
{% endtabs %}

## Next steps

1. Read the [README](./).
2. Explore the components.
3. Open an issue if you get stuck.

{% hint style="success" %}
You're all set! Your local environment is ready.
{% endhint %}
