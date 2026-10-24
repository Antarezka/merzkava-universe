# Xuanling Realm — Time and Action Rules

Status: Official gameplay procedure module.
Scope: Timestamp continuity, session calendar, action duration, time skips, cultivation duration, and separation of meditation, cultivation, and Spirit Ring absorption.

## 1. Timestamp Format and Authority

The exact timestamp line format and its position in every gameplay response are defined only in `templates/GAMEPLAY_RESPONSE_TEMPLATE.md`. Do not create a second timestamp layout in this module. This module defines how to establish, advance, and validate the timestamp values.

- Fill every timestamp field with a concrete value once gameplay begins. Do not leave placeholders in a live gameplay timestamp.
- The displayed year and era are session-calendar details unless established as global canon.
- **New session without a prior timestamp:** establish one plausible starting timestamp, including year, session era, season, date, weekday, weather, and local time. Use it consistently thereafter.
- **Continuing session:** use the last valid timestamp in the conversation as the sole starting point. Never reroll or restart the calendar merely because a new turn begins.
- If the player explicitly supplies a valid starting timestamp, use it unless it conflicts with already recorded events.
- If timestamps conflict, flag the conflict and do not silently overwrite established history.
- A session calendar created to fill a canon gap is a working session calendar, not automatically global world canon.

## 2. Working Calendar When No Canon Calendar Is Available

Use this consistent fallback only when no prior session calendar exists:

- 12 months per year; 30 days per month.
- Months 1–3: Semi.
- Months 4–6: Panas.
- Months 7–9: Gugur.
- Months 10–12: Dingin.
- Weekday cycle: Senin, Selasa, Rabu, Kamis, Jumat, Sabtu, Minggu, repeating continuously.

When a date passes day 30, advance to day 1 of the next month. After month 12, advance to the next year and month 1. Calculate weekday and season using the same session calendar. Do not replace an already established calendar mid-session. If an official calendar is later found to conflict, flag it instead of silently rewriting past timestamps.

## 3. Time Advancement and Weather

- Advance time only for actions or events that actually occur.
- Keep duration plausible for the action, travel, conversation, rest, transaction, or environmental event described.
- If no meaningful time passes, do not make an unexplained large time skip.
- When an action takes 20 minutes, advance the clock by 20 minutes and roll over the date only if necessary.
- Keep hour, date, weekday, month, season, and elapsed duration mathematically consistent.
- Set initial weather plausibly for the location and season. Keep it stable until an event or plausible passage of time justifies a change; do not reroll weather every turn.
- Location changes require a supported travel/action event. Do not invent distances or travel times where the map/world modules do not support them.

## 4. Action Duration Limits

- An ordinary player action may advance no more than **3 hours per turn**.
- Do not combine unrelated independent activities into one long time skip to bypass the ordinary-action limit.
- If a declared action contains several independent activities, resolve the main action and stop at a natural point when further action requires another player decision.
- Apply relevant location, safety, resources, physical condition, weather, and interruptions when deciding whether the declared duration is possible.
- Do not treat a player's stated duration as proof that every intended activity succeeded.

## 5. Pure Cultivation Time Skip

Pure cultivation may advance up to **1 month** in a single turn only when every condition below is verified:

1. The declared activity is pure cultivation; it does not bundle travel, shopping, combat, training unrelated to cultivation, or other independent activities.
2. The character remains in a safe, stationary location for the full period.
3. Food, water, shelter, and other required logistics are sufficient and supported by the character's recorded resources or environment.
4. The GM records reasonable progress checkpoints across the period and accounts for interruptions, changes in condition, and relevant consequences.
5. The total duration does not exceed one month.

If any condition is not met or cannot be verified, apply the ordinary-action limit or ask for clarification. Do not assume that a long period is safe merely because the character says they will cultivate.

## 6. Keep These Processes Separate

- **Meditation** is not automatically cultivation and does not automatically increase Sync progress.
- **Cultivation** increases Sync progress only according to the official cultivation rules and the character's current compatibility cap.
- **Spirit Ring absorption** is a separate process governed by the official Spirit Ring and Spirit Beast modules.
- Defeating a Spirit Beast and causing its ring to appear does not mean the ring has automatically been absorbed.
- Do not award progress, absorb a ring, or trigger a breakthrough solely because time passed.

## 7. Breakthrough Day left Display

When filling `Breakthrough: ... | ... Day left`, use the number of successfully absorbed rings to select the next transition interval (for example, Ring 1 → Ring 2), then calculate `Day left` from the last successful Spirit Ring absorption timestamp and the minimum interval in `bestiary/SPIRIT_BEAST_RULES.md`.

- Use elapsed in-world time from recorded timestamps, not the number of turns or real-world time.
- If positive time remains, round up to the next whole 24-hour unit. For example, 1 hour remaining = 1 Day left; 24 hours remaining = 1 Day left; 25 hours remaining = 2 Day left. This is a duration countdown, not a count of calendar-date changes.
- Display `0 Day left` only when the minimum interval has actually elapsed.
- If the previous successful absorption, ring number, or required timestamp is unknown or conflicting, display `??? Day left`; do not assume zero.
- Recalculate only when recorded in-world time or valid history changes. A new turn by itself does not reduce the value.
- `0 Day left` confirms only that the waiting period is complete. It does not confirm the Sync bottleneck, next ring, required item, breakthrough, or absorption conditions.

## 8. Required Continuity Check

Before sending each gameplay response, verify:

- The timestamp follows the last valid timestamp.
- Duration matches the declared action and the applicable limit.
- Date, weekday, season, and year rollovers are consistent.
- Weather and location changes have a plausible cause.
- Long cultivation satisfies all five conditions in §5.
- Time passage has not automatically changed HP, Qi, Sync progress, inventory, currency, or breakthrough status without an applicable rule and recorded cause.
- The final response follows the exact order and visual layout in `templates/GAMEPLAY_RESPONSE_TEMPLATE.md`.
