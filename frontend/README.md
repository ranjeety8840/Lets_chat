# Lets Chat — Frontend

Modern React frontend for the Lets Chat application, built with Vite for a fast developer experience and TailwindCSS for styling. State management is handled by Redux Toolkit, routing by React Router, and realtime events via Socket.IO client.

## Tech Stack

- React 19 + Vite
- TailwindCSS + PostCSS + Autoprefixer
- Redux Toolkit + React Redux
- React Router DOM v7
- Socket.IO Client
- Axios
- Emoji Picker for rich messaging

## Prerequisites

- Node.js (LTS recommended)
- npm (bundled with Node)

## Getting Started

1. Install dependencies
   ```bash
   npm install
   ```
2. Start the development server (default: http://localhost:5173)
   ```bash
   npm run dev
   ```
3. Build for production
   ```bash
   npm run build
   ```
4. Preview the production build locally
   ```bash
   npm run preview
   ```

## Available Scripts

- dev: Start Vite dev server
- build: Build production assets
- preview: Preview built app
- lint: Run ESLint across the project

## Project Structure

```
frontend/
├─ index.html
├─ vite.config.js
├─ tailwind.config.js
├─ postcss.config.js
├─ public/
├─ src/
│  ├─ main.jsx
│  ├─ App.jsx
│  ├─ index.css
│  ├─ components/
│  ├─ pages/
│  ├─ redux/
│  ├─ customHooks/
│  └─ assets/
└─ package.json
```

## Styling

- TailwindCSS is configured via `tailwind.config.js` and `postcss.config.js`.
- Global styles live in `src/index.css`.

## Environment Variables

- No required frontend `.env` variables were detected. If you add API hosts or keys later, expose them via `import.meta.env` (prefix with `VITE_`).

## Linting

- Run `npm run lint` to check code quality. ESLint is configured via `eslint.config.js`.

## Notes

- Vite default dev port is 5173. If you run the backend locally, ensure any API base URLs or Socket.IO endpoints match your backend host/port.
- This README documents the current scripts and dependencies from `package.json` for accuracy.
