# Lead and Develop High-Performing Teams, Module 3 Lab

## Name the situation
- **Who they are (role, not name), what you have observed, and how long it has been happening.:** A Senior Backend Engineer on our 10-person Foundations squad has consistently underestimated the development resources and time required for core sync and integration tasks over the past 3 months (for example, estimating local SQLite sync caching at 2 weeks when it actually took 5 weeks). This pattern has repeatedly shifted our entire initiative's timeline, delaying our Q4 core mobile-first launch milestones by over a month and causing significant team-wide planning friction.

## Make a diagnosis
- **Your diagnosis, plus one sentence on why. Is your frustration with their behavior, or with a decision you made?:** **System Problem.** The root cause is not the engineer's work ethic or ability, but rather a structural failure in our roadmap process: we do not have a robust capacity planner, meaning engineers are constantly pulled into ad-hoc requests (such as sales support and Procore hotfixes) with zero forward-looking visibility into which initiatives they are needed on. My frustration is with a systemic decision I made: I didn't include a comprehensive capacity planning tool or explicit resource-allocation buffers in our roadmap, forcing engineers to estimate tasks in a vacuum without accounting for context-switching overhead and competing demands.

## Write your opening line
- **One next action I will take in the next two weeks is:** Partner with our Engineering Manager and Tech Lead to design and integrate a bi-weekly capacity planner and allocation visualizer into our sprint planning and roadmapping cycle, then sit down with the engineer to co-create a more structured, context-aware estimation framework.
- **The first sentence of the conversation I need to have is:** "Looking back at our roadmap slips yesterday, I noticed that the local offline caching task ended up taking five weeks instead of the estimated two, which has delayed our main mobile timeline; I realize our current roadmapping process doesn't give you a clear capacity planner or show which initiatives you'll be needed on next, and I want to figure out how we can fix this systemic planning issue together."

## AI role-play
- **After you step out: what did the role-play change about how you will open this conversation for real?:** The role-play helped me realize that the engineer is not being careless with estimates; they are drowning in context-switching and feel immense pressure to provide "optimistic" estimates because they have no formal way to visualize or defend their actual capacity limits. By opening the conversation with a systemic diagnosis (focusing on the lack of a capacity planner in our roadmap) rather than accusing them of poor estimation, I can dismantle their defensiveness, validate their frustration with context-switching, and immediately establish a collaborative partnership to build a capacity planning system.

## Refine and complete your charter
- **What We Own. What this team owns.:** We own the Foundations initiative's customer outcomes and surfaces: 
    - PM 1 owns the decoupled Foreman Mobile App (iOS/Android), local offline SQLite database caching, push notifications, and frontline adoption metrics (KR1, KR2, and KR3 - reducing field-adoption driven churn). 
    - PM 2 owns the Enterprise back-office web dashboards, compliance exports, data completeness/compliance ratings (95%+), and enterprise buyer satisfaction metrics. 
    - Together, we share a single 10-person cross-functional engineering team, which is permanently allocated at an 80/20 capacity split (80% dedicated to PM 1's mobile/field-adoption work, 20% to PM 2's enterprise maintenance/compliance exports).
- **What is out of scope.:** Custom ERP integrations, custom financial reporting modules, heavy warehouse/inventory logistics, and pre-construction/bidding tools. These are strictly out of scope for the next 12 months under our strategic Hard No.
- **Cross-boundary decisions that need a joint call.:** Any change to the 80/20 engineering capacity allocation, any modification to the shared main corporate database schemas or central API gateway, and any feature request tied directly to sales agreements that touches the mobile app's offline synchronization engine.
- **How We Decide. Who decides feature and scope calls.:** 
    - PM 1 has final decision authority (the "D" in DACI) over mobile scope and field-adoption features. 
    - PM 2 has final decision authority over enterprise web dashboards and standard compliance data exports. 
    - The Product Lead (me) is the Approver ("A") and has final authority over all engineering resource allocations and roadmapping trade-offs across both PMs.
- **How cross-team conflicts escalate.:** 
    - If PM 1 and PM 2 disagree on shared resource allocations or boundary-crossing features, they must escalate to the Initiative Product Lead within 24 hours. 
    - The escalation must be done via a synchronous, 15-minute face-to-face or video call (not via Slack threads), presenting a simple two-option trade-off memo comparing user adoption impact vs. technical debt.
- **Who resolves escalations from outside the team.:** 
    - The Product Lead (me) owns and resolves all external escalations regarding roadmap features or custom ERP requests. I will respond to the external stakeholder within 48 hours, shielding the product squad and maintaining our 12-Month ERP Hard No.

## Show and swap your team charter
- **Where does the charter leave room for interpretation that could cause a conflict?:** The charter leaves room for conflict around what constitutes "enterprise maintenance/compliance" (the 20% allocation). Sales might try to repackage a custom SAP integration request as a "standard compliance data export" to slip it into PM 2's 20% engineering buffer. To resolve this, we must explicitly define that any work requiring custom code or bespoke database schema changes falls under "custom integration" and is a Hard No, while "compliance exports" must only leverage our existing, standard public APIs.
