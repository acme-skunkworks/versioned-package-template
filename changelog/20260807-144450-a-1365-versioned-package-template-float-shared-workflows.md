---
title: Float changelog-enrich shared-workflows pin to @v1
release_note: ''
version:
created_at: '2026-08-07T14:44:50Z'
merged_at:
branch: a-1365-versioned-package-template-float-shared-workflows-sha-pins
pr:
commit:
merge_strategy:
author: rob@acmeskunkworks.io
co_authors: []
category: chore
breaking: false
issues:
  - A-1365
stats:
  files_changed:
  loc_added:
  loc_removed:
  commits:
---

## Changed

- Float `.github/workflows/changelog-enrich.yml` reusable caller from the [A-821](https://linear.app/rheged-studio/issue/A-821)
  merge SHA pin to `acme-skunkworks/shared-workflows/.github/workflows/reusable-changelog-enrich.yml@v1`
  ([A-1365](https://linear.app/rheged-studio/issue/A-1365)), matching the
  `octavo` / `shared-workflows` exemplars now that `@v1` includes the enrich
  workflow.
