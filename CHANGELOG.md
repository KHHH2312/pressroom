# Changelog

## 1.6.0 — 2026-10-30

- Security: override transitive image-size to 2.0.4, fixing two high-severity DoS advisories.
- Probe PNG embedded in the suite; npm audit reports zero vulnerabilities.

## 1.0.0 — 2026-10-30

- First public release of Pressroom, a local-first deck studio for Windows.
- Markdown/text/.docx import with automatic layouts, agenda and closing.
- Fourteen layouts, six themes, brand kit with logo and footer.
- Native PPTX export: editable text and shapes, PowerPoint charts, images and speaker notes.
- Native chart editor (bar, line, pie, donut) from CSV/TSV/JSON.
- Deck library with autosave, duplicate, delete; undo and drag reordering.
- Optional AI draft with a bring-your-own OpenAI or Anthropic key.
- Portable Electron build: integrity gate, self-signed code signature, SHA-256 sums and a
  per-file manifest attached to the release.
