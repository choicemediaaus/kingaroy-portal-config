# Handover — Kingaroy master portal (configuration)

Written 2026-09-28. Read this before touching anything. Written for a
person who has never seen this repo and has no access to any conversation
about it.

## What this is, in one paragraph

Kingaroy (working name) supplies uniforms to childcare, councils and
schools and is separating from OzWear. Its customer ordering portals will
run on the Unified Uniform Portal platform as the platform's first client.
This repo holds Kingaroy's configuration and data only: portal options,
branding, supplier and catalogue data, users to invite, the domain plan
and the go-live steps. It deliberately holds **no application code**, no
secrets and as little personal information as possible.

## Current state

The platform hasn't been started (docs/DECISIONS.md D3). Data is being
gathered as CSV/JSON/xlsx and will be mapped to the platform's import
format once that exists. The client is choosing a new name. The legal
entity and ABN are open (D2). See docs/REMAINING.md for the full list.

## Working in it

```bash
git clone https://github.com/choicemediaaus/kingaroy-portal-config.git
```

No build, no dependencies. Edit data and docs, commit to `main`. Before
every commit, check nothing that looks like a key or token is staged.

## What does not come from git

| Value | Where it comes from | Where it is kept |
|---|---|---|
| Payment gateway credentials | Kingaroy's own merchant account | Platform secret store; 1Password › Choice › Kingaroy |
| Xero connection | Kingaroy's own Xero organisation | Platform secret store; 1Password › Choice › Kingaroy |
| Transactional email key | Sending service on Kingaroy's domain | Platform secret store; 1Password › Choice › Kingaroy |

Names are in `.env.example`. Nothing with a value has ever been committed.

## Where it runs

On the Unified Uniform Portal platform, Sydney or Melbourne region (scope
§14), as its own Client record. Hosting, database and deploys are the
platform's; see its repo once it exists. Domain: temporary one not yet
chosen; see docs/REMAINING.md.

## Known limits and decisions

- Separation from OzWear is non-negotiable: nothing shared (README, "Why").
- The brand doesn't use "OzWear", "Oz" or a "-wear" suffix (D1).
- Budgets, approvals and card versus account payment are per portal (D4).
- Customer list comes from Xero, cut down to business name, type and site
  count (D6).
- Invite lists are deleted from the repo once users exist in the platform.

## Who to call

Choice (Kate, kate@choicemedia.com.au). The platform is built in-house by
Choice (scope §15.2).
