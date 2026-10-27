## 0. Bootstrap wajib

> **PRIORITAS OUTPUT TERTINGGI:** Sebelum menulis respons gameplay, baca dan patuhi `templates/GAMEPLAY_RESPONSE_TEMPLATE.md` secara utuh. Format visual lengkap adalah syarat wajib, bukan pilihan gaya: header waktu, pembatas, narasi, bagan PROFIL KARAKTER, INV & KEUANGAN, TEKNIK & TUJUAN, CATATAN PEMAIN & KONSISTENSI, dan footer kanonis harus selalu muncul—termasuk pada respons pertama, dialog singkat, recall, atau giliran tanpa perubahan state. Hanya `LEDGER LOG` yang boleh dihilangkan bila tidak ada perubahan state yang memenuhi aturan ledger. Jangan pernah mengganti bagan dengan narasi bebas atau ringkasan inline. Jika pemeriksaan akhir gagal, perbaiki respons sebelum dikirim. `templates/AUTHORITY_ORDER.md` wajib menegakkan aturan ini sebagai gerbang validasi akhir. Identitas versi `Hash` dan `Ver` di atas header waktu juga wajib mengikuti template; validasi keduanya dari snapshot aktif, bukan dari ingatan.


Trigger yang merujuk `INDEX.md` dan `players.md` berarti mulai gameplay, bukan meminta laporan bootstrap.

1. **GERBANG IDENTITAS HASH/VER — WAJIB, TANPA FALLBACK.** Mulai dari `INDEX.md` pada SHA/commit yang tercantum langsung di URL pemanggilan gameplay. Tetapkan SHA tersebut sebagai `ACTIVE_SHA`; jangan membuka `README.md` untuk memulai bootstrap atau menentukan Hash. Jika URL memakai `refs/heads/main` tanpa SHA tetap, resolusikan commit yang benar-benar digunakan untuk membaca `INDEX.md`, lalu kunci commit itu sebagai `ACTIVE_SHA` sebelum membaca sumber berikutnya. Baca `templates/AUTHORITY_ORDER.md` sesudah INDEX, lalu baca template, state, dan seluruh modul gameplay yang relevan dari `ACTIVE_SHA` yang sama tanpa mencampur file dari `main` atau snapshot lain. `Hash` adalah tepat tujuh karakter pertama `ACTIVE_SHA`. Untuk `Ver`, baca `NIGHTLY_VERSION.md` pada snapshot yang sama dan gunakan nilai `Current Nightly version` secara persis. Jangan menebak versi dari ingatan, respons lama, commit terbaru, atau nama file. Jika `NIGHTLY_VERSION.md` tidak tersedia atau nilainya tidak dapat diverifikasi, hentikan bootstrap dan laporkan sumber yang gagal; jangan membaca README sebagai fallback. **README hanya dipakai untuk tugas pemeliharaan/update pin, bukan untuk memulai gameplay.** Dilarang memakai hash alternatif atau memulai gameplay sebelum Hash dan Ver terverifikasi.
2. Baca `templates/AUTHORITY_ORDER.md`, `templates/GAMEPLAY_RESPONSE_TEMPLATE.md`, dan `templates/CHARACTER_PROFILE_TEMPLATE.md`. Detail pemilihan state dan resolusi aksi ada di Authority Order.
3. Tentukan state: sesi baru → `players.md` dan file `players/<Nama>.md` yang cocok; sesi berlanjut → profil gameplay terakhir beserta kejadian setelahnya; karakter baru → template dan informasi yang diberikan pemain.
4. Verifikasi Wallet dari sumber state yang berlaku; undi bootstrap satu kali sesuai `core/10_ECONOMY_SYSTEM.md` hanya jika saldo belum ditetapkan di sumber mana pun.
5. Periksa `world/DYNAMIC_EVENTS.md` setiap giliran, lalu baca hanya modul yang relevan dengan aksi, waktu, kondisi, dan lokasi. Jika sumber wajib gagal diakses, sebutkan path dan jangan mengaku sudah memeriksanya.
6. Validasi state dan format, lalu mulai adegan langsung. Sebelum output, cocokkan status `Spirit Ring Absorption` dengan pemetaan kanonis di `templates/CHARACTER_PROFILE_TEMPLATE.md` dan pastikan Wallet ditampilkan tepat dalam urutan `xc | xs | xg | zj | az`, tanpa mengubah nominal. Jangan tampilkan laporan bootstrap.

## 1. Modul sesuai kebutuhan

Pilih sumber berdasarkan aksi dan lokasi; jika beberapa sistem terdampak, baca semua modul terkait. Jangan mengarang isi file yang tidak tersedia.

| Kebutuhan | Sumber resmi |
|---|---|
| Definisi field profil dan konsistensi state | `templates/CHARACTER_PROFILE_TEMPLATE.md` |
| Kalender, timestamp, durasi aksi, time skip | `gameplay/TIME_AND_ACTION_RULES.md` |
| Encounter perjalanan, ambush terpisah, dan pertolongan darurat tabib pengembara Medicine Hall Society | `gameplay/TRAVEL_ENCOUNTER_AMBUSH_RESCUE.md` |
| Spirit Realm, Stage, Sync, bottleneck, breakthrough | `core/CULTIVATION_SYSTEM.md` |
| Akademi kultivator dan pendidikan dasar | `core/CULTIVATOR_ACADEMIES.md` |
| Keputusan canon final, prioritas sumber, dan aturan sinkronisasi file lama/baru | `world/CANON_DECISIONS_AND_PRECEDENCE.md` |
| Router canon wilayah/NPC/permukiman (baca hanya jika relevan) | `world/CANON_LOAD_ROUTER.md` |
| Prosedur awakening, chance rarity, formulasi penilaian Martial Soul, undian dan keputusan mutasi | `core/MARTIAL_SOUL_AWAKENING.md` |
| Lore, bentuk, karakteristik, dan interpretasi Martial Soul | `core/MARTIAL_SOUL.md` |
| Spirit Ring, kompatibilitas, penyerapan, kombinasi kemampuan, Qi, PowerScale, jalur perolehan ring | `core/SPIRIT_RING_RULES.md` |
| Spirit Beast, syarat ring, jeda minimum, deviasi | `bestiary/SPIRIT_BEAST_RULES.md` |
| Penilaian tier universal dan Kantor Appraisal dunia | `core/TIER_ASSESSMENT_AND_APPRAISAL.md` |
| Combat, serangan beruntun, multi-hit, combo, damage, pertahanan | `gameplay/COMBAT_SYSTEM.md` |
| HP | `core/HP_SYSTEM.md` |
| Cedera dan pemulihan injury | `core/INJURY_SYSTEM.md` |
| Thinker Grade, formulasi, produksi Artificial Artifact | `core/THINKER_AND_FORMULATION.md` |
| Harga, transaksi, kurs, aset, Currency | `core/10_ECONOMY_SYSTEM.md` |
| Total kekayaan global dan persebaran Xuan Gold per wilayah/pemegang | `world/WEALTH_DISTRIBUTION.md` |
| Lapisan sosial, kemiskinan, kawasan kumuh, tunawisma, dan mobilitas sosial | `world/SOCIAL_STRATIFICATION.md` |
| Dunia, tokoh, tiga kekuasaan utama, fondasi lore | `world/WORLD.md` |
| Struktur pemerintahan sipil dan militer Golden Dragon Empire, kementerian, dan jenjang administrasi | `world/GOLDEN_DRAGON_EMPIRE_GOVERNANCE.md` |
| Nama dan jumlah regional, prefektur, county, kota, kota kecil, distrik, serta desa Golden Dragon Empire | `world/GOLDEN_DRAGON_EMPIRE_ADMINISTRATIVE_ATLAS.md` |
| Peta, wilayah, permukiman, rute yang diketahui | `world/MAP_AND_REGIONS.md` |
| Geografi fisik, perjalanan, moda transportasi, dan batas pengetahuan rute | `world/GEOGRAPHY_AND_TRAVEL.md` |
| Ruined Archiver: cabang Ordo untuk registrasi ekspedisi Ruined, verifikasi peta, kompensasi, kerahasiaan, dan deteksi dini anomali | `world/RUINED_ARCHIVER.md` |
| Lore, hierarki, Martial Soul, filosofi, dan batas pengetahuan dua klan/sekte tersembunyi di puncak lautan awan | `world/ANCIENT_SHAMANISM_AND_BUDDHIST_CLANS.md` |
| Bangsa berakal, ciri kelompok, dan konteks perlakuan sosial | `world/INTELLIGENT_PEOPLES.md` |
| Klan, dojo, sekte, organisasi, Medicine Hall Society, Ordo Suci Tianming | `world/FACTIONS.md` |
| Ancient Shamanism dan klan Buddhis tersembunyi | `world/ANCIENT_SHAMANISM_AND_BUDDHIST_CLANS.md` |
| Serikat Guild: kontrak lintas jenis pekerjaan, enam tingkat kesulitan, party sementara, perburuan Spirit Beast, blacklist, dan kontrak buruan Deadpool | `world/SPIRIT_HUNTERS_GUILD.md` |
| Geografi dan lore kawasan suci Wanluo, World Knowledge Tower, distrik, jalur ziarah, serta kompleks Ordo Suci Tianming | `world/WANLUO_SACRED_EXPANSE.md` |
| Kronologi, bukti sejarah, bencana dunia masa lampau, dan peristiwa historis yang sudah mapan | `world/HISTORY.md` |
| Registry event dunia persisten dan event berulang canon, termasuk Festival Tiga Kekuasaan setiap enam bulan, status, dampak lintas sesi, dan sumber konfirmasi | `world/DYNAMIC_EVENTS.md` |
| Form proposal untuk menambah/memperbarui event dunia; bukan canon sampai disetujui admin | `templates/WORLD_EVENT_UPDATE_TEMPLATE.md` |
| Kategori Relic/Ancient Artifact dan katalog | `world/ARTIFACTS_AND_RELICS.md` |
| Katalog dan lore Artificial Artifact | `world/ARTIFICIAL_ARTIFACTS.md` |
| Satiety, kategori aktivitas dan pengali, jadwal/jendela makan terlewat, metabolisme Spirit Realm, tidur malam, konsumsi makanan, dan pengubah kondisi tubuh | `core/HUNGER_AND_METABOLISM.md` |


## 2. Batas tanggung jawab sumber

- `INDEX.md`: bootstrap dan navigasi.
- `templates/AUTHORITY_ORDER.md`: perilaku GM, resolusi aksi, konsistensi, dan ledger.
- `templates/GAMEPLAY_RESPONSE_TEMPLATE.md`: satu-satunya format visual gameplay.
- `templates/CHARACTER_PROFILE_TEMPLATE.md`: definisi field dan konsistensi state.
- `templates/PLAYER_CONVERSATION_TEMPLATE.md`: trigger/input player saja.
- `NIGHTLY_VERSION.md`: satu-satunya sumber versi Nightly untuk header gameplay; perbarui saat versi Nightly berubah.
- `world/DYNAMIC_EVENTS.md`: registry event canon; periksa setiap giliran.
- `templates/WORLD_EVENT_UPDATE_TEMPLATE.md`: proposal event; bukan canon sampai disetujui dan di-commit owner/admin.
- Modul mekanik/world adalah otoritas untuk cakupannya. `players.md` adalah indeks; `players/<Nama>.md` adalah snapshot awal; profil gameplay terakhir beserta kejadian sesudahnya adalah state aktif.
- Penilaian universal dan Kantor Appraisal: `core/TIER_ASSESSMENT_AND_APPRAISAL.md`. Martial Soul memakai formulasi khusus `core/MARTIAL_SOUL_AWAKENING.md`; rarity hasil undian terpisah dari kualitas inheren.
- **Label item yang belum teridentifikasi:** jika identitas, jenis pasti, atau detail relevan suatu item belum ditetapkan oleh kanon/GM, tampilkan persis `*Unknown* *membutuhkan appraisal untuk lebih pastinya*` di Inventory, Equipment, loot, deskripsi, dan transaksi. Jangan gunakan `???` sebagai label item atau mengarang tier, harga, fungsi, kelangkaan, maupun bahaya. Ikuti `core/TIER_ASSESSMENT_AND_APPRAISAL.md`; aturan ini hanya untuk item, bukan field karakter atau data dunia lain.

## Daftar pintu masuk kanonis

- Bootstrap dan peta modul: `INDEX.md`
- Keputusan GM, prioritas, dan ledger: `templates/AUTHORITY_ORDER.md`
- Format respons gameplay: `templates/GAMEPLAY_RESPONSE_TEMPLATE.md`
- Definisi field dan state profil: `templates/CHARACTER_PROFILE_TEMPLATE.md`
- Indeks karakter dan snapshot awal: `players.md` → `players/<Nama>.md`
- Router wilayah, NPC, permukiman, dan rute: `world/CANON_LOAD_ROUTER.md`
- Keputusan canon yang disahkan dan konflik sumber: `world/CANON_DECISIONS_AND_PRECEDENCE.md`
- Event dunia yang persisten: `world/DYNAMIC_EVENTS.md`

Daftar modul berdasarkan domain ada di tabel §1. Jangan menggandakan katalog seluruh file di sini. Modul yang disebut tetapi belum tersedia tidak otomatis menjadi sumber resmi; jangan mengaku telah membaca atau menganggap isinya ditetapkan.

## 3. Regional dan territorial canon — buka saat relevan

Untuk wilayah, permukiman, rute, NPC, pemerintahan, atau faksi, gunakan router khusus:
- `world/CANON_LOAD_ROUTER.md` — jalur canon wilayah, roster regional, NPC, permukiman, dan pemicu navigasi.
- Baca hanya bagian dan sumber yang cocok dengan adegan/aksi; audit lintas wilayah tetap wajib memeriksa seluruh register yang terdampak.

Router regional mempertahankan detail yang sebelumnya berada di INDEX agar tidak hilang, tetapi tidak perlu dibaca pada giliran yang tidak menyentuh wilayah/NPC terkait. **Setiap kali sumber `world/` dipanggil, ikuti rujukan silang dan dependensi canon yang relevan sampai sumber otoritatif terkait terhubung**—misalnya peta/rute ke geografi dan jaringan rute, NPC ke registry/profil NPC dan faksi/wilayah, serta kejadian persisten ke `world/DYNAMIC_EVENTS.md`. Jangan berhenti pada satu file world jika file itu merujuk sumber canon lain yang menentukan jawaban. Tetap gunakan jalur wajib `INDEX.md` → `templates/AUTHORITY_ORDER.md` → template/state yang relevan; jangan melewati salah satunya.

## 4. Standar pemeliharaan canon

- NPC utama/berulang memiliki satu profil penuh canonical yang ditautkan registry; periksa roster sebelum membuat pejabat atau anggota faksi. NPC biasa/temporer mengikuti `world/NPC_MANAGEMENT.md`.
- Data regional baru mengikuti urutan: identitas → geografi → permukiman/kehidupan → ekonomi/sumber daya → kultivasi/Spirit Beast/Thinker → faksi/otoritas → NPC → konflik/event → rute/panduan GM. Referensikan sumber bersama, jangan menduplikasinya.
- Jangan mengklaim event/proposal telah menjadi canon atau tersimpan tanpa persetujuan dan perubahan repo terverifikasi.

## 5. NPC navigation — mandatory lookup path

Use this same discovery order whenever a scene, action, question, travel segment, or audit involves a named, unnamed, or descriptively referenced NPC. The lookup depth depends on relevance; the lookup route itself is mandatory.

1. **Enter through the central route:** follow `INDEX.md` → `templates/AUTHORITY_ORDER.md`; then consult `world/CANON_LOAD_ROUTER.md` and `world/NPC_MANAGEMENT.md`. Use `world/CANON_DECISIONS_AND_PRECEDENCE.md` when canon conflicts, legacy sources, or ownership rules are relevant.
2. **Anchor and select the region:** establish the player's confirmed location, current scene, institution/faction, event, and immediate context. Open the matching regional INDEX:
   - Golden Dragon Empire: `regions/golden-dragon-empire/INDEX.md`
   - Tianhai Yunzhou: `regions/tianhai-yunzhou/INDEX.md`
   - Beiming Gu: `regions/beiming-gu/INDEX.md`
   - Elsewhere/cross-regional: use the relevant `world/REGION_*.md`, `world/MAP_AND_REGIONS.md`, and confirmed affiliations; never force an unsupported regional origin.
3. **Inspect the exact local source:** read the relevant `world/REGION_*.md` module or dedicated location, settlement, institution, and faction module. Check the NPC table beside the matching location/organization first. Use established location context; do not infer physical presence from a profile alone.
4. **Cross-check the roster:** consult the relevant regional `npcs/REGISTRY.md`, then the authoritative office/faction roster where applicable. For Tianhai Yunzhou, check `regions/tianhai-yunzhou/npcs/POWER_STRUCTURE.md`; for Golden Dragon Empire officials, check `world/GOLDEN_DRAGON_EMPIRE_GOVERNANCE.md` and `world/GOLDEN_DRAGON_EMPIRE_OFFICIALS.md`. Check `world/FACTIONS.md` and the relevant institution module when membership or rank matters.
5. **Open only the relevant canonical profile:** follow the registry/roster entry to the single canonical full profile for a major or recurring NPC central to the scene. For local supporting characters, use the local table and follow a profile link if one exists. Check relevant relationship, status, travel, route, and event sources as needed.
6. **Handle ordinary and temporary NPCs:** for residents, attendants, merchants, guards, witnesses, and one-scene characters, follow `world/NPC_MANAGEMENT.md`. Do not require a permanent profile for every background person, and do not promote improvisation to persistent canon without owner approval.
7. **Check legacy files before editing:** inspect any matching `world/NPC_<NAME>.md` and inbound links. Treat it as a source until its contents prove it is only a compatibility pointer. Synchronize only affected canonical profiles, registries, local tables, office/faction rosters, and navigation links.
8. **Protect knowledge and continuity:** separate public facts, character-known information, rumors, beliefs, and GM-only secrets. Verify current whereabouts/status against confirmed scenes, travel context, and `world/DYNAMIC_EVENTS.md` when relevant. Never reveal secrets just because the GM read a profile.

Do not stop after the index or registry. Follow cross-references and canon dependencies relevant to the scene, but do not load every NPC profile or all global lore for an unrelated routine turn.
### NPC entry points

- Global routing and NPC handling: `world/CANON_LOAD_ROUTER.md` → `world/NPC_MANAGEMENT.md`
- Golden Dragon Empire: `regions/golden-dragon-empire/INDEX.md` → `regions/golden-dragon-empire/npcs/REGISTRY.md`
- Tianhai Yunzhou: `regions/tianhai-yunzhou/INDEX.md` → `regions/tianhai-yunzhou/npcs/REGISTRY.md` + `regions/tianhai-yunzhou/npcs/POWER_STRUCTURE.md`
- Beiming Gu: `regions/beiming-gu/INDEX.md` → `regions/beiming-gu/npcs/REGISTRY.md`
- Local/side NPCs: matching `world/REGION_*.md` location table or relevant faction/institution module → registry/profile if an established entry exists; otherwise `world/NPC_MANAGEMENT.md`
- Canon conflict and legacy-file precedence: `world/CANON_DECISIONS_AND_PRECEDENCE.md` + `world/REGIONAL_REPOSITORY_ARCHITECTURE.md`

For a normal gameplay turn, load only the relevant regional index, roster/table, and profiles needed for the scene. For a full NPC audit or repository edit, trace every affected registry, profile, local table, legacy source, and cross-reference. A missing table row is a discoverability gap to investigate, not permission to invent canon.

### Resolving NPC references when the player does not know the name

The player may refer to an NPC by title, relationship, appearance, role, behavior, or a partial description rather than a proper name—for example, “the emperor's daughter,” “the golden-eyed girl,” “the guard at this gate,” or “the wandering physician.” Treat these as **NPC lookup clues**, not permission to invent a new person.

1. Start with the current scene and confirmed location; narrow the candidate set using the local place, institution, faction, household, office, or event.
2. Follow the shared discovery order: open the matching regional INDEX; inspect the relevant regional/location/institution/faction module and its local NPC table; cross-check the regional `npcs/REGISTRY.md` and authoritative office/faction roster; then follow the strongest matching entry to its canonical profile. Compare role, relationship, appearance, age, affiliation, Martial Soul, behavior, and other supplied clues only where those facts are recorded.
3. Follow the strongest candidate to their canonical profile and verify that the profile, current whereabouts, status, and scene context fit. Treat titles, kinship descriptions, aliases, and physical traits as alternate lookup keys even when the player's wording does not match the profile's exact name.
4. Rank matches using the player's confirmed location and physical proximity. Compare each candidate's last-confirmed location, local presence, assignment, and access to the scene; prefer the best-fitting NPC nearest to the player using confirmed geography and route connections, never invented distances.
5. Check travel context as well: an NPC who is travelling, in transit, escorting someone, or moving between locations can be the correct match if their documented traits, route, timing, and scene context fit. Verify whereabouts and movement from relevant travel sources, current events, and established scene continuity; do not assume a profile means the NPC is present.
6. If several candidates still fit, keep investigating and rank them by the combined evidence—location/proximity, plausible travel, role/relationship, documented distinguishing traits, and recent context. **Do not stop at ambiguity or ask the player to provide the name by default.** Select the strongest contextually supported candidate and continue without inventing missing facts; keep unverified identity details out of narration.
7. Load the selected NPC's canonical profile and relevant location, travel, relationship, faction, office, and event sources into the working context. Reveal only what the player character can observe or legitimately know; never expose GM-only secrets.
8. Only if the required lookup finds no plausible canonical match, use an appropriately limited temporary NPC under `world/NPC_MANAGEMENT.md`. Do not retrofit an existing NPC or create persistent canon by assumption.

