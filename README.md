📓 Notes App

A small, password-locked personal diary built with React. Write free-form notes or checklists, review them in one place, and switch between light and dark mode — everything is saved in your browser, no account or backend needed.

Link: https://notes-app-seven-pied-91.vercel.app

## Features

- **Password lock** — set a password on first visit; you'll need it to get back into your notes after logging out.
- **Two kinds of notes**
  - *Normal notes* on a lined, notebook-style page that grows as you type.
  - *Todo lists* with custom checkboxes; add or remove tasks as you go.
- **Saved notes view** — every note is timestamped. Mark a note as done (it turns green and gets struck through), edit it, delete it, or clear everything at once.
- **Light / dark mode** — your choice is remembered between visits.
- **Works offline** — notes live in your browser's `localStorage`, so nothing leaves your device.

## Tech stack

- [React 19](https://react.dev/)
- [React Router 7](https://reactrouter.com/) for page routing
- [Create React App](https://create-react-app.dev/) (`react-scripts`) for the build tooling
- Plain CSS for styling

## Getting started

You'll need [Node.js](https://nodejs.org/) (v18 or newer) and npm.

```bash
git clone https://github.com/abeeraalam1/notes-app.git
cd notes-app
npm install
npm start
```

The app opens at [http://localhost:3000](http://localhost:3000).

### Other scripts

| Command         | What it does                                        |
| --------------- | --------------------------------------------------- |
| `npm start`     | Runs the app in development mode with live reload   |
| `npm run build` | Builds an optimized production bundle into `build/` |
| `npm test`      | Runs the test suite in watch mode                   |

## How to use it

1. **Set a password** the first time you open the app.
2. On **✍️ Write**, choose *Normal Note* or *Todo List*, write it, and hit **Save Note**.
3. Open **📓 View Notes** to see everything you've saved. From there you can tick a note off, **Edit** it (it reopens in the editor), **Delete** it, or **Clear All Notes**.
4. Use **🚪 Logout** to lock the diary again.

## Project structure

```
src/
├── App.js             # Routes, dark-mode toggle, login state
├── Navbar.js          # Top navigation and logout
├── PasswordPage.js    # Set / enter password
├── ProtectedRoute.js  # Redirects to login if not unlocked
├── DiaryPage.js       # Note and todo-list editor
├── ViewNotesPage.js   # List of saved notes with edit/delete/done
└── App.css            # Styling, including notebook lines and dark mode
```

## Good to know

- **Data is per-browser.** Notes are stored in `localStorage`, so they won't sync between devices or browsers, and clearing your browser data will erase them.
- **The password is a privacy lock, not encryption.** It's stored as plain text in the same browser storage as your notes, so it keeps casual eyes out but isn't real security. Don't store anything truly sensitive.

## Ideas for future improvements

- Hash the password and encrypt notes before storing them
- Search, tags, or categories for notes
- Export / import notes as a file
- Sync across devices with a backend

Data is per-browser. Notes are stored in localStorage, so they won't sync between devices or browsers, and clearing your browser data will erase them.
The password is a privacy lock, not encryption. It's stored as plain text in the same browser storage as your notes, so it keeps casual eyes out but isn't real security. Don't store anything truly sensitive.
Ideas for future improvements
Hash the password and encrypt notes before storing them
Search, tags, or categories for notes
Export / import notes as a file
Sync across devices with a backend
