Working title: Partner Commission Modeling Tool — Concept & Mockup
Role: Independent — built as a favour for a friend
Timeline: ~1-2 hours, single session


Situation
A friend working at an early-stage ISV was developing an internal proposal for a formal partner program — something the company had never had. The idea was to create a tiered commission structure that would incentivize external partners to sell the company's products, with commission rates and partner status tied to sales volume and commitment term.
The proposal was solid conceptually, but it was just words on a page. Without something tangible to demonstrate how the program would actually work — what a partner would earn, what tier they'd qualify for — it was difficult to make the business case feel real to leadership.
Obstacle

No existing program to reference: The company had no partner program, no commission history, and no established tier structure. Everything had to be modeled from scratch using proposed values.
Abstract without a visual: A written proposal describing commission tiers is easy to dismiss. Leadership needed to see the numbers move in response to real inputs to understand the program's potential.
Two distinct partner scenarios: The tool needed to serve both prospective new partners evaluating whether to join, and existing partners considering whether to expand their commitment — two different questions requiring different logic.

Action
During a conversation about the proposal, I offered to build a working mockup of the commission calculator. The layout and structure were clear in my head from prior experience with tiered pricing models, so the build took roughly one to two hours as a single focused session.
The tool was built in Excel with two tabs — one for new/prospective partners, one for existing partners — each driven by a shared structured data table (TblTiers) containing the tier thresholds, tier names, and commission rates.
New Partner tab: Takes quantity and commitment term (monthly or annual) as inputs, determines the applicable tier using an XLOOKUP with approximate match against the tier floor values, and returns the estimated commission value. If the quantity doesn't meet the minimum threshold for the first tier, the tool returns "Minimum not met" rather than a misleading result.
Existing Partner tab: Adds a second layer of analysis — it calculates both the partner's current tier based on existing sales and their projected tier based on the proposed new commitment. This gap analysis lets a partner rep walk into a conversation knowing exactly what a deal would do to their status and their earnings in a single view.
Both tabs use IFERROR to handle edge cases gracefully, and all rate and tier logic lives in the named structured table — meaning the program parameters could be updated in one place without touching any formulas.
Result

The tool was used as a live demonstration during my friend's internal presentation to leadership.
It gave the proposal immediate credibility — leadership could see exactly how the program would work in practice, not just in theory.
The company ultimately decided not to move forward with a partner program, and my friend left the organization shortly after.
The tool remained a mockup, but demonstrated the kind of partner program structure common across the software reseller and ISV space.

Reflection / Lessons Learned

Domain knowledge is a blueprint. Sixteen years in the reseller space means you internalize how these programs work — the tier logic, the incentive structures, the questions a partner rep actually needs answered. That domain knowledge meant the structure was clear before I opened Excel, even without having built one before.
Visual tools make abstract ideas concrete. A well-built model can do more for a proposal than a page of narrative. Showing leadership a number change in real time is more persuasive than describing how it would work.
Design for the real questions, not the obvious one. The new partner tab was the obvious ask. The existing partner tab — showing current vs. projected tier side by side — came from thinking about who would actually use the tool and what they'd need to know in a real partner conversation.

Tech Summary

Data: Dummy/proposed values — no proprietary or sensitive data
Tools: Excel
Modeling: Structured tables, named ranges, XLOOKUP with approximate match (-1), IFERROR handling
Design: Two-tab scenario structure, shared tier logic table, single-session build

Anonymization Notes
Product names have been replaced with generic placeholders. No real company, vendor, or partner data is included.
