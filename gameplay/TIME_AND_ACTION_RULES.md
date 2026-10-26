# Merzkava Universe — Time and Action Rules

Status: Official gameplay procedure module.
Scope: Timestamp continuity, session calendar, action duration, protected night sleep, time skips, cultivation duration, and separation of meditation, cultivation, and Spirit Ring absorption.

## 1. Timestamp Format and Authority

The exact timestamp line format and its position in every gameplay response are defined only in `templates/GAMEPLAY_RESPONSE_TEMPLATE.md`. Do not create a second timestamp layout in this module. This module defines how to establish, advance, and validate the timestamp values.

- Fill every timestamp field with a concrete value once gameplay begins. Do not leave placeholders in a live gameplay timestamp.
- The displayed year and era are session-calendar details unless established as global canon.
- **New session without a prior timestamp:** establish one plausible starting timestamp, including year, era, season, date, weekday, weather, and local time. During this bootstrap, choose the session era randomly. The choice may be guided by the player's background, origin, or relevant world context when that makes the result more coherent, but it must remain a genuine GM selection rather than a deterministic era forced by the character's background.
- Era names may include, but are not limited to, **Era Naga Emas**, **Era Bulan Darah**, **Era Paus Surgawi**, and **Era Kebangkitan Raja**. These are illustrative options, not a closed canon list. The GM may select another era name that fits the world's established lore; do not invent detailed historical facts merely from the name.
- In the initial template, `Era ???` means the session era has not yet been selected. Replace it with the selected era before sending the first live gameplay response; never leave `Era ???` in an actual gameplay timestamp after bootstrap.
- Treat the chosen era as the fixed era for that session. Do not randomly reroll it on each turn or on recall. A session-era selection is a session starting context, not automatic authorization to rewrite global history or contradict established world chronology.
- **Continuing session:** use the last valid timestamp and era in the conversation as the sole starting point. Never reroll or restart the calendar or era merely because a new turn begins.
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

- An ordinary player action may advance no more than **3 hours per turn**. **Exception: normal night sleep is a protected biological need and may advance beyond 3 hours in one turn.** Do not force normal sleep to be split into multiple actions.
- Do not combine unrelated independent activities into one long time skip to bypass the ordinary-action limit.
- If a declared action contains several independent activities, resolve the main action and stop at a natural point when further action requires another player decision.
- Apply relevant location, safety, resources, physical condition, weather, and interruptions when deciding whether the declared duration is possible.
- Do not treat a player's stated duration as proof that every intended activity succeeded.
- Normal night sleep is the explicit exception to the 3-hour limit. During protected night sleep, Satiety is locked at its value when sleep begins; do not reduce Satiety or count meal windows as missed while the character is asleep. Apply `core/HUNGER_AND_METABOLISM.md` when the character is awake.

## 5. Pure Cultivation Time Skip

Pure cultivation may advance up to **1 month** in a single turn only when every condition below is verified:

1. The declared activity is pure cultivation; it does not bundle travel, shopping, combat, training unrelated to cultivation, or other independent activities.
2. The character remains in a safe, stationary location for the full period.
3. Food, water, shelter, and other required logistics are sufficient and supported by the character's recorded resources or environment.
4. The GM records reasonable progress checkpoints across the period and accounts for interruptions, changes in condition, and relevant consequences.
5. The total duration does not exceed one month.
6. Account for hunger/metabolism using `core/HUNGER_AND_METABOLISM.md`: reduce Satiety only for active/awake time, with protected night-sleep periods excluded. The one-month cultivation allowance does not suspend other applicable systems.

If any condition is not met or cannot be verified, apply the ordinary-action limit or ask for clarification. Do not assume that a long period is safe merely because the character says they will cultivate.

## 6. Keep These Processes Separate

- **Meditation** is not automatically cultivation and does not automatically increase Sync progress.
- **Cultivation** increases Sync progress only according to the official cultivation rules and the character's current compatibility cap.
- **Spirit Ring absorption** is a separate process governed by the official Spirit Ring and Spirit Beast modules.
- Defeating a Spirit Beast and causing its ring to appear does not mean the ring has automatically been absorbed.
- Do not award progress, absorb a ring, or trigger a breakthrough solely because time passed.

`Spirit Ring Absorption` is the canonical profile status for the character's stage and eligibility. Mortal not actively undergoing Awakening = `not eligible yet | ??? Day left`; active Awakening = `pending | ??? Day left`; after Awakening, evaluate first-ring eligibility and retain `??? Day left` until first successful absorption; Spirit Realm 1–8 use `not eligible yet | N Day left` when requirements remain unmet or `eligible | 0 Day left` only when all character/process requirements are met; Spirit Realm 9 is always `max | ∞ Day left` because the nine-ring limit is reached. Before every attempted absorption, re-check the current state against `core/SPIRIT_RING_RULES.md`, `core/CULTIVATION_SYSTEM.md`, and `bestiary/SPIRIT_BEAST_RULES.md`. For a first ring, Mortal must have awakened their Martial Soul; no inter-ring waiting period or breakthrough bottleneck applies. For every later ring before the peak, verify the full official requirements, including the Sync progress/bottleneck condition, minimum interval, required item(s), body tolerance, and any other applicable conditions. At Spirit Realm 9, do not calculate eligibility or cooldown for a tenth ring. A physical ring being available is a separate requirement: do not mark a character ineligible solely because no target ring is currently present, but never narrate a completed absorption without a legitimately available ring.

If the character is not eligible and the player still insists, do not bypass the gate or award success. Resolve only a forced attempt, using the existing deviation and HP formula in `core/SPIRIT_RING_RULES.md` and the Injury System for any injury supported by the event. Do not invent missing numerical formulas, damage, odds, or permanent disabilities. Severe or life-threatening consequences are possible when supported by the official formula and the actual event; no specific injury or death is automatic.

**Formulasi kanonis `Day left` (wajib):**

Setiap kali penyerapan Spirit Ring berhasil, **inisialisasi `Day left` saat itu juga** berdasarkan interval minimum resmi menuju ring berikutnya. Tetapkan titik awal baru: `T_eligible = 0` tepat setelah keberhasilan tersebut. Jangan menunggu giliran berikutnya atau meminta riwayat tambahan untuk memulai hitung mundur.

Definisikan:
- `T_min` = interval minimum resmi untuk penyerapan berikutnya, sesuai jumlah ring yang telah berhasil diserap dan tabel interval di `bestiary/SPIRIT_BEAST_RULES.md`. Konversi interval ke durasi memakai kalender sesi yang berlaku; pada kalender fallback §2, 1 bulan = 30 hari.
- `T_eligible` = total durasi waktu dunia yang benar-benar dijalani secara normal di luar Kultivasi sejak penyerapan Spirit Ring terakhir yang berhasil; nilainya dimulai dari `0` tepat saat ring berhasil diserap.
- `T_remaining` = sisa interval yang harus dipenuhi.

Rumus:
```text
T_remaining = max(0, T_min - T_eligible)

Jika T_remaining = 0:
    Day left = 0
Jika T_remaining > 0:
    Day left = ceil(T_remaining / 24 jam)
```

`T_eligible` adalah akumulasi durasi yang memenuhi syarat, bukan selisih timestamp mentah. Waktu dari aksi normal, aktivitas harian, perjalanan, istirahat, atau tidur hanya dihitung selama waktu dunia benar-benar berlalu dan tidak tumpang tindih dengan durasi lain. **Semua durasi yang diklasifikasikan sebagai Kultivasi dikecualikan sepenuhnya dari `T_eligible`**, termasuk time skip Kultivasi hingga satu bulan. Timestamp dan kalender dunia tetap maju selama Kultivasi, tetapi `T_eligible` dan `Day left` tidak berubah akibat durasi tersebut.

Pembulatan dilakukan pada sisa interval: sisa 1 jam hingga 24 jam = `1 Day left`; sisa lebih dari 24 jam hingga 48 jam = `2 Day left`. Angka hanya menjadi `0 Day left` saat `T_eligible >= T_min`. Jangan mengurangi satu hari penuh hanya karena giliran berganti atau tanggal kalender berubah.

Jika karakter belum pernah berhasil menyerap Spirit Ring, jeda antarpenyerapan belum dimulai. Mortal yang tidak sedang menjalani Awakening memakai `not eligible yet | ??? Day left`; selama Awakening aktif gunakan `pending | ??? Day left`; setelah Awakening selesai, gunakan `??? Day left` dan tentukan status dari syarat penyerapan pertama. Dalam kondisi ini, `???` bukan data cooldown yang hilang; tidak ada cooldown yang perlu dihitung. Setelah penyerapan pertama berhasil, langsung inisialisasi `Day left` dari `T_min` dan `T_eligible = 0`; jangan gunakan `???` atau `Belum ditetapkan` untuk penyerapan yang baru berhasil. Gunakan `Belum ditetapkan Day left` hanya untuk state lama yang **pernah memiliki penyerapan berhasil** tetapi catatan waktu/riwayatnya tidak cukup untuk merekonstruksi cooldown secara andal. Jangan menebak atau menganggap cooldown selesai. Untuk ring kedua hingga kesembilan sebelum Spirit Realm 9, `Day left = 0` adalah gerbang wajib yang terpisah dari Sync/bottleneck, ketersediaan ring, item, toleransi tubuh, dan syarat resmi lainnya.

## Status Kanonis Spirit Ring Absorption

Status ditentukan oleh tahap karakter terlebih dahulu, lalu kelayakan proses penyerapan berikutnya. Tampilkan **tepat satu status**, jangan menampilkan alternatif sekaligus, dan jangan menambahkan alasan/label lain di dalam field profil.

- **Mortal, tidak sedang menjalani Awakening:** `Spirit Ring Absorption: not eligible yet | ??? Day left`
- **Proses Martial Soul Awakening sedang berlangsung:** `Spirit Ring Absorption: pending | ??? Day left`
- **Awakening selesai, belum pernah menyerap ring pertama, syarat ring pertama terpenuhi:** `Spirit Ring Absorption: eligible | ??? Day left`
- **Awakening selesai, belum pernah menyerap ring pertama, syarat ring pertama belum terpenuhi:** `Spirit Ring Absorption: not eligible yet | ??? Day left`
- **Spirit Realm 1–8, syarat penyerapan berikutnya belum lengkap:** `Spirit Ring Absorption: not eligible yet | N Day left`
- **Spirit Realm 1–8, seluruh syarat karakter/proses penyerapan berikutnya terpenuhi:** `Spirit Ring Absorption: eligible | 0 Day left`
- **Spirit Realm 9 (Spirit Primordial), batas puncak sistem:** `Spirit Ring Absorption: max | ∞ Day left`

Aturan:
- `pending` hanya digunakan selama proses Awakening benar-benar berlangsung, bukan sekadar karena karakter belum Awakening.
- Untuk Mortal yang tidak sedang menjalani Awakening, tampilkan `Spirit Ring Absorption: not eligible yet | ??? Day left`.
- Setelah Awakening selesai tetapi sebelum penyerapan pertama berhasil, `Day left` adalah `???` karena jeda belum dimulai. Awakening sendiri tidak otomatis memberikan ring atau membuat status `eligible`.
- Pada Spirit Realm 1–8, cooldown positif berarti `not eligible yet`. Cooldown nol hanyalah satu gerbang; status `eligible` hanya jika seluruh syarat resmi lain terpenuhi. Ketersediaan ring fisik tetap terpisah dari kelayakan karakter/proses.
- Spirit Realm 9 selalu `max | ∞ Day left`. Sembilan slot adalah batas sistem; jangan hitung cooldown ke ring kesepuluh, jangan tampilkan `eligible`, dan jangan menambahkan Spirit Realm atau slot kesepuluh tanpa revisi canon eksplisit pemilik.
- `Belum ditetapkan Day left` hanya untuk save lama yang diketahui pernah menyerap ring tetapi riwayat waktunya tidak cukup untuk merekonstruksi cooldown. Jangan gunakan untuk Mortal, Awakening, karakter yang belum pernah menyerap ring, atau Spirit Realm 9.

## 8. Required Continuity Check

Before sending each gameplay response, verify:

- The timestamp follows the last valid timestamp.
- Duration matches the declared action and the applicable limit.
- Date, weekday, season, and year rollovers are consistent.
- Weather and location changes have a plausible cause.
- Long cultivation satisfies all five conditions in §5.
- Time passage has not automatically changed HP, Qi, Sync progress, Satiety, inventory, currency, or breakthrough status without an applicable rule and recorded cause.
- `Day left` was not reduced by any duration classified as Kultivasi; only qualifying normal-life elapsed time was counted, and the interval is not marked complete unless its accumulated eligible duration reaches the official minimum.
- Any awake time that passed has been resolved against `core/HUNGER_AND_METABOLISM.md`; protected night sleep neither reduces Satiety nor counts as a missed meal window.
- The final response follows the exact order and visual layout in `templates/GAMEPLAY_RESPONSE_TEMPLATE.md`.
