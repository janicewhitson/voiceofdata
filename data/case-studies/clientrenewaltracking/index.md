---

---

# Customer Renewal Tracker
> **Role:** Senior Software Licensing Specialist (later part of Client Operations Specialists)
> 
> **Tools:** Excel

## The Problem
A mid-sized client with roughly 500 Adobe subscriptions across multiple divisions consistently submitted renewal POs that didn't match their actual entitlements. Orders were split across POs by division even though the publisher treated them as a single agreement, making it easy for quantities to drift. When a renewal order exceeds entitlement, the publisher rejects it — triggering revised POs from the client, revised invoices from us, and a real risk of missing the renewal window entirely. A lapsed renewal means employees lose access to the tools they need to work. The cost touches all three parties: the client's procurement team, the publisher's order processing, and our own account management.
## The Solution
Without being asked, I built a year-over-year renewal tracker in Excel to bring all of that into one place. Each renewal year captures the client's current entitlement per product (pulled from the licensing portal), what was actually ordered across every PO and division, and the variance between the two. The assigned vs. unassigned split on each license provided a utilization picture alongside the compliance one. As the tracker matured, I added year-over-year growth metrics and, later, the publisher's share of total orders for that client — both by volume and by revenue.
Before each renewal submission, I sent the Account Executive a summary. Once the metrics were in place, I highlighted them specifically. She had no prior visibility into how significant this publisher's volume was for that client.
## The Result
The tracker caught every over-ordering attempt before submission, eliminating rejected orders and the downstream rework for all three parties. It also gave the AE concrete data on a client relationship she had been managing without full context — while modest in the context of the publisher's overall volume, this client represented a significant portion of the Account Executive's own book of business — context she hadn't had visibility into before..
## The Rebuild
This portfolio version was reconstructed from memory using anonymized dummy data. The structure, formulas, and logic reflect the original file. The Excel version uses structured tables, dynamic cross-sheet COUNTIFS and FILTER formulas, and a tab-name extraction approach to keep each year's calculations self-contained. 

## Screenshots
Renewal Summary

![2024 Renewal Summary]({{ '/data/case-studies/clientrenewaltracking/CLT-2024-Summary.png' | relative_url }})

Multiple orders by division

![2024 Orders]({{ '/data/case-studies/clientrenewaltracking/CLT-2024-Orders.png' | relative_url }})

Formula for Assigned/Open

![Assigned/Open Formula]({{ '/data/case-studies/clientrenewaltracking/CLT-Formula.png' | relative_url }})
