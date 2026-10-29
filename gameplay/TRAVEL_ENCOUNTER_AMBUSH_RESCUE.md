# Merzkava Universe — Travel Encounter, Ambush & Emergency Rescue

**Status:** Official gameplay procedure.
**Scope:** Travel-segment encounter checks, separate ambush checks, and emergency rescue attempts involving wandering Medicine Hall Society healers.
**Authority:** This module governs these procedures and probabilities only. It does not override canon routes, dynamic events, combat, HP, injury, time, economy, faction lore, or character-state rules.

## 0. Wandering Teacher Encounters

For unplanned encounters with potential teachers or independent practitioners, also apply `world/OPEN_LEARNING_PATHS_AND_WANDERING_INSTRUCTORS.md`. This check is distinct from ambush and emergency rescue checks: do not combine their rolls, reuse their outcomes, or trigger them merely because the player is injured. Consider a single wandering-teacher/general encounter check when a scene provides a genuine opportunity—travel, exploration, public activity, entering a settlement, seeking instruction, or an appropriate time skip. The learning-path module defines the virtual d100 procedure and location-fit constraints.

A wandering teacher may appear without belonging to any faction, but must have a plausible route, purpose, knowledge, and reason to be present. Do not place one inside sealed/private/secure locations or hidden and dangerous areas without grounded access. Do not make a teacher automatically willing, able, safe, affordable, or personally invested in the player. Finding one does not grant techniques, Spirit Realm progress, Thinker Grades, artifacts, or examination passes; all official mechanics and character-state rules remain binding.

## 1. Mandatory Use

Whenever a player travels outside a settlement or through a route segment where an encounter could reasonably occur, consult this module. Before resolving travel, verify the confirmed route, terrain, transport, duration, intermediate stops, restrictions, and relevant events using `world/LOCATION_AND_ROUTE_NETWORK.md`, `world/MAP_AND_REGIONS.md`, `world/GEOGRAPHY_AND_TRAVEL.md`, relevant regional modules, `world/DYNAMIC_EVENTS.md`, and `gameplay/TIME_AND_ACTION_RULES.md`.

Do not invent routes, exact distances, travel times, local threats, named NPCs, medical stations, or confirmed presence from an unverified map gap. The probabilities below are GM mechanics, not evidence that a particular encounter, threat, healer, or route exists.

## 2. General Travel Encounter Check

Run one General Encounter check when the player genuinely enters a new, confirmed route segment. An encounter is not automatically hostile and does not automatically start combat.

| Confirmed segment character | Base chance |
|---|---:|
| Busy road outside a settlement | 5% |
| Regular intercity or trade route | 10% |
| Quiet village route | 15% |
| River crossing or forest route | 20% |
| Dense forest or remote mountain route | 25% |
| Wild zone with confirmed danger | 35% |

`P_E = clamp(0%, 60%, B_E + M_E)`

- `P_E`: final encounter probability.
- `B_E`: base chance from the table.
- `M_E`: evidence-supported modifiers in percentage points, such as recorded trade activity, a relevant active event, or a known local condition.
- Clamp the final chance to 0–60%. Do not add modifiers merely to make a scene more exciting.

Roll virtual d100 once; the check succeeds if the result is at or below `P_E`. Possible outcomes include a helpful, neutral, or friendly wandering NPC; a merchant, caravan, hunter, courier, or passing group; conversation, rumor, services, trade or help offers; signs of a Spirit Beast; environmental obstacles; or a suspicious/opportunistic person where the circumstances support it.

An encounter does not guarantee a reward, threat, or interaction the player must accept. NPCs act according to established traits, knowledge, affiliations, goals, relationships, resources, and circumstances. Do not make a neutral NPC hostile solely to force combat.

## 3. Separate Ambush Check

Ambush is checked separately from General Encounter. Run the check only when there is a plausible, evidence-supported basis for an ambush-capable threat, such as a recorded hostile group, credible local warning, relevant active threat, or a location/threat combination supported by canon. A dangerous-looking place alone does not prove that a specific attacker is present.

| Threat evidence before the check | Base chance |
|---|---:|
| No qualifying threat evidence | 0%; do not roll |
| Potential threat with limited evidence | 5% |
| Plausible ambush risk supported by context | 10% |
| Confirmed hostile threat nearby, outcome unresolved | 20% |
| Ambush already confirmed and underway | Do not reroll its existence |

`P_A = clamp(0%, 50%, B_A + M_A)`

`P_A` is the final ambush probability, `B_A` the base chance, and `M_A` evidence-supported modifiers in percentage points. Clamp to 0–50%. Terrain, weather, time, escort, or alertness can modify the chance only where they materially affect the threat's ability to attack or be detected. Do not double-count one condition. Roll virtual d100 once; success occurs at or below `P_A`.

Ambush means an active hostile or emergency threat, not merely an unfriendly conversation. Supported outcomes may include forced combat against hostile NPCs or a Spirit Beast, coercion under a credible threat demanding money or player-owned items, traps, natural disasters, sudden hazards, or another dangerous event supported by canon.

Probability alone does not determine attacker identity, number, strength, motives, loot, damage, or outcome. For combat use `gameplay/COMBAT_SYSTEM.md`; for injuries use `core/HP_SYSTEM.md` and `core/INJURY_SYSTEM.md`; resolve time using `gameplay/TIME_AND_ACTION_RULES.md` and `core/HUNGER_AND_METABOLISM.md` where relevant.

### Property and currency changes

Do not automatically subtract money or delete inventory because an extortion attempt occurs. Resolve the player's response and the NPC's actual actions. Record only currency or items truly surrendered, seized, lost, recovered, or otherwise changed, following `templates/AUTHORITY_ORDER.md` and `core/10_ECONOMY_SYSTEM.md`. Do not invent an automatic payment or guaranteed escape.

## 4. Segment Procedure and Continuity

1. Verify route, terrain, transport, duration, restrictions, and relevant active events.
2. Run one General Encounter check.
3. Separately run one Ambush check only if qualifying threat evidence exists.
4. If an ambush occurs, resolve it as the principal event. Do not automatically add a second unrelated encounter from the same check cycle.
5. If no ambush occurs, resolve a successful General Encounter, if any.
6. If neither check triggers, travel continues without a forced event.
7. If the player enters a genuine emergency, follow Section 5.

A segment is a confirmed route edge, not an arbitrary GM-created time slice. If travel across it takes multiple gameplay turns due to the action-duration limit, preserve its check status and results; do not reroll because a turn passed or narration continued. A new check cycle starts only when the player actually enters the next confirmed segment. A new material event may change the current situation but does not automatically reroll an old check.

Keep unresolved results in session continuity. If the result is unavailable in the current conversation, do not pretend to remember it or silently reroll; disclose the gap and reconcile from the latest verifiable state.

## 5. Emergency Rescue — Wandering Medicine Hall Society Healer

### 5.1 Activation and chance

Emergency Rescue becomes eligible when a resolved event leaves the player alive but in a genuine emergency requiring prompt assistance: for example, a life-threatening injury, incapacitation, dangerous exposure, severe poisoning, being trapped, or another urgent condition supported by the event. Do not trigger it for every minor wound or ordinary fatigue. Use official HP and injury rules; do not infer a diagnosis from an HP number alone. Under `core/HP_SYSTEM.md`, HP reaching 0 means death; this rescue procedure does not revive a dead character. The sole anti-cheat second-violation death rule is an absolute exception to all normal rescue.

This check is independent of General Encounter and Ambush. An emergency does not guarantee that a healer is nearby or that rescue succeeds.

| Current situation and location | Base chance to encounter a wandering healer |
|---|---:|
| Busy route or near a populated settlement | 20% |
| Ordinary interregional or intercity route | 10% |
| Remote forest or dangerous mountain wilderness | 5% |
| Concrete evidence of a nearby healer, medical mission, or Society activity | Add 10–20 percentage points |

`P_R = clamp(0%, 50%, B_R + M_R)`

`P_R` is the final probability of encountering a wandering healer, `B_R` is the single base chance selected from the location row, and `M_R` is the sum of distinct, evidence-supported modifiers in percentage points. The evidence row is a modifier, not an alternative base chance. Calculate `P_R = min(50%, max(0%, B_R + M_R))`. Do not infer a healer's presence just because the player needs one. The Medicine Hall Society is a neutral medical network, but universal staffing, free treatment, guaranteed supplies, and a healer at every location are not established. Consult `world/FACTIONS.md` and the relevant regional/service module when a specific branch or service point matters. If the character is already at a confirmed clinic or regional hall, use that service point's established location/staffing context rather than rolling to invent a wandering healer.

Perform one rescue check when the emergency first becomes established. Do not reroll every turn while the player remains injured or unconscious. A new check is allowed only when a materially new circumstance creates a legitimate new opportunity, such as reaching a populated route or a medical party newly entering the area. If a healer's presence is already confirmed, do not roll to decide whether they exist; resolve whether they can detect, reach, and assist the player. Never reroll whether an ongoing ambush exists.

### 5.2 Rescue and medical effort

On a successful check, the GM may introduce a wandering NPC affiliated with the Medicine Hall Society if consistent with the location and canon. Select or generate traits without contradicting established profiles, registries, or lore. Once introduced, the NPC's identity and personality persist.

At minimum, the healer attempts to move the player away from the ambush point or conceal them in a comparatively safer location, if their ability and circumstances permit. This is an attempt, not guaranteed extraction: attackers, terrain, the player's condition, the healer's capability, or other hazards may prevent or interrupt it.

After immediate safety is addressed, the healer provides care according to demonstrated/established competence, available medicine and tools, the patient's condition, time, surrounding danger, and personality. The rescue encounter roll is **not** a roll for treatment success. Resolve extraction, diagnosis, stabilization, procedures, and recovery as distinct steps supported by the scene and official rules. Finding a healer does not guarantee full recovery, freedom from injury, or survival. If the attempt fails, resolve the consequences fairly rather than granting automatic protection.

Personality is randomized by the GM when appropriate, while respecting known NPC canon. Suggested patterns:
- **Compassionate:** helps willingly and makes a sincere effort with available supplies.
- **Professional/pragmatic:** stabilizes the patient and provides appropriate care; may request a reasonable fee if consistent with the NPC.
- **Reluctant/indifferent:** offers limited aid, conserves scarce supplies, or avoids risky further treatment.
- **Materialistic:** may request payment or a guarantee before continuing treatment.
- **Exploitative:** may use the patient's vulnerability to demand money or items in exchange for further care.

These are behavior guides, not a closed list. Do not assume all Society members share one temperament. Personality affects willingness and effort, not automatic medical success: a compassionate healer can lack skill or supplies for a grave injury, while a reluctant healer may successfully perform a simple procedure.

A healer may stabilize the player, then demand payment for further treatment. If the player refuses, the healer may negotiate, limit further voluntary care, or leave if consistent with the established character. Do not retroactively erase aid already given. If the healer threatens or forcibly takes property, resolve that as an actual NPC action. Society affiliation does not prove the Society endorses extortion.

### 5.3 Medical and economic continuity

Apply treatment only to the extent supported by the healer's established ability, actual resources, and official HP/injury rules. For injury progress, use `core/INJURY_SYSTEM.md` and its class-specific rates per 24 in-world hours; use the treated rate only when the treatment and any structural/stabilization prerequisites are actually completed. For HP, use `core/HP_SYSTEM.md`: no numerical HP recovery may be invented, and injury progress never converts into HP. Stabilization is not a cure and does not itself restore HP unless an explicit official effect says so. Do not invent instant cures, rare medicine, or guaranteed outcomes. Record medicines used, injuries treated, residual symptoms, treatment time, and recovery requirements. Record fees, debts, item transfers, or property seizure only when they actually occur; currency and item state must match the continuous ledger and character profile. Preserve the healer's identity, affiliation, personality, knowledge, actions, promises, and relationship in later scenes.

If rescue or treatment creates a lasting world-level effect, follow the proposal workflow in `world/DYNAMIC_EVENTS.md`. Ordinary private treatment or a character-only injury change does not automatically qualify as a world event.

## 6. Fairness and Source Priority

- A probability is a chance, not a guarantee. Respect the roll; never reroll solely to obtain a preferred result.
- Do not force every encounter to be hostile, every ambush to be winnable, or every emergency to receive rescue.
- Do not create a healer solely to protect the player or suppress a plausible rescue solely to punish the player.
- Do not change currency, inventory, HP, injuries, time, or relationships without a resolved cause.
- A successful healer-encounter check only establishes a plausible encounter; it does not guarantee extraction, treatment success, HP recovery, injury recovery, or survival.
- Never use normal emergency rescue to override HP 0 death or the permanent death sanction defined in `templates/ANTI_CHEAT_HARD_GATE.md`.
- Preserve NPC agendas, knowledge boundaries, and established traits.
- This module does not override canon decisions, regional rules, combat, HP/injury, economy, time, or recorded dynamic events. When a conflict appears, follow the established source hierarchy and flag unresolved contradictions.

## 7. GM Quick Checklist

**Travel:** verify route and events → General Encounter check → separate Ambush check only when justified → resolve one coherent outcome → preserve segment state.

**Emergency:** verify genuine emergency → check rescue chance once → if successful, establish a plausible wandering Medicine Hall Society healer → attempt safety/extraction → resolve care, effort, payment, injuries, time, and continuity under official rules.
