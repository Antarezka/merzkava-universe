# Merzkava Universe — NPC Management and Continuity

**Status:** Canonical GM operating guidance.
**Purpose:** Keep NPCs grounded in the established map, with consistent whereabouts and independent motives.

## 1. One connected NPC ↔ Map path

Use the same connected path in either direction, depending on the scene's starting point:

- **NPC → Map:** open the canonical NPC profile, use `Home / usual residence`, `Usual base / duty location`, and `Last confirmed location / current whereabouts` to select the matching map/regional module, then ground the scene in its established local places, institutions, services, routes, and nearby NPC entries. A registry is only a locator when needed.
- **Map → NPC:** when a player enters or spends time in a location, use the map, local NPC entries, and relevant institutions/factions as context—not as an exhaustive census. Introduce established NPCs when their presence fits, but keep the place alive even when no listed character fits. Freely improvise plausible temporary residents, vendors, guards, travelers, students, passers-by, conversations, rumors, market activity, and other ordinary local events grounded in the region and terrain. These details do not need pre-existing profiles, roster entries, or event records. Use proportionate scrutiny: validate major/established NPCs, official roles, consequential faction authority, travel continuity, and lasting changes carefully; a light plausibility check is enough for incidental background activity. An organization may plausibly have a passing visitor or scene-level contact, but its existence alone does not establish a permanent local branch, office, jurisdiction, membership, or authority. Do not invent finer map geography or permanent services just to stage a scene. Keep one-off NPCs lightweight—no profile or registry entry.

Start from `INDEX.md` → `templates/AUTHORITY_ORDER.md` as usual. For Beiming Gu, use `world/REGION_BEIMING_GU.md` as the single regional source. If the map does not establish a finer location, keep it unknown. A profile, residence, regional affiliation, or local roster entry alone does not prove current physical presence; check last-confirmed location, duties, schedule, plausible travel, relationships, and active events. Never invent finer map details, identity, or concealed facts. Temporary NPCs and activities are scene-level improvisation, not canon; persistent named additions require owner approval.

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

Canonical full profiles for established named NPCs are maintained in `regions/golden-dragon-empire/npcs/`, `regions/tianhai-yunzhou/npcs/`, and `regions/beiming-gu/npcs/`. The Beiming Gu registry currently lists 23 canonical profiles: four established major NPCs, 12 clan heads, five dojo masters, and two owner-approved youth-circle NPCs. Verify each legacy `world/NPC_<NAME>.md` file before treating it as a compatibility pointer; when editing an established NPC, update the canonical profile in the relevant in-repository regional folder and synchronize affected links. These folders are part of the current repository architecture, not staging areas for an assumed external migration. Do not create a second profile merely because a local table is missing.

Within the current repository, use:
- `regions/<power>/INDEX.md` — regional NPC navigation and loading order.
- `regions/<power>/npcs/REGISTRY.md` — regional roster and links to canonical profiles.
- `regions/<power>/npcs/<NPC_Name>.md` — one detailed canonical profile when the NPC needs one.
- `world/REGION_*.md` and other relevant world modules — regional identity, local context, settlement details, and NPC tables where established.

The regional index, registry, local tables, and profile must point to the same canonical record without duplicating its full biography. Use the central `INDEX.md` to enter the path; do not assume settlement modules live under `regions/<power>/`.

## 4. Canonical profile template

Use `templates/NPC_PROFILE_TEMPLATE.md` for detailed recurring/major NPC profiles. Keep public identity, motivations, supported capabilities, knowledge boundaries, relationships, last-confirmed status, and source modules distinct. Do not invent secret lineage, rare abilities, affiliations, crimes, offices, or relationships and present them as canon.

## 5. Local placement and realism

### A. Required location fields for every established NPC profile

Every established recurring/major NPC profile must distinguish these fields, using consistent labels across all three regional branches:

- **Home / usual residence:** canon-supported home area, district, settlement, residence, or institution, from broadest to most specific.
- **Usual base / duty location:** where the NPC normally governs, works, studies, or serves, when distinct or relevant.
- **Last confirmed location / current whereabouts:** the last location established by canon or gameplay; it is not a guarantee of continuous presence.
- **Recurring visits / cover locations:** known repeat destinations, disguises, or temporary patterns, clearly distinguished from permanent residence or official membership.

Use official map names at the most specific level supported by canon (region → district/area → settlement/institution → named building). Do not invent a palace, street, campus placement, district, coordinates, or route to fill a field. If finer detail is unknown, state **“Exact district/building not established”** or **“Belum ditetapkan.”** Regional affiliation alone does not establish a specific residence.

### B. High-ranking NPC residence and travel tendency

High-ranking figures—including sovereigns, senior rulers, clan heads, senior institutional leaders, and exceptionally powerful figures—normally remain at their established residence or principal base and travel relatively rarely. Treat their residence as the default likely location once established; do not assume they wander around the world or conveniently appear wherever the player goes.

They may leave for a credible reason grounded in duties, goals, security needs, relationships, emergencies, or established events. Record confirmed journeys and last-known whereabouts. Do not invent routine trips or claim an NPC is physically present without support. This is a behavioral tendency, not an absolute restriction.

**Explicit exception — Beiming Nerva:** Nerva frequently turns up in Tianhai Yunzhou and sometimes uses a student disguise at Beichen Cultivator Academy. Preserve this established recurring behavior; do not apply the usual stay-at-home tendency to her as if she were an ordinary high-ranking NPC. Her visits do not mean she is always there, and her disguise does not establish official enrollment.

### C. Placement and continuity checks

1. Check the location/settlement description, its local NPC table, relevant official rosters, faction membership, and known routes. Fill home/base/last-confirmed-location fields only from those sources.
2. Match occupation, resources, authority, and services to the settlement. A remote village does not automatically have capital-level services or elite experts.
3. An NPC's presence in a regional module does not prove they are physically present in the current scene, available to meet, or known to the player.
4. A temporary location change does not change canonical home or the repository location of the canonical profile.
5. Regional presence does not establish that a faction controls every settlement in that region.
6. If an officeholder or faction member is established by an authoritative roster, reference it instead of inventing a conflicting holder.

## 6. Agency and knowledge boundaries

### Mandatory player-facing NPC naming, classification, and introductions

- Wrap **every NPC reference** in double backticks in all player-facing output, including narrative, dialogue attribution, combat, events, descriptions, tables, and logs.
- **Respect established scene context.** If earlier dialogue or an agreed arrangement already identifies who the player is meeting or whom the NPC reference means—for example, a named meeting invitation, an agreed appointment, a direct referral, or an introduction in a prior scene—use that established identity. Do not reset the person to ``npc ???`` merely because the current turn begins a new scene. A name appearing only in a GM-only profile, roster, or registry does not by itself mean the player-character knows it.
- **Reserve ``npc ???`` for significant, story-relevant, or potentially recurring people whose identity is genuinely unknown to the player-character.** Until a valid in-world introduction/discovery, do not leak their concealed name through narration, dialogue labels, tables, or other output. Preserve their identity internally for continuity.
- **Proactive introduction is mandatory for an unidentified significant NPC once conversation makes it natural.** Do not wait for the player to ask. The NPC may introduce themself in dialogue, or a companion/host may introduce them—for example, if a princess brings a friend to sit with the player, either the princess introduces the friend or the friend naturally gives their own name. Do this at the first reasonable conversational opportunity, not as an awkward interruption. Delay only when the scene gives a clear reason, such as active danger, deliberate concealment/disguise, an explicit wish to remain anonymous, inability to communicate, or no natural opportunity yet; maintain ``npc ???`` only while that reason or genuine lack of identification remains.
- **Ordinary background/service NPCs do not use ``npc ???``.** For incidental people such as food vendors, beggars, fishermen, guards, gatekeepers, porters, or passers-by, use a clear role-based label such as ``NPC: Penjaga gerbang``. Keep them lightweight; do not force a personal name or a formal introduction just to identify them.
- **When a background/service NPC introduces their name or the name becomes known in-world, retain the role/profession with the name** in the player-facing label, such as ``Penjaga Gerbang: Wang Lan``. Continue using that role/title plus name for relevant references; never revert to ``npc ???`` while the player-character knows the identity.
- Multiple genuinely unidentified significant NPCs may each display as ``npc ???``, but their distinct identities and continuity must remain separate internally. These presentation rules do not change NPC canon, profile ownership, or permission to improvise temporary NPCs under `world/NPC_MANAGEMENT.md`.


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
- **Arcanist Grade is an independent and important part of the assessment.** If a person has a poor-looking Spirit Ring configuration but is credibly known to be an Arcanist, NPCs may understand that the person has developed a different field of capability rather than judging their entire worth by cultivation alone. The higher and more relevant the established Arcanist Grade, the more reason a knowledgeable observer has to take their expertise seriously; do not invent a numerical social bonus or assume Arcanist Grade automatically means combat strength.
- The Great Tianhai War/world-calamity legacy is a concrete reason for this respect: Arcanists from across the world, including most of Tianhai Yunzhou's Arcanists, spread across nearly the entire world to deploy mass-produced one-use concealment Artificial Artifacts that protected inhabited areas from otherworldly gates and descending Tier 7–9 Demonic Beasts. Their work saved many populated areas. Some participants had awakened Martial Souls but had not yet obtained any Spirit Ring; they still made a meaningful contribution through Arcanistry knowledge and artifact deployment. This is a recorded example that a person's value cannot be reduced to Spirit Rings. Do not generalize that every Arcanist in the effort was ringless; assess each individual only from known facts.
- This historical legacy is especially salient in Tianhai Yunzhou, where Arcanistry knowledge originated and where Arcanist institutions, advanced artifact work, and the catastrophe's rescue effort have enduring significance. Residents there—and NPCs who study Arcanistry, Artificial Artifacts, or the Great Tianhai War—may treat Arcanist Grade and proven contributions as a major positive consideration, sometimes regarding a weak ring configuration as understandable or secondary. This does not force universal admiration: personal prejudice, competing interests, unknown credentials, or evidence of poor conduct may still affect their judgment.

### B. Social reactions and stakes

- Ordinary residents and inexperienced NPCs may rely more heavily on the visible configuration and common reputation. A configuration that looks poor can make them more dismissive, hesitant to trust the person, or pessimistic about being rescued by them.
- In a rescue or emergency, a vulnerable NPC who sees a rescuer's apparently weak configuration may lose hope, doubt that help will work, hesitate to cooperate, or prepare emotionally for failure. Portray this as a context-sensitive reaction, not a mandatory identical response from every person.
- Other NPCs may remain hopeful because of desperation, personal values, prior relationships, lack of alternatives, or evidence beyond the ring configuration. Fear and hope are individual; do not make every bystander react alike.
- A strikingly strong, well-balanced, or unusually high-age configuration may inspire respect, confidence, fear, envy, suspicion, or heightened expectations, depending on the observer's personality, interests, and relationship to the person. Admiration is not automatic obedience.

### C. Experts, teachers, and regional outlook

- Experienced Spirit Realm cultivators, instructors, veteran hunters, tacticians, and qualified Arcanists should look beyond the first impression when their expertise and available evidence justify it. Cultivation experts may assess technique, Martial Soul compatibility, ring abilities, combat decisions, discipline, adaptability, body condition, and long-term growth potential; Arcanist-aware observers also consider verified Arcanist Grade, relevant specialization, artifact knowledge, and demonstrated contributions. Keep Arcanist capability separate from combat power unless an established ability or artifact makes it relevant.
- An expert may still criticize a poor configuration honestly. The distinction is that a qualified observer can recognize a remediable weakness, identify what kind of training might help, or judge that a person has potential if guided along a path considered sound by that observer. Do not guarantee improvement or invent a training solution without support.
- The observer's idea of a “correct path” depends on their own experience, school, values, and regional tradition; it is not one universally correct doctrine. Use established regional sources and the NPC's actual background rather than stereotyping every resident of a power.
- Golden Dragon Empire's central academies provide established foundational education; Tianhai Yunzhou's academies are comparatively flexible and have distinct movement, defense, adaptation, and technical traditions; Beiming Gu's harsh environments, defensive terrain, and survival experience may lead some trained observers to value practical survival, resilience, and performance under pressure. These regional influences do not automatically identify an NPC with Soul-Nyuma or Soul-Zoun. Determine a tradition only from the NPC's actual teacher, school, doctrine, methods, or documented expertise, following `core/SPIRIT_REALM_TRADITIONS.md`.
- If the NPC's school, training, values, or expertise are unknown, do not assign them a detailed regional doctrine by assumption. Let their reaction follow established personality, role, knowledge, and immediate interests.

### D. Exceptional configurations as reference

The confirmed ring-age configuration recorded for Beiming Han in `world/WORLD.md` is an extraordinary high-end comparison. Its nine ring ages and colors are established canon; apply the high-age color bands in `core/SPIRIT_RING_RULES.md`. Colors for Spirit Rings from Heaven Realm beings older than 15,000,000 years remain unspecified and must not be guessed. In play, use Beiming Han as a comparison only when the NPC plausibly knows of him or has access to the relevant information; most NPCs should not automatically know his exact configuration.

## 7. Relationships and continuity

- Record meaningful relationships with their basis: witnessed event, family tie, employment, debt, rivalry, agreement, or other confirmed cause.
- Use the canonical profile's relationship field to record direction and, where useful, a disposition such as pro, contra, neutral, or mixed. A label describes that NPC's own stance; it does not establish reciprocal feelings.
- A regional youth circle is a relationship/navigation aid, not a new NPC system, faction, academy, or event. Each recurring NPC's detailed profile remains the single canonical home; registries and indexes only link to it.
- Membership in a circle does not prove every member has met in person, knows another member's identity/secrets, shares a location, or is available in a scene. Verify presence and knowledge as usual.
- Keep each circle within its own major power by default. Cross-power relationships or acquaintance require an established canon basis or a recorded in-world event; a recurring visitor is not automatically a member of the host power's circle.
- Change a relationship only after a scene or confirmed event justifies it.
- Record important persistent changes with cause, time, involved parties, and consequences.
- Keep whereabouts and injuries aligned with the latest confirmed scene.
- Record persistent world consequences in `world/DYNAMIC_EVENTS.md` and/or `world/HISTORY.md` when appropriate.
- Gameplay continuity in the current conversation is not automatically saved to GitHub.

## 8. Scene improvisation and repository integrity

- Ordinary scene details and temporary background NPCs are allowed whenever they are plausible in context. They may speak, react, bargain, refuse, gossip, offer small opportunities, and pursue immediate interests. The GM does not need to register each person or document each routine activity first.
- A scene-level detail can be treated as true for the current scene without automatically becoming permanent or world-wide canon. Keep continuity in the conversation, and only record lasting changes when their consequences warrant it.
- Apply careful verification to established/major NPCs, official appointments, enduring relationships, permanent shops or services, faction jurisdiction, route/geography changes, and other persistent consequences. Do not let these checks block ordinary scene flow.
- Do not promote improvised details into permanent canon when they alter persistent world structure without the required canon basis/owner approval. Mark proposed persistent additions **Proposal — pending owner confirmation**.
- Keep all regional canon, registries, and NPC profiles inside `Antarezka/merzkava-universe` unless the owner explicitly changes the architecture. Do not create or imply a separate repository per major power.
- Before adding or reorganizing a recurring/major NPC, verify the current regional module, registry, canonical profile links, and duplicates; synchronize only affected in-repository navigation references.
- Never claim a persistent repository update without a verified commit.
