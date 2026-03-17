# InvoiceHound Landing Page

Simple validation landing page for InvoiceHound — email capture to validate demand before building.

## Before Going Live

### 1. Set up Formspree (takes 2 minutes)

1. Go to [formspree.io](https://formspree.io) and sign in with `derekschatz.ai@gmail.com`
2. Click **+ New Form** → name it "InvoiceHound Early Access"
3. Copy the form endpoint — looks like `https://formspree.io/f/abcd1234`
4. In `index.html`, find and replace both instances of `FORM_ID` with your actual ID:
   ```
   action="https://formspree.io/f/FORM_ID"
   ```
   → Replace `FORM_ID` with the code from step 3 (e.g., `xabcd1234`)

There are **two forms** on the page (hero + bottom CTA) — update both.

---

## Deploy to Vercel (Drag & Drop)

1. Go to [vercel.com](https://vercel.com) and log in
2. Click **Add New → Project**
3. Drag the entire `landing/` folder into the upload zone
4. Click **Deploy**
5. Done — you'll get a `*.vercel.app` URL instantly

> No build step. No config. It's a static HTML file.

---

## Deploy to Netlify (Drag & Drop)

1. Go to [app.netlify.com/drop](https://app.netlify.com/drop)
2. Drag the `landing/` folder into the drop zone
3. Done — you'll get a `*.netlify.app` URL instantly

---

## Deploy via Vercel CLI

```bash
cd ~/clawd/products/invoicehound/landing
npx vercel login   # opens browser OAuth
npx vercel --yes   # deploy after login
```

> **Note:** Vercel CLI requires browser authentication. Run `npx vercel login`, complete the OAuth flow in your browser, then run `npx vercel --yes` to deploy.

---

## Tracking Signups

- Formspree dashboard shows all submissions in real-time
- You can set up email notifications in Formspree settings (Settings → Notifications)
- Export CSV from the Formspree dashboard any time

---

## What to Watch

- **Signup rate** — if >5% of visitors sign up, the pain is real
- **Traffic source** — track UTM params if you share on different channels
- **Email engagement** — follow up manually with early signups to validate ICP

---

## Files

```
landing/
├── index.html   ← The entire page (single file, no dependencies)
└── README.md    ← This file
```
