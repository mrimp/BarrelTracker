# BarrelTracker — Barrel Registry Specification (v1.0)

This document defines the **barrel registry model** used by BarrelTracker to represent physical barrels, their specifications, and lifecycle state.

The barrel registry is the **authoritative source of truth** for barrel identity and hardware context.  
Snapshots and events reference barrels — they do not define them.

---

## 1. Design Principles

- A barrel is a **physical object**, not just an ID
- Hardware specs are entered **once**, not inferred
- History is never deleted by default
- Retired barrels remain readable but do not rank
- Registry must scale from **3 barrels to dozens**
- Model must support future **multi-rifle** expansion

---

## 2. Barrel Registry Structure

```json
{
  "registry": {
    "rifles": {
      "R1": {
        "rifleId": "R1",
        "label": "Match Rifle",
        "createdAt": "2025-12-24T00:00:00Z"
      }
    },

    "barrels": {
      "B1": {
        "barrelId": "B1",
        "label": "B1",
        "rifleId": "R1",

        "status": "active",
        "retiredAt": null,

        "specs": {
          "twistIn": 8.5,
          "boreIn": 0.276,
          "contour": "1.25 straight",
          "lengthIn": 32,
          "chamber": "284 Shehane – Smith reamer #2",
          "rifling": "5R",
          "maker": "Bartlein"
        },

        "tags": ["match"],
        "notes": "Primary match barrel"
      }
    }
  }
}
