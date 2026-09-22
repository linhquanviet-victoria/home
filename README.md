# Linh Quán Việt – Bếp Cô Lan website

Static one-page website with an online ordering form. No server needed — hosts free on GitHub Pages, just like the Lan Nails Spa site.

## Files
- `index.html` — the whole website (HTML + CSS + JavaScript in one file)
- `images/` — logo, food photos, menu flyer

## 1. Make online orders reach your email (Web3Forms — free, required)
Orders are emailed to you with no backend using **Web3Forms**.

1. Go to <https://web3forms.com>
2. Enter **linhquanviet@gmail.com** → they email you an **Access Key**
3. Open `index.html`, find this line near the bottom (in the `<script>`):
   ```js
   const WEB3FORMS_KEY = 'PASTE-YOUR-WEB3FORMS-KEY-HERE';
   ```
4. Replace the placeholder with your key, e.g. `const WEB3FORMS_KEY = 'abcd-1234-...';`
5. Save.

Until you do this, the order form runs in **demo mode** (shows a success message but does NOT send the email).

## 2. Publish free on GitHub Pages → https://linhquanviet.github.io
1. Create a free GitHub account with the username **linhquanviet** (at <https://github.com/signup>).
2. Create a new **public** repository named exactly `linhquanviet.github.io`.
3. Upload everything in this folder (`index.html` and the `images` folder) — drag-and-drop works on github.com.
4. In the repo: **Settings → Pages → Source = "Deploy from a branch" → main / root → Save.**
5. Wait ~1 minute. Your site is live at **https://linhquanviet.github.io**

To update later: edit the file on GitHub (or re-upload) and it republishes automatically.

## What the site includes
- **Vietnamese / English language toggle** (🌐 button in the top nav; remembers the visitor's choice). Menu dishes always show both the Vietnamese name and the English description.
- Business info: address (1012 Tillicum Road), hours (Fri/Sat/Mon 9AM–7PM), phone, email, Google map
- Full menu as a photo card grid with prices (Mì gói trộn/Xôi/Bún **$19**, Bánh mì **$11**), matching the printed menu
- Online order cart: pick items + quantities, auto-calculated food total
- Pickup day (only shows open days) & pickup time
- Pickup **or** Delivery. Delivery asks for address, requires $50+ order, and notes the $5–$10 fee is confirmed by you.
- Customer notes (nhiều/ít hành, ớt, pate…)
- Photo gallery + Facebook link

## Things you may want to change
- **Facebook link**: in `index.html` search for `https://www.facebook.com/` and paste your real page URL.
- **Prices / menu items / translations**: search for `const MENU = [` — each dish has `vi` (Vietnamese name), `en` (English), and each category has a `price`. Add/remove items freely.
- **Delivery minimum**: search for `const DELIVERY_MIN = 50;`
- **Menu photos — `item1` … `item20`**: every dish uses `images/item<N>.jpg/.jpeg`, where **N is the dish's position in the menu** (1–20, top to bottom). To change a dish's photo, just replace that `item<N>` file in `images/` (keep the same name). The numbered order is:
  1 Lòng gà (Mì) · 2 Xá xíu (Mì) · 3 Heo quay (Mì) · 4 Bánh mì cá nục · 5 Bánh mì Cô Lan · 6 Bánh mì xá xíu · 7 Bánh mì xíu mại · 8 Bánh mì phá lấu · 9 Bánh mì thịt nướng · 10 Bánh mì heo quay · 11 Bánh mì lòng gà xé · 12 Xôi lòng gà · 13 Xôi thập cẩm · 14 Xôi phá lấu · 15 Xôi heo quay · 16 Xôi cá nục · 17 Bún thịt nướng & chả giò · 18 Bún cá nục · 19 Bún phá lấu · 20 Bún heo quay
  - Slots **item8** (phá lấu) and **item20** (bún heo quay) are branded green "photo coming soon" placeholders — drop in a real photo to replace them. Resize new photos to ~1100px wide so pages stay fast.
- **⚠️ Delete before publishing — copyrighted competitor photos**: these files in `images/` are from the Ba Le (Vancouver) reference site and must NOT be published: `1-Viet-sausage-scaled-300x300.jpg`, `2-Grilled-pork-scaled-300x300.jpg`, `3-veggie-scaled-300x300.jpg`, `4-bacon-scaled-300x300.jpg`, `opla-300x300.png`, `Grilled-pork-vermicelli--e1648866537783-300x300.png`, plus the two `media2F...` files. They are not used by the site; delete them (they'd otherwise be uploaded to your public repo). Use only your own photos, or stock licensed for commercial use.
