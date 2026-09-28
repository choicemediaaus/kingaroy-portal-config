# Decisions — Kingaroy portal configuration

Newest last. Each entry: date, decision, reason, who decided.

## D1 — 2026-09-28 — The new brand stands fully on its own

**Decision.** Kingaroy does not use or lean on the "OzWear" name anywhere:
not in the brand name, the domain (temporary or final), email addresses,
portal copy, page titles or metadata.

**Reason.** ozwear.com.au is being sold and Kingaroy is separating from
OzWear (separation of data, domain, gateway and accounting confirmed with
the seller). A brand that leans on OzWear would tie Kingaroy to a name it
won't control after the sale.

**Background — rights to the OzWear name.** Whether Kingaroy keeps any
right to use "OzWear" after the sale has not been established. It does not
need an answer: because OzWear isn't used, the question doesn't affect
anything.

**Decided by:** Kate.

## D2 — 2026-09-28 — Legal entity after separation (OPEN)

**Open.** Which legal entity is the Kingaroy business after separation,
and its ABN/ACN? If Kingaroy currently trades under the entity being sold,
the new entity must exist before any domain, payment gateway, Xero
organisation or sending domain is set up in its name.

Until this is settled: configuration and data work only. Nothing
registered, nothing connected.

## D3 — 2026-09-28 — The platform hasn't been started

**Fact.** The Choice Master Portal platform has not been started. The
scope ("OzWear Master Portal Platform Scope", 10 Sep 2026) is still a
draft, and there is no platform repo yet.

**Consequence.** For now this repo gathers Kingaroy's data in plain
CSV/JSON. It gets mapped to the platform's import format once that
format exists. Kingaroy is the "second client is real" trigger in scope
§12, so onboarding work belongs in the platform plan from the start,
not afterwards.

## D4 — 2026-09-28 — Portals are built to a brief; payment and budgets vary per portal

**Decision (Kate).** Each Kingaroy customer portal can be configured to
its own brief. Budgets, approvals, and card versus account payment
differ from portal to portal. They are portal settings, not
Kingaroy-wide answers. Kate will write a portal variations document
based on what has been done for OzWear. It describes platform options
every client gets (scope §5.3, §7.6–7.8), so its long-term home is the
platform repo.

## D5 — 2026-09-28 — Mail

**Plan (Kate).** New mail setup on the new domain, likely Microsoft 365.
Portal notifications (order confirmations and similar) send through a
separate transactional email service, with SPF/DKIM/DMARC on the same
domain set up to work alongside Microsoft 365.

## D6 — 2026-09-28 — Customer list comes from Xero

Kingaroy supplies childcare, council and schools. The list of
organisations will come from a Xero customer export. Only the business
name, type and site count go into this repo. Contact people's names,
emails and phones stay out (minimum personal information).

## D7 — 2026-09-28 — Platform renamed; scope has its own home

**Decision (Kate).** The platform is called the **Unified Uniform Portal**
for now (working name), replacing "OzWear Master Portal Platform" /
"Choice Master Portal", which was only a starting title. The scope is
saved in its own repo, `unified-uniform-portal` (docs/SCOPE.md and a
.docx), which becomes the platform repo when the build starts. The
portal options brief moved there too. D3 still stands: no platform code
exists yet.

## D8 — 2026-09-28 — OzWear has no part in the platform; Kingaroy is its first client

**Decision (Kate).** OzWear has nothing to do with the Unified Uniform
Portal. The platform scope (unified-uniform-portal/docs/SCOPE.md) was
rewritten with every OzWear mention removed and Kingaroy as the first
client. Because Kingaroy has no existing portals, the scope's migration,
WordPress and rollback sections were replaced by onboarding (§11) and
launch and fallback (§15.4). The separation rules in this repo still
apply: they are about Kingaroy's own accounts, domain and brand.

A review page for Kingaroy (unified-uniform-portal/review/) collects
section-by-section feedback by email.
