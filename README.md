# MailChimp Transactional — Demo Docs

A complete Mintlify documentation site for a mock "MailChimp Transactional" API,
built as a demo surface for the Mintlify Enterprise AE on-site.

The point: show docs auto-generating from an OpenAPI spec, with a hand-written guide
layer on top — the exact hybrid story for the MailChimp account.

## What's inside

```
docs.json                 Site config (theme, nav, colors, OpenAPI hookup)
openapi.json              OpenAPI 3.1 spec — drives the auto-generated reference + playground
introduction.mdx          Landing page
quickstart.mdx            5-minute send walkthrough (cURL / Node / Python)
authentication.mdx        API key auth
essentials/sending.mdx    Sync vs async, scheduling, tracking
essentials/webhooks.mdx   Event types + signature verification
essentials/versioning.mdx Versioning + release-cadence story (the demo money page)
api-reference/introduction.mdx   Reference landing; "regenerates from the spec"
logo/, favicon.svg        Branding assets
```

## Run it locally (preview before the demo)

Requires Node.js v20.17.0+ (use an LTS version).

```bash
npm i -g mint        # install the Mintlify CLI
mint dev             # run from this directory (where docs.json lives)
```

Open http://localhost:3000. The preview hot-reloads as you edit.

## Deploy a live, shareable site

1. Push this folder to a new GitHub repo.
2. Go to https://mintlify.com/start, sign in with GitHub, and select the repo.
3. Install the Mintlify GitHub App (Dashboard → Settings → GitHub App → select this repo only).
4. Push to the default branch — Mintlify auto-builds and deploys to
   `https://<your-project>.mintlify.app`.

## The live demo beat (what to actually show)

1. Open the **API Reference → Messages** section — point out it's generated
   entirely from `openapi.json`, including the interactive playground.
2. Edit one thing in `openapi.json` (e.g. add a property or a new endpoint),
   save, and show the reference + playground update with no manual page edits.
3. Open `essentials/versioning.mdx` — narrate the 3–4-releases-per-year story
   and how branch-based versioning maps to their release cadence.
4. Connect it back: "This is exactly the manual-docs liability you described —
   gone."
