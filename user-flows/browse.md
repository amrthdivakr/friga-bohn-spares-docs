# Browse models (`/browse`)

Model catalogue. This is the “find a compressor/unit first” entry point.

## Layout

- Search input (models / model numbers)
- Filter sidebar — category tree from metaobjects
- Sort bar — New, A–Z, Z–A
- Grid of model cards (image, name, category breadcrumb)
- Pagination at the bottom (cursor-based, reflected in `page`, `cursor`, `direction` params)

## How filtering works

Everything is URL-driven. Changing search, sort, or category updates query params and re-runs the loader — no client-side fetch layer.

| Param | Purpose |
|-------|---------|
| `q` | Free-text search |
| `filter` | Category handle |
| `sort` | `new`, `alpha-asc`, `alpha-desc` |
| `page` | Display page number |
| `cursor` / `direction` | Cursor pagination |

Filters and sort reset pagination back to page 1.

## Card click

→ `/models/:handle` for that model’s compatible parts list.

## Who sees what

Same catalogue for everyone here — no login required, no B2B pricing on model cards (models aren’t products).

## Edge cases

- Empty search + no filter = full paginated list sorted by “new” (updated_at desc).
- Search queries bypass short cache (`CacheNone`) so results stay fresh.
- Categories without a parent show under “Uncategorised” in the sidebar.
