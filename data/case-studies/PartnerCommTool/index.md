---

---

# Partner Commission Modeling Tool — SOAR Case Study

> **Working title:** Partner Commission Modeling Tool — Concept & Mockup
>
> **Role:** Independent — built as a favor for a friend
>
> **Timeline:** ~1–2 hours, single session

---

## Situation

A friend working at an early-stage ISV was developing an internal proposal for a formal partner program—something the company had never had. The concept was a tiered commission structure to incentivize external partners to sell company products, with commission rates and partner status tied to sales volume and commitment term.

The proposal was strong conceptually, but it was still narrative-only. Without a working model to demonstrate expected earnings and tier outcomes, it was hard to make the business case tangible for leadership.

## Obstacle

* **No baseline program:** There was no existing partner program, no commission history, and no established tier framework.
* **Abstract proposal risk:** Written descriptions of tier mechanics were easy to dismiss without an interactive model.
* **Dual-use requirement:** The tool needed to support both prospective partners (join decision) and existing partners (expand decision), which required separate scenario logic.

## Action

During a conversation about the proposal, I offered to build a working Excel mockup. Based on prior experience with tiered pricing and reseller program design, I could define layout and logic quickly, and completed the first usable version in a single focused 1–2 hour session.

I built the workbook with two tabs backed by one shared structured data table (`TblTiers`) containing tier floors, tier names, and commission rates.

The model included:

* A **New Partner** tab that accepted quantity and term (monthly vs annual), then determined tier using approximate-match `XLOOKUP` against tier floors and returned estimated commission.
* A **minimum-threshold guardrail** that returned “Minimum not met” when input volume fell below the first tier.
* An **Existing Partner** tab that calculated both current tier and projected tier based on expanded commitment, enabling side-by-side status/earnings comparison.
* Shared tier/rate logic in `TblTiers` so program parameter updates could be made centrally without rewriting formulas.
* `IFERROR` handling to keep outputs clear when users entered incomplete or edge-case inputs.

## Result

* **Presentation utility:** The tool was used as a live demonstration in the internal leadership presentation.
* **Decision clarity:** Leadership could see how tiers and payouts changed with inputs in real time, making the proposal far easier to evaluate.
* **Outcome:** The company eventually chose not to launch the partner program, and the mockup did not advance to production.
* **Transferable value:** Even as a concept artifact, it demonstrated a practical partner-program structure common in ISV/reseller channels.

## Reflection / Lessons Learned

* Deep **domain knowledge** accelerates design decisions, even under tight time constraints.
* Interactive models often communicate strategy more effectively than narrative-only proposals.
* Building for **actual user questions** (for example, “current vs projected tier”) creates higher practical value than solving only the obvious first scenario.

---

## Tech Summary (for quick scanning)

* **Data:** Dummy/proposed values only (no proprietary production data)
* **Tools:** Excel
* **Modeling:** Structured tables, named ranges, approximate-match `XLOOKUP`, `IFERROR`
* **Design:** Two-tab scenario model, centralized tier logic table, rapid single-session build

## Artifacts (Optional)

No visuals are included currently. A sanitized demo workbook or wireframe screenshot may be added later.

## Anonymization Notes

All identifying product/company references have been generalized. No real partner, customer, or financial data is included.
