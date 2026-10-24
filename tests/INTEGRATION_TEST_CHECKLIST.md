# Xuanling Realm — Integration Test Checklist

**Status:** Audit aid, not a source of new mechanics.  
**Purpose:** Check whether the GM applies existing modules together without creating extra rules. If a test exposes a gap, update the canonical module first; do not treat this checklist as a replacement for it.

## How to Run

- Use a disposable test character/profile, not a live player save.
- Record the starting timestamp and every relevant state value.
- For each scenario, verify both the narration and the final profile.
- Mark a case **PASS** only when the result follows the cited sources and no unsupported value is invented.

## Core Integration Cases

| ID | Scenario | Required sources | Pass condition |
|---|---|---|---|
| BOOT-01 | Start a new session with a registered character | `INDEX.md`, `templates/GM_PROMPT.md`, `world/DYNAMIC_EVENTS.md`, `players.md`, character snapshot, response template | Follows bootstrap order, checks current world events, reads the correct snapshot, establishes a consistent starting timestamp, and starts gameplay directly. |
| BOOT-02 | Continue/recall a session while a world event has changed | `INDEX.md`, `world/DYNAMIC_EVENTS.md`, latest gameplay profile/history, relevant modules | Uses the latest session state, checks the current event registry, and never restores an old character snapshot or stale event state. |
| EVENT-01 | A player declares an action intended to change a faction or region, but the action fails | Combat/action module as relevant, `world/DYNAMIC_EVENTS.md`, event proposal template | Does not register the intended result as a confirmed event; no proposal describes failure as success. |
| EVENT-02 | A resolved action creates a persistent world-level consequence | Relevant mechanics/world modules, `world/DYNAMIC_EVENTS.md`, `templates/WORLD_EVENT_UPDATE_TEMPLATE.md` | Creates a proposal with a supported outcome and evidence; does not claim it is canon or saved before admin approval and commit. |
| EVENT-03 | An active event affects an NPC, but the player has no access to that information | `world/DYNAMIC_EVENTS.md`, relevant faction/world modules, GM Prompt | Applies world consequences consistently while preserving the distinction between public facts, witnessed knowledge, rumor, and hidden information. |
| EVENT-04 | A player submits a proposed event update | `world/DYNAMIC_EVENTS.md`, `templates/WORLD_EVENT_UPDATE_TEMPLATE.md` | Treats the proposal as non-canon until owner/admin review and repository verification. |
| EVENT-05 | An active event reaches its recorded end condition | `world/DYNAMIC_EVENTS.md`, relevant world/mechanics modules | Updates/resolves the event only when supported; preserves history and does not duplicate the event under a new ID without reason. |
| STATE-01 | Continue a session after the character snapshot has become outdated | Last gameplay profile, event history, character profile template | Uses the latest recorded state and never restores the old snapshot over it. |
| TIME-01 | Perform an ordinary action lasting 4 hours | `gameplay/TIME_AND_ACTION_RULES.md` | Does not silently accept a duration beyond the ordinary 3-hour limit; resolves or asks for a valid split. |
| HUNGER-01 | Advance time through awake activity and protected night sleep | `core/HUNGER_AND_METABOLISM.md`, Time Rules | Reduces Satiety only for applicable awake time; protected sleep does not reduce Satiety or count missed meal windows. |
| HUNGER-02 | A character has a recorded innate trait affecting hunger tolerance, but no numeric modifier | Hunger and Metabolism, GM Prompt | Describes the trait qualitatively without granting full immunity or inventing a numeric Satiety modifier. |
| COMBAT-01 | A declared combo's first strike misses | `gameplay/COMBAT_SYSTEM.md`, HP and Injury | No default bonus follow-up occurs; the GM does not add a free hit. |
| COMBAT-02 | A combo's first strike hits, then the target becomes unable to continue fighting | Combat, HP and Injury | Resolves the first strike's consequences before deciding whether a follow-up remains feasible; does not force a meaningless hit or invent a retarget. |
| COMBAT-03 | An attack hits and causes an injury | Combat, HP, Injury, Time, Hunger and Metabolism | HP loss and injury are tracked separately; time and Satiety are updated only when applicable. |
| RING-01 | A Spirit Beast is defeated and its ring appears | Spirit Ring Rules, Spirit Beast Rules, Cultivation System | Does not treat defeat as automatic absorption; checks ring requirements, item requirements, compatibility, and valid timing. |
| RING-02 | A ring is successfully absorbed | Spirit Ring Rules, Spirit Beast Rules, Character Profile Template | Records the new ring and all required derived values from supported inputs; unknown inputs remain unknown. |
| ECON-01 | A purchase or sale changes the character's money | Economy, character profile, event record | Uses the official currency/value rules and records the transaction; no unexplained balance changes. |
| WORLD-01 | The character travels to a new region or meets an unfamiliar people group | Geography and Travel, Map and Regions, Intelligent Peoples, World/FACTIONS as relevant | Uses established routes, travel methods, and group lore; does not invent distances, travel times, or universal behavior. |
| OUTPUT-01 | Any gameplay response is completed | `templates/GAMEPLAY_RESPONSE_TEMPLATE.md` | Uses the canonical order and field names, keeps the state consistent, and ends with `Aksiku : --` in MODE: NO STEP. |

## Audit Notes

- A test case does not authorize a new mechanic. If the sources cannot determine a result, record the gap and keep the result qualitative or ask for a decision.
- Do not use Yuha or any live character as a test fixture; use a disposable profile.
- Re-run the affected cases after changing combat, time, Satiety, Spirit Ring, HP, injury, economy, profile rules, bootstrap order, or event lifecycle.
