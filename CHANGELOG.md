# Changelog

## v4.5.25 — 2026-01-18
- Offline hardening: blocks network calls and logs attempts.
- Added **Offline Self-Test** panel (Guide) to verify: no network, no remote assets, storage OK.
- Added **Portable mode** export/import bundle (data + UI settings).
- Documentation: badges, screenshots section, browser notes, and release checklist.

## v4.3.0
- Fix: ShotMarker **archive CSV** imports now split into correct per‑string targets (e.g., R1/R2/R3) instead of collapsing or over‑splitting.
- Fix: Target↔chrono pairing now matches **true target/string count** from ShotMarker archive exports.
- UI: “Last” column clarified as **Last session** with compact cell rendering + tooltip.
- UI: Import notes are **grouped/capped** to avoid noisy debug spam.
- Maintains: local‑only, deterministic scoring; vertical‑first; confidence‑weighted ranking.
