# Invoice Generator

A single-page invoice generator that produces a PDF matching a fixed invoice
format. No build step, no server — open `index.html` in a browser, or deploy
the folder to Vercel as a static site.

## Usage

Open `index.html`. Edit any field on the left; the preview on the right updates
live. Click **Download PDF** to save the invoice.

- **Everything is editable**: your details, the *Bill To* client block, invoice
  number, date, line items, and the terms text.
- **Line items**: use **+ Add item** and **Delete** to change how many rows the
  invoice has. Each item has a description, an optional detail line (e.g.
  `12 Hours x $50/hour`), and an amount.
- **Total** is calculated automatically from the item amounts and shown as
  `$X,XXX.XX USD`.
- **Filename** is generated from the invoice date, title, and number, e.g.
  `July_2026__PPC_SEO_GEO_Consultancy_Invoice__2457.pdf`.

## Deploying to Vercel

This is a static site — no configuration needed.

1. Push this repo to GitHub (already done on the working branch).
2. In Vercel, **New Project → Import** this repository.
3. Framework preset: **Other**. Leave build command empty and output
   directory as the repository root. Deploy.

## Files

- `index.html` — the app (form, live preview, styling, and logic).
- `html2pdf.bundle.min.js` — vendored PDF library (html2pdf.js v0.10.2), so the
  tool works offline with no external CDN dependency.
