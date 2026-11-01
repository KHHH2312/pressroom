# Changelog

## 1.16.0 — 2026-11-01

- Alt text now reaches the exported deck. The Alt text field on an image slide is written into the PPTX as the picture's description, falling back to the caption and then the slide title, and the brand logo is announced as `<deck title> logo`. Screen readers read what you typed.

## 1.15.0 — 2026-11-01

- Presenter time limit: set a budget in minutes in the presenter bar; the timer turns amber at four fifths of it and red past the line. 0 means no limit.

## 1.14.0 — 2026-10-30

- Presenter blank screen: B (or the Blank button) blacks out the projected slide without leaving presenter view; the next-slide preview and timer keep running.

## 1.13.0 — 2026-10-30

- Presenter view previews the following slide.
- Pull slides from another deck, after the current slide or at the end.
- Deck-wide find & replace, including speaker notes when asked.

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
