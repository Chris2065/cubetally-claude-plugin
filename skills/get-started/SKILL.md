---
name: get-started
description: Use when someone first connects CubeTally or asks what CubeTally can do. Gives a short business summary and suggests next questions.
---

Help the user get a first useful answer from CubeTally.

1. If the CubeTally tools are not available, tell the user to connect CubeTally from the connector settings and sign in with their CubeTally account. They pick one company and decide whether to allow changes.
2. Call get_business_summary for this month. Give a short plain summary: money invoiced and collected, overdue balance, jobs completed and scheduled, and new leads. If that tool is refused, the user's CubeTally role does not include reports; call low_stock_report instead.
3. Offer three next questions, for example what is low on stock, which invoices are overdue, or which jobs are unassigned.

Keep answers short. Never invent numbers; only report what the tools return.
