# maxxborer.com

Source assets and deployable static files for [maxxborer.com](https://maxxborer.com/) — the personal landing page of a Senior Frontend Engineer.

The site is intentionally small: a responsive contact page, technology list, résumé link, and social links. It does **not** use a client-side JavaScript framework or a runtime application server.

## Repository layout

| Path | Purpose |
| --- | --- |
| [`dist/index.html`](dist/index.html) | Shipped HTML and CSS, with metadata, responsive layout, and accessibility considerations |
| [`dist/assets/`](dist/assets/) | Versioned font and social-preview assets |
| [`assets-source/og.svg`](assets-source/og.svg) | Editable social-preview artwork |
| [`assets-source/README.md`](assets-source/README.md) | Reproducible steps for rendering the social-preview image |
| [`wrangler.jsonc`](wrangler.jsonc) | Cloudflare Workers static-assets deployment configuration |

## Publishing model

The repository contains the **deployable output** in `dist/`; no compilation step is required before publishing these files. The Wrangler configuration serves `dist/` as static assets on the custom domain.

If you are looking for more substantial source-code examples, see [my GitHub profile](https://github.com/maxxborer#selected-work) and [engineering notes](https://github.com/maxxborer/maxxborer/blob/main/ENGINEERING.md).
