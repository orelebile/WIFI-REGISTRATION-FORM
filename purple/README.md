# Purple splash page build

Purple's HTML splash page editor has separate **HTML**, **CSS** and **JS**
tabs, so the files here map straight onto them:

| File | Paste into |
| --- | --- |
| `splash.html` | HTML tab |
| `splash.css` | CSS tab |
| — | JS tab: leave the boilerplate alone |

The root `landing.html` + `css/landing.css` remain the standalone version you
can open in a browser. This folder is the Purple-ready copy of the same page.

## Differences from the standalone version

1. **No `<link rel="stylesheet">`.** Purple serves the CSS tab itself; a link
   to a `css/` folder would 404.
2. **No `<!DOCTYPE>`/`<head>`/`<body>`** if the boilerplate already provides
   them — in that case paste only the `<main>` block.
3. **Images come from snippets, not paths.** Upload artwork in the template's
   image library and reference it with the `[[!ImageUrl]]` snippet. It works
   in the HTML, CSS and JS tabs alike.
4. **jQuery is already loaded** by the template. Do not add it.

## Still to wire up

Both need the exact snippet text from the **Snippets panel on the HTML tab** —
the names differ between template versions, so copy them from your editor
rather than typing them from memory:

- `splash.html` — the `AUTH-SNIPPET-HERE` marker on the FREE 30 MINUTES link.
  Purple's boilerplate JavaScript binds the connect action to elements
  carrying its authentication data attribute. Without it the button is inert.
- `splash.css` — `REPLACE-WITH-IMAGEURL-SNIPPET` for the promo banner photo.

## Note on the registration form

The Google Apps Script POST in `index.html` fires **before** the visitor is
authenticated, so it only reaches Google if `script.google.com` (and the
`*.googleusercontent.com` redirect target) are in the walled garden allow
list. If submissions come back empty, check that first — the failure is
silent from the visitor's side.
