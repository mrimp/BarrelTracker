# Known limitations & browser notes

This app is designed to be **fully offline** and to run as a **single HTML file**.

## file:// quirks (offline)
- **Storage scope can vary:** Some browsers treat each `file://` path as a separate origin. That can make localStorage feel inconsistent. If you see this, use **Portable mode** to export/import your data.
- **Drag/drop restrictions:** Some managed browsers block drag/drop of files or do not provide full paths (security). Use the file picker buttons if drag/drop is blocked.
- **Downloads prompt:** Exporting JSON triggers a browser download. If downloads are blocked, allow downloads for local files (or use a different browser profile).

## GitHub Pages (https://) differences
- `https://` origins generally have **more consistent storage** than `file://`.
- If you use both `file://` and Pages, they do not share localStorage (different origins). Use **Portable mode** when switching.

## Extensions & injected assets
- Some browser extensions inject scripts/styles and can produce noisy console messages or “remote refs” in self-test. Try Incognito or disable extensions if you get weird results.

## Supported browsers
- Chrome / Edge (recommended)
- Firefox (works, but `file://` storage behavior can be different)
- Safari (not the primary target; `file://` restrictions vary)
