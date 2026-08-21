# Buko Technologies

Marketing site for [Buko Technologies](https://www.bukotechnologies.com) —
served from this repo via GitHub Pages (see `CNAME`).

## The product: Winnow

**Present isn't the same as exploitable.**

Companies that ship a connected product — device plus cloud plus apps — get blocked by
enterprise customers' *product* security questionnaires before a contract can close.
Not "is MFA on in your tenant," but: what does the device collect, what does it talk to
on our network, how is firmware signed, what's in your SBOM, can one customer reach
another customer's fleet, what happens when you find a vulnerability.

Every tool in this category verifies by reading a manifest. That proves almost nothing.
An SBOM with 400 CVEs usually contains about six that anyone could actually reach — the
rest were compiled out, are never called, or need an interface the device doesn't expose.
Today that gets defended by hand, in email, every single time.

Winnow verifies three ways:

| Tier | Method | Who else does this |
|------|--------|--------------------|
| 1. Read the manifest | Parse SBOM, build config, fleet/cloud setup | Everyone. Table stakes. |
| 2. Work out what's reachable | Is the vulnerable code in the shipped artefact, on a callable path, behind an exposed interface? Can one tenant reach another's fleet? | The gap |
| 3. Actually try it | Push an unsigned update and confirm rejection; capture what the device really transmits; probe the tenant boundary | Nobody |

Tier 2's output is a **defensible VEX document** — "trust us, it's fine" turned into
something the customer's security team can independently check.

**Target:** companies shipping connected products into enterprises — robotics, industrial
IoT, medical devices, smart building, automotive. Narrower than generic SMB security, but
the pain is worse, deal sizes are larger, and the compliance platforms (Vanta, Drata)
don't serve it — they do *company* compliance, not *product* assurance.

**Why it's a subscription, not a transaction:** for a product, every release changes the
SBOM and the CVE picture. Answers go stale on their own. Winnow runs from the build
pipeline, so re-verification is structural rather than a feature to argue for.

**Tailwind:** the EU Cyber Resilience Act and sector rules (medical, automotive) mandate
SBOM and vulnerability handling for products with digital elements. Regulation manufactures
dated, mandatory demand. *(Verify current timelines before quoting them.)*

**Scope, deliberately narrow.** Not a firmware binary analysis platform (integrate with
one, don't rebuild it), not SAST/DAST, not a pentest, not an on-device agent, not a
certification body.

Status: pre-launch. The site collects early-access interest.

**Build the claim library from public standards only** — ETSI EN 303 645, NIST IR 8259,
IoTSF, ISO/SAE 21434, CRA requirements. Never from questionnaires received at a day job;
those belong to that employer and its customers.

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
