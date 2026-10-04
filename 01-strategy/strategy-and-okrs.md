# Craft an Advanced Product Strategy, Module 1 Lab

## Write your one-page strategy
- **Winning aspiration: define winning in the customer's terms, not internal metrics. What does success look like for the specific person you serve?:** 
  To be the undisputed single source of truth for commercial construction projects by becoming the most loved, easiest-to-use daily utility for frontline field crews (foremen and superintendents), ensuring 100% real-time data accuracy for general contractors without manual office-entry overhead.

- **Where to play: segment, geography, and use case, explicitly. Which customers, markets, and surfaces will you focus on?:** 
  - **Target Segment:** $50M+ Enterprise General Contractors (retaining current footprints) and $5M–$50M Mid-Market General Contractors (expanding and preventing churn).
  - **Geography:** North America.
  - **Channel:** Direct B2B sales and Customer Success-driven expansion.
  - **Core Use Cases:** High-frequency, frontline operations—specifically daily logging, photo capture, safety reports, and rapid field-to-office operational loops.
  - **Exclusions (The No's):** We will NOT build pre-construction/bidding tools, we will NOT handle heavy warehouse/inventory logistics, and we will NOT build custom back-office ERP integrations.

- **How to win: your differentiator. What can you do that your specific competitors cannot easily replicate?:** 
  **Frictionless Field Capturing & Real-Time Response Loops:** We make mobile logging, photo capturing, and field-office communication *faster, easier, and more interactive* than WhatsApp. Critically, we replicate the near-zero **Time-to-Response** that makes WhatsApp so addictive. 
  In legacy B2B software, when a foreman uploads a site issue, it enters a slow back-office email queue. In Meridian, it triggers real-time, push-notified chat threads where the office can reply in one tap. By matching the immediate feedback loop of personal texting (double checks, instant notifications), foremen know their blocking questions will be resolved in minutes, making them actively *prefer* Meridian over unauthorized text chains. Competitors with heavy, legacy database software cannot match this live operational loop without a complete architectural rebuild.

- **Capabilities required: what you must be world-class at. What will you build, buy, or partner for?:** 
  1. **Offline-First Synchronization (Build):** Rock-solid local caching and background syncing so the mobile app never fails on-site, even with zero network connectivity.
  2. **Real-Time field-to-Office Notification & Quick-Reply Engine (Build):** A high-speed messaging broker that delivers instant push notifications and "one-tap replies" for office staff, ensuring near-zero communication latency.
  3. **Voice-to-Text & Smart OCR Progress Extraction (Build/Partner):** Allowing foremen to "speak" their daily logs while walking the site, automatically converting audio to structured daily log entries.

- **Management systems: the metrics and rituals that keep your choices alive quarter to quarter.:** 
  - **Core Metrics:**
    1. *Frontline Adoption Rate (%):* The percentage of active projects where daily logs and photos are submitted via the Meridian mobile app rather than desktop or skipped entirely.
    2. *Foreman Log Submission Time (Min):* The active minutes spent by a foreman to draft and submit a compliant daily progress report.
  - **Rituals:**
    1. *Weekly Field Walks:* Every PM and designer spends at least one full day on-site with active superintendents/foremen.
    2. *Bi-Weekly Operational Sentiment:* Simple in-app micro-surveys measuring frontline software friction.
    3. *Monthly Adoption-Driven Churn Audits:* Tracking early warning signs (e.g., when a foreman reverts to WhatsApp) to proactively trigger Customer Success intervention.

## Name your one hard no
- **Your one hard no:** 
  We will **NOT** build any new custom ERP integrations or bespoke back-office financial reporting modules for the next 12 months. We will rely entirely on our existing standard open APIs.
  
  **Why this protects focus:** Custom ERP integrations (e.g., with legacy versions of Sage, Oracle, or SAP) are incredibly high-touch, slow-moving projects that consume massive engineering resources. For our 10-person squad, spending time on bespoke back-office connections is a trap. It satisfies the legacy, non-user buyer during a sales cycle but does absolutely nothing to address the zero frontline adoption crisis. By enforcing a hard "no" on ERP customization, we preserve 100% of our capacity to design, build, and refine the mobile-first frontline experience that will actually save our mid-market segment from churning.

## Write your three OKRs
- **Objective:** Establish Meridian as the undisputed daily habit for frontline field crews, turning raw field activity into high-value compliance data for general contractors.
- **KR1:** Increase the percentage of weekly active projects where 80%+ of Daily Logs are submitted directly from the field via the Meridian mobile app (vs web/bypassed) within 4 hours of shift end from 15% to 70% by Q4 2026.
- **KR2:** Reduce the average time to submit a compliant, photo-verified, and geo-weather-tagged daily progress log from 25 minutes to under 3 minutes via mobile (maintaining a 95%+ data-completeness rating) by Q4 2026.
- **KR3:** Decrease mid-market ($5M–$50M project size) monthly account churn rate driven by "lack of field adoption" from 4.2% to under 1.0% by Q4 2026.

## AI pressure-test
- **Which challenge from the AI is most valid, and why?:** 
  The **Surveillance Barrier** challenge is the most valid. Foremen and field crews are notoriously skeptical of new software tools, often viewing them as corporate surveillance designed to track their locations, micromanage their time, and audit their mistakes. If they perceive Meridian as a tool for the office to monitor them, they will actively resist using it—no matter how fast or easy the interface is. They will continue to run projects on private WhatsApp groups to keep their operational sanctuary.
  
- **What would you change based on the pushback, and what would you defend?:** 
  - **What we will change:** We will design features that give value *directly* to the foremen before sending data to the office. We will implement "private work-in-progress drafts" and auto-generated field tools (like offline weather logs and instant crew-hour calculators) so they view the app as a site assistant that saves them personal administrative headache, rather than a tracker.
  - **What we will defend:**
    - *The ERP Integration Wall (Hard No on ERP):* We will defend our hard "no" on custom ERP integrations. With a team of only 10, custom back-office work is a massive resource sink that doesn't solve frontline adoption. We will lose some enterprise sales deals in the short term to ensure we stop mid-market churn.
    - *Our 'How to Win' Defensibility:* We will defend that while competitors can copy our messaging UI, they cannot replicate our deep site-by-site trust and structured, offline-first operational engine which automatically binds conversation metadata into compliant daily logs.
