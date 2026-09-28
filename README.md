# kingaroy-portal-config

Configuration, branding, catalogue data, users to invite, domain plan and
go-live steps for **Kingaroy** (working name) as the first client on the
**Unified Uniform Portal** platform (working name; formerly "Choice Master Portal").

This repo contains **no application code**. The portal is not a separate
application: Kingaroy is a Client record (scope §5.1) on the shared
platform, and everything here is data the platform reads.

## What's here

| Path | What it is |
|---|---|
| `choice.json` | Build record read by the Choice Hub. Secret names only. |
| `HANDOVER.md` | For someone who has never seen this repo. |
| `.env.example` | Names of Kingaroy's per-client connections, values blank. |
| `docs/DECISIONS.md` | Decisions, newest last. |
| `docs/REMAINING.md` | What isn't finished, and go-live steps in order. |
| `docs/PORTAL-OPTIONS.md` | Pointer: the portal options brief now lives in the platform repo. |
| `docs/PLATFORM-GAPS.md` | Things Kingaroy needs that the platform can't do by configuration. |
| `docs/ONBOARDING-LOG.md` | Every onboarding step that needed a developer. |
| `docs/branding/` | Name shortlist, trade-mark and domain checks. |
| `docs/client-forms/` | Forms the client fills in. |
| `brand/` | Brand assets, once the name is decided (not created yet). |

## Why it is set up this way

**A client, not a build.** Choice keeps the IP in the platform and offers
it as a service. If Kingaroy needs something configuration can't do, it's
written up as a platform gap and built for every client. Nothing named
"Kingaroy" goes into platform code; terminology, stages, suppliers and
branding are data (scope §5.3).

**Separation from OzWear.** ozwear.com.au is being sold and Kingaroy is
separating from OzWear; the separation is confirmed with the seller.
Kingaroy therefore has its own Client record, suppliers, production
stages, payment gateway and merchant account, Xero organisation, sending
domain, hub branding and user accounts. Nothing is shared with the OzWear
client, and tenant isolation between the two is tested in the platform's
suite.

**A rebrand that stands on its own.** The new brand doesn't use or lean on
"OzWear" anywhere (DECISIONS.md D1). "Kingaroy" is a working name until
the branding workstream settles the real one.

**A temporary domain first.** kingaroy.ozwear.com.au goes with the sale.
A temporary domain, registered to the Kingaroy entity, carries the portal
until the final domain exists, with its end date and swap plan in
docs/REMAINING.md.

**Pilot for onboarding.** Kingaroy has no existing portals, so there is no
migration. It is the first client onboarded from scratch, and the
onboarding log feeds the platform's self-serve onboarding.

**Nothing registered from here.** Domains, DNS, gateway, Xero, secrets and
publishing happen from the Hub side after review. The legal entity and
ABN (D2) must be settled first.
