---
title: "Rewrite repo identity and docs for the deploy-target archetype"
release_note: null
version:
created_at: "2026-07-13T15:07:11Z"
merged_at:
branch: "a-941-docs-rewrite-repo-identity-docs-for-the-deploy-target"
pr:
commit:
merge_strategy:
author: "hello@robeasthope.com"
co_authors: []
category: docs
breaking: false
issues: ["A-941"]
stats:
  files_changed:
  loc_added:
  loc_removed:
---

## Changed

- Pointed the template's identity and docs at the versioned, non-npm
  **deploy-target** archetype instead of the npm-package one ([A-941](https://linear.app/acme-skunkworks/issue/A-941)).
- `infrastructure/repo-config.yaml`: dropped `npmScope` / `npmRegistryUrl` /
  `githubPackagesRegistryUrl`; kept only `defaultBranch` + `nodeVersionFile`.
- `package.json`: renamed to `@acme-skunkworks/versioned-package-template` and
  pointed `homepage` / `bugs` / `repository` at the `versioned-package-template`
  repo.
- `README.md` + `CLAUDE.md`: reframed as the fourth archetype (release-please →
  git tags + GitHub Releases, no publish); replaced the Release workflow section
  with the deploy-target model (the orchestrator cuts the tag + Release; there is
  no in-repo release/publish workflow); documented the in-repo
  `changelog-enrich.yml` (`mode: enrich`) leg; and referenced the
  `initialise-versioned-repo` skill ([A-946](https://linear.app/acme-skunkworks/issue/A-946)).

## Removed

- Deleted the npm-specific documentation: the npm-OIDC Trusted Publishing,
  `npm-release` environment, "Enable the Release workflow", "Bootstrap publish",
  and "Manual publish" sections, plus the `pkg-release.yml` / `act:release:dry`
  references throughout.

## Fixed

- Corrected the `GO/NO GO` required-check ruleset guidance to require the
  **road-runner-bot bypass** ([A-944](https://linear.app/acme-skunkworks/issue/A-944)): the in-repo `changelog-enrich.yml` pushes
  `changelog/**` directly to `main` as `road-runner-bot[bot]`, which the required
  check would otherwise reject. Human PRs still have to satisfy `GO/NO GO`.
