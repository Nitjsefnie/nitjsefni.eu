# Contributing to nitjsefni.eu

This is a personal landing page, so feature requests are mostly not
applicable — but issues and pull requests are welcome for anything that is
objectively broken: a rendering bug in a browser I do not use, an
accessibility failure, a bad contrast ratio, a typo, a dead link.

## LLM and agent contributions are welcome

You may use an LLM or a coding agent to write your contribution. There is
no penalty, no separate review queue, and no expectation that you rewrite
its output by hand. Much of this repo was built that way.

Two conditions, and they are about honesty rather than provenance:

1. **Disclose the model** with a trailer on each commit it authored:

   ```
   Co-Authored-By: <Model Name> <noreply@example.com>
   ```

   e.g. `Co-Authored-By: Claude Opus 4.8 <noreply@anthropic.com>`. One
   primary-author trailer per commit.

2. **Do not submit claims you have not verified.** If you say the page
   breaks in a browser, say which browser and version and what you saw.
   A layout claim that nobody actually loaded is not a bug report.

If a maintainer's reply reads like it was drafted by an agent, it probably
was. That is fine in both directions.

## The constraints

These are design decisions, not oversights. A patch that violates one will
be declined however well it is built:

- **No browser-side JavaScript.** None. Not a snippet, not an analytics
  tag, not a "tiny" enhancement.
- **No third-party requests at page load.** No CDN, no Google Fonts, no
  external images. The webfont is self-hosted in `fonts/` for exactly this
  reason. The GitHub stat widgets are static SVGs served from the same
  origin, rendered out-of-band by
  [`gh-widgets`](https://github.com/Nitjsefnie/gh-widgets).
- **One file.** The page is `index.html`, all of it — markup and CSS
  together. No build step, no preprocessor, no framework, no splitting the
  CSS into a separate stylesheet.

## Getting it running

```sh
python3 -m http.server 8000
```

Then open <http://localhost:8000/>. Opening `index.html` directly off disk
works too; the fonts resolve either way.

## Tests

There are none, and none are wanted. The verification is: load the page,
resize the window, and check it in more than one browser. If your change
touches layout, say in the PR which browsers and widths you actually looked
at.

## House style

- Semantic HTML first; classes only where a selector genuinely needs one.
- CSS custom properties for colours. Both light and dark schemes must work
  — the page follows `prefers-color-scheme`.
- The page is ~14 KB. Keep it that way; a change that adds a lot of weight
  needs to be worth it.
- No linter, no formatter. Match the surrounding file.

## Pull requests

Small and single-purpose. Include what changed and why, and a screenshot
for anything visual. `fonts/` is JetBrains Mono under Apache-2.0 — the
source in this repo is MIT, and that split stays as it is.
