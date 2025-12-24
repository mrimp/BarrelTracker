# BarrelTracker

Local-first companion to NodeLab: import NodeLab snapshot JSONs, track barrel round count (incl. sighters), and rank barrels over life.

## Live app
https://mrimp.github.io/BarrelTracker/

**Track barrel performance over time. Trust the right barrel when it matters.**

BarrelTracker is a lightweight, fully standalone companion to NodeLab that helps long-range shooters track barrel health, performance trends, and lifecycle events across the life of a barrel.

It is designed to answer one question clearly:

> *Which barrel should I trust today — and why?*

All analysis runs locally in your browser. No accounts. No cloud. No noise.

---

## What BarrelTracker Does

BarrelTracker ingests snapshot exports from NodeLab and builds a time-ordered performance history for each barrel. It tracks:

- Total round count (including sighters, by design)
- Vertical dispersion at distance
- Velocity SD
- Confidence-weighted performance
- Performance trends as barrels age
- Key lifecycle events (setback, rethroat, lot changes, optic removal, notes)

Results are summarized into:
- **Current form** (recent performance window)
- **Aging signal** (performance trend over time)
- **Rankings** that favor vertical consistency at distance

The goal is not to predict failure — it’s to surface *signal* early and conservatively.

---

## Day-0 Baseline (Recommended Workflow)

BarrelTracker works best when every barrel starts with a clean baseline.

**Day-0 best practice:**
- Same load
- Same distance (e.g. 1000y)
- ~20 record shots per barrel
- One NodeLab snapshot per barrel

Import those snapshots once. From there, BarrelTracker builds history automatically as you continue shooting and importing new data.

---

## Ranking Philosophy (Short Version)

- Vertical dispersion matters most at distance
- Low-confidence data is discounted
- Recent performance matters more than old data
- Worsening trends are penalized
- Missing data is handled gracefully

There are no hard pass/fail rules. BarrelTracker stays conservative by default.

Advanced users can tune weighting and wi


