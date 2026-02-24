# do_one_blog

Astro blog starter configured for Cloudflare Pages.

## Requirements

- Node.js 20+
- npm 10+
- Cloudflare account for deployment

## Local development

```bash
npm install
npm run dev
```

App runs at `http://localhost:4321`.

## Build

```bash
npm run build
```

Build output is generated in `dist/`.

## Write blog posts

Add Markdown or MDX files in:

```text
src/content/blog/
```

## Deploy option A (recommended): GitHub + Cloudflare Pages dashboard

1. Push this repo to GitHub.
2. In Cloudflare dashboard, create a Pages project and connect the repo.
3. Set build command to `npm run build`.
4. Set output directory to `dist`.
5. Add environment variable `SITE_URL` (for example `https://your-domain.com`).

## Deploy option B: CLI with Wrangler

Login and create the project once:

```bash
npx wrangler login
npx wrangler pages project create <project-name>
```

Then deploy:

```bash
npm run build
npm run deploy -- --project-name <project-name>
```

Deploy to production branch:

```bash
npm run deploy:prod -- --project-name <project-name>
```

## Domain setup

After attaching a custom domain in Cloudflare Pages, update `SITE_URL` to the same domain.
