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