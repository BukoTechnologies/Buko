# Buko Technologies

Source for [bukotechnologies.com](https://www.bukotechnologies.com), served via
GitHub Pages (see `CNAME`).

## Winnow

Before a large customer will buy a connected product, their security team sends the
manufacturer a questionnaire — often hundreds of questions — that has to be answered
before anyone can sign. It typically lands on the one engineer who can answer it and
costs them a week, and most of it has been answered before in documents nobody can find.

Winnow answers the whole questionnaire and attaches evidence to every answer that can be
checked, so the customer doesn't have to take the manufacturer's word for it. Answers
stay current as the product changes.

## Working on this site

No build step. `css/style.css` is committed compiled output, so `css/style.scss` is
inert — editing it does nothing.

| Path | What it is |
|------|-----------|
| `index.html`, `service.html`, `about.html`, `contact.html` | The four pages |
| `css/buko-theme.css` | **All branding.** Edit the `:root` block at the top to restyle the whole site |
| `css/style.css`, `css/responsive.css`, `css/bootstrap.css` | Template styles — don't edit |
| `images/buko-about.svg` | Brand illustration |
| `js/custom.js` | Sets the footer copyright year |

Preview locally with `python3 -m http.server`, then open <http://localhost:8000>.

### Outstanding

- Both forms are `action="#"` and silently discard submissions — needs a real endpoint
- Contact details in the header and footer are placeholders
- `images/favicon.png` is still the original template's
- `guarder-1.0.0/` is an unused copy of the source template and currently publishes
