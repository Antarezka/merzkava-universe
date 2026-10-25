# Merzkava Universe — Three-Power Repository Architecture

## Purpose

Use one central hub and **exactly three canonical regional repositories**, one for each major power. The navigation pattern is inspired by a repository: central INDEX → the correct regional module → local geography/settlement and NPC table → detailed NPC profile only when needed.

**“Region” here means a major power—not an individual province, valley, city, or village.** The three repository boundaries are exactly the names established by `world/WORLD.md`:

1. **Golden Dragon Empire**
2. **Tianhai Yunzhou**
3. **Beiming Gu**

Do not create a fourth global NPC repository or one repository per subregion. Do not invent regional repository URLs.

## 1. Responsibility boundaries

### Central repository: `Antarezka/merzkava-universe`

The central repository owns:
- Global `INDEX.md` and verified links to the three major-power repositories.
- `templates/AUTHORITY_ORDER.md` and global GM/navigation procedures.
- Global world canon, shared mechanics, common templates, and cross-power rules.
- Cross-region references, global history/events, and rules that apply across multiple powers.
- Temporary legacy regional files, plus compatibility pointers at old `world/NPC_*.md` paths. Canonical named NPC profiles have been staged under `regions/<power>/npcs/`; these folders remain inside the central repo until separate regional repositories are created and verified.

The central repository is the navigation hub, not the long-term home of detailed local NPC profiles after migration.

### Golden Dragon Empire repository

Owns all established canon within the Golden Dragon Empire: its established geographic regions and lower-level administrative areas; settlements, villages, routes, transit links; governance and officials; public services; local economy/resources; factions and institutions; and local NPC tables/registry plus canonical detailed profiles.

### Tianhai Yunzhou repository

Owns all established canon within Tianhai Yunzhou: geographic areas, floating settlements/cities, districts, routes and interregional transit terminals; governance, academies, Thinker Institute, clans, services, local economy/resources, factions and institutions; and local NPC tables/registry plus canonical detailed profiles.

### Beiming Gu repository

Owns all established canon within Beiming Gu: established geographic areas, settlements, villages, routes, border connections and local transit; governance, factions, institutions, economy/resources, customs and local life; and local NPC tables/registry plus canonical detailed profiles.

Lawless Territories are not automatically a fourth major-power repository or automatically part of Beiming Gu. Keep their ownership under the agreed world structure and reference current canon from the central index until the owner establishes otherwise.

## 2. Standard layout inside each regional repository

Use this as a guide; do not create empty files just to satisfy the tree.

- `README.md` — identity, scope, and entry point.
- `INDEX.md` — local navigation and required loading order.
- `REGION_OVERVIEW.md` — geography, climate, identity, resources, and boundaries of the whole power.
- `regions/<Region_Name>.md` — a subregion when it needs a separate file.
- `settlements/<Settlement_Name>.md` — a city, town, village, hamlet, or other settlement when it needs a separate file.
- `npcs/REGISTRY.md` — local directory grouped by region/settlement and role; one row per important/recurring NPC.
- `npcs/<NPC_Name>.md` — one detailed canonical profile for a recurring/major NPC when persistent continuity needs it.
- `factions/<Faction_Name>.md` — organization record when its complexity warrants a separate file.
- `routes/ROUTE_NETWORK.md` — confirmed connections, travel modes, transfer points, and costs when route complexity warrants it.
- `institutions/<Institution_Name>.md` — complex institutions when needed.

Do not split simple content into unnecessary files. Preserve established file names and canon during migration unless renaming is safe and all references are updated.

## 3. NPC organization — mirror the useful part of the approach

The local location/settlement module should contain NPC tables **beside the place or organization they belong to**, not in an unrelated global list. Group entries under the appropriate city, village, institution, faction, or other established location. Use the existing canon and avoid filling tables with invented characters.

A local NPC table is a short locator/summary. Recommended columns are public identity, role, age (if known), official capability/tier (if known), signature technique/approach, public traits/behavior, and a canonical source/profile link. Adjust fields to fit the character; do not invent a cultivation tier or technique for a non-cultivator.

Use a detailed NPC profile only when the character is recurring or major and needs persistent continuity. Every detailed profile has one canonical home. Local NPC tables, registry rows, settlement modules, faction modules, and institution modules link to that profile instead of duplicating the biography.

The registry is the region-wide navigation list; the tables embedded beside locations provide the immediate context for scenes. Both must point to the same canonical profile and agree on identity, role, affiliation, and last confirmed status.

## 4. Mandatory navigation

For gameplay, lore questions, audits, or repository edits:

1. Read the central `INDEX.md` and `templates/AUTHORITY_ORDER.md`.
2. Identify which of the three major powers owns the location. A subregion name determines a file inside that power's repository, not a separate repository.
3. Open the verified repository link for that power from the central index.
4. Read its `INDEX.md` and follow its local loading order.
5. Read the relevant subregion/settlement module and its local NPC table; consult `npcs/REGISTRY.md` for a broader roster audit.
6. Open only the canonical NPC profiles and faction/institution records relevant to the scene.
7. For travel, verify origin, destination, intermediate transfers, transport type, and cost in the route network and shared travel rules.
8. If a repository link is missing or inaccessible, state the exact gap and use central legacy files only as temporary fallback. Never guess a URL or claim to have fetched inaccessible data.

Do not fetch every NPC profile for an ordinary scene. Load all relevant regional modules and registries for a complete roster audit or migration.

## 5. Migration state and safety

A design document does not itself create regional repositories or migrate files.

Until each destination repository URL and its contents are verified:
- Treat existing `world/REGION_*.md` and region-specific governance/institution files in the central repo as regional canon still awaiting repository migration.
- Canonical named NPC profiles are staged under `regions/golden-dragon-empire/npcs/`, `regions/tianhai-yunzhou/npcs/`, and `regions/beiming-gu/npcs/`; the Beiming Gu profiles cover Beiming Han, Beiming Xenhwa, and Beiming Jingheng. Verify each old `world/NPC_*.md` file before treating it as a compatibility pointer.
- Do not delete or overwrite the regional source modules, invent destination URLs, or claim the three-repository separation is complete.
- The current in-repo staging step is not a substitute for creating and verifying the three destination repositories.

For each power, migrate and verify one coherent set:
1. Create/verify that power's repository and local `INDEX.md`.
2. Migrate the relevant geography, settlement, NPC tables, routes, governance, faction, institution, and NPC profile data without losing established content.
3. Build/check the local NPC registry and ensure each recurring/major NPC has one canonical detailed profile where needed.
4. Check local tables, registry rows, profile links, and authoritative rosters for conflicts and duplicates.
5. Update internal links and confirm destination files can be fetched.
6. Add the verified repository URL to the central `INDEX.md` and Authority Order route.
7. Only then mark that power migrated. Remove central legacy duplicates only after the owner-approved destination and every dependent link are verified.

## 6. Registry row format

Use one row per individual:

| Public name / identity | Current or last-confirmed location | Role | Affiliation | Public traits / goal | Canonical profile/source | Status |
|---|---|---|---|---|---|---|
| Not established | Not established | Not established | Not established | Not established | Link to canon source if one exists | Not established |

This is a format template, not a claim that any NPC exists. Every entry must be grounded in established canon.
