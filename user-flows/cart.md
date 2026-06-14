# Cart (`/cart`)

Editable basket before anything becomes a quote.

## What the user sees

- Line items: image, name, part code, unit price, quantity, line total
- Remove action per line
- **Generate Quote** primary CTA at the bottom

Pricing on the page respects login state:

- B2B with catalog pricing → prices from the cart line (already contextualised)
- Everyone else → base variant prices fetched from Admin API for display

## Generate Quote flow

1. User clicks Generate Quote
2. Server reads Storefront cart, builds Admin API draft order line items
3. Attaches purchasing entity (B2B company contact or customer id when logged in)
4. Creates draft order, **clears the cart**
5. Redirect to `/quote/{draftOrderNumericId}`

Fails with 400 if cart is empty. Other errors surface as action response (not fully polished UI yet).

## Line item mutations

Standard Hydrogen cart actions hit this route’s `action`:

- Remove lines
- Update quantities

All go through `ensureCartPricing` so buyer context stays attached to the cart cookie.

## Who needs to be logged in?

Quote generation works without login in principle (customer id optional on draft order), but B2B pricing and company attribution need a session. Real-world expectation: distributors are logged in before quoting.

## Next step

→ [quote.md](./quote.md)
