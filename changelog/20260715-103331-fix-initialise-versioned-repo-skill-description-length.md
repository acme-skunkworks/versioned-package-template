---
title: Trim the initialise-versioned-repo skill description under the 1024-byte limit
release_note: Shorten the initialise-versioned-repo skill description so skill-aware editors no longer warn about its length.
version:
created_at: '2026-07-15T10:33:31Z'
merged_at: '2026-07-15T11:09:15Z'
branch: fix-initialise-versioned-repo-skill-description
pr: 14
commit: 7c9f94b
merge_strategy:
author: hello@robeasthope.com
co_authors: []
category: fix
breaking: false
issues: []
stats:
  files_changed: 5
  loc_added: 58
  loc_removed: 30
---

## Fixed

- Trimmed the `initialise-versioned-repo` skill's `description` frontmatter from
  1114 bytes to 993 bytes so it clears the 1024-byte skill-description limit. Skill
  loaders (e.g. the Zed editor) warn that over-long descriptions consume extra
  model-context tokens; the template seeded every spawned repo with the over-limit
  description, so each inherited the warning. The rewrite keeps the same meaning and
  trigger phrasing — just tighter wording (dropped filler, folded the ruleset list,
  condensed the "Use right after…" clause). Applied in lockstep to both the
  `.claude/skills/` copy and the `.agents/skills/` Cursor mirror, and the skill's
  `package.json` + `SKILL.md` `metadata.version` are bumped `0.1.0` → `0.1.1`.
