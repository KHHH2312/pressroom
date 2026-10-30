# Third-party components

Pressroom bundles or depends on the following. No fonts are bundled; slide themes use families
that ship with Windows, and the app UI uses system Segoe UI / Georgia / Consolas.

| Component | Version | License | Use |
|---|---|---|---|
| [pptxgenjs](https://github.com/gitbrent/PptxGenJS) | 4.0.1 | MIT | Native PowerPoint generation |
| [mammoth](https://github.com/mwilliamson/mammoth.js) | 1.13.0 | BSD-2-Clause | `.docx` text extraction |
| [jszip](https://github.com/Stuk/jszip) | 3.10.2 | MIT or GPL-3.0-or-later | ZIP container used by pptxgenjs |

Transitive dependencies are recorded in `package-lock.json`. They are installed at build time and
are not modified.

**Image parsing note.** pptxgenjs depends on `image-size`. That package's advisory covers its
JXL, HEIF and ICNS parsers; Pressroom only accepts PNG, JPEG and WebP data URLs (enforced in deck
normalisation and import parsing), so those parsers are not reached by user content. `npm audit`
still reports the transitive advisory against the dependency itself.

“PowerPoint” is a trademark of Microsoft Corporation. Pressroom is not affiliated with Microsoft,
OpenAI, Anthropic or any presentation vendor.
