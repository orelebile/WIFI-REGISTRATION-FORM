# WIFI-REGISTRATION-FORM

Captive-portal pages for the BURS public WiFi hotspot, served through a
third-party hotspot platform.

## Pages

| File | Role |
| --- | --- |
| `index.html` | Registration form. Posts to a Google Apps Script endpoint (`scriptURL` in the inline `<script>`). |
| `landing.html` | "Powered by UPICtv" page — promo banner, FREE 30 MINUTES action, app store badges, contact details. |

Styles live in `css/index.css` and `css/landing.css`. Keep them separate from
the markup — no inline `<style>` blocks or `style="..."` attributes.
Artwork goes in `assets/` (see `assets/README.md`).

## Constraints

- **No CDNs, no Google Fonts, no external requests.** A captive-portal page
  has to render before the visitor has internet access. Type uses a local
  stack; icons and the UPICtv wordmark are inline SVG.
- **Platform snippet tokens** such as `[[!PoweredBy]]` must appear in the HTML
  as literal text — never commented out, escaped, or moved into CSS/JS. The
  platform substitutes them at serve time, so they show as raw text when a
  page is opened locally. That is expected. Wrap them in `<div class="snippet">`
  so injected markup stays centred and can't overflow.
- Pages are phone-first; the design target is a ~500px-wide column.

## Working preferences

- **Attach files in the chat.** When a file is created or changed, send it
  with the file-sharing tool so it can be downloaded directly — pushing to the
  branch alone is not enough.
- Verify visual changes by rendering the page and looking at a screenshot
  before saying it is done.
