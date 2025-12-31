# Changelog

## v4.3.0
- Fix: ShotMarker **archive CSV** imports now split into correct per‑string targets (e.g., R1/R2/R3) instead of collapsing or over‑splitting.
- Fix: Target↔chrono pairing now matches **true target/string count** from ShotMarker archive exports.
- UI: “Last” column clarified as **Last session** with compact cell rendering + tooltip.
- UI: Import notes are **grouped/capped** to avoid noisy debug spam.
- Maintains: local‑only, deterministic scoring; vertical‑first; confidence‑weighted ranking.
