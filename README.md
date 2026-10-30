# Deploy Test Project

A small React single-page app used to test deploying a static site and checking its behavior once it's live.

It has two pages, **Home** (`/`) and **About** (`/about`), handled in the browser by React Router, plus a "page not found" view for unknown paths.

## Requirements

- Node.js 18, 20 or 22+
- npm

## Scripts

| Command | What it does |
|---|---|
| `npm install` | Install dependencies |
| `npm run dev` | Start the local dev server |
| `npm run build` | Build the production files into `dist/` |
| `npm run preview` | Serve the built `dist/` folder locally |

## Build output

`npm run build` produces static files only (HTML, JS, CSS) in the `dist/` folder. There is no server code, so any static host can serve it.

## Environment variables

Values are read at build time and shown on the page. They are embedded in the public JavaScript bundle, so **never put secrets in them**.

| Variable | Example | Purpose |
|---|---|---|
| `VITE_APP_NAME` | `My React App` | Title shown on the page |
| `VITE_APP_ENV` | `production` | Environment label shown on the page |
| `VITE_BUILD_TIME` | *(set automatically)* | Build timestamp, set by the `build` script |
