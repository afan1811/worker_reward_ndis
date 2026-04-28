# Spark — Worker Recognition POC

A clickable proof-of-concept for a worker reward & recognition tool, built for an
NDIS SIL discovery conversation. Single-file static site — no build step.

Built by [Cavalray](https://cavalray.com).

## What it does

- Email-gated sign-in screen captures who's trying the demo (forwarded to
  `afan@cavalray.com` via Formsubmit).
- Worker grid with eight fake support workers.
- Pick a worker → choose a recognition scenario → award points.
- Activity feed and leaderboard update in real time.
- State persists locally per browser via `localStorage`. "Reset demo" button
  wipes it clean.

## Local preview

Just open `index.html` in any browser — no server needed.

## Deploying to Vercel

The site is plain static HTML, so it just works on Vercel's static hosting.

```bash
npm install -g vercel
vercel        # preview deploy
vercel --prod # production
```

Or connect this repository to a Vercel project and every push to `main` will
deploy automatically.

## Email capture activation (one-time)

The form posts to Formsubmit. Before sharing the link with anyone:

1. Open the deployed site.
2. Sign in with your own email.
3. Check `afan@cavalray.com` for the Formsubmit activation email.
4. Click the activation link inside it.

After that, every submission lands in your inbox cleanly.

## File layout

```
.
├── index.html       # The whole app — HTML, CSS, JS in one file
├── vercel.json      # Clean URLs + basic security headers
└── README.md        # You are here
```
