# Buko Technologies

Source for [bukotechnologies.com](https://www.bukotechnologies.com), served via
GitHub Pages (see `CNAME`).

## What the site is for

Buko finds and fixes data exposure in apps built on Supabase: tables with
row-level security missing or too loose. It checks a team's own schema, writes the
policies that fix it, and blocks bad changes in CI. The site is a one-page
early-access sign-up.

Earlier versions of the site covered a firmware bug hunter, Winnow (security
questionnaires) and Husk (an agent sandbox test kit). All are retired and can be
found in git history.

## Working on this site

No build step and no frameworks. The page is plain HTML and one stylesheet, plus
a few lines of inline JavaScript that set the footer year and play the report
animation once on load.

| Path | What it is |
|------|-----------|
| `index.html` | The one page |
| `css/site.css` | **All styling.** The palette and fonts are in the `:root` block at the top |
| `images/favicon.png` | Browser tab icon |
| `images/evan.jpg` | Founder headshot (metadata stripped) |

Fonts (Archivo and IBM Plex Mono) load from Google Fonts. Headlines use the extra-wide cut of Archivo.

Preview locally with `python3 -m http.server`, then open <http://localhost:8000>.

### Outstanding

- `images/favicon.png` is still the original template's

### Early-access sign-ups

Both forms post to Formspree form `xrpqrjne`, which emails each sign-up. The `source` field says which form it came from. Manage it at formspree.io.

### Security note

The original template's `js/bootstrap.js` had one extra line that downloaded and ran
a script from `leostop.com` on every page view. The redesign removed the template's
JavaScript, CSS, fonts and images entirely, so the site no longer ships any of it.
Don't re-add files from that template.
