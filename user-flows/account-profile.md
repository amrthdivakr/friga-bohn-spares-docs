# Account — Profile (`/account/profile`)

Minimal profile edit.

## Fields

- First name
- Last name

Submit via `PUT` form → Customer Account API `customerUpdate` mutation.

## Feedback

Action returns error message or updated customer fragment. No password change on this form (would need separate Shopify flows).

## Who uses it

Any logged-in customer. B2B users might rarely touch this if names are managed centrally — still useful for typos.
