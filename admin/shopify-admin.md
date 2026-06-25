# Shopify Admin

Minimal steps for common admin tasks on the Friga Bohn spares store.

---

## Orders

Use the Shopify Admin to view and manage orders.

### View orders list

- Go to **Orders**
- Browse the list or search by order name (e.g. `#1042`) or customer

### Open an order

- Click a row → order detail page
- Review line items, customer, company, PO number, shipping address, totals

### Set payment status

- Open the order
- In **Payment** section, click **Mark as paid** (or change status as needed)
- Confirm if prompted

### Set fulfilment status

- Open the order
- In **Fulfilment** section, click **Mark as fulfilled** (or create a fulfilment)
- Add tracking if required → save

---

## Draft orders

Storefront **quotes** are draft orders. Name format e.g. `#D1042` — number after `D` is the quote id on the site.

### View drafts list

- Go to **Orders** → **Drafts**
- Browse or search by draft name or customer

### Open a draft

- Click a row → draft detail page
- Review line items, customer, company, location, totals

### Complete a draft manually

- Open the draft
- Click **Mark as paid** / **Create order** (wording may vary) to convert to an order
- Normally the customer does this from the storefront quote page

### Delete a draft

- Open the draft
- Click **Delete draft order** → confirm

---

## Products

Each product is a **spare part**. Models are metaobjects, not products.

### Find a product

- Go to **Products**
- Search by title or **Part code** metafield

### Open a product

- Click a row → product detail page

### Edit title or status

- Change **Title** at the top
- Set **Status** to **Active** (visible) or **Draft** (hidden from storefront)

### Edit price

- Scroll to **Variants**
- Open the variant → set **Price**
- Save

### Add or change images

- In **Media**, click **Add media** or select existing image
- Upload image or pick from library
- Set featured image if needed
- Save

### Edit metafields

Pinned fields on the product page:

- **Model Series** — link to the model this part belongs to
- **Part Category** — link to part type
- **Part Code** — part number (e.g. `PDVE00572`)
- **Part Name (French)** — French part name

To change a reference field, click the field → search and select the metaobject → save.

### Publish to sales channels

- In **Publishing** / **Sales channels**, ensure the Online Store (and any other required channels) are checked
- Save

---

## Metaobjects

Models and categories live here — not under Products.

### View entries

- Go to **Content** → **Metaobjects**
- Pick a type:
  - **Model**
  - **Model Category**
  - **Parent Model Category**
  - **Part Category**
- Browse the list or search

### Open an entry

- Click a row → entry detail page

### Edit a model

- Open the **Model** entry
- Edit fields:
  - **Code** — nameplate series code
  - **Name** — display name
  - **Model Image** — upload or select file
  - **Category** — link to Model Category
  - **Description**
  - **Compatibility Document** — upload or select PDF
- Save

### Publish an entry

- After saving, set status to **Published** (if shown as draft)
- Unpublished entries may not appear on the storefront

### Upload a file for metaobject fields

- Go to **Content** → **Files** → upload
- Or upload directly when editing a file field on the metaobject entry

---

## Customers

### View customers list

- Go to **Customers**
- Browse or search by name or email

### Open a customer

- Click a row → customer detail page

### Edit name or email

- Click **Edit** on name or contact details
- Save

### Set role (storefront permissions)

- On the customer page, find metafield **role**
- Set to one of:
  - `Distributor`
  - `Distributor Location Admin`
  - `Distributor Admin`
  - `Accounts`
  - `Web Admin`
- Save — spelling and capitals must match exactly

### View company link

- On the customer page, check **Company** / **B2B** section for linked company and location

---

## Companies

### View companies list

- Go to **Customers** → **Companies**
- Browse or search by company name

### Open a company

- Click a row → company detail page

### View locations and contacts

- On the company page, open **Locations** tab — list of company locations
- Open **Customers** / **Contacts** tab — users linked to this company

### Edit company name

- Click **Edit** on company name → save

### Set restrict catalog prices

- On the company page, find metafield **restrict_catalog_prices**
- Set to **true** or **false**
- When true, buyers at this company see list prices instead of catalog prices
- Save

### Add a contact to the company

- On the company page, click **Add customer** (or **Add contact**)
- Select or create customer → assign to a location → save

---

## Catalogs

B2B catalog pricing per dealer. Usually created by catalog-sync — use manual steps for new locations or exceptions.

### View catalogs

- Go to **Markets** → **Catalogs** (or **B2B** → **Catalogs**)
- Click a catalog to see linked price list and company locations

### Create a price list (if none exists)

- Go to **Markets** → **Catalogs** → **Price lists** (or **Products** → **Price lists**)
- Click **Create price list**
- Name it (e.g. dealer name)
- Set currency to **EUR**
- Save

### Create a catalog

- Go to **Markets** → **Catalogs**
- Click **Create catalog**
- Enter title (e.g. dealer name)
- Select the **Price list**
- Under **Context** / **Company locations**, assign the dealer’s company location(s)
- Save

### Add fixed prices to a price list

- Open the price list
- Click **Manage** / **Add prices**
- Search products by part code or title
- Set fixed price per variant → save
- Bulk pricing is normally handled by catalog-sync

---

## Policies

Shown in the storefront footer at `/policies`.

### View policies

- Go to **Settings** → **Policies**
- Four types: Privacy, Refund, Shipping, Terms of service

### Create or edit a policy

- Click the policy to open (or **Create from template** if empty)
- Enter **Title**
- Enter body text in the editor
- Save

### Add policies to the website footer

- Go to **Content** → **Menus**
- Open the **Footer** menu
- Add policies to the menu items
- Save

### Add translations to policies

- Go to **Apps** → **Translate & Adapt**
- Open the **Policies** section
- Add translations for the policies
- Save
