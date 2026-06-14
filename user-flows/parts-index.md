# Parts catalogue (`/parts`)

Global parts search — when you have a part number and don’t care which model it belongs to (yet).

## Difference from model detail

| | `/parts` | `/models/:handle` |
|---|----------|-------------------|
| Scope | All parts | Parts for one model |
| Entry | Home (parts search), header “Parts” | Model card |
| Filters | Part categories (global) | Part categories for that model |

Otherwise the UX is intentionally similar: search, filters, sort, grid, pagination.

## Card contents

- Title (FR name when locale is French)
- Part code
- Thumbnail
- Price (catalog-aware for B2B)
- In-stock badge

Click → `/parts/:handle`

## URL params

Same idea as browse: `q`, `filter`, `sort`, `page`, `cursor`, `direction`.

## TBD

- Cross-link from a part card to “see all models this fits” isn’t on the index — that’s on the part detail page.
