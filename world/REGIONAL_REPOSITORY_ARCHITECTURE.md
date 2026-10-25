# Merzkava Universe — Three-Power Repository Architecture

## Purpose

Use one central hub and **exactly three canonical regional repositories**, one for each major power. This follows the navigation pattern used by `inggo-alvn/Core`: a central index points to a regional index, which points to local geography, settlement records, NPC registries, and canonical NPC profiles.

**“Region” here means a major power—not an individual province, valley, city, or village.** The three repository boundaries are:

1. **Golden Dragon Empire**
2. **Tianhai Yunzhou**
3. **Beiming Gu**

Do not create a fourth, separate global NPC repository or one repository per subregion.

## 1. Responsibility boundaries

### Central repository: `Antarezka/merzkava-universe`

The central repository owns:
- Global `INDEX.md` and links to the three major-power repositories.
- `templates/AUTHORITY_ORDER.md` and global GM/navigation procedures.
- Global world canon, shared mechanics, common templates, and cross-power rules.
- Cross-region references, global history/events, and rules that apply across multiple powers.
- Temporary legacy regional/NPC files until migration to the three regional repositories is complete and verified.

The central repository is the navigation hub, **not** the long-term home of detailed local NPC profiles after migration.

### Regional repository A: Golden Dragon Empire

Owns all established canon within the empire:
- Its seven established geographic regions and all lower-level administrative areas, settlements, villages, hamlets, districts, routes, and transit links.
- Empire governance, officials, regional administrations, public services, local economy/resources, factions, institutions, and locally grounded daily life.
- The empire's local NPC registry and canonical full profiles for its recurring/major NPCs.

### Regional repository B: Tianhai Yunzhou

Owns all established canon within Tianhai:
- Tianhai's geographic areas, floating settlements/cities, local districts, routes, and interregional transit terminals.
- Tianhai governance, academies, Thinker Institute, clans, services, local economy/resources, factions, and local life.
- Tianhai's local NPC registry and canonical full profiles for its recurring/major NPCs.

### Regional repository C: Beiming Gu

Owns all established canon within Beiming Gu:
- Beiming's established geographic areas, settlements, villages, routes, border connections, and local transit.
- Its governance, factions, institutions, local economy/resources, customs, and local life as established by canon.
- Beiming Gu's local NPC registry and canonical full profiles for its recurring/major NPCs.
- Lawless Territories are not automatically a fourth major-power repository. Keep their ownership under the agreed world structure; until the owner defines a separate repository, link/reference their current canon from the central index and do not silently assign them to Beiming Gu.

## 2. Standard layout inside each of the three repositories

Use this layout as a guide, not as a requirement to create empty files:

- `README.md` — identity, scope, and entry point.
- `INDEX.md` — local navigation and required loading order.
- `REGION_OVERVIEW.md` — overall geography, climate, identity, resources, and boundaries of the whole power.
- `regions/<Region_Name>.md` — a province/valley/subregion when it needs a separate file.
- `settlements/<Settlement_Name>.md` — a city, town, village, hamlet, or other settlement when it needs a separate file.
- `npcs/REGISTRY.md` — one local NPC registry, grouped by region/settlement and role.
- `npcs/<NPC_Name>.md` — one canonical full profile for each recurring/major NPC.
- `factions/<Faction_Name>.md` — organization record when its complexity warrants a separate file.
- `routes/ROUTE_NETWORK.md` — confirmed connections, travel modes, transfer points, and costs when route complexity warrants it.
- `institutions/<Institution_Name>.md` — complex institutions when needed.

Do not create empty files just to satisfy the tree. Simple content can remain in the overview or local index until complexity justifies a separate module. Preserve established file names and canon during migration unless renaming is safe and all references are updated.

## 3. NPC ownership and continuity

1. Each power repository owns one regional NPC registry, grouped by subregion/settlement and meaningful role.
2. A recurring or major NPC has exactly one canonical full profile, stored in the repository of their established primary home or affiliation.
3. Regional overview, settlement, faction, and institution files link to the canonical profile; they do not duplicate the biography.
4. An NPC's temporary location change does not automatically transfer their profile to another repository. Keep canonical ownership stable unless the owner approves a transfer.
5. A cross-power NPC keeps one canonical profile in the agreed home repository; other repositories link to it and record only relevant local presence or assignments.
6. Background and temporary scene NPCs do not require permanent profiles unless they become recurring or materially important.
7. Keep public knowledge, NPC knowledge, beliefs, player-character knowledge, and GM-only information distinct.

## 4. Mandatory navigation

For gameplay, lore questions, audits, or repository edits:

1. Read the central `INDEX.md` and `templates/AUTHORITY_ORDER.md`.
2. Identify which of the **three major powers** owns the location. A subregion name determines a file inside that power's repository, not a separate repository.
3. Open the verified repository link for that power from the central index.
4. Read the regional `INDEX.md` (or `README.md` if no regional index exists) and follow its local loading order.
5. Read the relevant subregion/settlement file and that power's NPC registry.
6. Open only the canonical NPC profiles and faction/institution records relevant to the current scene.
7. For travel, verify origin, destination, intermediate transfers, transport type, and cost in the route network and shared travel rules.
8. If a repository link is missing or inaccessible, state the exact gap and use central legacy files only as temporary fallback. Never guess a URL or claim to have fetched inaccessible data.

Do not fetch every NPC profile for an ordinary scene. Load all relevant regional registries for a complete roster audit or migration.

## 5. Migration state and safety

The desired structure is three regional repositories, but **a design document does not itself create those repositories or migrate files**.

Until each destination repository URL and contents are verified:
- Treat existing `world/REGION_*.md`, `world/NPC_*.md`, and region-specific governance/institution files in the central repo as legacy canon.
- Do not delete, overwrite, or claim those files have been moved.
- Do not invent destination URLs.
- Do not claim the three-repository separation is complete.

For each power, migration must be performed and checked as one coherent set:
1. Create/verify that power's repository and its local `INDEX.md`.
2. Migrate the relevant geographic, settlement, route, governance, faction, institution, and NPC files without losing established content.
3. Build/check the local NPC registry and ensure each major/recurring NPC has one canonical full profile.
4. Update internal links and confirm the destination files can be fetched.
5. Add the verified repository URL to the central `INDEX.md` and Authority Order route.
6. Only then mark that power migrated. Remove a central legacy duplicate only after the owner-approved destination and every dependent link are verified.

## 6. Registry row format

Use one row per individual:

| Public name / identity | Current or last-confirmed location | Role | Affiliation | Public traits / goal | Canonical profile | Status |
|---|---|---|---|---|---|---|
| Not established | Not established | Not established | Not established | Not established | Link to canonical profile | Not established |

This is a format template, not a claim that any NPC exists. All entries must be grounded in established canon.
