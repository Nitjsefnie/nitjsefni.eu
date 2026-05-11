# nitjsefni.eu

Source of [https://nitjsefni.eu/](https://nitjsefni.eu/) — my personal landing page.

A single hand-rolled HTML file plus a self-hosted webfont. Pure HTML + CSS,
no JavaScript, no third-party requests at page-load time, no analytics. The
"GitHub stats" widgets on the page are SVGs rendered by a separate cron job;
the renderer lives in [`Nitjsefnie/gh-widgets`](https://github.com/Nitjsefnie/gh-widgets)
and writes the SVGs into `/widgets/` on this server.

## Contents

| Path | What |
|---|---|
| `index.html` | The whole page. ~12 KB. |
| `fonts/` | Five [JetBrains Mono](https://github.com/JetBrains/JetBrainsMono) woff2 weights (Apache-2.0, ~95 KB each). Served from `/fonts/` instead of Google Fonts so the page has zero third-party requests. |

## License

The HTML/CSS source in this repo is MIT (do whatever, attribution appreciated).
JetBrains Mono is Apache-2.0 by JetBrains.
