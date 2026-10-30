# Merzkava Universe — World Dynamic Events

**Status:** Canonical registry and operating rules for persistent world-changing events.
**Scope:** Shared world state across sessions. This file is not a character save and does not replace character profiles, gameplay history, or official mechanics.

## 1. Purpose and Authority

World Dynamic Events record consequential events that can change the shared world beyond one character's immediate scene: wars, faction leadership changes, territorial control, public disasters, major trade disruption, exposed secrets, destroyed landmarks, treaties, and similar lasting developments.

- This file is the single canonical source for registered dynamic world events.
- Official mechanics remain governed by their relevant core/gameplay modules. An event record cannot silently create or override mechanics.
- A player's declared action is intent, not proof that the action succeeded.
- Only outcomes established through valid gameplay resolution and reviewed evidence may be proposed as events.
- A proposal is not canon. It becomes canonical only after repository owner/admin approval and commit.
- No automatic GitHub write, automatic save, or admin authority is implied by in-game narration.

## 2. When to Check This File

The GM must fetch the latest version of this file on every gameplay turn, including initial CONVO and recall, after reading INDEX and the required core prompt/response template.

At the start of a turn:
1. Check event records whose status is **ACTIVE** and whose location, actors, causes, or consequences could intersect the current scene.
2. Check whether the current character could know each relevant fact. Separate public knowledge, witnessed facts, faction knowledge, and GM-only information.
3. Apply only effects supported by the event record and relevant official modules.
4. Do not force unrelated events into the scene. A registered event may continue off-screen without being narrated every turn.
5. If this file cannot be fetched, state that dynamic-event verification is unavailable; do not claim to have checked it or invent its contents.

## 3. What Qualifies as a Dynamic World Event

Record an event when the resolved outcome has a meaningful persistent effect on one or more of:
- a region, settlement, route, landmark, or resource;
- a faction, institution, ruler, army, or organization;
- a public threat, disaster, conflict, treaty, or political condition;
- the world's shared knowledge or the evidence available to groups;
- future access, services, trade, security, or other world conditions.

Do **not** create a world event for every ordinary action, conversation, meal, training session, private purchase, or character-only status change. Keep those in the character's current profile/session record unless they create a verified world-level consequence.

## 4. Event Status and Lifecycle

Each event must have one status:
- **PROPOSED** — submitted for review; not canon and must not be used as established fact.
- **ACTIVE** — approved and currently affects the world.
- **RESOLVED** — the event's active condition has ended; retain it as history if consequential.
- **SUPERSEDED** — replaced by a newer canonical event or correction; preserve the reference trail.
- **REJECTED** — reviewed but not accepted; do not use as canon.

Only the repository owner/admin changes a proposal to ACTIVE or changes canonical event status in the repository. A GM may explain that an event update is proposed, but must never describe an unapproved proposal as a saved or official world fact.

## 5. Canonical Event Record Schema

Use one record per event. Preserve these fields; write `???` when the source genuinely does not establish a value.

- **Event ID:** stable unique ID, e.g. `WDE-0001`.
- **Title:** short, neutral name.
- **Status:** PROPOSED / ACTIVE / RESOLVED / SUPERSEDED / REJECTED.
- **First Occurred:** in-world timestamp or `???`.
- **Last Updated:** in-world timestamp and/or repository update note.
- **Location / Scope:** specific region, route, faction, or world-wide scope.
- **Trigger and Confirmed Outcome:** what actually happened, not what was merely attempted.
- **Evidence / Source:** gameplay timestamp, approved session record, witnessed result, or owner/admin verification. Do not invent evidence.
- **Involved Actors:** only known participants; distinguish confirmed participation from rumor.
- **Persistent Effects:** concrete current effects supported by the outcome.
- **Knowledge Distribution:** public facts, faction/individual knowledge, rumors, and hidden facts kept separate.
- **Duration / End Condition:** known time limit, condition for resolution, or `ongoing / unknown`.
- **Related Events / Modules:** links to prior event IDs and relevant world/mechanics modules.
- **Continuity Notes:** conflicts, uncertainty, dependencies, and what must not be assumed.

## 6. Event Resolution and World Continuity

- Resolve the player action using the normal official mechanics first. Only then decide whether the outcome qualifies for a world event.
- Record outcomes, not attempted intentions. Failed, partial, interrupted, or uncertain actions must be described accordingly.
- A consequence must be proportionate to the resolved event; do not infer a whole faction's collapse from one NPC's defeat unless the established circumstances support it. Consequences are neutral causal outcomes, not inherently punishments: record beneficial, neutral, harmful, or mixed persistent effects when supported by the resolved outcome. Do not manufacture an adverse effect merely to make an event feel important, and do not record a benefit that has not been established.
- Event effects persist until their recorded end condition is met or a later verified event changes them.
- Update an existing event when its state changes; create a linked new event when a distinct consequential development occurs. Do not duplicate the same event under multiple IDs.
- Do not advance off-screen event outcomes just because turns pass unless a recorded condition, official rule, or established NPC/faction agenda supports the change.
- New events must not silently contradict established history, geography, faction structure, or mechanics. Record unresolved contradictions for admin review.
- Events do not automatically reveal private information to every character. Apply the Knowledge Distribution field.
- A world event does not update a character's HP, inventory, currency, relationships, or other personal state by itself; those changes require their own valid causes and records.

## 7. Player Save / Update Workflow

1. During play, the GM resolves the action and keeps the confirmed outcome in the active conversation.
2. If it has a persistent world impact, the GM prepares an **event update proposal** using `templates/WORLD_EVENT_UPDATE_TEMPLATE.md`.
3. The proposal identifies whether to create, update, resolve, or supersede an event and includes the evidence/source. Unknown facts remain `???`.
4. The player may submit the proposal to the repository owner/admin. Player submission alone does not alter canon.
5. The owner/admin checks consistency against this registry, relevant world modules, official mechanics, and the session record.
6. After approval, the owner/admin commits the update to this file and any other directly affected canonical files. Update INDEX only if the source map or bootstrap procedure changes.
7. Verify the committed file and event status. Until verified, the event remains a proposal and must not be treated as saved.
8. Character-only progress is handled through the applicable character save/profile workflow, not inserted into this shared world-event registry.

## 8. Canonical Event Registry

Recurring festivals and other standing calendar observances are recorded separately from one-off active incidents. A recurring event can be canon even when the next edition's exact date, host, or attendance has not yet been established.

### 8A. Recurring Canonical World Events

#### WDE-0001 — Festival Tiga Kekuasaan

- **Status:** ACTIVE — recurring world observance.
- **First Occurred:** ???; the historical first edition has not been established.
- **Last Updated:** Canon established by repository owner; see current repository commit history.
- **Location / Scope:** Hosted in turn by one of the three major powers: Golden Dragon Empire, Tianhai Yunzhou, or Beiming Gu. Each edition takes place in the host power's designated festival grounds / central public square. The exact venue must follow established regional geography; do not invent a permanent venue before it is established.
- **Schedule:** Every six in-world months (twice per in-world year). The event is not monthly. The host rotates among the three powers; do not assume the first host, the next host, or a fixed rotation order unless an established calendar, prior edition, or owner decision confirms it.
- **Purpose:** Strengthen peaceful relations among the three powers, support cultural exchange, encourage trade and mutual understanding, and let visitors encounter a broad but general view of the wider world.
- **Participants and representation:** Each of the three powers is represented, alongside delegates and participants from its known sects, clans, factions, dojos, institutions, and other established groups. Representatives of hidden mountain factions may attend if their existence and access to the festival are known/discovered in the story. Do not assume every faction sends a delegate to every edition without evidence, and do not expose secret groups or identities to characters who have not discovered them.
- **Cultural and trade grounds:** Stalls and displays may feature each power's characteristic textiles and crafts, locally produced goods, Artificial Artifacts, engravers and their work, catalogs of Spirit Beasts known to occur specifically in each power's territory, regional foods, clothing, appearance, customs, and other established cultural differences. Demonstrations must respect actual lore and the knowledge of the people presenting it; catalogs are not proof that every beast can be found everywhere.
- **Combat exchange:** Friendly sparring is a headline attraction. Killing is forbidden. Designated referees and festival security supervise matches and intervene to stop lethal escalation. The rules and consequences of any incident follow established combat, injury, law, and faction modules; the festival does not grant plot armor or make serious misconduct consequence-free.
- **Cultural performances:** Each power presents characteristic dances and other established performing arts as a friendly showcase of regional beauty and identity. Do not invent a supposedly ancient or official dance tradition as established canon unless a source or later owner-approved detail supports it.
- **Night Lantern Festival:** A night-time lantern release is a major tradition for couples and is also open as a personal act of prayer, goodwill, or hope for any wish. Do not assume every participant is romantically paired or that a wish produces supernatural effects.
- **Security and social tension:** The festival is intended to be peaceful, not unrealistically free of conflict. Small and medium crimes, prejudice, misunderstandings, trade disputes, rivalry, and tension among visitors who reject differences may occur when supported by the scene. A major incident is possible only when its trigger and escalation are established. Do not force a crime into every edition or every player's scene; resolve incidents using the relevant official modules and register persistent consequences only after valid resolution.
- **GM use:** This is a recurring, optional world-facing opportunity to introduce general lore, cultural variety, regional goods, combat philosophies, and inter-power relationships naturally—especially when a player has stayed in one region for a long time. The GM may surface relevant invitations, rumors, travel opportunities, or consequences through the world and NPC agendas, but must not force attendance, dump all world lore at once, or treat knowledge presented at the festival as automatically known by every character.
- **Duration / End Condition:** Recurs every six in-world months; each edition ends according to its established schedule and events. The observance itself remains ongoing.
- **Evidence / Related Modules:** Owner-confirmed canon; `world/WORLD.md`, `world/MAP_AND_REGIONS.md`, `world/GEOGRAPHY_AND_TRAVEL.md`, the relevant `world/REGION_*.md` modules, `world/FACTIONS.md`, `core/ARCANISTRY_AND_FORMULATION.md`, `world/ARTIFICIAL_ARTIFACTS.md`, `bestiary/SPIRIT_BEAST_RULES.md`, `gameplay/COMBAT_SYSTEM.md`, `core/INJURY_SYSTEM.md`, and `gameplay/TIME_AND_ACTION_RULES.md`.
- **Continuity Notes:** The next host, exact date, exact venue, festival duration, detailed match rules, and specific performances/booths remain unassigned until supported by the established calendar, regional canon, prior editions, or a later owner decision. Do not fabricate these as fixed facts.

### Active Events

_No one-off active dynamic incidents registered yet._

### Resolved / Historical Events

_No resolved dynamic events registered yet._

### Pending Proposals

_Proposals awaiting owner/admin review are not canon. They may be tracked outside this canonical registry until approved._

## 9. Relationship to Other Sources

- `INDEX.md` controls bootstrap order and points the GM here on every gameplay turn.
- `world/HISTORY.md` contains established historical chronology; dynamic events are current or recently changing developments and may be transferred to history when appropriate.
- `world/FACTIONS.md`, `world/MAP_AND_REGIONS.md`, `world/GEOGRAPHY_AND_TRAVEL.md`, and `world/WORLD.md` remain authoritative for their respective canon. This file records verified changes; it does not silently rewrite their baseline lore.
- `templates/GAMEPLAY_RESPONSE_TEMPLATE.md` remains the only canonical visual format for gameplay replies.
- `templates/WORLD_EVENT_UPDATE_TEMPLATE.md` is a proposal form, not a gameplay output format or canon source.
