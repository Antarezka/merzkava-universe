# Merzkava Universe — NPC Management and Continuity

**Status:** GM guidance scaffold.  
**Purpose:** Keep NPCs consistent across regions and interactions without treating undocumented details as canon.

## 1. Sources of Truth
- Regional NPC presence belongs in the relevant `world/REGION_*.md` module.
- Full profiles for important named NPCs should follow `templates/NPC_PROFILE_TEMPLATE.md` and be linked from their regional module.
- Faction leaders and members may also be referenced in `world/FACTIONS.md` and the relevant faction records.
- Persistent world-scale events belong in `world/DYNAMIC_EVENTS.md`; confirmed historical changes belong in `world/HISTORY.md` when appropriate.
- Gameplay state is not automatically saved to GitHub. Do not claim that an NPC profile or event has been persistently updated unless the owner has actually approved and committed the change.

## 2. NPC Categories
- **Background NPC:** A brief, situational character with no established long-term role. Do not silently promote improvised details into permanent canon.
- **Recurring NPC:** A character who returns or has a continuing relationship with the player. Preserve established identity, personality, knowledge, and prior interactions.
- **Major NPC:** A character with significant authority, influence, unique capabilities, or persistent story relevance. Give them a full profile.
- **Unknown identity:** Use an appropriate unknown/public-facing identity until the character learns the name through a credible in-world source. Do not expose profile-only secrets as player knowledge.

## 3. Minimum NPC Consistency Rules

**Terminology standard:** use **Spirit Realm** for the nine numbered cultivation tiers. When recording an NPC's cultivation, use `Spirit Realm N — Spirit [official tier], [stage] Stage`; do not shorten it to `Realm` or call it `Cultivation Realm`. `Mortal` is a pre-Spirit-Realm status, not Spirit Realm 0. Preserve unrelated proper names such as `Heaven Realm` when they refer to a distinct historical or cosmological concept.
1. Every established NPC should have a coherent role, public personality, immediate goal, and boundaries for likely behavior.
2. NPCs act according to their goals, information, abilities, relationships, and circumstances; they do not exist solely to serve the player.
3. Separate facts known to the NPC, beliefs that may be wrong, facts known to the player, and GM-only secrets.
4. Do not invent secret lineage, rare abilities, affiliations, crimes, relationships, or past events and present them as established canon.
5. Do not make every NPC hostile, helpful, omniscient, or equally important. Their response must fit their role and situation.
6. An NPC's strength and techniques must be consistent with the official cultivation, Martial Soul, Spirit Ring, Thinker, combat, and injury modules.
7. Do not assign exact stats, hidden powers, or an outcome-changing capability without a valid source or explicit owner-approved addition.
8. Record persistent changes only when they actually occur in gameplay; do not retroactively rewrite prior interactions.

## 4. Agency and Decision Framework
For an established NPC, use the following questions when deciding their behavior:
- What do they want right now?
- What do they know, and how did they learn it?
- What are they trying to protect, gain, avoid, or conceal?
- What resources, authority, relationships, and limitations do they have?
- What would make them cooperate, refuse, negotiate, flee, deceive, or fight?
- What consequences would follow from their choice?

This is a reasoning checklist, not an automatic simulation engine. Do not claim that NPCs perform unseen daily actions or update their state automatically unless a specific canon event or recorded continuity supports it.

## 5. Regional NPC Registry
Each regional module should contain a compact registry with links to full profiles for important NPCs. Avoid copying full profiles into multiple files; link to one canonical profile to reduce contradictions.

Recommended fields: public name, location, role, affiliation, publicly known traits, and canonical profile link.

## 6. Encountering New NPCs
- Use the relevant region and faction modules to establish whether the person or role is already documented.
- If no named NPC is established, the GM may portray a minor situational character only within the latitude granted by the Authority Order. Keep improvised details proportionate and do not assert major secrets or world-changing lore.
- If the player asks for a permanent or important NPC, mark new details as pending owner confirmation until they are accepted into the repository.
- An NPC's name is not automatically known to the player merely because it appears in a reference file.

## 7. Continuity Record
When an NPC's state changes significantly, track the change in the current conversation and, if persistent world canon is intended, submit it through the owner's approved repository workflow. Include the cause, time, involved characters, and consequences. Do not claim a GitHub save without a verified commit.

## 8. Owner To-Do
- [ ] Define when background NPC improvisation is permitted
- [ ] Decide where full NPC profiles should live if profile count grows
- [ ] Define how owner-approved persistent NPC changes are submitted
- [ ] Add confirmed NPCs to regional registries
