# Buko Technologies

Marketing site for [Buko Technologies](https://www.bukotechnologies.com) —
served from this repo via GitHub Pages (see `CNAME`).

## The product: SteelCurtain

**Configured isn't the same as enforced.**

When a small company lands an enterprise customer, procurement sends a security
assessment before the contract can be signed. The deal stops moving while someone
answers hundreds of questions from memory over a weekend, and some of those answers
end up more optimistic than true.

Every tool in this category verifies by reading a setting. Anyone who has actually
attacked these environments knows how little that proves — "MFA is enabled" and
"MFA cannot be bypassed" are different sentences, separated by an excluded group, a
legacy protocol, or a service principal nobody has looked at since setup.

SteelCurtain verifies controls three ways:

| Tier | Method | Who else does this |
|------|--------|--------------------|
| 1. Config read | Query the API, read the setting | Everyone. Table stakes. |
| 2. Reachability | Solve the whole policy set for bypass paths | Nobody, at this market size |
| 3. Active probe | Safely attempt the bypass against a consented canary account, record the result | Nobody |

That verified state then drives everything else: questionnaire answers with evidence
attached, a prioritised list of real gaps, and continuous re-verification so you're
told the day a claim you signed your name to stops being true.

**Target:** small and medium businesses that sell to enterprises. The wedge is the
blocked deal — urgent, dated, expensive. Verification is the differentiator, and
continuous re-verification is what makes it a subscription rather than a one-off
transaction.

**Scope, deliberately narrow.** Microsoft 365 / Entra ID only. Not an EDR, not a SIEM,
not backup, not incident response, not a pentest, not a SOC 2 audit.

Status: pre-launch. The site collects early-access interest.

## Repo layout

| Path | What it is |
|------|-----------|
| `index.html`, `service.html`, `about.html`, `contact.html` | The four pages |
| `css/buko-theme.css` | **All branding.** Edit the `:root` block at the top to restyle the whole site |
| `css/style.css`, `css/responsive.css`, `css/bootstrap.css` | Original template styles — don't edit |
| `images/buko-about.svg` | Hand-drawn brand illustration |
| `js/custom.js` | Sets the footer copyright year |

Built on the free "Guarder" HTML template (Bootstrap 4 + jQuery), heavily
rewritten. There is **no build step** — `css/style.css` is committed compiled
output, so `css/style.scss` is inert. All restyling goes through
`css/buko-theme.css`, which loads last and overrides the template.

To preview locally: `python3 -m http.server` then open <http://localhost:8000>.
