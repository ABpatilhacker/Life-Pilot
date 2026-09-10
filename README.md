# LifePilot

LifePilot is a frontend-only productivity workspace for the Sankalp Tech Club college project.

## Run it

Open the folder in VS Code and launch `index.html` with Live Server. A small static server also works:

```bash
python3 -m http.server 4173
```

Then open `http://localhost:4173`.

## Frontend architecture

- **HTML5 pages** provide the public landing page, auth flow and authenticated workspace routes.
- **CSS** is split into `style.css`, `responsive.css` and `animations.css`.
- **Vanilla JavaScript** provides page modules in `js/`.
- **`js/storage.js`** is the data adapter. It seeds believable demo data and exposes collection methods such as `getTasks`, `addTask`, `updateTask` and `deleteTask`. These contracts are intentionally shaped so they can later be replaced with Spring Boot REST calls without changing the UI layer.
- **`js/app.js`** owns shared navigation, theme handling, modals, toasts and common helpers.

## Demo behavior

The login and registration forms are frontend-only. Data is stored in the browser's `localStorage`, including tasks, goals, habits, expenses, events, focus sessions, theme and settings. Use the **Use the demo account** button on the login page for a quick start.

No Spring Boot, MySQL, real authentication or backend API is included yet.
