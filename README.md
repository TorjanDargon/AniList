# AniList — Anime Episode Tracker

A single-file, manga-styled anime watchlist organizer. Search a title, drop it onto your dashboard, and track your episode progress across four lists: Watching, Plan to watch, On hold, and Completed.

No sign-up, no backend, no build step — just one HTML file.

## Features

- **Live search** powered by the [Jikan API](https://jikan.moe/) (a free, unofficial MyAnimeList API) — search by title and see cover art, type, episode count, and year before adding
- **One-click add** — select a search result and it's added straight to your Watching list
- **Episode tracker** — bump your current episode up or down per title, with a progress bar that fills as you go
- **Status tabs** — move titles between Watching, Plan to watch, On hold, and Completed; hitting the final episode auto-marks a title Completed
- **Dashboard stats** — live counts for series in progress, episodes logged, and completed titles
- **Saves automatically** — your list persists in the browser via local storage, no account needed
- **Manga-inspired UI** — angular panel-style cards, halftone progress fills, and bold display type

## Running it locally

This is a static HTML file with no dependencies to install.

1. Clone or download this repo
2. Open `index.html` directly in a browser, **or**
3. For the best experience, use a local server (recommended so the browser treats it as a proper page rather than a `file://` path):
   - In VS Code, install the **Live Server** extension, right-click `index.html`, and choose **Open with Live Server**

## Deploying for free

Since it's a single static file, you can host it anywhere that serves static sites:

- **GitHub Pages** — push this repo, then enable Pages in the repo's Settings (Branch: `main`, folder: `/root`). Your file needs to be named `index.html` for it to load at the root URL.
- **Netlify Drop** — drag and drop `index.html` at [app.netlify.com/drop](https://app.netlify.com/drop) for an instant live link.

## A note on your data

Your watchlist is saved to the browser's local storage, tied to the exact URL you use to open the app. That means:

- Refreshing the page is always safe — your list stays put
- Opening the app from a **different URL** (e.g. moving from `localhost` to a deployed GitHub Pages link) starts you off with an empty list, since local storage doesn't carry over between addresses
- Clearing your browser's site data for that URL will also clear your list

## Tech

- Vanilla HTML, CSS, and JavaScript — no frameworks, no build tools
- [Jikan API v4](https://docs.api.jikan.moe/) for anime search
- Google Fonts (Bebas Neue, Inter)

## License

Free to use, modify, and share.
