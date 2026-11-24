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

No build step and no frameworks. The page is plain HTML and one stylesheet, plus
a few lines of inline JavaScript that set the footer year and play the terminal
animation once on load.

| Path | What it is |
|------|-----------|
| `index.html` | The one page |
| `css/husk.css` | **All styling.** The palette and fonts are in the `:root` block at the top |
| `images/favicon.png` | Browser tab icon |

Fonts (Martian Mono and Instrument Sans) load from Google Fonts.

Preview locally with `python3 -m http.server`, then open <http://localhost:8000>.

### Outstanding

- `images/favicon.png` is still the original template's

### Waitlist sign-ups

The waitlist form posts to Formspree form `xrpqrjne`, which emails each sign-up. Manage it at formspree.io.

### Security note

The original template's `js/bootstrap.js` had one extra line that downloaded and ran
a script from `leostop.com` on every page view. The redesign removed the template's
JavaScript, CSS, fonts and images entirely, so the site no longer ships any of it.
Don't re-add files from that template.
