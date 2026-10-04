# Master Product Financials & Strategic Bets, Module 5 Lab

## Make your evaluation and funding decision

- **What assumption is doing the most work? If this number is 20-30% off, what changes?:**
  The assumption doing the most work is the **Standard-to-Enterprise upsell rate (assumed to grow from 6% to 8%)**. Because the business case relies on a very small absolute conversion delta (just 2 percentage points), even a minor deviation completely breaks the financial model.

  **If this target of 8% is 30% off:**
  - **Target rate is 30% off:** If the 8% target is 30% lower than expected, the actual upsell rate lands at **5.6%** ($8\% \times 0.7$). Because 5.6% is *lower* than our baseline of 6%, we actually generate *fewer* upgrades than we would have without building the feature (22 upgrades vs. 24 baseline). The incremental ARR is **$0**, and we completely write off the entire $180,000 engineering cost.
  - **Scenario B (The 2% incremental lift is 30% off):** If the assumed 2% conversion lift is 30% lower than expected (a 1.4% lift, meaning a total upsell rate of **7.4%**), total upgrades drop from 32 to 29.6. True incremental upgrades drop from 8 to **5.6**, and true incremental ARR drops from $224,000 to **$156,800**. This causes the payback period on our $180,000 build to jump from 9.6 months to **13.8 months**, making the business wait over a year just to break even on a highly speculative feature.

- **What is the structural problem in this case? Look past the headline numbers for something that does not hold up on closer inspection.:**
  There are three major structural problems in this case:
  1. **Double-counting baseline revenue as incremental revenue:** The business case claims the *entire* 8% upsell pool ($896,000 ARR from 32 upsells) as the "Expected Return" to justify the $180,000 build and a 2.4-month payback period. In reality, 6% of Standard accounts were already upselling ($672,000 ARR baseline). The true *incremental* ARR is only the 2% delta (8 upsells = $224,000 ARR). This means the actual payback period is **9.6 months** ($180,000 / $224,000 ARR), not 2.4 months.
  2. **The "Zero-CAC" Enterprise Upsell Assumption:** The model notes "Standard CAC $620" but completely omits Enterprise CAC or the high-touch Sales/Account Management commissions and resources required to upgrade standard accounts to $28,000/year enterprise contracts.

- **Is the kill criterion complete and actionable? Does it name the consequence, or hand the decision back to the room?:**
  The kill criterion (*"if Standard-to-Enterprise upsell has not reached 7% by end of Q3, the AI estimation feature is paused and the Q4 engineering capacity reallocated before headcount is committed"*) is structured well on paper: it has a clear metric (7%), a timeline (end of Q3), and a concrete consequence (pause and reallocate).
  
  However, it suffers from two major flaws:
  1. **It is a lagging metric:** Upsell rates are measured over quarters and are highly dependent on sales cycle length and sales team performance. Waiting until the end of Q3 to measure Standard-to-Enterprise upsell means wasting months of engineering capacity on a feature that may have 0% actual user adoption.
  2. **It lacks leading indicators:** A high-integrity kill criterion must include a leading indicator of user engagement (e.g., *"% of active PMs drafting at least 3 bids using the AI feature within 30 days of launch"*). Without this, the team cannot diagnose whether a failure is due to product utility or sales execution.

- **Your verdict: FUND / FUND WITH ONE CONDITION / DO NOT FUND. If a condition, name it; otherwise explain in one sentence.:**
  **DO NOT FUND.**
  
  **Explanation:** The business case is built on inflated, double-counted incremental returns ($896k vs. $224k actual) and represents a massive strategic distraction from Meridian's existential field-adoption crisis, violating our strict 12-month hard no on pre-construction/bidding tools.

---

## Write your business case

- **The strategic bet. What specific outcome are you backing, who does it serve, and what is the mechanism that connects the product decision to a financial result?:**
  **[Selected M2 Rock: Rock #2 (Item #1) — Build offline-first mobile experience for job sites with poor connectivity]**

  We are investing in a robust **Offline-First Synchronization Engine** (with local SQLite database caching and automated background syncing) for our foreman-facing mobile app container. 
  
  This serves frontline field crews (foremen and superintendents) working on commercial construction sites with poor, intermittent, or non-existent network connectivity. 
  
  **The mechanism:** When a foreman attempts to log site progress or upload photos and the sync fails or hangs, they instantly abandon the app and revert to paper or WhatsApp. By guaranteeing that every log, photo, and safety report is captured instantly local-first and synchronized seamlessly in the background without user intervention, we eliminate the primary physical point of software friction. This drives our frontline mobile daily logging rate from 15% to 70% (KR1), securing the flow of real-time site data that General Contractors buy Meridian for. This direct frontline utility prevents mid-market account churn (KR3) and unlocks bottom-up growth.

- **The assumptions. List the assumptions your case rests on, then rank them: which one, if wrong, most changes your conclusion?:**
  1. **[Load-bearing] Connectivity is the primary friction point:** Foremen bypass Meridian for WhatsApp primarily because of uploading lag and connection-drop failures, rather than a fundamental resistance to digital logging. (If wrong, solving offline sync won't drive Weekly Active Users (WAU), and the bet fails).
  2. **Adoption directly drives retention:** Solving frontline adoption (reaching 70% daily log rate) will successfully reduce our mid-market monthly churn from 4.2% to under 1.0%. (If wrong, our Lifetime Value (LTV) expansion model breaks).
  3. **Engineering capability is sufficient:** Our 10-person squad can implement a stable local-cache architecture within 3 months without requiring a complete backend API overhaul.
  4. **Data conflict resolution is seamless:** The background sync can resolve concurrent operational updates gracefully without causing data-loss or corrupting project records.

- **The expected return. What does the bet generate and when? Express it at unit level (per customer) and at scale (what volume hits target).:**
  - **Unit Level:** For each mid-market General Contractor ($35,000 average ACV), eliminating field friction stabilizes their subscription. This shifts customer lifetime from 2.0 years (LTV $70,000 at 4.2% monthly churn) to 8.3 years (LTV $291,500 at 1.0% target monthly churn)—representing an **incremental LTV increase of $221,500 per customer (a 4.1x LTV:CAC multiple improvement)**.
  - **At Scale:** Over 12 months, preventing 57 accounts from churning saves **$2,020,000 in ARR**, and securing high field adoption drives 30 organic new logo wins ($1,050,000 ARR) through field word-of-mouth, totaling **$3,070,000 in saved/new ARR**. The cost of this 3-month engineering phase is **$450,000** (one quarter of our $1.8M fully-loaded squad budget). This represents a Year 1 **ROI of 582%** on the specific build cost and a **payback period of 1.7 months** against the saved ARR.

- **The kill criterion. Name the specific metric, threshold, timeline, and financial consequence that tells the team to stop. Actionable, not a conversation.:**
  If by **Month 3 (December 31, 2026)**, the **Weekly Active User (WAU) rate** of frontline foremen across our 15 pilot projects is below **45%** OR the **daily log mobile sync failure rate** on low-connectivity sites remains above **2%** (from a 12% baseline), we will **immediately halt the offline-sync stream, cancel all scheduled downstream mobile features (photo markup and weather integrations), and reallocate the remaining Q4 engineering capacity to building standard compliance exports (CSV/JSON templates)** to safeguard our cash runway, saving $1.35M of the remaining annual budget.

---

## Stress-test and finalize

- **Paste your finalized business case here.:**
  ### Business Case One-Pager: Offline-First Sync Engine (M2 Backlog: Rock #2 / Item #1)
  
  **The Strategic Bet**
  We are investing in a robust **Offline-First Synchronization Engine** (with local SQLite database caching and automated background syncing) for our foreman-facing mobile app container, directly executing **Rock #2 (Item #1)** from our Module 2 outcome roadmap. This serves frontline field crews (foremen and superintendents) working on commercial construction sites with poor, intermittent, or non-existent network connectivity. When a foreman attempts to log site progress or upload photos and the sync fails or hangs, they instantly abandon the app and revert to paper or WhatsApp. By guaranteeing that every log, photo, and safety report is captured instantly local-first and synchronized seamlessly in the background without user intervention, we eliminate the primary physical point of software friction. This drives our frontline mobile daily logging rate from 15% to 70% (KR1), securing the flow of real-time site data that GCs buy Meridian for. This direct frontline utility prevents mid-market account churn (KR3) and unlocks bottom-up growth.
  
  #### 1. Unit Economics & Financial Assumptions
  - **Average Mid-Market ACV:** $35,000 ($2.9k/month per general contractor)
  - **Current Segment Monthly Churn:** 4.2% (40.3% annualized) due to zero frontline adoption
  - **Target Segment Monthly Churn:** 1.0% (11.4% annualized) post-mobile adoption
  - **Baseline LTV:** $70,000 (Average lifetime of ~2.0 years)
  - **Target LTV:** $291,500 (Average lifetime of ~8.3 years) — **a 4.1x LTV expansion delta of +$221,500 per customer**
  - **Current CAC:** $15,000 (High due to long sales cycles trying to justify a non-adopted platform)
  - **Target CAC:** $10,000 (33% reduction driven by high field adoption and organic word-of-mouth referrals)
  - **Current LTV:CAC Ratio:** 4.7:1 -> **Target LTV:CAC Ratio:** 29.2:1 (or 24.3:1 if CAC remains at $12,000)
  
  #### 2. Expected Strategic & Financial Return
  - **Build Cost (3 Months):** $450,000 (Loaded cost of 10-person squad + 1 PM + 1 UX Designer for one quarter)
  - **Year 1 Segment Return:** **$3,070,000 ARR** — comprised of **$2,020,000 saved ARR** (preventing 57 accounts from churning) + **$1,050,000 new ARR** (30 new logo wins driven by field referrals).
  - **ROI (on Build Cost):** 582% ROI in Year 1.
  - **Payback Period:** **1.7 months** against saved ARR ($450,000 build cost / $2,020,000 saved ARR over 12 months).
  
  #### 3. Key Assumptions (Ranked by Risk)
  1. **[Load-bearing] Connectivity is the primary friction point:** Foremen bypass Meridian for WhatsApp primarily because of uploading lag and connection-drop failures, rather than a fundamental resistance to digital logging. *If connectivity is NOT the primary friction point (e.g., they bypass it because they view it as corporate surveillance), then our 3-month offline-sync build will yield 0% adoption change, resulting in a $450,000 write-off.*
  2. **Adoption directly drives retention:** Solving frontline adoption (reaching 70% daily log rate) will successfully reduce our mid-market monthly churn from 4.2% to under 1.0%.
  3. **Engineering capability is sufficient:** Our 10-person squad can implement a stable local-cache architecture within 3 months without requiring a complete backend API overhaul.
  4. **Data conflict resolution is seamless:** The background sync can resolve concurrent operational updates gracefully without causing data-loss or corrupting project records.
  
  #### 4. CFO Stress-Test Sensitivity Checks
  - **Check 1: Load-Bearing Failure:** If the load-bearing assumption fails and WAU is unaffected, we halt further mobile feature capacity at Month 3, capping our losses at $450,000 and saving the remaining $1.35M of our annual budget. We will also pair the offline build with "private work-in-progress drafts" features to dissolve the surveillance barrier.
  - **Check 2: Retention Sensitivity:** If annualized churn is **10 percentage points higher than projected** (21.4% annualized or ~1.9% monthly, instead of 11.4%), LTV drops to $163,551. At our target CAC of $10,000, the LTV:CAC is **16.4:1**. Even if CAC runs high at $15,000, LTV:CAC remains **10.9:1** — well above the 3:1 venture standard.
  - **Check 3: Payback Reality Check:** If customer acquisition cost runs **20% higher than projected** ($12,000 instead of $10,000 target): at standard ACV of $35k ($2.9k MRR), the payback period is **4.1 months**. The business is highly willing to wait for this, as it is far below the 12-month B2B SaaS benchmark.
  
  #### 5. Strict Kill Criterion
  > If by **Month 3 (December 31, 2026)**, the **Weekly Active User (WAU) rate** of frontline foremen across our 15 pilot projects is below **45%** OR the **daily log mobile sync failure rate** on low-connectivity sites remains above **2%** (from a 12% baseline), we will **immediately halt the offline-sync stream, cancel all scheduled downstream mobile features (photo markup and weather integrations), and reallocate the remaining Q4 engineering capacity to building standard compliance exports (CSV/JSON templates)** to safeguard our cash runway, saving $1.35M of the remaining annual budget.
  
  **CFO Verdict:** *"I would approve this case because it directly targets our largest revenue risk (4.2% monthly churn losing $2.6M ARR annually) with highly resilient unit economics (retains >10:1 LTV:CAC even under stress-test scenarios), and establishes a high-integrity, actionable kill criterion that stops further engineering bleed if pilot adoption fails."*
