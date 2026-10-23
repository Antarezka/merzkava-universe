# Xuanling Realm — Turn-Based Combat System

**Status:** Official combat mechanics v1.
**Scope:** Turn order, initiative, comparative combat power, hit chance, damage as a percentage of HP, defense, injury, Realm-gap consequences, and Thinker/Artificial Artifact integration.

This module uses `core/HP_SYSTEM.md` for maximum HP and `core/SPIRIT_RING_RULES.md` for PowerScale, ring age, compatibility, and Qi. It does not replace those formulas.

## 1. Core Principles

- Combat is turn-based. Resolve one meaningful combat action per turn, then update the scene and state before the next action.
- PowerScale is the baseline comparison for characters whose PowerScale can be calculated. It is not damage, a hit guarantee, or an automatic victory.
- Readiness, technique, usable energy, position, awareness, and relevant equipment affect combat outcomes.
- Do not invent a character's equipment, techniques, ring age, Qi, HP, artifact functions, or combat history.
- A fight is resolved through the sequence of actions and consequences, not by a single roll that automatically decides the whole battle.
- Death remains permanent unless an established official mechanic explicitly prevents it.
- If a required numerical input is unknown or PowerScale cannot be calculated for a combatant, do not fabricate a precise Combat Power. Resolve only the supported parts and identify the missing input.

## 2. Initiative — Who Acts First

Use the first applicable rule:

1. **Established action:** If a combatant has already launched a valid attack, prepared an ambush, or gained initiative through a clearly established event, resolve that advantage first.
2. **Clear situational advantage:** If position, awareness, speed, restraint, or another recorded fact clearly gives one side initiative, that side acts first. Explain the cause.
3. **Unclear initiative:** Each side rolls a virtual d100 (1–100). The higher result acts first. A tie is rerolled. State the rolls; never claim a roll occurred unless it was actually resolved.

Initiative decides order, not whether an attack automatically hits. A first strike can still miss, be blocked, or be countered when the established situation allows it.

## 3. Combat Readiness Inputs

Before calculating an attack, record these scores from established facts. Each score is 0–100; it is not a new character-profile field.

- **E — Equipment readiness:** suitability, condition, protection, and actual availability of equipment for this action.
- **T — Technique readiness:** relevant technique mastery, control, and suitability for the chosen action.
- **Q — Energy readiness:** current usable Qi or stamina as a percentage of the character's recorded maximum or supported available capacity. If no valid current/max values exist, mark Q unknown instead of guessing.
- **S — Situation factor:** the concrete tactical situation, selected from the table below.

Do not score a factor from personality or narrative praise alone. Explain the evidence briefly when a score materially affects the result.

### 3.1 Readiness multiplier

When E, T, and Q are all known:

`Readiness = 0.70 + 0.001E + 0.001T + 0.001Q`

Range: 0.70–1.00. This represents reduced effectiveness when combat preparation or usable energy is poor; it does not create power beyond the baseline.

### 3.2 Situation multiplier

| Established situation | Multiplier |
|---|---:|
| Severe disadvantage | 0.80 |
| Disadvantage | 0.90 |
| Neutral / no supported edge | 1.00 |
| Advantage | 1.10 |
| Decisive advantage | 1.20 |

Use only the category supported by current position, awareness, terrain, restraint, numbers, or other concrete circumstances. Do not count the same fact twice. If the situation cannot be assessed, use 1.00 and state the uncertainty.

## 4. Effective Combat Power

For a combatant with a valid PowerScale:

`Effective Combat Power (ECP) = PowerScale × Readiness × Situation × Artifact Factor`

- PowerScale comes only from `core/SPIRIT_RING_RULES.md`.
- Readiness is calculated by §3.1 when all three inputs are known.
- Situation is selected under §3.2.
- Artifact Factor is defined in §7. If no relevant Artificial Artifact effect applies, use 1.00.
- If a required input is unknown, do not pretend the ECP is exact. Compare only supported values or resolve the action qualitatively until the missing data is established.

PowerScale already includes total Spirit Ring age and overall ring compatibility. Do **not** multiply ring age or compatibility into ECP again. Ring abilities may affect a specific action only through a documented ability or an explicitly established effect.

## 5. Hit Chance

When both combatants have calculable ECP:

`Power Ratio (R) = Attacker ECP / Defender ECP`

`Base Hit Chance = clamp(10, 90, 50 + 25 × (R − 1))%`

Then apply a situational accuracy adjustment only when supported by a concrete, non-duplicated factor:

| Accuracy circumstance | Adjustment |
|---|---:|
| Severe disadvantage | −20 percentage points |
| Disadvantage | −10 percentage points |
| Neutral | 0 |
| Advantage | +10 percentage points |
| Decisive advantage | +20 percentage points |

Final Hit Chance is clamped to **5%–95%**. Do not apply the same positional or awareness advantage both as a Situation multiplier and an accuracy adjustment; choose the place where it matters most.

Resolve the attack with a d100 roll: the attack hits if the result is equal to or below Final Hit Chance. State the chance and roll. A hit still allows defense or mitigation; a miss does not automatically mean the defender gets a free attack.

If ECP cannot be calculated, do not invent a numeric hit chance. Use established narrative facts and the initiative roll only where applicable, and flag the missing combat baseline.

## 6. Damage as a Percentage of Maximum HP

Damage is calculated only after an attack hits and the chosen action is supported by the character's known abilities.

### 6.1 Base damage by action class

| Action class | Base damage |
|---|---:|
| Basic physical strike | 5% of target's maximum HP |
| Trained combat technique | 8% |
| Spirit Ring ability / documented special technique | 12% |
| Decisive or high-output technique | 18% |

Choose the class based on the actual documented move and its demonstrated scope, not merely the narration used to describe it. The 18% class is not automatically available to every character; the technique must be established and the character must be able to perform it. These percentages are baseline damage before power ratio and defense.

### 6.2 Power-ratio adjustment

`Power Damage Factor = clamp(0.50, 1.50, √R)`

`Damage before defense = Target Max HP × Base Damage % × Power Damage Factor`

This caps the effect of a large power gap so a single hit does not scale without limit. Round final HP damage up to the nearest whole HP, with a minimum of 1 HP for a successful damaging hit.

### 6.3 Defense reduction

Choose a defense reduction only from established armor, a defensive technique, a barrier, or an applicable artifact effect:

| Demonstrated defense against this attack | Damage reduction |
|---|---:|
| No meaningful defense | 0% |
| Limited defense | 10% |
| Moderate defense | 25% |
| Strong defense | 40% |
| Exceptional defense | 50% |

`Final Damage = round up(Damage before defense × (1 − Defense Reduction))`

Defense reduction cannot exceed 50% through this generic table. A special ability may exceed this only if its official description explicitly supports it. Do not apply the same defense twice.

Use **target maximum HP** from `core/HP_SYSTEM.md` as the percentage base. Subtract the resulting integer damage from current HP; never set current HP above maximum or automatically restore it when Realm/Stage changes. If current HP or maximum HP is unknown, report the missing value instead of fabricating a final HP total.

## 7. Thinker and Artificial Artifact Integration

Thinker Grade is independent from cultivation Realm. The production chance matrix in `core/THINKER_AND_FORMULATION.md` governs **making** an Artificial Artifact; it is not a combat hit chance and must never be reused as one.

For combat:

1. Confirm that the character actually owns, carries, controls, and can activate the Artificial Artifact.
2. Confirm its recorded tier and documented function. Do not invent powers, range, ammunition, energy source, durability, or limitations.
3. If an artifact's function is relevant to the current action, apply that documented effect to the applicable step: initiative, ECP, hit chance, damage, defense, range, or battlefield control.
4. If two Artificial Artifacts directly contest the same function and both tiers and functions are known, use this comparison modifier:
   - Each tier the acting artifact exceeds the opposing relevant artifact: **+5% Artifact Factor**, up to **+20%** total.
   - Each tier it falls below the opposing relevant artifact: **−5% Artifact Factor**, down to **−20%** total.
   - Equal tiers: no tier modifier.
   - Artifact Factor = 1.00 plus/minus the applicable modifier.
5. The tier comparison applies only when the artifacts have relevant, comparable functions. A higher-tier artifact does not automatically defeat an unrelated artifact, a cultivator, or a technique. If the opponent has no comparable artifact, do not assign a tier-comparison bonus; use only the artifact's documented function.
6. Do not apply a tier modifier twice or add an effect already included in E, T, Situation, hit chance, or defense. If the artifact's function is unknown, its combat effect is `???` until established.

Relics, Ancient Artifacts, and Artificial Artifacts remain distinct by origin. Do not apply Artificial Artifact tier rules to the other categories unless their own official rules say so.

## 8. One-Realm Gap and Injury Consequences

A character one full Spirit Realm below an opponent can still fight and can win through supported tactical, equipment, technique, energy, or ring advantages. A Realm gap alone does not automatically decide the fight.

However, if the higher-Realm combatant lands a damaging hit on the lower-Realm combatant, injury is expected in addition to HP loss. The lower-Realm combatant cannot simply avoid injury by narration. Injury may be avoided only when the lower-Realm combatant has a **clear, evidence-backed overall readiness advantage**, including:
- better relevant equipment readiness;
- better usable Qi/energy readiness; and
- a meaningful advantage in Spirit Ring age/quality or relevant ring ability, where a valid comparison exists.

Technique mastery and tactical situation may also contribute, but do not replace the three checks above. If those comparisons are unknown or do not show a clear advantage, record at least a light injury when the higher-Realm combatant's damaging hit lands. More serious injuries must be proportionate to the actual attack and consequences; do not assign a severity solely because the attacker is higher Realm.

This rule applies to a **one-Realm difference**. Larger gaps require the GM to assess the actual canon and circumstances; do not extrapolate automatic outcomes or invent a universal Realm multiplier.

## 9. Turn Resolution and State Updates

For each combat turn:

1. Establish initiative if not already established.
2. State the acting combatant and one main action.
3. Check whether the action is possible with current position, condition, equipment, and usable energy.
4. Calculate ECP and hit chance if all required values are available.
5. Resolve hit/miss and defense.
6. Calculate HP damage using §6 if a damaging hit lands.
7. Record injury, interrupted actions, broken/damaged equipment, resource use, changed position, and other consequences only when supported.
8. Update current HP, Qi/stamina, condition, position, and timestamp according to valid events and `gameplay/TIME_AND_ACTION_RULES.md`.
9. End the turn at a natural decision point. Do not resolve multiple independent major actions for one combatant in a single turn.

A combatant may surrender, retreat, become incapacitated, or die when the events and rules support that result. Do not force a fight to continue after a valid ending condition, and do not grant plot armor.

## 10. Undefined Inputs and Special Damage

- If a numeric input, ability effect, resource cost, or combat baseline is not established, mark it unknown and do not fabricate precision.
- Spirit Ring deviation is not automatically a combat attack. If its own numeric damage rule remains undefined, keep that damage qualitative rather than applying an arbitrary attack class.
- Do not invent healing rates, injury recovery durations, stamina costs, artifact charges, or special exceptions.
- Record damage as `HP lost: N (X% of target maximum HP)` and update the profile's current/max HP.
- Revisit and revise this module only through an explicit canon change by the repository owner.
