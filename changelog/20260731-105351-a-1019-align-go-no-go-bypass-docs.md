---
title: "Align GO/NO GO bypass docs with npm template parity (A-1019)"
release_note:
version:
created_at: "2026-07-31T10:53:51Z"
merged_at:
branch: "a-1019-harden-parent-package-templates-so-the-release-bootstrap"
pr:
commit:
author: "rob@acmeskunkworks.io"
co_authors: []
category: docs
breaking: false
issues: ["A-1019"]
stats:
  files_changed:
  loc_added:
  loc_removed:
---

## Changed

- Dropped stale "npm-package template has no bot bypass" wording from README /
  CLAUDE.md / init-skill comments. Deploy targets already provision road-runner-bot
  on GO/NO GO (A-944); npm packages now need the same enricher bypass
  ([A-1019](https://linear.app/acme-skunkworks/issue/A-1019)) — documented as
  estate-wide rather than deploy-target-only.
