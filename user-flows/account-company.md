# Account — Company (`/account/company`)

Distributor Admin only. Company-level B2B settings.

## Loader shows

- Company name
- List of company locations (name + id)
- Catalogs tied to locations (title, price list name, fixed price count)
- **Restrict catalog prices** toggle — reads company metafield, controls whether contacts see negotiated catalog pricing vs base prices

## Actions

Toggle restrict catalog prices:

- Updates company metafield via Admin API
- Invalidates customer session cache so pricing context refreshes on next request

Forbidden if not Distributor Admin or missing company context.

## Why it matters on the storefront

When restrict is on, `getCatalogPricingContext` / cart pricing logic treats the company differently — affects part cards, cart totals, and draft order line prices.

Distributor Admin is the person who understands this toggle; location admins and buyers just see the outcome.

## Not on this page

- Creating locations (Shopify admin / separate process)
- Assigning catalogs to locations
- Per-user role edits → [account-users.md](./account-users.md)
