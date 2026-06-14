# Account shell (`/account/*`)

Layout wrapper for everything under account. Requires login — loader calls `handleAuthStatus()` and loads customer from session.

## Hero block

Shows:

- Name, role label, email
- Company name + location (from first company contact, when B2B)

## Nav buttons (role-dependent)

| Link | Who sees it |
|------|-------------|
| Orders | Everyone except Web Admin |
| Users | Web Admin, Distributor Admin, Distributor Location Admin |
| Profile | Everyone |
| Addresses | Everyone |
| Company | Distributor Admin only |

Web Admin lands on `/account/users` by default (`account._index` redirect). Everyone else → `/account/orders`.

## `/account` index

Just a redirect — no standalone dashboard page.

## Child routes

Content renders in `<Outlet />` below the hero. Shared customer object passed via outlet context on some pages.

## Cache

Account layout sets `Cache-Control: no-cache` — always fresh customer info.
