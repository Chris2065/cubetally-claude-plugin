---
name: collect-overdue
description: Use when the user asks which invoices are overdue, who owes money, or wants help following up on unpaid invoices in CubeTally.
---

Help the user collect overdue invoices.

1. Call list_invoices with status overdue. Sort by balance, largest first, and show customer, invoice number, balance and days past due.
2. If the user wants contact details, call list_customers for those customers.
3. If asked, draft a short, polite reminder for each customer in the chat. CubeTally does not send messages or take payments through this plugin, so tell the user to send the reminder or the payment link from CubeTally.
