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

## DOSROKA terms

`assets-source/dosroka/terms.md` mirrors the approved terms from the bot repository. After updating the approved text, copy it here verbatim and regenerate the committed static page with Pandoc:

```sh
pandoc --from=commonmark-raw_html --to=html5 --wrap=none \
  --template=assets-source/dosroka/terms-template.html \
  --metadata='title:DOSROKA: условия использования и обработка данных' \
  --output=dist/products/dosroka/docs/terms.html assets-source/dosroka/terms.md
```

The page at `/products/dosroka/docs/terms` works without scripts. The Telegram Instant View template is in [`assets-source/dosroka/instant-view.txt`](assets-source/dosroka/instant-view.txt); test it against the deployed URL in Telegram's editor. The plain URL stays usable in a browser and does not require Instant View.

If you are looking for more substantial source-code examples, see [my GitHub profile](https://github.com/maxxborer#selected-work) and [engineering notes](https://github.com/maxxborer/maxxborer/blob/main/ENGINEERING.md).
