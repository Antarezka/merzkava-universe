# Merzkava Universe — NPC Management and Continuity

**Status:** Canonical GM operating guidance.
**Purpose:** Keep NPCs locally grounded, independent, consistent, and navigable without turning every passer-by into a permanent character record.

## 1. Sources of truth and file structure

- Target architecture: `world/REGIONAL_REPOSITORY_ARCHITECTURE.md`. There are exactly three regional repositories, one for each major power: Golden Dragon Empire, Tianhai Yunzhou, and Beiming Gu. The central repo is the global navigation hub.
- Do not create a separate repository for each province, valley, city, or village, and do not create a separate global NPC repository. NPCs belong in the repository of their canonical home/affiliation among the three powers.
- After a power's repository URL is verified and registered in the central `INDEX.md`, that repository's NPC registry is the first stop for NPCs in its territory, local authority, settlement context, and local encounters.
- `templates/NPC_PROFILE_TEMPLATE.md` is the canonical format for a major or recurring NPC's full profile; the three regional repositories should use this standard or link back to it.
- A full profile lives in one canonical file. Local registries, settlement files, and faction files link to it instead of duplicating the biography.
- Migration safety: until the three destination repositories are verified and their contents checked, the existing `world/REGION_*.md` and `world/NPC_*.md` files remain legacy canon in the central repository. Do not delete, overwrite, or claim to have moved them.
- `world/FACTIONS.md` and dedicated faction modules define organization-level structure and confirmed membership.
- `world/DYNAMIC_EVENTS.md` records persistent changes; `world/HISTORY.md` records confirmed historical changes where appropriate.
- `world/LOCATION_AND_ROUTE_NETWORK.md` defines route modeling and travel checks.
- Gameplay continuity in the current conversation is not automatically saved to GitHub. Never claim a persistent update without a verified repository commit.

## 2. NPC tiers and when to create a profile

**Background NPC:** A situational resident, vendor, porter, guard, traveler, customer, or passer-by. Portray them as needed. Keep details proportionate; do not create a permanent profile unless they become recurring or materially important.

**Recurring NPC:** A person who returns, has an ongoing relationship with the player, holds a continuing local role, or is likely to matter later. Record them in the regional registry and create one full profile when continuity, motives, capabilities, or relationships need persistent tracking.

**Major NPC:** A ruler, senior official, faction leader, prominent expert, powerful opponent, or person whose decisions have lasting consequences. Use a full profile and link it from the region and relevant faction records.

**Unidentified person:** Use a public description or role until the character has a credible in-world way to learn their name. A name in a file does not mean the player-character knows it or that the NPC is present.

## 3. Regional placement and local realism

1. Check the current region's settlement table, NPC registry, local authorities, and known route network.
2. Check relevant faction and official rosters before inventing an officeholder or organization member.
3. Match occupation, resources, influence, and services to the settlement. A remote village should not automatically have elite healers, advanced Thinker workshops, major academies, or capital-level public services.
4. Place people where their work, responsibilities, relationships, and access make sense. Do not make all NPCs appear at the player's convenience.
5. Regional presence does not establish faction control over every settlement in that region.
6. A name in a reference file does not mean the NPC is physically present, available, or known to the player.

## 4. Minimum agency record

For each recurring or major NPC, establish where canon supports it: current role/location/affiliation/public identity; public personality; immediate and long-term goals; knowledge sources and limits; resources, authority, relationships, and constraints; reasons to cooperate, bargain, refuse, deceive, flee, or fight; behavioral boundaries; current status and last confirmed interaction.

NPCs have their own goals and can act off-screen only when world state, timeline, and available information justify it. Do not claim a fully simulated daily schedule or unseen action without a defined procedure or recorded event.

## 5. Knowledge separation

Keep **public knowledge**, **NPC knowledge**, **NPC beliefs that may be wrong**, **player-character knowledge**, **GM-only information**, and **unconfirmed proposals** distinct. Never leak a hidden identity, secret lineage, rare ability, secret affiliation, crime, relationship, or past event merely because it appears in an NPC profile. Give meaningful secrets a plausible discovery path where appropriate.

## 6. Capability and terminology consistency

- Use official cultivation, Martial Soul, Spirit Ring, Thinker, combat, HP, injury, and time modules to resolve capabilities.
- Use `Spirit Realm N — Spirit [official tier], [stage] Stage` for the nine numbered cultivation tiers. `Mortal` is a pre-Spirit-Realm status, not Spirit Realm 0.
- Do not assign a power level, technique, Spirit Ring, artifact, title, or capability that changes an outcome unless a canon source or owner-approved addition supports it.
- Political tendencies, public-service orientation, and law-enforcement strictness are separate dimensions; do not treat one as proof of secret faction membership or automatic misconduct.
- Do not inflate every NPC's power or make every NPC hostile, helpful, omniscient, or equally important.

## 7. Regional NPC registry format

List important and recurring NPCs only. Use one row per individual and link to their one canonical full profile or authoritative roster.

| Public name / identity | Current location | Role | Affiliation | Public traits / goal | Profile or canon source | Status |
|---|---|---|---|---|---|---|
| Belum ditetapkan | Belum ditetapkan | Belum ditetapkan | Belum ditetapkan | Belum ditetapkan | — | Not established |

Do not duplicate biographies. If an officeholder is defined by a canonical imperial roster, cross-reference it and record only the region-relevant presence or assignment. If the exact assignment is unknown, say so rather than creating an office.

## 8. Relationships and continuity

- Record meaningful relationships with their basis: shared event, family tie, employment, debt, rivalry, agreement, or witnessed action.
- Change a relationship only after a scene or confirmed event gives a reason.
- Record important changes with cause, time, involved parties, and consequences.
- Keep current whereabouts and injuries aligned with the latest confirmed scene.
- If a character leaves a region, update active scene state; do not erase their canonical home or affiliation.
- Persistent canon updates require the owner's approved workflow and a verified commit.

## 9. Improvisation boundary

- Minor situational details may be improvised only within the latitude allowed by `templates/AUTHORITY_ORDER.md`.
- Do not promote improvised names, prices, shops, authorities, routes, or relationships into established canon without approval when they affect persistent world structure.
- If a missing fact matters to a major decision, mark it unknown or ask the owner rather than guessing.
- Proposed additions must be labeled **Proposal — pending owner confirmation**.
