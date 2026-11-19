# Mawutech QA Intelligence — Frontend

React + Vite dashboard for the MQI Phase 1 API.

## Setup
- Node.js 20+
- Copy .env.example to .env and set VITE_API_URL to the backend API origin.
- Run npm install, then npm run dev.
- Build production assets with npm run build.

## Features
- Administrator sign-in using backend-issued JWT
- Project creation and overview
- Authorized website registration
- Playwright smoke-test trigger
- Test history with status, HTTP response and duration

OpenAI keys and service secrets must remain on the backend. The backend hostname allowlist is authoritative; frontend checks are not a security boundary.

## Deploy to Netlify

1. Import this repository into Netlify and select the `main` branch (or the reviewed deployment branch).
2. Netlify reads `netlify.toml`: build command `npm run build`, publish directory `dist`, Node.js 22, SPA fallback and baseline security headers.
3. In Site configuration → Environment variables, add `VITE_API_URL` with the deployed backend URL ending in `/api` (for example, `https://your-api-host.example.com/api`).
4. Trigger a new deploy after saving the variable.
5. Add the exact deployed frontend origin to the backend's `FRONTEND_ORIGIN` environment variable and redeploy the backend.

Only public configuration belongs in `VITE_*` variables. Never place OpenAI, JWT, database or Cloudinary secrets in the frontend environment.
