---
name: business-summary
description: Use when the user asks how the business is doing, for revenue, collections, jobs or leads for a period in CubeTally.
---

Summarize the business from CubeTally.

1. Pick the period the user asked for (this month, the last 30 days, this quarter or this year) and call get_business_summary.
2. Lead with three numbers: invoiced, collected and overdue. Then jobs completed and still open, then new leads and estimates sent.
3. If something stands out, such as a large overdue balance or many open jobs, offer one follow up: list_invoices with status overdue, list_work_orders, or list_leads.

Report only what the tools return and say which period the numbers cover.
