# Prioritization & Roadmapping, Module 2 Lab

## Prioritize your Rocks and your Hard Nos

### The 3 Rocks (Do Now - laser-focused on M1 OKRs)

- **Rock #1: Item #7 - Create a foreman-facing mobile app (separate from the PM web app)**
  * **How it connects to M1 OKR:** This is the foundational "container" for our entire bottom-up adoption strategy. To increase mobile daily log submissions from 15% to 70% (KR1) and reduce adoption-driven churn (KR3), we must decouple the complex, cluttered administrative web app from what the foreman sees. A dedicated, clean mobile app designed specifically for a foreman on a muddy, high-speed job site is the single most important vehicle for securing daily field habits.

- **Rock #2: Item #1 - Build offline-first mobile experience for job sites with poor connectivity**
  * **How it connects to M1 OKR:** Construction sites are notorious for zero-to-poor network coverage. If a foreman's log or photo upload fails even once due to signal drops, they will immediately abandon the app and revert to paper or personal WhatsApp chats. Building rock-solid offline-first local caching and background syncing directly enables KR1 and KR2 by guaranteeing their logs are captured instantly on-site, even with zero network connectivity.

- **Rock #3: Item #4 - Simplify the daily log: reduce from 14 required fields to 4**
  * **How it connects to M1 OKR:** This is our silver bullet for **KR2** (reducing foreman log completion time from 25 minutes to under 3 minutes). Every extra input field is a point of friction that drives foremen away. By cutting the required fields down to the absolute bare minimum of 4 critical operational compliance items (e.g., photo upload, crew count, work description, and weather), we transform log entry from a painful 25-minute desk chore into a friction-free, sub-3 minute on-site tap.

---

### ❌ The 3 Hard Nos (Avoid This Quarter - protecting the 10-person squad)

- **❌ Hard No #1: Item #13 - Refresh the web UI (feedback: "looks outdated" from prospects)**
  * **Why not this quarter:** Cosmetic web UI refreshes for sales prospects consume massive designer and front-end developer bandwidth but provide **zero** functional value to the foreman in the field, doing absolutely nothing to solve our critical field-adoption crisis and mid-market churn.

- **❌ Hard No #2: Item #10 - Build an executive reporting dashboard with custom KPIs**
  * **Why not this quarter:** While executive dashboards are highly requested by buyers during renewals, building bespoke analytical metrics is a resource-intensive trap. More importantly, custom dashboards are useless without clean data. We must freeze executive dashboards until we have stabilized frontline mobile adoption to feed those dashboards with actual, real-time job site data.

- **❌ Hard No #3: Item #14 - Build a subcontractor portal with document sharing**
  * **Why not this quarter:** Developing a secure multi-tenant subcontractor document portal requires a complex access-permission architecture and massive file storage infrastructure. Building this would fully consume our 10-person squad for the entire quarter, leaving no bandwidth to build the critical offline-first syncing or log-simplification Rocks.

---

## Show and swap

- **Do the Rock selections feel traceable to a clear strategy, or do they read like a feature list?:** 
  They are deeply traceable to our core strategy of "Frictionless Field Capturing" and eliminating "Time-to-Response" gaps to compete with WhatsApp. Decoupling the app (Item 7), making it work offline (Item 1), and cutting fields to 4 (Item 4) are the exact physical prerequisites to achieving that frictionless state. It is not a random grab-bag of features; it is a laser-focused, interconnected adoption engine where each Rock directly reinforces the others.

- **Pick one Hard No and make the case for why it should actually be a Rock.:**
  Let's take **Item #10 (Build an executive reporting dashboard with custom KPIs)**. A desperate Sales or CS Rep would argue: *"We have two massive enterprise renewals at risk right now because they want to see custom KPIs. If we don't build this dashboard, they will churn, costing us $200k ARR this quarter. It must be a Rock!"* 
  
  Our strategic rebuttal: *"Building that dashboard is building a pipe with no water. GCs are threatening to churn because the data inside their reports is empty or manually double-entered weeks late, because their field foremen are bypassing our tool. Even if we spend the quarter building custom charts, those charts will show blank graphs because of 0% adoption. We must focus on the field adoption Rocks first to fill the database; once the water is flowing, building the dashboard in Phase 2 is trivial."*

---

## Review and refine

- **Does every Now item read as a strategic bet, or does it sound like a feature description?:** 
  Every Now item is phrased as a strategic bet. Instead of flat feature descriptions like "Build a chat button," they are "Eliminate core input friction and connectivity hurdles" and "Collapse communication latency." They are framed as systemic outcomes and behaviors that we are enabling for the foreman, making our product intentions crystal clear.

- **Can you trace every Now item back to one of your OKRs?:** 
  Yes, seamlessly:
  * *"Eliminate core input friction & connectivity hurdles"* -> **KR1** (mobile daily logs submitted directly from field) and **KR3** (reduce adoption-driven churn).
  * *"Collapse communication latency"* -> **KR1** and **KR3** (provides the instant response loop foremen need to stay in the app).
  * *"Sub-3 minute daily logging"* -> **KR2** (reduce daily log submission time to under 3 minutes).
  * *"Dissolve the surveillance barrier"* -> **KR1**, **KR2**, and **KR3** (removes the psychological blocker to active daily app adoption).

- **If someone who had never seen your strategy read the Now column, would they know what problem you are solving this quarter?:** 
  Absolutely. The theme of the Now column is unmistakably focused on **eliminating the friction, latency, and connectivity barriers** that force foremen to abandon our software for personal WhatsApp/SMS chats. It is 100% focused on capturing frontline site activity at the source.

---

## Save your roadmap

- **Where did you save your roadmap? (link or file):** 
  _[02-roadmap/visual-roadmap.html](https://github.com/mariaquijada/product-leadership-final/blob/main/02-roadmap/visual-roadmap.html)_

