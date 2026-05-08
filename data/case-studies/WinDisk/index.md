---

---

# Windows Disk Utilisation Report Automation

<div class="project-tools case-study-tools" aria-label="Tools used">
  <span class="expertise-tag project-tool-pill">Excel</span>
  <span class="expertise-tag project-tool-pill">Power Query</span>
</div>


---

## The Problem

A Service Delivery Manager team was receiving raw system export data monthly and manually identifying high-utilisation disks across their client base — a process their team lead described as taking a "ridiculous number of hours" each month.

## The Solution
The ask came informally: the team lead's manager had heard I was good with Excel and suggested he reach out. A few hours of trial and error later, the team had a self-service tool. Paste the raw export into the data tab, enter the number of results you want on the Report tab, and the formatted client-ready report generates automatically — plain-English sentences listing each at-risk disk by server, disk ID, utilization percentage, and remaining capacity.

## The Result
The tool was rolled out to a team of five and required no ongoing support or rework.

## The Rebuild
Revisiting it in 2026 for this portfolio, I rebuilt the backend significantly — the Power Query transformation was always part of the tool, but the original version still relied on a brittle chain of helper columns and ROW()-dependent lookups in Excel to navigate the data. The rewrite pushed that logic into PQ instead, outputting one clean row per disk, pre-sorted by utilisation. The report tab now pulls directly from that output with a single formula. Fewer moving parts, easier to maintain, same output.

---

## Tech Summary

Data: Sanitised client export data (server names retained, client identity removed)

Tools: Excel · Power Query (M)

Transformation: Unpivot, metric-based grouping, pivot and null consolidation to restructure positional raw data into a clean one-row-per-disk output

Design: Single data entry tab, user-controlled output count, auto-generated client-ready report, built for non-technical users

## Screenshots

Raw Data

![Raw Data]({{ 'data/case-studies/WinDisk/WinDiskRaw.png' | relative_url }})

Final Report

![Report]({{ 'data/case-studies/WinDisk/WinDiskReport.png' | relative_url }})

Some of the PowerQuery Code

![Code]({{ 'data/case-studies/WinDisk/WinDiskPQ.png' | relative_url }})


<a class="resume-button" href="{{ 'data/case-studies/' | relative_url }}" aria-label="Back to Projects">
  <span>Back to Projects</span>
</a>
