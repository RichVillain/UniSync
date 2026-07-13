# Provenance

The planning documents in `docs/` (`CONSOLIDATION.md`, `QUICK_REFERENCE.md`) originated inside the
[`RichVillain/Ndrap-platform`](https://github.com/RichVillain/Ndrap-platform) monorepo:

- Authored 2026-07-12 on branch `claude/uploads-batches-eisenhower-gzlel7`
- Committed to `Ndrap-platform` `main` as `docs/UNISYNC_CONSOLIDATION.md`, `docs/UNISYNC_QUICK_REFERENCE.md`,
  and `docs/UNISYNC_LOCAL_FILES_INDEX.md` in commit `12cbd71ae57685efbd85d0dbb50eb4c82723b967`

`Ndrap-platform`'s own archive notes (`reference/ndrap-eco-v2/ECO_V2_README.md`) already state that UniSync
"is its own project, not part of the NDrap ecosystem archive." This repository is that separation made real:
the UniSync-specific context and planning content has been moved here, and the corresponding files were
removed from `Ndrap-platform` on branch `claude/unisync-context-data-migration-n96d5w`.

## What changed on extraction

- Repository-relative paths were rebased: anything that pointed at `services/engine/unisync/...` inside the
  monorepo now points at `services/engine/...` here, since this whole repository *is* UniSync.
- `docs/UNISYNC_LOCAL_FILES_INDEX.md` was **not** copied verbatim — it was primarily a file index of
  `Ndrap-platform`'s own (unrelated) directory tree. The UniSync-relevant parts of it are folded into this
  file and into `docs/QUICK_REFERENCE.md`.
- References to `Ndrap-platform`'s governance doc (`docs/CANON.md`) were kept as historical context rather
  than as a live dependency — this repository will grow its own governance doc as needed.
- No source material (the five uploaded PDFs/docx) has been committed to either repository yet. Extracting
  their content into `docs/MATH_SPEC.md`, `docs/VISION.md`, and the calculator implementations is still
  Sprint 1 of `docs/CONSOLIDATION.md`.
