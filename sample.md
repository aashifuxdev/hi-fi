# Getting Started main branch

Welcome to the Hi-Fi project. This guide walks you through installing, configuring, and running the project for the first time.

> **Note:** You need Node.js 18 or later installed before you begin.

## Installation

Clone the repository and install dependencies:

```bash
git clone https://github.com/aashifuxdev/hi-fi.git
cd hi-fi
npm install
```

## Configuration

Create a `.env` file in the project root:

```env
API_URL=https://api.example.com
PORT=3000
```

| Variable  | Required | Description                 |
| --------- | -------- | --------------------------- |
| `API_URL` | Yes      | Base URL of the backend API |
| `PORT`    | No       | Local port (default `3000`) |

> **Warning:** Never commit your `.env` file to version control.

## Running the project

- **Development:** `npm run dev`
- **Production:** `npm run build && npm start`

## Next steps

1. Read the [README](README.md).
2. Explore the components.
3. Open an issue if you get stuck.
