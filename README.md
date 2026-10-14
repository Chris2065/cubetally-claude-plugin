# CubeTally for Claude

CubeTally is inventory, field service and accounting software for small and midsize businesses. This plugin connects Claude to your own CubeTally company so you can ask about it in plain words and get answers from live data.

## What you can do

- See what is low on stock and how much to reorder, then turn it into a draft purchase order
- Look up products by name, SKU or barcode and check stock by location
- Review customers, invoices, work orders, estimates, purchase orders and sales leads
- Get a business summary: invoiced, collected, overdue, jobs completed and open, new leads
- Record a stock count or adjustment with a reason, and add a new product

Changes only happen after you confirm them in the chat, and only if you allowed changes when you connected CubeTally. Purchase orders are always created as drafts and are never sent to a supplier. Every change is logged in CubeTally with your name.

## What is included

- **CubeTally connector**: the remote server at `https://cubetally.com/mcp`, declared in `.mcp.json`. It has 13 tools: `search_products`, `get_inventory_levels`, `low_stock_report`, `list_customers`, `list_invoices`, `list_work_orders`, `list_estimates`, `list_purchase_orders`, `list_leads`, `get_business_summary`, `adjust_stock`, `create_product` and `create_purchase_order_draft`.
- **Skills**: `get-started`, `reorder-check`, `business-summary`, `collect-overdue` and `stock-count`. They are plain instructions in `skills/` that tell Claude which CubeTally tools to call and to confirm before any change.

The plugin runs no local code, has no hooks and installs no packages.

## Setup

1. Install the plugin.
2. When Claude asks you to connect CubeTally, sign in with your CubeTally account, pick one company and choose whether to allow changes.
3. Ask something like "What is low on stock right now?"

You need a CubeTally account on a paid plan. Start a free trial at https://cubetally.com.

To disconnect, remove the connection in Claude, or in CubeTally under Settings, Integrations, Connected assistants.

## Data and privacy

The plugin sends requests only to `https://cubetally.com`, the CubeTally service the user signs in to. CubeTally returns only what your CubeTally role allows, for the one company you picked. Sign in uses OAuth; your CubeTally password is never shared with Claude. Tool calls count against your plan's monthly API allowance.

- Privacy policy: https://cubetally.com/privacy
- Terms: https://cubetally.com/terms
- Documentation: https://cubetally.com/developers/docs#automation-connections
- Support: https://cubetally.com/contact or info@cubetally.com

## License

MIT, see `LICENSE`.
