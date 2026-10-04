# Impact vs. Effort Prioritization Matrix: Meridian Backlog

This document details the prioritization analysis for the 14 backlog items using an **Impact vs. Effort Matrix** tailored for Meridian Foundations' 10-person squad. 

To ensure the roadmap is realistic, we have applied the **Product School Reality Check**:
*   **Estimated Impact:** 1 to 5 (how much it moves our frontline adoption & mid-market retention OKRs under optimistic conditions).
*   **Reality-Checked Impact:** **Halved** (Impact / 2) to account for user inertia and adoption friction.
*   **Estimated Effort:** 1 to 5 (how much design, PM, and dev effort we initially assume it takes).
*   **Reality-Checked Effort:** **Doubled** (Effort * 2, capped at 5) to account for construction environment complexity, offline edge cases, and testing cycles.

---

## 1. Prioritization Quadrants

Based on the **Reality-Checked** scores, items are mapped into four distinct strategic quadrants:

```
                  HIGH IMPACT
                      │
     PLAN CAREFULLY   │     ROCKS (DO NOW)
     (High Effort)    │     (Low Effort / High Impact)
                      │
     [Item 1, 7]      │     [Item 4]
                      │
──────────────────────┼─────────────────────── LOW EFFORT
                      │
     AVOID (HARD NO)  │     FILL GAPS (QUICK WINS)
     (High Effort)    │     (Low Effort / Low Impact)
                      │
     [Item 3, 5, 9,   │     [Item 2, 6, 8, 11]
      10, 12, 13, 14] │
                      │
                  LOW IMPACT
```

---

## 2. Complete Backlog Prioritization Table

| # | Backlog Item | Est. Impact | Est. Effort | Reality Impact (x0.5) | Reality Effort (x2) | Priority Quadrant | Strategic Decision & Connection to OKRs |
|---|---|:---:|:---:|:---:|:---:|---|---|
| **1** | **Build offline-first mobile experience** | 5.0 | 2.5 | **2.5** | **5.0 (max)** | **Rock / Do Now** (High Effort, High Impact) | **PRIORITIZE (Rock #2):** Core baseline requirement. If the app fails offline, foremen will bypass it. Connects to **KR1 & KR2**. |
| **2** | **Add photo markup and annotation tool** | 3.0 | 1.5 | **1.5** | **3.0** | **Fill Gaps (Quick Win)** | **PLAN:** Useful for the field, but we will utilize standard OS photo markups rather than building a custom drawing tool. |
| **3** | **Migrate data model to multi-project** | 3.0 | 2.0 | **1.5** | **4.0** | **Avoid This Quarter** | **DEFER:** Pure back-end tech debt. Important for future scale, but does not move our active foreman adoption metrics today. |
| **4** | **Simplify daily log (14 fields to 4)** | 5.0 | 1.0 | **2.5** | **2.0** | **Rock / Do Now** (Low Effort, High Impact) | **PRIORITIZE (Rock #3):** The ultimate leverage point. Directly drops foreman log time to under 3 minutes. Connects to **KR2**. |
| **5** | **Build compliance checklist generator** | 3.0 | 2.5 | **1.5** | **5.0 (max)** | **Avoid This Quarter** | **DEFER:** Office workflow feature requested by Sales. Takes massive engineering focus away from the active job site experience. |
| **6** | **Add real-time weather to scheduling** | 2.0 | 1.0 | **1.0** | **2.0** | **Fill Gaps (Quick Win)** | **PLAN:** We will auto-fill weather on the *mobile log* (helps foreman), but scheduling integration on the web is a distraction. |
| **7** | **Create foreman-facing mobile app** | 5.0 | 2.5 | **2.5** | **5.0 (max)** | **Rock / Do Now** (High Effort, High Impact) | **PRIORITIZE (Rock #1):** The essential vehicle for our bottom-up adoption strategy. Decouples field from administrative web UI. Connects to **KR1 & KR3**. |
| **8** | **Fix Procore integration (broken for 2 GCs)**| 4.0 | 1.0 | **2.0** | **2.0** | **Fill Gaps (Quick Win)** | **DO NOW (Patch):** Low-effort fix to prevent immediate churn of 2 at-risk accounts. Handled by a single support developer. |
| **9** | **Add AI-assisted RFI drafting** | 2.0 | 2.0 | **1.0** | **4.0** | **Avoid This Quarter** | **DEFER:** AI is a shiny distraction. Foremen do not want or trust AI to draft contractual and legally binding RFI documents on-site. |
| **10**| **Build executive dashboard with custom KPIs** | 4.0 | 2.0 | **2.0** | **4.0** | **Hard No (Avoid)** | **VETO:** Custom executive dashboards are a trap. We cannot build reports on data that does not exist due to zero field adoption. |
| **11**| **Enable push notifications for schedule** | 3.0 | 1.5 | **1.5** | **3.0** | **Fill Gaps (Quick Win)** | **PLAN:** Good field utility. Will be scheduled in Next/Later once the standalone foreman mobile app container is live. |
| **12**| **Add a time-tracking module** | 4.0 | 3.0 | **2.0** | **5.0 (max)** | **Hard No (Avoid)** | **VETO:** Complex payroll rules, geo-fencing, and legal compliance. Would completely consume our 10-person squad. |
| **13**| **Refresh the web UI** | 3.0 | 2.5 | **1.5** | **5.0 (max)** | **Hard No (Avoid)** | **VETO:** Purely cosmetic web UI changes for sales demos. Zero impact on job site foremen and field adoption. |
| **14**| **Build subcontractor portal** | 3.0 | 3.0 | **1.5** | **5.0 (max)** | **Hard No (Avoid)** | **VETO:** Building a secure, multi-tenant portal from scratch is a massive undertaking. Out of scope for our immediate adoption focus. |

---

## 3. Analysis & Key Takeaways

1.  **Why "Easy" Features Become "Hard":**
    *   Many items that look simple initially (like *Item #13: Refreshing Web UI* or *Item #12: Time Tracking*) expand exponentially under the reality check. UI refreshes trigger infinite regression bugs across legacy browsers, and time-tracking leads to complex legal and wage-and-hour compliance rules.
2.  **The Priority Defensibility:**
    *   By forcing the Reality-Checked math, we clearly defend why we are ignoring shiny requests from Enterprise Sales (like *AI-RFI Drafting*) and cosmetic requests (like *Web UI Refreshes*). 
    *   We mathematically justify putting our limited 10-person squad's weight behind **Item 1 (Offline Sync)**, **Item 4 (Log Simplification)**, and **Item 7 (Foreman-focused Mobile App)**. These are the only bets that structurally change the bottom-up adoption equation.
