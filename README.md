# Portfolio (Vue 3 + Vite)

A simple personal portfolio site built with **Vue 3 + TypeScript + Vite**.


## Tech Stack

- **Vue 3** (JS framework)
- **TypeScript** (static typing)
- **Vite** (dev server + build tool)

## Project Structure

Key source files:

- `src/main.ts` – app entry point
- `src/App.vue` – root layout
- `src/components/` – UI components (Header, Navbar, Footer, etc.)
- `src/data/` – static content used by components (navigation, profile info)
- `src/types/` – TypeScript type definitions

## Run locally

Install dependencies:

```sh
npm install
```

Run development server:

```sh
npm run dev
```

You can open the app by navigating to `http://localhost:5173/` in your browser.

## Build

Build for production:

```sh
npm run build
```

## Type checking

Run type checking (uses `vue-tsc`):

```sh
npm run type-check
```

## 📌 Notes

- This repo is intentionally small and framework-focused so it is easy to extend.