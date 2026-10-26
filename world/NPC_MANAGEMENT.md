# Merzkava Universe — NPC Management and Continuity

**Status:** Canonical GM operating guidance.
**Purpose:** Keep NPCs easy to find by location, consistent with world canon, and independent in their motives. Follow the regional-module pattern: central INDEX → relevant regional module → location/faction NPC table → detailed profile only when needed.

## 1. One navigation path

For NPC lookup, creation, auditing, or gameplay, follow this order:

1. Read the central `INDEX.md` and `templates/AUTHORITY_ORDER.md`.
2. Read `world/WORLD.md` to confirm the exact canonical major-power names.
3. Identify the NPC's established home/affiliation or the scene's location.
4. Open the relevant regional/settlement module and inspect the NPC table for that location, settlement, institution, or faction.
5. Follow the link to a detailed NPC profile only when one exists and is relevant.
6. Check authoritative official/faction rosters, route modules, `world/DYNAMIC_EVENTS.md`, or `world/HISTORY.md` when needed.
7. If a source does not establish a fact, label it unknown. Never invent a path, name, role, affiliation, ability, or destination repository.

The regional module's NPC table is the first lookup point for local NPCs. Do not make the player or GM hunt across unrelated files to discover which NPCs belong to a place.

## 2. Regional boundaries and canon

There are exactly three major-power regions, using the names exactly as written in `world/WORLD.md`:

1. **Golden Dragon Empire**
2. **Tianhai Yunzhou**
3. **Beiming Gu**

Do not create alternate formal names, a fourth global NPC repository, or a separate repository for every province, city, or village.

The single repository `Antarezka/merzkava-universe` is the permanent central home for Merzkava Universe canon under the current architecture. The three major powers are organized in in-repository regional folders and modules; they are not separate GitHub repositories. Regional NPC registries are canonical navigation directories within this same repository once their entries and links are established. Do not propose, assume, or perform external regional-repository migration.

**Legacy-file safety:** existing `world/REGION_*.md`, `world/NPC_*.md`, and other regional canon files remain valid sources unless their actual contents establish a different role. Do not treat a file as a compatibility pointer from its name alone, and do not delete or overwrite it merely because a regional profile or registry exists elsewhere in this repository.

## 3. NPC structure — follow the regional-module pattern

### A. Local NPC tables live beside their location

In each regional module, group NPCs under the appropriate existing location, settlement, institution, or faction heading. Keep each table close to the place or organization it describes instead of collecting every local NPC into an unrelated global list.

Recommended table fields:

| NPC / public identity | Role | Age | Capability / official tier | Signature technique or approach | Public traits / behavior | Canon source / profile |
|---|---|---|---|---|---|---|
| Not established | Not established | Not established | Not established | Not established | Not established | Link to canon source if one exists |

Use only fields that make sense for the NPC. For a non-cultivator, say so instead of inventing a tier or technique. Use official capability terminology and mechanics from the relevant world modules.

### B. Detailed profiles are for continuity, not for every passer-by

- **Background NPC:** situational resident, vendor, guard, porter, traveler, customer, or passer-by. Usually keep them in the local scene; no permanent profile is required.
- **Recurring NPC:** returns, has an ongoing relationship, or holds a continuing role. Include them in the relevant local table; create or retain a detailed profile when continuity needs it.
- **Major NPC:** ruler, senior official, faction leader, prominent expert, powerful opponent, or person whose decisions have lasting consequences. Keep a local table entry and link to one detailed canonical profile or authoritative roster.
- **Unidentified person:** show only a credible public description or role until the character learns their identity in-world.

A detailed profile has exactly one canonical home. Regional, settlement, institution, and faction modules link to it; they do not copy its full biography. A local table entry is a locator/summary, not a second full profile.

### C. Where detailed profiles live

Canonical full profiles for established named NPCs are maintained in `regions/golden-dragon-empire/npcs/`, `regions/tianhai-yunzhou/npcs/`, and `regions/beiming-gu/npcs/`. The Beiming Gu registry currently lists 21 canonical profiles: four established major NPCs, 12 clan heads, and five dojo masters. Verify each legacy `world/NPC_<NAME>.md` file before treating it as a compatibility pointer; when editing an established NPC, update the canonical profile in the relevant in-repository regional folder and synchronize affected links. These folders are part of the current repository architecture, not staging areas for an assumed external migration. Do not create a second profile merely because a local table is missing.

Within the current repository, use:
- `regions/<power>/INDEX.md` — regional NPC navigation and loading order.
- `regions/<power>/npcs/REGISTRY.md` — regional roster and links to canonical profiles.
- `regions/<power>/npcs/<NPC_Name>.md` — one detailed canonical profile when the NPC needs one.
- `world/REGION_*.md` and other relevant world modules — regional identity, local context, settlement details, and NPC tables where established.

The regional index, registry, local tables, and profile must point to the same canonical record without duplicating its full biography. Use the central `INDEX.md` to enter the path; do not assume settlement modules live under `regions/<power>/`.

## 4. Canonical profile template

Use `templates/NPC_PROFILE_TEMPLATE.md` for detailed recurring/major NPC profiles. Keep public identity, motivations, supported capabilities, knowledge boundaries, relationships, last-confirmed status, and source modules distinct. Do not invent secret lineage, rare abilities, affiliations, crimes, offices, or relationships and present them as canon.

## 5. Local placement and realism

1. Check the location/settlement description, its local NPC table, relevant official rosters, faction membership, and known routes.
2. Match occupation, resources, authority, and services to the settlement. A remote village does not automatically have capital-level services or elite experts.
3. An NPC's presence in a regional module does not prove they are physically present in the current scene, available to meet, or known to the player.
4. An NPC's temporary location change does not automatically change their canonical home or the in-repository location of their canonical profile.
5. Regional presence does not establish that a faction controls every settlement in that region.
6. If an officeholder or faction member is established by an authoritative roster, reference it instead of inventing a conflicting holder.

## 6. Agency and knowledge boundaries

For recurring/major NPCs, establish where canon supports it: role and affiliation; public personality; immediate and long-term goals; knowledge sources and limits; resources, relationships, and constraints; reasons to cooperate, bargain, refuse, deceive, flee, or fight; behavioral boundaries; and current status/last confirmed interaction.

NPCs have their own goals. They are not automatically friendly, hostile, omniscient, or available whenever the player wants them. Do not claim a fully simulated daily schedule or unseen action without an established procedure or recorded event.

Keep separate public knowledge, what the NPC actually knows, beliefs that may be wrong, player-character knowledge, GM-only information, and proposals awaiting owner confirmation. A secret in a profile is not automatically known to the player.

## 6A. Spirit Ring Configuration and NPC Perception

Spirit Ring configuration is a meaningful social signal in Merzkava Universe. NPCs may form impressions from the actual ages, distribution, and overall quality of a person's known Spirit Rings—not merely from the number of rings or the person's current Spirit Realm. A configuration dominated by comparatively young/low-age rings, especially when its stronger rings do not offset that pattern, can lead observers to judge the person as having a weak foundation, limited achievements, or a low chance of succeeding in a dangerous situation. These are social judgments, not objective proof of the person's true ability or future ceiling.

### A. What an NPC can judge

- Base the reaction on what that NPC can actually observe or credibly know: visible ring characteristics, a witnessed display, a reliable appraisal/report, prior encounters, or established public knowledge. Do not let every NPC automatically know exact ring ages, hidden abilities, or the complete configuration.
- Distinguish the real configuration from the observer's information. If only ring colors or a partial display are known, the NPC may make a rough impression but must not state hidden ages or details as fact. Spirit Ring color and Beast Age Grade are separate classifications; do not infer one directly from the other.
- Consider the whole arrangement: how many rings are relatively low-age versus high-age, their order/distribution when known, and whether the known abilities or combat record provide a reason to revise the first impression. Do not invent a universal score, fixed percentage, or rigid cutoff for “good” and “bad” configurations.
- A weak-looking configuration does not automatically make its owner weak, incompetent, dishonest, or doomed. It creates a plausible initial impression that may change through demonstrated skill, tactics, courage, teamwork, achievements, or other credible evidence.
- **Thinker Grade is an independent and important part of the assessment.** If a person has a poor-looking Spirit Ring configuration but is credibly known to be a Thinker, NPCs may understand that the person has developed a different field of capability rather than judging their entire worth by cultivation alone. The higher and more relevant the established Thinker Grade, the more reason a knowledgeable observer has to take their expertise seriously; do not invent a numerical social bonus or assume Thinker Grade automatically means combat strength.
- The Great Tianhai War/world-calamity legacy is a concrete reason for this respect: Thinkers from across the world, including most of Tianhai Yunzhou's Thinkers, spread across nearly the entire world to deploy mass-produced one-use concealment Artificial Artifacts that protected inhabited areas from otherworldly gates and descending Tier 7–9 Demonic Beasts. Their work saved many populated areas. Some participants had awakened Martial Souls but had not yet obtained any Spirit Ring; they still made a meaningful contribution through Thinker knowledge and artifact deployment. This is a recorded example that a person's value cannot be reduced to Spirit Rings. Do not generalize that every Thinker in the effort was ringless; assess each individual only from known facts.
- This historical legacy is especially salient in Tianhai Yunzhou, where Thinker knowledge originated and where Thinker institutions, advanced artifact work, and the catastrophe's rescue effort have enduring significance. Residents there—and NPCs who study Thinker disciplines, Artificial Artifacts, or the Great Tianhai War—may treat Thinker Grade and proven contributions as a major positive consideration, sometimes regarding a weak ring configuration as understandable or secondary. This does not force universal admiration: personal prejudice, competing interests, unknown credentials, or evidence of poor conduct may still affect their judgment.

### B. Social reactions and stakes

- Ordinary residents and inexperienced NPCs may rely more heavily on the visible configuration and common reputation. A configuration that looks poor can make them more dismissive, hesitant to trust the person, or pessimistic about being rescued by them.
- In a rescue or emergency, a vulnerable NPC who sees a rescuer's apparently weak configuration may lose hope, doubt that help will work, hesitate to cooperate, or prepare emotionally for failure. Portray this as a context-sensitive reaction, not a mandatory identical response from every person.
- Other NPCs may remain hopeful because of desperation, personal values, prior relationships, lack of alternatives, or evidence beyond the ring configuration. Fear and hope are individual; do not make every bystander react alike.
- A strikingly strong, well-balanced, or unusually high-age configuration may inspire respect, confidence, fear, envy, suspicion, or heightened expectations, depending on the observer's personality, interests, and relationship to the person. Admiration is not automatic obedience.

### C. Experts, teachers, and regional outlook

- Experienced Spirit Realm cultivators, instructors, veteran hunters, tacticians, and qualified Thinkers should look beyond the first impression when their expertise and available evidence justify it. Cultivation experts may assess technique, Martial Soul compatibility, ring abilities, combat decisions, discipline, adaptability, body condition, and long-term growth potential; Thinker-aware observers also consider verified Thinker Grade, relevant specialization, artifact knowledge, and demonstrated contributions. Keep Thinker capability separate from combat power unless an established ability or artifact makes it relevant.
- An expert may still criticize a poor configuration honestly. The distinction is that a qualified observer can recognize a remediable weakness, identify what kind of training might help, or judge that a person has potential if guided along a path considered sound by that observer. Do not guarantee improvement or invent a training solution without support.
- The observer's idea of a “correct path” depends on their own experience, school, values, and regional tradition; it is not one universally correct doctrine. Use established regional sources and the NPC's actual background rather than stereotyping every resident of a power.
- Golden Dragon Empire's established orthodox central academies and its clan/dojo traditions can shape a more structured or orthodox assessment when supported by the specific NPC's education. Tianhai Yunzhou's more flexible academies and its distinct movement, defense, adaptation, and technical traditions may support a different assessment when relevant. Beiming Gu's harsh environments, defensive terrain, survival experience, and established cold/defensive or mobility traditions may lead some of its trained observers to value practical survival, resilience, and performance under pressure. These are available contextual influences, not rules that every regional NPC shares.
- If the NPC's school, training, values, or expertise are unknown, do not assign them a detailed regional doctrine by assumption. Let their reaction follow established personality, role, knowledge, and immediate interests.

### D. Exceptional configurations as reference

The confirmed ring-age configuration recorded for Beiming Han in `world/WORLD.md` is an extraordinary high-end comparison. Its nine ring ages and total are established canon; color mapping above 499,999 years remains undefined and must not be guessed. In play, use Beiming Han as a comparison only when the NPC plausibly knows of him or has access to the relevant information; most NPCs should not automatically know his exact configuration.

## 7. Relationships and continuity

- Record meaningful relationships with their basis: witnessed event, family tie, employment, debt, rivalry, agreement, or other confirmed cause.
- Change a relationship only after a scene or confirmed event justifies it.
- Record important persistent changes with cause, time, involved parties, and consequences.
- Keep whereabouts and injuries aligned with the latest confirmed scene.
- Record persistent world consequences in `world/DYNAMIC_EVENTS.md` and/or `world/HISTORY.md` when appropriate.
- Gameplay continuity in the current conversation is not automatically saved to GitHub.

## 8. Controlled additions and repository integrity

- Minor situational details may be improvised only within the latitude allowed by `templates/AUTHORITY_ORDER.md`.
- Do not promote improvised NPC names, prices, shops, authorities, routes, or relationships into established canon without approval when they affect persistent world structure.
- Mark unapproved additions **Proposal — pending owner confirmation**.
- Keep all regional canon, registries, and NPC profiles inside `Antarezka/merzkava-universe` unless the owner explicitly changes the architecture. Do not create or imply a separate repository per major power.
- Before adding or reorganizing an NPC, verify the current regional module, registry, canonical profile links, and duplicates; then update all affected in-repository navigation references together.
- Never claim a persistent repository update without a verified commit.
