# Model detail (`/models/:handle`)

Shows one refrigeration model and the parts that fit it.

## Hero section

- Back link to `/browse`
- Model image, name, category tag, short description
- **Compatibility PDF** button when the model has a document URL on the metaobject — opens/downloads the PDF, doesn’t navigate away

## Parts list (main content)

Same patterns as browse, but scoped to this model:

- Search within parts (`q`)
- Part category filter sidebar (only categories that actually have parts for this model)
- Sort + pagination
- Cards show part name, code, price, stock indicator

Click a card → `/parts/:partHandle`

## No parts state

If the model exists but has zero linked parts, the filters/grid are hidden and a “no parts found” message is shown. User can still read model info and download the compatibility PDF if present.

## Pricing

Logged-in B2B customers with a company location get **catalog prices** on part cards. Guests and non-B2B accounts see base/variant pricing from the product.

## Navigation context

Users often arrive here from browse or home model search. The part detail page links back here (“back to {model} parts”), so this page is the hub between model discovery and part selection.
