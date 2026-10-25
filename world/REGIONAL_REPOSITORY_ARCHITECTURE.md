# Merzkava Universe — Regional Repository Architecture

**Purpose:** Keep the central repository as the world-wide navigation hub while each major region owns its detailed local canon and NPC records. This follows a hub-and-spoke navigation pattern: one global index, region-specific sources, and explicit links instead of duplicated biographies.

## 1. Responsibility boundaries

### Central repository: `Antarezka/merzkava-universe`

The central repository owns:
- `INDEX.md`: global entry point, repository directory, and mandatory loading route.
- `templates/AUTHORITY_ORDER.md`: mandatory GM procedure, source precedence, and rules for following the route.
- Global world canon and mechanics that apply across multiple regions.
- The regional repository directory and cross-region navigation rules.

The central repository must not become a second, competing copy of the detailed NPC roster maintained by a regional repository after that region has been migrated.

### Each regional repository

A regional repository is the canonical source for that region's detailed local content:
- Regional overview, geography, settlements, local life, resources, economy, and confirmed route connections.
- Local NPC registry, grouped by settlement or meaningful subregion.
- One canonical full profile for each recurring or major NPC whose primary home/assignment belongs to that region.
- Region-specific government, factions, institutions, services, and local event references as needed.
- Links to global mechanics and cross-region canon in the central repository, rather than copied rulebooks.

## 2. Standard regional repository layout

Use these paths consistently where applicable:

- `README.md` — region identity, scope, and entry points.
- `INDEX.md` — region-local navigation and required loading order.
- `REGION_OVERVIEW.md` — geography, identity, climate, resources, local life, and boundaries.
- `settlements/<Settlement_Name>.md` — detailed settlement records when a settlement needs its own module.
- `npcs/REGISTRY.md` — region-wide NPC index grouped by settlement/subregion.
- `npcs/<NPC_Name>.md` — canonical full profile for one recurring or major NPC.
- `factions/<Faction_Name>.md` — separate organization record when its complexity warrants one.
- `routes/ROUTE_NETWORK.md` — confirmed connections and transfers, if route complexity warrants a dedicated file.

Do not create empty files just to satisfy the tree. Keep simple content in the region overview until its complexity justifies a separate module. Existing canon may retain established file names during migration; do not rename or move it in a way that loses information.

## 3. NPC placement and canonical ownership

1. Every region has one registry entry point. The registry lists public identity/name, current or last-confirmed location, role, affiliation, public-facing traits/goal, canonical profile link, and status.
2. Each recurring or major NPC has exactly one canonical full profile. Do not copy the biography into the regional overview, settlement file, faction file, or central repository.
3. Local settlement and faction files link to the canonical profile and record only relevant local context, presence, office, or assignment.
4. An NPC whose location changes is not automatically reassigned to a different canonical repository. Keep profile ownership based on established primary affiliation/home unless the owner approves a transfer; update current whereabouts and cross-links.
5. For a cross-region NPC, the primary profile remains in one agreed home repository. Other regions link to it and maintain only locally relevant context.
6. Background and temporary scene NPCs do not need permanent profiles unless they become recurring or materially important.
7. A profile's GM-only information is not automatically public or known by the player-character.

## 4. Mandatory AI navigation

For any gameplay, lore answer, audit, or repository edit involving a region:

1. Read the central `INDEX.md` and `templates/AUTHORITY_ORDER.md`.
2. Resolve the region and open its exact repository link from the central regional repository directory.
3. Read that regional repository's `INDEX.md` or `README.md` and follow its local loading route.
4. Read the relevant settlement/subregion entry and its NPC registry.
5. Open only the canonical NPC profiles and faction/institution records relevant to the current scene or task.
6. For travel, also verify origin, destination, intermediate transfers, and global travel rules in the central repository.
7. If a regional link is missing, inaccessible, or points to a different repository, state the specific gap. Never invent a repository URL or claim to have read inaccessible data.

Do not fetch every NPC profile in the world for an ordinary scene. Do fetch all relevant regional registries when performing a complete roster audit, cross-region comparison, or migration.

## 5. Migration safety rule

**A repository is not considered migrated merely because this architecture document exists.** The central regional repository directory must contain a verified URL for the destination repository, and its regional index/registry must be checked before canonical ownership is changed.

Until a destination is verified and the migration is confirmed:
- Existing regional files and NPC profiles in `merzkava-universe` remain the accessible legacy canon.
- Do not delete, rename, or overwrite the legacy profiles.
- Do not publish a fake or guessed regional repository URL.
- Do not claim the regional repositories are fully separated.
- Once a destination is verified, copy/migrate the relevant files with their content and cross-links checked, update the regional repository directory, then update the central index and Authority Order. Only remove legacy duplicates after the destination content and links are verified.

## 6. Registry entry format

Use one row per individual:

| Public name / identity | Current or last-confirmed location | Role | Affiliation | Public traits / goal | Canonical profile | Status |
|---|---|---|---|---|---|---|
| Not established | Not established | Not established | Not established | Not established | Link to canonical profile | Not established |

The table is a template, not a claim that any listed NPC exists. Keep names and facts grounded in established canon.
