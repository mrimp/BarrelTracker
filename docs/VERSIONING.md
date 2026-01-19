# Versioning & tags

BarrelTracker uses **Semantic Versioning**: `MAJOR.MINOR.PATCH`.

- **PATCH**: bug fixes, UI tweaks, small features (no breaking changes)
- **MINOR**: new features that are backwards compatible
- **MAJOR**: breaking changes (schema changes that can’t be auto-migrated)

## Source of truth
The app version is defined in `BarrelTracker_LATEST.html`:

- `window.BT_APP.version` (string)
- the HTML `<title>` (kept in sync)

## Tag flow
1. Bump version + update `CHANGELOG.md`.
2. Commit: `release: vX.Y.Z`.
3. Tag: `git tag -a vX.Y.Z -m "BarrelTracker vX.Y.Z"`.
4. Push: `git push && git push --tags`.
5. Create a GitHub Release from the tag.
