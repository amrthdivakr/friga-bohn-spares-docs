# Quote (`/quote/:number`)

Read-only view of a Shopify **draft order**. Created from cart via Generate Quote.

`:number` is the numeric id from the draft order GID (e.g. `gid://shopify/DraftOrder/12345` → `/quote/12345`).

## Two modes on one page

**Quote mode (default)**  
- Line items, totals, quote name as subtitle  
- Download PDF  
- Share link → `/quote/:number/share`  
- **Generate invoice** button (when allowed)

**Form mode**  
- Same line items, read-only  
- Order details form: PO number, company, contact, email, phone, shipping address  
- Confirm order → completes the draft order in Shopify  
- Cancel → back to quote mode without submitting

Mode toggle is client state only (`useState`); URL doesn’t change between quote and form.

## Generate invoice (confirm order)

On submit:

1. `draftOrderUpdate` — PO, contact, shipping address, payment terms (receipt template)
2. `draftOrderComplete` — converts draft to a real order (retries if Shopify says “not finished calculating”)
3. Redirect to `/invoice/{orderNumericId}`

Validation: email format, phone E.164 (`+33612345678` style).

Failures → `/cart/error` with message in session flash.

## Who can generate an invoice?

- Not logged in: allowed (guest checkout path)
- Logged in owner of the draft order: yes
- Distributor Location Admin / Distributor Admin: yes
- Someone else’s quote while logged in: button hidden

If draft is already `COMPLETED`, generate is disabled; link to existing invoice shown when `draftOrder.order` exists.

## Share / PDF

Route: `/quote/:number/share`

Fullscreen client-rendered PDF (`@react-pdf/renderer`), no chrome. Useful for email attachments or print. Same data as download on the main quote page.

Data loader is cached (`CacheLong`).

## Status lifecycle

```
Cart → draftOrderCreate → OPEN quote page
                      → form submit → draftOrderComplete → invoice page
```

See also [cart flow strategy](../cart%20flow%20strategy.md) for the Shopify mapping.
