# nitjsefni.eu

Source of [https://nitjsefni.eu/](https://nitjsefni.eu/) — my personal landing page.

A single hand-rolled HTML file plus a self-hosted webfont. Pure HTML + CSS,
no browser-side JavaScript, no third-party requests at page-load time, no
analytics. The
"GitHub stats" widgets on the page are SVGs rendered by a separate cron job;
the renderer lives in [`Nitjsefnie/gh-widgets`](https://github.com/Nitjsefnie/gh-widgets)
and writes the SVGs into `/widgets/` on this server.

## Contents

| Path | What |
|---|---|
| `index.html` | The whole page. ~14 KB. |
| `fonts/` | Five [JetBrains Mono](https://github.com/JetBrains/JetBrainsMono) woff2 weights (SIL Open Font License 1.1, ~95 KB each; licence text in `fonts/OFL.txt`). Served from `/fonts/` instead of Google Fonts so the page has zero third-party requests. |

## License

The HTML/CSS source in this repo is MIT (do whatever, attribution appreciated).
JetBrains Mono is under the SIL Open Font License 1.1, copyright The
JetBrains Mono Project Authors; the licence text is in
[`fonts/OFL.txt`](fonts/OFL.txt).
