# Home (`/`)

Landing page. One job: get the user to the right catalogue fast.

## What’s on the page

- Hero with a search bar
- Dropdown to search **Models** or **Parts** (defaults to models)
- **Browse** button → `/browse` with no query
- **Search** button → runs the same navigation as submitting the search field

## Typical paths

**Know the model number**
1. Leave search type on Models
2. Type model name / number, hit Search
3. Lands on `/browse?q=…` with results pre-filtered

**Know the part number**
1. Switch dropdown to Parts
2. Search → `/parts?q=…`

**Just browsing**
- Browse button, or header nav “Models” / “Parts”

## Notes

- Search state lives only in the URL on the destination page — refreshing home clears the input (by design, it’s not synced back from `?q=`).
- French locale uses `/fr` prefix on all outbound links; home itself is `/fr` when language is FR.

## Open questions

- Should home remember last search type (models vs parts) in local storage? Not implemented.
