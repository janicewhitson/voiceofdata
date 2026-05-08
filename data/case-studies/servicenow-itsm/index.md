# ServiceNow Overview — Managed Services ITSM Reporting

> Power BI  ·  Client-facing  ·  Q3 2024

<div class="project-tools case-study-tools" aria-label="Tools used">
  <span class="expertise-tag project-tool-pill">Power BI</span>
  <span class="expertise-tag project-tool-pill">DAX</span>
  <span class="expertise-tag project-tool-pill">Bookmarks</span>
  <span class="expertise-tag project-tool-pill">Dynamic titles</span>
  <span class="expertise-tag project-tool-pill">ITSM</span>
  <span class="expertise-tag project-tool-pill">ServiceNow</span>
</div>


## Situation

An enterprise insurance client receiving managed IT services had an existing Power BI report built on ServiceNow data — incidents, problems, and change requests. When the report's original developer left, ownership transferred to me. On review, it was apparent the report had drifted from what the managed services team actually needed: it was visually dense, and only a fraction of what it contained was regularly referenced in client meetings.

## Obstacle

There was no formal requirements document to work from. The internal managed services lead needed something presentable to the client quickly, and I was carrying a full project load at the time. The original report's custom visual — decorative but not functional — was a performance liability. There was also no formalised SLA agreement with this client, which ruled out the standard SLA tracking most ITSM reports default to.

## Action

Rather than patching the existing report, I rebuilt it around what actually got discussed in meetings. I replaced the custom visual with native Power BI components, which resolved the load time issue immediately. Without formal SLAs to track, I used Time to Resolve and Reassignment Count as proxies — both meaningful signals for a managed services team monitoring service quality.

The report was structured across four pages: an incident matrix, an incident charts view (built separately after stakeholders disagreed on whether they wanted tables or visuals), a problems page, and a change requests page. A bookmark-based toggle allowed switching between monthly and quarterly views — functionality that would now be handled more cleanly via parameters.

Dynamic titles were built using DAX so page headers automatically reflected the current quarter and year based on the data — a small detail that reduced manual maintenance and kept the report feeling current.

A v1 was ready within three to four days for the internal lead to present to the client. Feedback from that session was minor — a couple of layout adjustments — with no structural changes required.

## Result

The reworked report was approved with minimal revision after a single client-facing review. The problems page captured real-world impact clearly — the July 2024 CrowdStrike outage produced a spike of over 600 enterprise infrastructure incidents in a single month, visible immediately in the data without any additional annotation. The report went on to serve as the ongoing delivery for that client's managed services engagement.

## Key decisions

Time to Resolve over SLA tracking. With no formalised SLA in place, standard SLA compliance metrics would have been misleading. Resolve time and reassignment counts gave the managed services team actionable signals without implying contractual benchmarks that didn't exist.

Two incident pages instead of one. When the internal team and client stakeholders had different preferences for how to consume the data, the pragmatic solution was to build both — a matrix view and a charts view — rather than pick a winner.

Native visuals only. The original report's custom visual was removed entirely. Native Power BI visuals loaded faster, rendered more reliably, and were sufficient for everything the report needed to communicate.

## Screenshots
Incident Overview

![ServiceNow ITSM Incident Overview]({{ '/data/case-studies/servicenow-itsm/SN-ITSM-IncidentOverview.png' | relative_url }})

Incident Charts

![ServiceNow ITSM Incident Charts]({{ '/data/case-studies/servicenow-itsm/SN-ITSM-IncidentCharts.png' | relative_url }})

Problems

![ServiceNow ITSM Problems]({{ '/data/case-studies/servicenow-itsm/SN-ITSM-Problems.png' | relative_url }})

Change Requests

![ServiceNow ITSM Change Requests]({{ '/data/case-studies/servicenow-itsm/SN-ITSM-Change.png' | relative_url }})
