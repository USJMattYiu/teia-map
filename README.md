# teia-map

Static visualization of the TEIA users chain (Feb 2022 to Feb 2026), rendered with p5.js from a local frozen dataset.

## Files

- `index.html` - main app and rendering logic.
- `users_2022_2026.json` - local dataset consumed by the app.
- `source.svg` - source artwork/asset file.

## Run locally

Because the app fetches a local JSON file, serve the folder over HTTP instead of opening `index.html` directly.

Example with Python:

```bash
python3 -m http.server 8000
```

Then open:

- `http://localhost:8000/`
- Optional viewer highlight: `http://localhost:8000/?viewer=<wallet_address>`

## Controls

- `Space`: toggle color mode
- `Enter`: draw all users immediately
- `Arrow keys`: pan (after full draw)
- `Z` / `X`: zoom in / out (after full draw)
- `Esc`: reset view (after full draw)
- `Mouse click`: inspect a visible user

## Notes

- Data is loaded from `./users_2022_2026.json` with no-store cache mode.
- User info links out to OBJKT user and token pages when available.
