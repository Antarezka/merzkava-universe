# SAFE VERSION — Merzkava Universe

## Known-good rollback baseline

- **Label:** SAFE VERSION v4.0.10
- **Preserved rollback branch:** `SAFE-VERSION-v4.0.10`
- **Pinned commit:** `429a48b75cc290e7b720689d38a84eacbff438d9`
- **Short hash:** `429a48b`
- **Version:** `Nightly-v4.0.10` (the verified version associated with this snapshot)
- **Purpose:** Preserve the exact repository state accepted as the known-good RP baseline before future changes.

## Recovery rule

If a future change causes a critical regression, do not rebuild the system from memory and do not immediately overwrite the current default branch.

1. Stop further edits and identify the last known-good state.
2. Open the protected branch [SAFE-VERSION-v4.0.10](https://github.com/Antarezka/merzkava-universe/tree/SAFE-VERSION-v4.0.10) or the exact pinned commit above.
3. Compare the broken state against this baseline before changing anything.
4. Restore only from this verified snapshot. Prefer a revert or a recovery branch first; do not force-push or delete current history as the first response.
5. Verify the required bootstrap, authority order, gameplay response template, character profile template, narrative dynamics, player state, world routers, core mechanics, and version file against the baseline.
6. Update the README pin only after the chosen recovery state has been verified.

## Baseline authority and protected structure

This snapshot preserves the repository structure and routing as they existed at the pinned commit. Treat that structure as the recovery reference, including:

- `INDEX.md` — mandatory bootstrap and source router.
- `templates/AUTHORITY_ORDER.md` — source precedence and GM authority.
- `templates/GAMEPLAY_RESPONSE_TEMPLATE.md` — canonical gameplay output, visual panels, ledger, and validation.
- `templates/CHARACTER_PROFILE_TEMPLATE.md` — character fields and defaults.
- `templates/NARRATIVE_DYNAMICS.md` — narrative density, Merzkava context, social dynamics, and NPC behavior.
- `players.md` and `players/<Nama>.md` — player registry and character state.
- `world/DYNAMIC_EVENTS.md`, `world/WORLD_NAVIGATION_TREE.md`, `world/CANON_LOAD_ROUTER.md`, and `world/CANON_DECISIONS_AND_PRECEDENCE.md` — persistent events, world navigation, canon loading, and precedence.
- Canon modules under `core/` and `world/` as routed by `INDEX.md`.
- `NIGHTLY_VERSION.md` — authoritative Nightly version for the pinned snapshot.

The repository's own `INDEX.md` and authority hierarchy determine the exact modules required for a given action. This list is a recovery checklist, not a replacement for the canonical router.

## Preservation policy

- Keep this branch unchanged as a recovery point. It is preserved by repository workflow; GitHub branch-protection enforcement is not enabled on this branch.
- Do not use it as the development branch.
- Do not move its branch pointer to a newer commit.
- Do not delete it while it is the designated Safe Version.
- Future Safe Versions should use a new branch name and a new verified snapshot; retain this one until the replacement is confirmed.

**Status:** Known-good snapshot preserved. This record documents the rollback procedure; it does not claim that a future restore has already been tested.
