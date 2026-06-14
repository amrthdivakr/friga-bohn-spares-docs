# Invoice (`/invoice/:number`)

View for a completed Shopify **order** (post–draft-order-complete).

`:number` is the order numeric id.

## Page content

Uses the same `CartSection` shell as quote/cart but `mode="invoice"`:

- Read-only line items and totals
- Order details form pre-filled from order data (display / PDF, not editable for re-submit on this page)
- Download invoice PDF
- Share → `/invoice/:number/share`

Subtitle shows Shopify order name (e.g. `#1042`).

## How users get here

1. Quote page → fill form → confirm (primary path)
2. Account → orders → open invoice card / table row
3. Direct link if they saved the URL

## Share / PDF

Route: `/invoice/:number/share`

Same pattern as quote share: lazy-loaded fullscreen PDF, long cache on order fetch.

## vs Quote page

| | Quote | Invoice |
|---|-------|---------|
| Shopify object | Draft order | Order |
| Editable cart | No | No |
| Can convert further | Yes → invoice | No (already ordered) |
| PO / address capture | On quote form | Already on order |

## Access control

Loader fetches order by id from Admin API. No per-customer auth check on the page itself yet — anyone with the numeric id could load it. **Worth revisiting** for production (tokenised links or session check).
