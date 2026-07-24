# wrldai-legal

Public legal pages for WrldAI tools, hosted on GitHub Pages.

This repository is **public by design** and contains nothing but published
legal text. No source code, no credentials, no client data.

| Page | URL | Used by |
|---|---|---|
| `index.html` | `https://<user>.github.io/wrldai-legal/` | Meta app → App Settings → Basic → **Privacy Policy URL** |

## Why this is a separate repository

The privacy-policy URL must be publicly reachable by Meta's crawler (no login,
not robots-blocked). The `wrldai` repository cannot be made public — it holds
client-confidential material — so the published pages live here instead, and
nothing sensitive is ever exposed to satisfy a platform requirement.

## Source of truth

`index.html` is the published rendering of
`wrldai/docs/instagram-publisher-privacy.md`. Edit the markdown in `wrldai`
first, then mirror the change here so the two cannot drift.

## Enabling Pages

Settings → Pages → Source: *Deploy from a branch* → Branch: `main`, folder
`/ (root)` → Save. The URL is live within a minute or two.
