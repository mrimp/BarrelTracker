# BarrelTracker — Lifecycle Events Specification

This document defines **event types**, **data structure**, **UI behavior**, and **migration rules** for lifecycle events in BarrelTracker.

Events annotate the barrel timeline to explain *why* performance (POI, vertical, SD, confidence) changes over time.  
Events **do not affect scoring** — they provide context only.

---

## 1. Event Purpose

Lifecycle events capture **non-barrel-wear changes** that may influence results, including:

- Gunsmith work (setback, rethroat)
- Tuner adjustments
- Component lot changes
- Scope removal / reinstall (travel)
- Scope swaps
- Action or torque work
- Free-form notes

Events appear as markers on charts and as rows in the event timeline.

---

## 2. Event Type Enum (Final)

```ts
type BarrelEventType =
  | "setback"
  | "rethroat"
  | "tuner_change"
  | "powder_lot"
  | "bullet_lot"
  | "primer_lot"
  | "brass_lot"
  | "scope_swap"
  | "scope_reinstall"
  | "action_work"
  | "note";
