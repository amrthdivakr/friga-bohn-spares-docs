# Cart error (`/cart/error`)

Dead-end recovery page when quote → invoice conversion blows up.

## When you land here

- `draftOrderUpdate` user errors
- `draftOrderComplete` failures after retries
- Other checkout-ish failures that stash a message in session (`cartError`)

Loader reads the flash message once, clears it from session, and renders. If there’s no message, redirects to `/account/orders`.

## What the user sees

- Warning icon + “Something went wrong”
- The actual error message from Shopify (or our fallback string)
- Extra hint when message contains “not finished calculating” — tells them to check invoices in account (order may have completed despite the error)
- Link back to **Orders**

## Not a general error boundary

Only cart/quote/invoice pipeline errors use this route. Random 404s and loader throws go elsewhere.
