# Font attribution

Unbounded Regular 400, version 1.600, by the Unbounded Project / Web 3.0 Technologies Foundation.

- Source: https://github.com/w3f/unbounded/blob/main/WOFF/Unbounded-Regular.woff2
- Upstream Git blob: `5db9542d06bcd5248c9a02ed43c90909d35cf03e`.
- License: SIL Open Font License 1.1; see [Unbounded-OFL.txt](Unbounded-OFL.txt).
- The original WOFF2 is redistributed unchanged, with its complete character set. No subsetting.
- Arial is a system fallback; no Arial font file is bundled.

All files in `dist/assets/` use a content hash in their filename and receive immutable browser caching via `dist/_headers`. When replacing an asset, use its new SHA-256 prefix in the filename and update all references in `dist/index.html`. HTML and the stable favicon URLs use revalidation instead of immutable caching. The PNG favicon also serves as the home-screen icon; it has an opaque background for that purpose.
