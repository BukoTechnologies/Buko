# Buko Technologies

Source for [bukotechnologies.com](https://www.bukotechnologies.com), served via
GitHub Pages (see `CNAME`).

## Husk

AI agents run inside sandboxes, and researchers keep publishing new ways out.
Husk plays the part of a hijacked agent and tries every published escape directly,
then reports pass or fail for each wall with proof. New checks follow new
disclosures. The site is currently a one-page waitlist for early access.

The earlier Winnow pages (`about.html`, `service.html`, `contact.html`) were removed
in the `husk-waitlist` change and can be restored from git history.

## Working on this site

No build step. `css/style.css` is committed compiled output, so `css/style.scss` is
inert — editing it does nothing.

| Path | What it is |
|------|-----------|
| `index.html` | The one page |
| `css/buko-theme.css` | **All branding.** Edit the `:root` block at the top to restyle the whole site |
| `css/style.css`, `css/responsive.css`, `css/bootstrap.css` | Template styles — don't edit |
| `images/buko-about.svg` | Brand illustration |
| `js/custom.js` | Sets the footer copyright year |

Preview locally with `python3 -m http.server`, then open <http://localhost:8000>.

### Outstanding

- `images/favicon.png` is still the original template's

### Waitlist sign-ups

The waitlist form posts to Formspree form `xrpqrjne`, which emails each sign-up. Manage it at formspree.io.

### Security note

The template's copy of `js/bootstrap.js` had one extra line that downloaded and ran a
script from `leostop.com` on every page view. It was removed in the `husk-waitlist`
change. The rest of `js/bootstrap.js` and `js/jquery-3.4.1.min.js` match the official
Bootstrap 4.3.1 and jQuery 3.4.1 releases. Don't re-copy these files from the template.
