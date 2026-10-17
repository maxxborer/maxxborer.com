# Social preview

`og.svg` is the editable 1200×630 source. The name uses Unbounded Regular 400, version 1.600, matching the website. The other lines use Arial Regular.

For native export, install these actual fonts locally and verify their resolution with `fc-match Unbounded` and `fc-match Arial`. The SVG also references the repository's WOFF2 for browser rendering. Font binaries do not need to be added to this directory.

Export with Inkscape and ImageMagick:

```sh
inkscape assets-source/og.svg --export-width=2400 --export-filename=/tmp/og.png
convert /tmp/og.png -resize 1200x630 -sampling-factor 4:4:4 -strip -interlace Plane -quality 85 /tmp/og.jpg
```

Copy the JPEG into `dist/assets/og-unbounded.<sha256-prefix>.jpg` using the first 12 characters of its SHA-256 hash, then update both `og:image` and `twitter:image` in `dist/index.html`. Keep previously published hashed previews available for clients that cached their URLs. This source directory is not deployed; the site still needs no build step.
