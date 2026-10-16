# Chotu Garment (Wholesale)

Single-file storefront + admin panel, powered by Supabase.

## Files
- `index.html` – storefront (home, shop, product, about, contact, cart/checkout) and admin panel (`#/admin`)
- `supabase/schema.sql` – database tables, security rules, order function, image bucket

## Setup
1. Run `supabase/schema.sql` in Supabase SQL Editor (already applied to project `blocbngvbvsiyflyvxcr`).
2. In `index.html`, edit the `CFG` block: Supabase URL, publishable key, WhatsApp, email, phone.
   Never put a service role key in this file.
3. Supabase > Authentication > Users > Add user, then make it admin:
   `insert into profiles(id,full_name,role) select id,'Owner','admin' from auth.users where email='YOUR_EMAIL';`
4. Host with GitHub Pages: Settings > Pages > Branch main, folder / (root).
