# Geralt of Rivia — Hobbies Dashboard 2026

An interactive personal dashboard combining **books read** and **games played** in 2026.

## What is included

- 58 books
- 13 games
- Personal ratings preserved exactly
- Red + white visual theme
- Book and gaming icons in the corners
- Search
- Book / Game / All filters
- Clickable cards
- Storyline shown inside the detail modal
- Spoiler-labelled ending/resolution section
- Author information for books
- Add Entry button
- Local browser persistence with `localStorage`
- Responsive layout for desktop and mobile
- No framework or build step required

## Important storyline note

The storyline data is embedded directly in `index.html`.

The earlier version had a CSS contrast problem: the storyline text was using a very light text colour on a white modal, which made the story appear missing. This GitHub version fixes that contrast so the storyline is clearly readable.

Some titles are intentionally marked for confirmation where the title is ambiguous (for example **First Light**) rather than attaching the wrong plot to the entry.

## Files

```text
geralt-of-rivia-hobbies-dashboard/
├── index.html
├── README.md
├── vercel.json
└── .gitignore
```

## Run locally

You can simply double-click `index.html`.

For a local development server:

```bash
python3 -m http.server 8000
```

Then open:

```text
http://localhost:8000
```

## Put it on GitHub

1. Create a new GitHub repository, for example:
   `geralt-of-rivia-hobbies-dashboard`
2. Upload:
   - `index.html`
   - `README.md`
   - `vercel.json`
   - `.gitignore`
3. Commit the files.

Because this is a static HTML site, you do **not** need Node.js, React, npm, or a build command.

## Deploy on Vercel

Import the GitHub repository into Vercel.

Use:

- Framework preset: **Other**
- Build command: leave empty
- Output directory: `.`
- Install command: leave empty

Vercel can then serve `index.html` directly.

## Adding books and games

Click **＋ Add Entry** in the dashboard.

Choose:

- `book` or `game`
- title
- rating
- author for a book

New entries are stored in the browser's `localStorage`.

### Important limitation

`localStorage` is browser-specific. If you open the public website on another computer or phone, that device will not automatically have entries you added on your original device.

For a future version where your collection syncs across devices, use a database such as Supabase or Firebase.

## Data

Current collection: **71 total titles**.

Game rating average: **8.62/10**.

The dashboard's overall average and 10/10 count are calculated automatically from the entries.

## License

Personal project. You can modify and publish the dashboard as you wish.
