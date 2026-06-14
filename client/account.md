# Account

## Sign in

- Click account icon
- Complete login on Friga Bohn screen
- Returned to the site when done

## Sign out

- In account area, click **Sign Out** (top right)

## Account navigation

From the buttons under your name (depends on role):

- **Orders** — quotes and invoices (most users)
- **Users** — manage team (admins)
- **Profile** — name
- **Addresses** — delivery addresses
- **Company** — distributor admin only

Web Admin users land on **Users** instead of Orders.

---

## Orders (`/account/orders`)

### Switch view

- Tabs: All / Recent / Drafts / Orders

### Open a recent quote

- Click a card under Recent quotes

### Open a recent invoice

- Click a card under Recent invoices

### See all quotes

- **View all** under Recent quotes → full quote list

### See all invoices

- **View all** under Recent invoices → full invoice list

### Find a quote in the table

- Sort by column header
- Use search if shown
- Change page at bottom
- Click a row → quote page

### Find an invoice in the table

- Sort by column header
- Search by order number (e.g. `#1042`)
- Change page
- Click a row → invoice page

### Location orders (distributor admin)

- Open a location (when shown) → `/account/locations/...`
- Same table actions, scoped to that location

---

## All quotes (`/account/orders/quotes`)

### Back to orders hub

- Click **Orders** link at top

### Open a quote

- Click a card

### Change page

- Pagination

---

## All invoices (`/account/orders/invoices`)

### Back to orders hub

- Click **Orders** link at top

### Open an invoice

- Click a card

### Change page

- Pagination

---

## Location orders (`/account/locations/...`)

Distributor admin only.

### View quotes for location

- Quotes table — sort, search, paginate, click row

### View invoices for location

- Invoices table — sort, search by `#`, paginate, click row

---

## Profile (`/account/profile`)

### Update name

- Edit first / last name
- Save

---

## Addresses (`/account/addresses`)

### Add an address

- Fill in the **Create** form at the top
- Tick **Set as default** if needed
- Click **Create**

### Edit an address

- Change fields on the address card
- Click **Save**

### Delete an address

- Click **Delete** on the card

### Set default on save

- Tick **Set as default address** before Save or Create

---

## Users (`/account/users`)

Admins only (Web Admin, Distributor Admin, Location Admin).

### Add a user

- Click **Add user**
- Enter name, email, role
- Pick company / location if required for role
- Submit

### Edit a user

- Click edit on a row
- Change fields in the modal
- Save

### Sort / browse users

- Click column headers
- Use pagination

### Close modal without saving

- Click X or outside modal

---

## Company (`/account/company`)

Distributor admin only.

### View company details

- Company name, locations list, catalog list (read-only)

### Restrict catalog prices

- Toggle **Restrict catalog prices**
- Confirm in the dialog
- Affects what prices users at your company see

### Cancel price toggle

- Click **Cancel** in the confirmation dialog
