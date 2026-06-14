# Account — Orders (`/account/orders`)

Main post-login hub for quotes and invoices. Heavy page — behaviour changes a lot by role.

## Tabs / views

URL param `view`:

- `all` — recent quote cards + recent invoice cards + two tables (default)
- `recent` — emphasises card sections
- `drafts` — quotes table focus
- `orders` — invoices table focus

(Web Admin never sees this page — redirected to Users.)

## Role: Distributor Location Admin

Scoped to **their company location** only.

- Recent cards: last 4 quotes + last 4 invoices for the location
- Tables paginate with separate cursor params for invoices (`iSort`, `iDir`, `iAfter`, `iBefore`, `iName`) and quotes (`qSort`, `qDir`, …)
- Name search filters on order name / draft number

## Role: Distributor Admin

Sees company-wide data with **location cards** at the top — each card links to `/account/locations/:locationId` for a location-scoped drill-down (same table layout as location admin but filtered by `location_id`).

Also gets the combined tables on the main orders page.

## Role: Standard customer / contact

Scoped to their own customer id — quotes and invoices they’re associated with.

## Document cards

Click a quote card → `/quote/:number`  
Click an invoice card → `/invoice/:number`

## “View all” links

- `/account/orders/quotes` — paginated quote list only
- `/account/orders/invoices` — paginated invoice list only

Same role scoping rules apply on those sub-pages.

## Location drill-down (`/account/locations/:location`)

Distributor Admin only. Shows location name + invoice/quote tables for that location id. Forbidden for other roles.

## Tables

Sortable columns, pagination, name filter. Rows link out to quote or invoice pages.

## TBD

- Unified search across quotes + invoices?
- Export CSV for admins
