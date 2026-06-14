# Part detail (`/parts/:handle`)

Product page for a single spare part.

## Header / buy box

- Back link → parent model’s parts list (`/models/:modelHandle`)
- Image (placeholder icon if missing)
- Title, part code, category tag
- Price in EUR
- Quantity selector (1–10)
- **Add to cart** — posts to `/cart` via Hydrogen `CartForm`
- If already in cart: **Remove from cart** instead; quantity changes auto-update the cart line via fetcher

Add is disabled when out of stock or variant unavailable.

## Below the fold

- HTML description when present
- Compatible models block + link to compatibility PDF (from the model series metaobject)
- “Other parts for {model}” grid — same-model siblings, quick way to keep shopping without going back

## Cart behaviour

- Line item carries a `_code` attribute with the part code (used on cart display)
- Cart pricing context is ensured on load (`ensureCartPricing`) so B2B catalog prices apply before add

## 404

Part must be tied to a model series. Orphan products without that relationship return 404.

## Typical flow

```
browse → model → part → add to cart → cart → generate quote
```

Or from parts index if they searched by part number directly.
