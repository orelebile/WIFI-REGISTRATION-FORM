# Assets

Drop the artwork for `landing.html` here:

| File | Used for | Notes |
| --- | --- | --- |
| `upic-banner.jpg` | Promo banner photo behind the teal panel | ~720 x 630, centre-cropped. A gradient fallback shows if the file is missing. |
| `upic-logo.png` | UPICtv wordmark | Optional. The page ships with an inline SVG version; to use the real logo, swap the `<svg class="brand__logo">` block in `landing.html` for `<img src="assets/upic-logo.png" alt="UPICtv" class="brand__img">`. |

Keep everything local — a captive-portal page has to render before the
visitor has internet access, so no CDN or Google Fonts links.
