# Account — Addresses (`/account/addresses`)

CRUD for customer shipping addresses (Customer Account API).

## List view

Each saved address shown as a card with edit/delete. One can be marked default.

## Create

“Add address” opens inline form — company, name lines, street, city, territory, zip, country, phone, default checkbox.

## Update / delete

Per-address forms post with `addressId`. Delete and set-default are separate intents in the same action handler.

Country dropdown uses shared `COUNTRY_OPTIONS` list.

## Errors

Keyed by address id in action response — inline on the relevant card.

## Relation to quote flow

Quote → invoice form collects shipping address on the draft order. Saved addresses here don’t auto-populate that form yet (quote form uses customer profile mapping via `mapCustomerToFormData` — mostly name/email/company from B2B contact, not address book).

Something to wire up later if users expect it.
