# wrldai-legal

Public legal pages for WrldAI tools, hosted on GitHub Pages.

This repository is **public by design** and contains nothing but published
legal text. No source code, no credentials, no client data.

## Pages

Base URL: `https://mikeexit.github.io/wrldai-legal/`

| Page | URL | Used by |
|---|---|---|
| `legal.html` | `…/legal.html` | Human index of every policy below |
| `index.html` | `…/` | **EXIT**'s Meta app + LinkedIn app → **Privacy Policy URL**. This URL is already submitted to Meta, so it stays put; LinkedIn coverage was folded into it rather than opening a second page for the same product. |
| `juice/index.html` | `…/juice/` | JUICE OS's Meta app + LinkedIn app → **Privacy Policy URL** |
| `wrldai/index.html` | `…/wrldai/` | WrldAI's Meta app + LinkedIn app → **Privacy Policy URL** |

One policy per product, each covering both Instagram and LinkedIn for that
product's own accounts. A separate repository per app is **not** required:
platforms need a reachable URL, not a dedicated repo, and one repo with one
page per product is less to keep in sync.

## What these pages must keep saying

Each policy describes a **private internal publishing tool** — no end users
but the account owner, no data about anyone else, tokens held only in a local
environment file, and nothing published without a recorded human approval.
Two disclosures matter and must not be dropped:

- **Images become public.** Instagram publishes stills only from a publicly
  fetchable URL, so images are uploaded to a public assets repo first. The
  policies say so plainly.
- **Each product's own product is out of scope.** The EXIT *mobile app* has
  its own users and its own separate privacy policy
  (`ExitAppModern/docs/privacy-policy.md`); these pages cover only the
  publishing tool and must not be confused with it.

If what the tool accesses or stores changes, update the affected page and the
date at its top.

## Why this is a separate repository

The privacy-policy URL must be publicly reachable by the platform's crawler
(no login, not robots-blocked). The `wrldai` repository cannot be made public —
it holds client-confidential material — so the published pages live here
instead, and nothing sensitive is ever exposed to satisfy a platform
requirement.

**Social media assets do NOT belong here.** Published images host in
`mikeExit/wrldai-social-assets`, one folder per product. This repo is legal
text only; the separation is enforced in code
(`wrldai/orchestrator/media/hosting.py` refuses this repo as a host).

## Enabling Pages

Settings → Pages → Source: *Deploy from a branch* → Branch: `main`, folder
`/ (root)` → Save. The URL is live within a minute or two.
