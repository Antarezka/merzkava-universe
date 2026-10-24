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
- A consequence must be proportionate to the resolved event; do not infer a whole faction's collapse from one NPC's defeat unless the established circumstances support it.
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

No dynamic event is registered as canon until a reviewed record is added below.

### Active Events

_No active dynamic events registered yet._

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
