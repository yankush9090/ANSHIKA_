# Surprise Web Experience

A simple, single‑page surprise website featuring a login portal, looping background videos, a heartfelt “100 Things” section, a photo gallery with lightbox, interactive reveal cards, and background music.

## Features
- Login gate with username/password to reveal the main content
- Two side‑by‑side background videos on the login screen
- “100 Things That Make You Perfect” animated list
- Responsive photo gallery with square thumbnails and lightbox viewer
- Reveal cards that flip on click/tap and play a sound
- Background audio with a toggle button

## Tech Stack
- HTML, CSS, and vanilla JavaScript
- Local assets for videos (`videos/`), photos (`photos/`), and music (`music/`)

## Project Structure
```
For her/
├── css/styles.css        # Styles for layout, gallery, reveal cards, etc.
├── js/app.js             # Login handling, gallery/lightbox, audio toggle, reveal cards
├── index.html            # Main page markup
├── photos/               # Image assets used by gallery and reveal section
├── videos/               # Background/login videos (mp4)
└── music/                # Audio files (mp3)
```

## Getting Started
1. Place your media in the appropriate folders:
   - Videos: `videos/1.mp4`, `videos/2.mp4` (H.264/AAC recommended)
   - Photos: `photos/*.jpg` or `photos/*.jpeg` (any dimensions)
   - Music: `music/*.mp3`
2. Open `index.html` directly or serve the folder with a local server.
   - Example (Python): `python -m http.server 8000` and open `http://localhost:8000/For%20her/index.html`
   - If autoplay is blocked on mobile, ensure `<video autoplay muted loop playsinline>` is present.

## Configuration
- Credentials: update `correctUsername` and `correctPassword` in `js/app.js`.
- Gallery thumbnails: controlled via `.gallery img { aspect-ratio: 1/1; object-fit: cover; }` in `css/styles.css`.
- Reveal cards: image framing can be tuned via `object-position`. Specific images (e.g., `16.jpg`, `18.jpg`, `20.jpg`, `22.jpg`) are biased to `center top` to keep faces visible.
- Audio: background and reveal sounds are loaded from `music/`. Toggle button reflects playback state.

## Tips
- Use forward slashes in paths (e.g., `photos/1.JPG`) for web compatibility.
- Prefer H.264/AAC for videos to maximize browser support.
- If thumbnails look cramped, adjust `.gallery` grid `gap` and `minmax(...)` values.

## Notes
- This is a static site; no backend required.
- Assets are local; ensure file names in `index.html` match files in your folders.
