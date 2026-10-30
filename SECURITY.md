# Security

Pressroom is a local desktop app. Its attack surface is the files you import, the generated deck,
and the optional AI call you initiate with your own key.

## What is in scope

- The **renderer is untrusted**: deck content is escaped, images must be local PNG/JPEG/WebP data
  URLs, and the renderer is sandboxed with context isolation. Navigation, window-open, webviews and
  permissions are denied. CSP allows no remote scripts, styles or images.
- The **embedded server** binds to `127.0.0.1` on a random port. Static file serving is path-checked,
  API bodies are size-capped, and requests never expose files outside the web root. There is no
  authentication surface because there is no remote access.
- **Imports**: markdown is parsed, never executed. `.docx` is text-extracted with mammoth. Images
  are restricted to PNG/JPEG/WebP; the `image-size` advisory affecting JXL/HEIF/ICNS parsers is not
  reachable through accepted formats.
- **AI keys** live in the app's browser storage, are sent only to the chosen provider on an explicit
  Draft action, and are never persisted by the server.
- **Release integrity**: the packaged app is checked against the source tree before publishing; any
  changed file, unexpected file or stray script aborts the release. The installer is signed with a
  self-signed certificate and published with SHA-256 sums and a per-file manifest.

## Out of scope

- Someone with code execution as the same Windows user can read the deck files and tokens; that is
  the environment the app runs in.
- The self-signed certificate is not trusted by Windows; SmartScreen will warn. Verify the download
  against the published SHA-256 checksums.

## Reporting

Open a private security advisory on the repository. Include the version, reproduction and impact.
No public issue for credential or file-access flaws.
