# User flows — rough notes

Scratch docs for how people move through the spares storefront. Written from the current implementation, not the ideal end state — expect gaps and things marked TBD.

Locale prefix `/fr` applies to French; paths below omit it for brevity.

## Catalogue

| Page | Route | Doc |
|------|-------|-----|
| Home | `/` | [home.md](./home.md) |
| Browse models | `/browse` | [browse.md](./browse.md) |
| Model detail | `/models/:handle` | [model-detail.md](./model-detail.md) |
| Parts catalogue | `/parts` | [parts-index.md](./parts-index.md) |
| Part detail | `/parts/:handle` | [part-detail.md](./part-detail.md) |

## Cart & documents

| Page | Route | Doc |
|------|-------|-----|
| Cart | `/cart` | [cart.md](./cart.md) |
| Quote | `/quote/:number` | [quote.md](./quote.md) |
| Quote PDF | `/quote/:number/share` | [quote.md](./quote.md#share--pdf) |
| Invoice | `/invoice/:number` | [invoice.md](./invoice.md) |
| Invoice PDF | `/invoice/:number/share` | [invoice.md](./invoice.md#share--pdf) |
| Cart error | `/cart/error` | [cart-error.md](./cart-error.md) |

## Account

| Page | Route | Doc |
|------|-------|-----|
| Login | `/account/login` | [login.md](./login.md) |
| Account shell | `/account/*` | [account-overview.md](./account-overview.md) |
| Orders hub | `/account/orders` | [account-orders.md](./account-orders.md) |
| Profile | `/account/profile` | [account-profile.md](./account-profile.md) |
| Addresses | `/account/addresses` | [account-addresses.md](./account-addresses.md) |
| Users (admin) | `/account/users` | [account-users.md](./account-users.md) |
| Company settings | `/account/company` | [account-company.md](./account-company.md) |

Related technical write-up: [cart flow strategy](../cart%20flow%20strategy.md)
