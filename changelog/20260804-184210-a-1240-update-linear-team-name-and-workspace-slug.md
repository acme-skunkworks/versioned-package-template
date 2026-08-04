---
title: Update Linear team name and workspace slug
release_note: ""
version:
created_at: "2026-08-04T18:42:10Z"
merged_at:
branch: a-1240-versioned-package-template-update-linearteamname
pr:
commit:
author: rob@acmeskunkworks.io
co_authors: []
category: chore
breaking: false
issues:
  - A-1240
stats:
  files_changed:
  loc_added:
  loc_removed:
---

## Changed

**Point Linear identity at Rheged Studio ([A-1240](https://linear.app/rheged-studio/issue/A-1240))**

- `config.json` — `linearWorkspaceSlug` `acme-skunkworks` → `rheged-studio` (skill configs are gitignored and updated locally via initialise `--set`)
- 14 changelog entries — rewrite committed `linear.app/acme-skunkworks` URLs to `linear.app/rheged-studio`
