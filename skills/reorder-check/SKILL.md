---
name: reorder-check
description: Use when the user asks what is low on stock, what to reorder, or wants a purchase order for low items in CubeTally.
---

Build a reorder list from CubeTally.

1. Call low_stock_report. List each item with quantity on hand, minimum level, shortfall and the suggested reorder quantity, most urgent first.
2. If the user names a product, use search_products and get_inventory_levels to show stock by location.
3. Only if the user asks for a purchase order: group the items by supplier, say exactly which lines and quantities will go on the draft, and wait for a clear yes. Then call create_purchase_order_draft once per supplier. Tell the user the draft is not sent to the supplier and can be reviewed in CubeTally.

Never order more than the user approved. If the change tools are not offered, explain that changes were not allowed when CubeTally was connected.
