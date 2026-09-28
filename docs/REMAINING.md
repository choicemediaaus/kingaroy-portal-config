# Remaining — what is not finished

An honest running list. Go-live steps are at the bottom, in order. They
are provisional until the platform exists and its README and docs/ can
be checked.

## Status at 2026-09-28 (end of first session)

- Scope read (attached to the project). The platform has NOT been started
  (DECISIONS.md D3), so data is gathered as CSV/JSON/xlsx for now.
- Waiting on the client:
  - A reply to the naming email. The shortlist is in docs/branding/NAME-IDEAS.md.
  - The completed docs/client-forms/Kingaroy-portal-getting-started.xlsx
    (portal checklist, suppliers, production steps, order cycles, payments).
  - A Xero customer export (business names only).
- Kate to check domains for Kitted Uniforms and Good Stitch Uniforms.
- Kate is writing a portal variations document based on OzWear portals.
  The list of options so far is in docs/PORTAL-OPTIONS.md.
- Entity and ABN/ACN (DECISIONS.md D2) are deferred. They must be settled
  before any domain, gateway, Xero organisation or sending domain is set up.

## Waiting on Kate

- Accept or reject the tracked changes in the platform scope (sent
  2026-09-28): the 11 portal options, plus gaps G1-G7 from Kingaroy's
  operations feedback (docs/PLATFORM-GAPS.md). Decide how far returned
  stock goes (G7 vs §13 out of scope).
- The scope document is still titled "OzWear Master Portal Platform";
  worth a neutral name now OzWear is being sold.

## Not started yet

- brand/ folder (waits on the name decision)

## Done 2026-09-28 (second session)

- README.md, HANDOVER.md, choice.json, .env.example (names only)
- docs/PLATFORM-GAPS.md (no confirmed gaps yet) and docs/ONBOARDING-LOG.md
- Removed a stale .git/index.lock left by the first session
- Published to GitHub: choicemediaaus/kingaroy-portal-config (private), via
  GitHub Desktop. GitHub settings from the kit (branch protection etc.) not
  needed until the repo gains dependencies/CI.

## Domain

- Temporary domain: not yet chosen. When it is, add its end date and the
  swap plan (301 redirects, email, TLS re-issue) here that same day.
- kingaroy.ozwear.com.au belongs to whoever buys ozwear.com.au. It may
  redirect to the temporary domain only while it still exists.

### Swap plan, temporary to final domain (fill in names when known)

1. Add the final domain to the portal in the platform; TLS issues on DNS
   verification (scope §5.2). Check the certificate before switching.
2. Make the final domain primary. The temporary domain 301-redirects every
   path to the same path on the final domain, for at least twelve months.
3. Email: add the final domain to Microsoft 365, move mailboxes to it,
   keep the temporary domain as an alias for the same twelve months.
   Set up SPF/DKIM/DMARC for transactional sending on the final domain,
   then switch the portal's sending address.
4. Update portal branding, email templates and PDFs to the new domain.
5. Tell customers; update choice.json. Let the temporary domain lapse only
   after the twelve months and after checking its traffic has stopped.

## OzWear-branded materials to replace before go-live

- None listed yet. Needs an inventory of existing Kingaroy materials.

## Go-live steps, in order (provisional)

Nothing below is done from this repo. It's prepared here and run from the
Hub side after review. The portal stays in draft mode until step 10.

1. Settle the legal entity and ABN/ACN (D2). Blocks everything below.
2. Platform exists, with Kingaroy's Client record in a Sydney or Melbourne
   region, and the OzWear/Kingaroy isolation test in its suite.
3. Temporary domain: confirm .com.au eligibility for the entity (else a
   .au direct), register through Choice's Crazy Domains reseller account
   with the entity as registrant, record name/renewal/end date in
   choice.json and fill in the swap plan above the same day.
4. Microsoft 365 on the domain; transactional sending with SPF, DKIM and
   DMARC alongside it (D5).
5. Kingaroy's own payment gateway and merchant account connected
   (scope §15.1); credentials into the platform secret store and 1Password.
6. Kingaroy's own Xero organisation connected (scope §7.13).
7. Import configuration: hub branding, terminology, suppliers, production
   stages, order cycles, catalogue (mapped from this repo's data).
8. Build each customer portal from its answers to docs/PORTAL-OPTIONS.md.
9. Invite Kingaroy staff (client-staff accounts, MFA) and customer users;
   then delete the invite list from this repo and record the deletion.
10. Review, then publish from the Hub.
11. When the final domain exists: register to the entity, delegate by DNS,
    run the swap plan, keep the temporary domain redirecting for at least
    twelve months.
