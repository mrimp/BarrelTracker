# Release checklist (BarrelTracker)

BarrelTracker ships as a **single, self‑contained HTML file** (`BarrelTracker_LATEST.html`).

## 1) Pre-flight smoke test
- [ ] Open `BarrelTracker_LATEST.html` via **file://** (double‑click) in Chrome/Edge.
- [ ] If GitHub Pages is enabled, open the site build too.
- [ ] In both contexts run: **Guide → Offline Self‑Test → Run** (should pass).
- [ ] Import a known-good AMP session and confirm:
  - [ ] Sessions render and can be edited
  - [ ] Ranking updates
  - [ ] Export JSON works
  - [ ] Portable mode export/import works

## 2) Version bump
- [ ] Update `window.BT_APP.version` and `<title>` in `BarrelTracker_LATEST.html`.
- [ ] Update the top section in `CHANGELOG.md`.
- [ ] Commit with message: `release: vX.Y.Z`.

## 3) Tag & release
- [ ] Create an annotated tag: `git tag -a vX.Y.Z -m "BarrelTracker vX.Y.Z"`.
- [ ] Push commits and tags: `git push && git push --tags`.
- [ ] Create a GitHub Release for the tag and attach the repo ZIP (optional).

## 4) Verify release artifacts
- [ ] Download the release ZIP from GitHub.
- [ ] Confirm `BarrelTracker_LATEST.html` runs offline from the downloaded ZIP.
- [ ] Confirm README “Run it” instructions are correct.
