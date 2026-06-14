# Login (`/account/login`)

Not a visible page — loader immediately redirects into Shopify Customer Account OAuth.

## Flow

1. User clicks account icon (or hits a protected `/account/*` route while logged out)
2. Browser goes to `/account/login` (no locale segment on this route)
3. Loader detects locale from `return_to` param or `Referer` (so `/fr/...` paths get French login UI)
4. `customerAccount.login()` redirect to Shopify hosted auth
5. After success → `account/authorize` callback → back to storefront

Optional query params forwarded to Shopify: `acr_values`, `login_hint`, `login_hint_mode`, `locale`.

## Logout

POST to `/account/logout` from account shell (sign out button in legacy menu markup — hero uses nav links instead).

## Notes

- Because this route sits outside `($locale)`, storefront i18n in context is always EN; locale detection is custom (see loader).
- No “create account” on storefront — provisioning is assumed to happen elsewhere (admin / invite).
