# aicademy post-mortem

A static, single-page retrospective of aicademy (2023–2025), an AI-powered study platform.

Everything the site needs is in `public/`: one `index.html` with inline CSS and JS, plus `favicon.svg`. There is no build step. Fonts load from Google Fonts.

## Preview locally

```bash
npx serve public
```

Or open `public/index.html` directly in a browser.

## Deploy to Cloudflare Pages

**From the dashboard (Git integration):**

1. Cloudflare dashboard → Workers & Pages → Create → Pages → Connect to Git.
2. Pick this repository and the branch to deploy.
3. Framework preset: `None`. Build command: leave empty. Build output directory: `public`.
4. Save and deploy, then add your custom domain under the project's Custom domains tab.

**From the command line:**

```bash
npx wrangler pages deploy public --project-name aicademy
```

## Sources

Content comes from aicademy's 2023–2024 pitch decks, ads and data model. Traction figures are from the June 2023 deck.
