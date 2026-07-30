# Kronos Bio *

Kronos Bio was a clinical-stage biopharmaceutical company in the life-sciences sector, backed by GV,
working on cancer therapeutics. It entered the API Evangelist network as a GV portfolio lead.

## Enrichment status: no API surface

The enrichment pipeline ran on 2026-07-19 and found no API, developer portal, SDK, or documentation
surface to harvest:

- `kronosbio.com` and `www.kronosbio.com` both return a GoDaddy domain-parking lander.
- The lander answers HTTP 200 with `text/html` for **every** path. A control request to a
  nonsense path returned byte-identical content to `/.well-known/security.txt`, so the apparent
  `/.well-known/*` and `/llms.txt` hits are a wildcard, not real documents. See
  `well-known/kronos-bio-well-known.yml` for that negative result.
- `ir.`, `docs.`, `api.`, and `developer.` subdomains do not resolve.
- No GitHub organization or public repositories were found.

The only real artifact harvested is `security/kronos-bio-domain-security.yml` — live DNS/TLS posture
for the parked domain.

Backed by: gv — https://kronosbio.com
