# Buko Technologies

Marketing site for [Buko Technologies](https://www.bukotechnologies.com) —
served from this repo via GitHub Pages (see `CNAME`).

## The product: SteelCurtain

**Don't lose the deal to a security questionnaire.**

When a small company lands an enterprise customer, procurement sends a security
assessment before the contract can be signed — often hundreds of questions about
access control, encryption, incident response. The deal stops moving while
someone answers it from memory over a weekend, and some of those answers end up
more optimistic than true.

SteelCurtain does three things:

1. **Answers the questionnaire.** Connects to the accounts a business already
   uses and maps each question to what's actually configured, so every claim is
   backed by evidence rather than recollection.
2. **Fixes the gaps.** Most of what these forms ask about — MFA, password
   policy, phishing protection — is already included in the tools the customer
   pays for, just switched off. SteelCurtain turns it on.
3. **Keeps the answers true and reusable.** Configuration drifts; SteelCurtain
   watches what was attested to and flags it when it stops being accurate. The
   same record answers the next review and the annual cyber insurance renewal.

**Target:** small and medium businesses that sell to enterprises, plus anyone
facing a cyber insurance renewal. The wedge is the blocked deal — an urgent,
dated, expensive problem. The security remediation is the fulfillment.

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
