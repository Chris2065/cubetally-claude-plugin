---
name: stock-count
description: Use when the user reports a physical count, found or damaged stock, or wants to correct a quantity or add a new product in CubeTally.
---

Record stock changes in CubeTally only after the user confirms.

1. Find the product with search_products. If more than one matches, ask which one. If none match and the user wants it added, collect a name, SKU and unit, and use create_product after confirming.
2. Call get_inventory_levels to show the current quantity at each location.
3. State the exact change: product, location, old quantity, new quantity and the reason. Wait for a clear yes.
4. Call adjust_stock with the reason. Report the old and new quantity from the result.

If the change tools are not offered, explain that changes were not allowed when CubeTally was connected and that the user can reconnect with changes allowed.
