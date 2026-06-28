# Account

This page provides a comprehensive guide to the account section of the website. It includes instructions for signing in, signing out, account navigation, and accessing orders, invoices, and profile.

> ↑ [Go back to Website Documentation](./README.md)

## Sign in

Sign in to your account to access your orders, invoices, and profile.

- Click account icon
- Complete login on Friga Bohn screen
- Returned to the site when done

## Sign out

- In account area, click **Sign Out** (top right)

## Account navigation

Navigate to your account to access your orders, invoices, and profile. 

From the buttons under your name (depends on role):

- **Orders** — quotes and invoices (most users)
- **Users** — manage users (admins)
- **Profile** — update name
- **Addresses** — add and edit delivery addresses and set as default
- **Company** — company, catalog and location details, add locations and set price visibility restrictions (distributor admin only)

---

## Orders (`/account/orders`)

Navigate to your orders to view quotes and invoices. Tables to manage draft orders and orders.

> ↗ [How to View and Access Customer Order Invoices](./account/orders-page.md)

### Switch view

- Tabs: All / Recent / Drafts / Orders

### View locations (distributor admin only)

- Click a location card
- View drafts and orders for that location

### View a recent quote document

- View a card under Recent quotes
- Click Open button to open the quote
- Click Download button to download the quote
- Click Copy icon to copy the quote number to clipboard

### Open a recent invoice document

- View a card under Recent invoices
- Click Open button to open the invoice
- Click Download button to download the invoice
- Click Copy icon to copy the invoice number to clipboard

### See all quotes documents

- **View all** under Recent quotes → full quote list

### See all invoices documents

- **View all** under Recent invoices → full invoice list

### Find a draft order in the table

- Sort by column header
- Columns supporting sorting will have a sort icon
- Search by order number (e.g. `#D1042`)
- Change page at bottom
- Click a row → draft order page

### Find an order in the table

- Sort by column header
- Columns supporting sorting will have a sort icon
- Search by order number (e.g. `#1042`)
- Change page at bottom
- Click a row → order page

---

## All quotes (`/account/orders/quotes`)

Navigate to all quotes to view all quotes documents.

### Back to orders hub

- Click **Orders** link at top

### Open a quote

- Click a card

### Change page

- Pagination

---

## All invoices (`/account/orders/invoices`)

Navigate to all invoices to view all invoices documents.

### Back to orders hub

- Click **Orders** link at top

### Open an invoice

- Click a card

### Change page

- Pagination

---

## Location orders (`/account/locations/...`)

Navigate to location orders to view quotes and invoices for a location. Distributor admin only.

### View quotes for location

- Quotes table — sort, search, paginate, click row

### View invoices for location

- Invoices table — sort, search by `#`, paginate, click row

---

## Profile (`/account/profile`)

Navigate to your profile to update your name.

> ↗ [Managing Customer Account Details and Addresses](./account/profile-and-addresses.md)

### Update name

- Edit first / last name
- Save

---

## Addresses (`/account/addresses`)

Navigate to your addresses to add, edit and delete delivery addresses and set as default.

> ↗ [Managing Customer Account Details and Addresses](./account/profile-and-addresses.md)

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

Navigate to users to manage users. Admins only (Web Admin, Distributor Admin, Location Admin).

> ↗ [Managing User Accounts and Permissions](./account/manage-users.md)

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

Navigate to company to view company details, add locations, view active catalogs and restrict catalog prices. Distributor admin only.

> ↗ [How to Add a Company Location and set Price Visibility](./account/company-page.md)

### View company details

- Company name, locations list, catalog list (read-only)

### Restrict catalog prices

On - Distributors and Location Admins see base prices
Off - All users see prices from the catalog

- Toggle **Restrict catalog prices**
- Confirm in the dialog
- Affects what prices users at your company see

> ↑ [Go back to Website Documentation](./README.md)