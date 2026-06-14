# Account — Users (`/account/users`)

B2B user management. **Not** a general “my account” page — admin tooling.

## Who can access

| Role | Access |
|------|--------|
| Web Admin | Full list across companies |
| Distributor Admin | Users in their company |
| Distributor Location Admin | Users at their location |
| Everyone else | 403 |

Web Admin default landing after login.

## Main UI

- Sortable, paginated users table (`uSort`, `uDir`, `uAfter`, `uBefore`)
- **Add user** opens modal form
- Row actions: edit, (de)activate depending on permissions

## Add / edit user modal

Collects name, email, role, company location assignment. Roles available in the dropdown depend on who’s logged in (`assignableRoles`).

Creates or updates:

- Shopify Customer (Customer Account API / Admin depending on path)
- Company contact linkage for B2B
- Role metafield

## Permissions model (simplified)

- `canManageUsers` — create/edit/deactivate
- `canSeeAllUsers` — Web Admin sees cross-tenant
- Distributor roles only manage users at or below their level

Exact rules live in `~/lib/roles.ts` — this doc is the user-facing summary.

## Failure modes

- 403 if role not allowed
- Action errors returned to modal (duplicate email, invalid role, etc.)

## TBD

- Invite email copy / onboarding link
- Audit log of who changed what
