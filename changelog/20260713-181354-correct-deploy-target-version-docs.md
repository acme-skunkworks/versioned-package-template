---
title: Correct deploy-target changelog version-stamping docs
release_note:
version:
created_at: '2026-07-13T18:13:54Z'
merged_at: '2026-07-13T18:54:33Z'
branch: correct-deploy-target-version-docs
pr: 11
commit: ce9ac1f
merge_strategy:
author: hello@robeasthope.com
co_authors: []
category: docs
breaking: false
issues: []
stats:
  files_changed: 3
  loc_added: 41
  loc_removed: 8
---

## Changed

- Corrected the changelog docs in `CLAUDE.md` and `changelog/README.md`, which
  wrongly claimed a deploy target's `version` field is stamped at release and that
  the release-orchestrator sources its GitHub-Release notes from the version-stamped
  entries. Neither holds for this archetype: the in-repo `mode: enrich` path fills
  only `merged_at`/`commit`/`pr`/`stats` and never touches `version`, there is no
  `finalise` step, and the orchestrator's `kind: deploy` release-cut reads the
  version from `.release-please-manifest.json` and sources its notes from the
  release-please PR body. The `version` field is now documented as permanently blank
  on this deploy target — retained only for octavo-schema parity — and the
  release-notes source is pointed at the release-please PR body.
