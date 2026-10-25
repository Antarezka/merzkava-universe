# Merzkava Universe — In-Repository Regional Architecture

## Purpose

This document defines how to organize the three major powers **inside the existing repository** `Antarezka/merzkava-universe`. It does not call for creating separate GitHub repositories or migrating content outside this repository.

The three major powers, named exactly as established by `world/WORLD.md`, are:
1. **Golden Dragon Empire**
2. **Tianhai Yunzhou**
3. **Beiming Gu**

These are world/canon ownership boundaries represented by directories and modules—not GitHub repository boundaries.

## 1. One repository, clear source ownership

The single official repository is `Antarezka/merzkava-universe`.

- `INDEX.md` is the global entry point and mandatory bootstrap/navigation index.
- `templates/AUTHORITY_ORDER.md` defines GM behavior and procedure.
- `world/` contains global canon and cross-power modules: world foundations, history, geography, route networks, events, factions, social structures, and government/institution modules whose scope is defined by their content.
- `regions/golden-dragon-empire/` contains regional navigation and detailed canon specific to Golden Dragon Empire.
- `regions/tianhai-yunzhou/` contains regional navigation and detailed canon specific to Tianhai Yunzhou.
- `regions/beiming-gu/` contains regional navigation and detailed canon specific to Beiming Gu.
- `core/`, `gameplay/`, `bestiary/`, `templates/`, and `players/` retain their existing global/system responsibilities.

Do not create external regional repositories, a separate global NPC repository, or a separate repository for any province, valley, city, village, academy, institution, or faction. Do not move global rules into a regional folder just because the rules mention a region. Follow canon scope and the existing INDEX.

Lawless Territories are not automatically a fourth major power or automatically part of Beiming Gu. Follow the established world structure and current canon.

## 2. Regional directory layout

Keep regional content under the existing `regions/` directory. The established naming pattern is:

- `regions/<power>/INDEX.md` — local navigation and loading order.
- `regions/<power>/npcs/REGISTRY.md` — roster index for that power.
- `regions/<power>/npcs/<NPC_NAME>.md` — canonical detailed profiles for established recurring/major NPCs.

Add further folders or modules for settlements, routes, institutions, factions, governance, local services, and economy **inside the relevant power directory only when the canon and amount of detail warrant it**. Avoid creating empty files or splitting simple content into unnecessary modules. Preserve established names and content unless a deliberate, fully cross-referenced revision is needed.

Global or cross-power material remains under its current global `world/` or system path. If a world module contains regional information, do not duplicate or relocate it blindly: check its scope, dependencies, and canonical authority first.

## 3. NPC organization

Each NPC has one canonical detailed profile. Store regional NPC profiles under `regions/<power>/npcs/` according to established origin or canonical affiliation. Do not create a fourth NPC repository.

- `npcs/REGISTRY.md` is the region-wide navigation list.
- Location, settlement, faction, and institution modules may include short NPC tables for immediate scene context.
- Tables and registry rows link to the same canonical profile; they must agree on identity, role, affiliation, and last confirmed status.
- Do not invent unknown ages, tiers, techniques, affiliations, motives, or other canon to fill a table.
- Inspect each legacy `world/NPC_*.md` file before deciding whether it is still a source, a duplicate, or a compatibility pointer. Never delete it merely because a similarly named regional profile exists.

For Beiming Gu, `regions/beiming-gu/npcs/REGISTRY.md` records 21 canonical profiles: Beiming Han, Beiming Xenhwa, Beiming Jingheng, Beiming Nerva, 12 clan heads, and 5 dojo masters. Keep that registry and its profile links synchronized.

## 4. Mandatory navigation and source loading

For gameplay, lore questions, audits, and repository edits:

1. Read the central `INDEX.md` and `templates/AUTHORITY_ORDER.md`.
2. Identify the major power responsible for the location or subject.
3. Read the appropriate regional `INDEX.md` inside this same repository.
4. Follow its local loading order and read the relevant geography, settlement, route, institution, faction, governance, and/or economy modules.
5. Use the regional NPC registry for roster checks; open only the canonical NPC profiles relevant to the scene unless conducting a complete audit.
6. For travel, verify the origin, destination, intermediate transfers, transport type, and cost against route modules and shared travel rules.
7. Read global modules when they govern the subject or span multiple powers.
8. If a required file cannot be fetched, state the exact gap. Never claim to have read inaccessible content.

Do not fetch every NPC profile for an ordinary scene. Load the complete relevant module set and registries for a comprehensive audit.

## 5. Repository maintenance and safety

All regional restructuring and canon maintenance happens in the existing `Antarezka/merzkava-universe` repository.

- Do not create, request, or migrate to separate regional GitHub repositories.
- Do not invent external repository URLs or change the canonical repository URL.
- Do not delete or overwrite a source module until its content, dependencies, and replacement have been inspected and verified.
- When moving content between folders within this repo, preserve canon and update every affected index, relative link, registry, and cross-reference in the same maintenance pass.
- Mark a change complete only after verifying the resulting files and links on the repository's actual default branch.
- Keep regional scaffolds explicitly incomplete where the canon is not established. Missing settlements, routes, administration, prices, customs, or NPCs are unconfirmed—not an invitation to invent permanent canon.

## 6. NPC registry row format

Use one row per individual when a registry needs a table:

| Public name / identity | Current or last-confirmed location | Role | Affiliation | Public traits / goal | Canonical profile/source | Status |
|---|---|---|---|---|---|---|
| Not established | Not established | Not established | Not established | Not established | Link to canon source if one exists | Not established |

This is a format template, not a claim that an NPC exists. Every entry must be grounded in established canon.
