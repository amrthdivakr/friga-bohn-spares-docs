# Orders

## Cart (`/cart`)

### Review lines

- Open cart from header icon
- Check name, code, price, quantity, line total

### Change quantity

- Use the number field on a line — saves automatically

### Remove a line

- Click the bin icon on that row

### Request a quote

- Click **Generate quote**
- Cart is cleared after success
- You are taken to the quote page

### Empty cart

- Message shown with **Continue shopping** → Home

---

## Quote (`/quote/...`)

### Review quote

- Read line items and total (cannot edit here)

### Download quote PDF

- Click **Download quote**

### Share quote link

- Click **Share quote**
- Use device share, or link is copied to clipboard

### Start order (generate invoice)

- Click **Generate invoice**
- Form appears on the same page

### If quote already converted

- **View invoice** button instead — opens invoice page

---

## Quote — order form (same page, after Generate invoice)

### Fill in details

- Purchase order number
- Company name
- First / last name
- Email
- Phone (format `+33612345678`)
- Address, city, country, state/province, zip

### Cancel

- Click **Cancel** → back to quote view

### Confirm order

- Click **Confirm order**
- On success → invoice page
- On failure → error page (see below)

---

## Quote PDF view (`/quote/.../share`)

### View or print PDF

- Page opens as full-screen PDF
- Use browser print or save as PDF

---

## Invoice (`/invoice/...`)

### Review invoice

- Line items, totals, order details (read-only)

### Download invoice PDF

- Click **Download invoice**

### Share invoice link

- Click **Share invoice**
- Share or copy link

---

## Invoice PDF view (`/invoice/.../share`)

### View or print PDF

- Full-screen PDF
- Print or save from browser

---

## Something went wrong (`/cart/error`)

### Read the message

- Note what failed

### Check orders anyway

- If message mentions processing delay, check **Orders** in account

### Go back

- Click **Back to orders**
