A PalmPay-style "Fast Checkout" modal built on top of a Paystack-like checkout page, using Next.js (App Router), React, and Tailwind CSS.

## What's in here

A single-page checkout demo (`src/app/page.tsx`) with a floating action button that opens a 3-state modal:

1. **Transfer summary** — bank details and a "Pay" button.
2. **PIN entry** — 4 animated PIN dots, a hidden numeric input (works with the native mobile keyboard), and a "Secured Input" badge. Confirming shows a loading spinner, then advances to success.
3. **Success** — an animated checkmark, "Payment Sent!", and "View Receipt" / "Back to checkout" actions.

All three states live in one modal container and transition with a horizontal slide (CSS `transform`, no animation libraries). Closing via "Back to checkout" also triggers a matching loading/success sequence on the underlying checkout page: the whole card slides away and a centered confirmation takes its place.

## Getting started

```bash
npm install
npm run dev
```

Open [http://localhost:3005](http://localhost:3005) (the dev server runs on port 3005, see `package.json`).

## Stack

- Next.js 16 (App Router)
- React 19
- Tailwind CSS v4
- [Remixicon](https://remixicon.com/) for icons

## Deployment

Deployed on [Netlify](https://www.netlify.com/) via the [Next.js Runtime](https://docs.netlify.com/frameworks/next-js/overview/) — push to `main`/`master` and Netlify builds and deploys automatically once the site is linked.

## Notes

- This Next.js version has breaking changes from what you may know — see `AGENTS.md` before making changes; it points at the bundled docs in `node_modules/next/dist/docs/`.
