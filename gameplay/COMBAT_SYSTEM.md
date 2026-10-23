# Xuanling Realm — Combat System

**Status:** Combat baseline v1.  
**Purpose:** Give the GM one repeatable method for resolving varied fights without inventing abilities or overloading every scene with calculations.

## 1. Core Rules

- Use this module for combat resolution, `core/SPIRIT_RING_RULES.md` for PowerScale/Qi, and `core/HP_SYSTEM.md` for maximum HP.
- PowerScale is a baseline comparison, not a guaranteed hit or victory.
- A turn is a combatant's opportunity to perform **one declared action**. It is not a limit of one physical hit: an action may contain several strikes when the established move or circumstances support them.
- Do not invent combo rules, extra hits, bonus damage, techniques, equipment, costs, or effects. A dedicated combo rule can be added later without changing this basic turn structure.
- Resolve actions in order and apply consequences. Do not decide the whole fight with one roll.
- Death is permanent unless an established official mechanic says otherwise.

## 2. Resolve Each Turn

Follow this short sequence:

1. **Initiative:** Respect an attack already underway, an ambush, or a clear established advantage. If neither side has initiative, both roll virtual d100; higher result acts first, ties reroll.
2. **Action and feasibility:** Identify the declared action, its target, range, required ability, current resources, and whether the character can perform it in the current situation.
3. **Compare combat readiness:** Use the PowerScale baseline and only relevant, evidenced advantages or disadvantages. Do not count the same advantage twice.
4. **Resolve the action:** Determine hit/miss, defense, damage, and any documented special effect.
5. **Update state:** Record HP/Qi or stamina changes, injuries, position, equipment, and elapsed time when they actually change. Stop at a natural decision point.

Initiative determines who acts first; it does not guarantee a hit. A defender may block, evade, counter, or be interrupted only when the situation and established abilities support it.

## 3. Combat Rating and Hit Chance

When both characters have a valid PowerScale:

**Combat Rating = PowerScale × Readiness Factor × Relevant Artifact Factor**

- **Readiness Factor:** choose one overall factor based on current usable energy, applicable technique, equipment, and tactical position.
- Use **0.80** for a clear severe disadvantage, **0.90** for a disadvantage, **1.00** when neither side has a clear evidenced advantage, **1.10** for an advantage, and **1.20** for a decisive advantage.
- This is one combined assessment, not a separate bonus for each category. Do not add another multiplier or accuracy bonus for the same facts.
- **Relevant Artifact Factor:** use **1.00** unless an owned, available artifact has a documented effect relevant to this specific action. A higher tier alone is not a universal combat bonus.
- Missing information is not proof of an advantage or disadvantage. If a missing key value prevents a fair comparison, do not claim an exact numeric result; resolve only what the evidence supports.

Calculate the ratio:

`R = Attacker Combat Rating / Defender Combat Rating`

**Hit chance = clamp(10%, 90%, 50% + 25% × (R − 1))**

Roll d100. The attack hits if the roll is at or below the hit chance. If the combat rating cannot be calculated, do not invent a numeric hit chance; resolve the supported parts qualitatively.

## 4. Damage and Defense

Use the move's documented effect when it exists. If no specific damage value exists, use this baseline:

| Action type | Base damage |
|---|---:|
| Basic physical attack | 5% of target maximum HP |
| Trained combat technique | 8% |
| Spirit Ring ability or documented special technique | 12% |
| Documented high-output/decisive technique | 18% |

These are baseline classes, not permission to invent a move. Choose the lowest class that accurately fits the documented action. The 18% class requires a clearly established technique and sufficient ability/resources to use it.

**Power adjustment:** `Damage = Target Max HP × Base Damage % × clamp(0.50, 1.50, √R)`

Then apply only a defense that is actually present and relevant:

| Defense demonstrated against the attack | Reduction |
|---|---:|
| None or ineffective | 0% |
| Limited | 10% |
| Moderate | 25% |
| Strong | 40% |
| Exceptional, explicitly supported | 50% maximum |

Round final damage up to a whole HP; a successful damaging hit deals at least 1 HP. Record damage as `HP lost: N (X% of target maximum HP)`. Use target maximum HP as the damage base, but subtract the result from current HP. If current or maximum HP is unknown, do not fabricate it; consult `core/HP_SYSTEM.md`.

## 5. Multiple Hits, Combos, and Special Effects

- One declared action can contain multiple hits when the established move or situation supports them. Do not force every strike into a separate turn merely because there are multiple hits.
- **Combo bonuses are not defined yet.** A future combo rule can grant additional attacks/bonuses once its conditions and effects are decided. Until then, do not award extra hits, damage, accuracy, or other bonuses merely because the narration calls something a combo.
- For a documented multi-hit move, apply only the number of hits and effects supported by its description. If the move does not define how its hits resolve, state the uncertainty and avoid inventing precision.
- Control, piercing, area attacks, damage over time, healing, counters, and other special effects use their documented effects. Do not force them into a damage formula when their main effect is not HP damage.
- Do not apply a full single-target damage value to every target of an area attack unless its documented rules support that result.

## 6. Realm Difference and Injury

A lower-Realm fighter can defeat a higher-Realm opponent when the recorded situation and relevant advantages support it; Realm alone is not an automatic result.

When the combatants differ by **one Realm**, a damaging hit from the higher-Realm combatant is expected to cause injury to the lower-Realm combatant. Avoiding injury requires clear evidence of an overall advantage that addresses all three:
1. Better equipment readiness.
2. More usable Qi/energy for the relevant action.
3. A meaningful Spirit Ring age/quality or relevant ability advantage.

Tactics and technique may contribute, but do not silently replace all three conditions. If the evidence is incomplete, apply at least a light injury and scale severity to the actual event. Do not extrapolate this rule into an invented universal multiplier for larger Realm gaps.

## 7. PowerScale, Spirit Rings, and Thinker

- PowerScale comes only from `core/SPIRIT_RING_RULES.md`; it already includes total Spirit Ring age and overall ring compatibility. Do not multiply those factors again.
- A Spirit Ring ability affects combat only through its established ability and actual use.
- The production chance matrix in `core/THINKER_AND_FORMULATION.md` governs artifact creation, **not** attack accuracy.
- Before applying an Artificial Artifact, confirm ownership/access, tier, documented function, limitations, and whether that function applies to the current action. Relics, Ancient Artifacts, and Artificial Artifacts remain distinct categories.
- If artifact effects or other required values are undefined, mark them unknown instead of making up a number.

## 8. State and Missing Rules

After each resolved action, update only changes caused by the action: current HP, usable Qi/stamina, injury, position, equipment, inventory, and time. Do not restore HP, refill resources, or remove consequences without an established cause.

If a rule or input is missing:
- Do not invent numerical precision or claim an undefined rule is official.
- Resolve the parts that are supported by the current sources.
- Keep undefined special damage or effects qualitative.
- Flag the missing rule so it can be added deliberately to this module later.

**GM quick check:** initiative → action feasibility → combat rating/hit → defense/damage/effects → state update.