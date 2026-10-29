## 0. Bootstrap wajib

> **GERBANG BOOTSTRAP TERTINGGI:** gameplay selalu dimulai dari `INDEX.md` pada sumber/commit yang dipanggil; setelah itu wajib baca dan patuhi `templates/AUTHORITY_ORDER.md`. Kedua file ini—bukan README—mengendalikan bootstrap, hierarki keputusan, dan validasi state. `README.md` hanya papan publik untuk changelog, versi, dan pemeliharaan pin/referensi; README tidak boleh dipakai untuk memulai gameplay, menentukan aturan, memilih sumber alternatif, atau menjadi fallback ketika file bootstrap gagal. `templates/GAMEPLAY_RESPONSE_TEMPLATE.md` adalah satu-satunya pemilik format visual respons. Template gameplay wajib dipakai utuh setiap giliran; hanya `LEDGER LOG` yang kondisional. Jangan menyalin spesifikasi format ke INDEX—cukup tegakkan hierarki dan rujuk sumber pemiliknya.


Trigger yang merujuk `INDEX.md` dan `players.md` berarti mulai gameplay, bukan meminta laporan bootstrap.

1. **GERBANG IDENTITAS HASH/VER — WAJIB, TANPA FALLBACK.** Mulai dari `INDEX.md` pada SHA/commit yang tercantum langsung di URL pemanggilan gameplay. Tetapkan SHA tersebut sebagai `ACTIVE_SHA`; jangan membuka `README.md` untuk memulai bootstrap atau menentukan Hash. Jika URL memakai `refs/heads/main` tanpa SHA tetap, resolusikan commit yang benar-benar digunakan untuk membaca `INDEX.md`, lalu kunci commit itu sebagai `ACTIVE_SHA` sebelum membaca sumber berikutnya. Baca `templates/AUTHORITY_ORDER.md` sesudah INDEX, lalu baca template, state, dan seluruh modul gameplay yang relevan dari `ACTIVE_SHA` yang sama tanpa mencampur file dari `main` atau snapshot lain. `Hash` adalah tepat tujuh karakter pertama `ACTIVE_SHA`. Untuk `Ver`, baca `NIGHTLY_VERSION.md` pada snapshot yang sama dan gunakan nilai `Current Nightly version` secara persis. Jangan menebak versi dari ingatan, respons lama, commit terbaru, atau nama file. Jika `NIGHTLY_VERSION.md` tidak tersedia atau nilainya tidak dapat diverifikasi, hentikan bootstrap dan laporkan sumber yang gagal; jangan membaca README sebagai fallback. **README hanya dipakai untuk tugas pemeliharaan/update pin, bukan untuk memulai gameplay.** Dilarang memakai hash alternatif atau memulai gameplay sebelum Hash dan Ver terverifikasi.
2. Baca `templates/AUTHORITY_ORDER.md`, `templates/GAMEPLAY_RESPONSE_TEMPLATE.md`, `templates/CHARACTER_PROFILE_TEMPLATE.md`, serta **wajib muat `templates/NARRATIVE_DYNAMICS.md` dan `templates/ANTI_CHEAT_HARD_GATE.md` sebelum gameplay**. Authority Order mengatur keputusan dan batas GM; Narrative Dynamics adalah pemilik aturan operasional narasi; Anti-Cheat Hard Gate adalah otoritas penegakan tertinggi atas bypass, manipulasi state, rollback, dan sanksi. Jangan menduplikasi checklist narasi di INDEX: terapkan modul Narrative Dynamics setiap giliran. Ingat bahwa sebutan dunia bagi orang yang player sebut “kultivator” adalah **ahli Spirit Realm**. Skala Spirit Realm, Martial Soul, Spirit Ring, dan Spirit Beast wajib mengikuti modul mekanik resmi, bukan improvisasi naratif.
3. **HARD GATE IDENTITAS PLAYER — EXACT MATCH SAJA.** Cocokkan nama input dengan `players.md` secara persis dan case-sensitive; jangan gunakan fuzzy match, kemiripan ejaan/bunyi, koreksi otomatis, transliterasi, normalisasi Unicode, atau penghapusan/penyetaraan diakritik. Contoh jika registry berisi `Yuha`: hanya `Yuha` yang cocok; `Yuma`, `Yuka`, `Yûha`, dan `Yūhá` adalah nama yang tidak terdaftar dan harus masuk jalur karakter baru—bukan dianggap alias atau typo Yuha. Jika nama kosong atau hanya placeholder seperti `(Nama Karaktermu)`, hentikan bootstrap identitas dan tanyakan hanya apakah nama terlupa ditulis atau ada kesalahan penulisan; jangan menawarkan pilihan karakter/wilayah/realm/spesies. Jika nama konkret diberikan tetapi tidak cocok persis, perlakukan sebagai karakter baru dan lanjutkan jalur bootstrap baru berdasarkan informasi yang sudah ada; jangan menebak karakter terdaftar yang dimaksud dan jangan bertanya apakah nama itu typo. Jika nama cocok persis, muat hanya `players/<Nama>.md` yang sesuai dari `ACTIVE_SHA`. Pembuatan karakter baru tidak berarti menyimpan atau mengubah GitHub secara otomatis. Untuk karakter baru, ikuti `templates/CHARACTER_PROFILE_TEMPLATE.md`; bila latar sudah tersedia, isi ambiguitas wajar secara konservatif tanpa menanyakan setiap field. Jika hanya nama yang tersedia dan latar minimum belum ada, tanyakan latar yang diperlukan tanpa menyodorkan menu wilayah/realm/spesies.

   **HARD GATE ARAH NARASI PEMBUKA:** Jika latar karakter belum memberi konteks Merzkava yang konkret, pembukaan wajib menghubungkannya dengan satu aspek dunia yang relevan dan berdampak—misalnya pekerjaan, pendidikan, layanan, biaya/akses, Awakening, alat, atau aktivitas NPC. Ikuti `templates/NARRATIVE_DYNAMICS.md`; jangan mengulang checklist narasi di sini, memaksakan lore, mengubah premis/agensi karakter, atau memberi kemampuan yang belum sah.

Ikuti `templates/NARRATIVE_DYNAMICS.md` untuk penerapan narasi, improvisasi adegan, kehidupan ahli Spirit Realm dan Thinker, skala Martial Soul/Spirit Ring/Spirit Beast, otonomi NPC, serta batas canon. Pilih kaitan sesuai konteks dan pengetahuan tokoh; jangan memaksakan banyak sistem, mengubah latar/agensi/state, memberi kemampuan belum sah, atau menciptakan canon, institusi, harga, dan prosedur baru. Jika detail belum terverifikasi, pertahankan ketidakpastian yang wajar.

Kewajiban mengarahkan pembukaan ini berlaku ketika konteks memang memungkinkan; jangan menyisipkan sistem secara paksa ke adegan darurat, tidur, keintiman, atau fokus emosional sempit. Sesudah pembukaan, lanjutkan secara proporsional mengikuti tindakan pemain dan perkembangan adegan—bukan mengulang kaitan yang sama setiap giliran. Sebelum mengirim, pastikan kaitan itu terasa melalui sebab-akibat dan tetap lulus pemeriksaan identitas dunia Merzkava; jika tidak relevan atau melanggar canon/agensi, revisi.
4. **Kunci kontinuitas state sebelum narasi:** untuk sesi berlanjut, tetapkan lokasi dan state terakhir yang terverifikasi sebagai baseline. Lokasi, Equipment, Inventory, aset, Wallet, dan state persisten lain tidak berubah tanpa aksi/peristiwa sah yang menjelaskan perubahan. Jangan memakai snapshot awal untuk menimpa state sesi berlanjut; ikuti prosedur kontinuitas di `templates/AUTHORITY_ORDER.md`.
5. Verifikasi Wallet dari sumber state yang berlaku. Untuk karakter baru tanpa saldo eksplisit, tetapkan Wallet sebagai bagian dari satu jalur bootstrap profil di `templates/CHARACTER_PROFILE_TEMPLATE.md`, berdasarkan latar dan kondisi ekonomi yang masuk akal; jangan menjalankan undian uang terpisah. `core/10_ECONOMY_SYSTEM.md` mengatur kurs, harga, dan transaksi. Snapshot atau saldo eksplisit yang sudah ada selalu dipertahankan.
6. Periksa `world/DYNAMIC_EVENTS.md` setiap giliran, lalu baca hanya modul yang relevan dengan aksi, waktu, kondisi, dan lokasi. Jika sumber wajib gagal diakses, sebutkan path dan jangan mengaku sudah memeriksanya.
7. Validasi state dan format, termasuk menampilkan `Thinker Grade: ???` bila Grade belum terverifikasi, lalu mulai adegan langsung. Sebelum output, cocokkan status `Spirit Ring Absorption` dengan pemetaan kanonis di `templates/CHARACTER_PROFILE_TEMPLATE.md` dan pastikan Wallet ditampilkan tepat dalam urutan `xc | xs | xg | zj | az`, tanpa mengubah nominal. Jangan tampilkan laporan bootstrap.
8. **HARD GATE GM OPTIONS — SATU-SATUNYA PENGATURAN PREFERENSI PLAYER:** gunakan hanya `Provide GM options: (Yes/No)` pada footer sesuai `templates/GAMEPLAY_RESPONSE_TEMPLATE.md` dan `templates/AUTHORITY_ORDER.md`. Jangan menambahkan pengaturan preferensi gameplay lain. Jika player menyisakan `(Yes)`, berikan tepat 3 bullet options dengan label `**A**. *...*`, `**B**. *...*`, dan `**C**. *...*`; setiap opsi maksimal 4 baris kecuali konteks memerlukan lebih. Jika player menyisakan `(No)`, jangan tampilkan opsi rekomendasi. Jika footer masih berisi `(Yes/No)` sekaligus atau tidak ada pilihan tunggal yang dapat diverifikasi, gunakan default tanpa opsi rekomendasi; jangan menebak atau mengambil preferensi dari sesi lain. Pilihan eksplisit yang terverifikasi dalam sesi berlanjut tetap berlaku sampai player mengubahnya. Opsi tidak boleh melanggar canon, kelayakan karakter, pengetahuan karakter, atau agensi player.

## 1. Modul sesuai kebutuhan

Pilih sumber berdasarkan aksi dan lokasi; jika beberapa sistem terdampak, baca semua modul terkait. Jangan mengarang isi file yang tidak tersedia.

| Kebutuhan | Sumber resmi |
|---|---|
| Definisi field profil dan konsistensi state | `templates/CHARACTER_PROFILE_TEMPLATE.md` |\n| Standar narasi, deteksi stagnasi, otonomi dunia, dan konsekuensi | `templates/NARRATIVE_DYNAMICS.md` |
| Anti-cheat, bypass, warning wajib, rollback, eskalasi sanksi, dan pengecualian kematian permanen | `templates/ANTI_CHEAT_HARD_GATE.md` |
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
| **Jalur Thinker tunggal — wajib:** pendidikan dasar → tahap fokus (durasi minimum dan Satiety) → Apprentice Examination/Grade 1 → ujian Grade berikutnya dengan Tier target → Condition Score wajib mulai Grade 2 → kuota dan perbandingan kompetitif Grade 3–7 → engraver blueprint pribadi Grade 7–10 → prasyarat khusus Grade 8–10 → provenance, kepemilikan, waktu, Satiety, dan ledger | `core/THINKER_AND_FORMULATION.md` (otoritas mekanik tunggal); `world/TIANHAI_ACADEMIES_AND_THINKER_INSTITUTE.md` hanya untuk administrasi institut dan konteks regional |
| Harga, transaksi, kurs, aset, Currency | `core/10_ECONOMY_SYSTEM.md` |
| Total kekayaan global dan persebaran Xuan Gold per wilayah/pemegang | `world/WEALTH_DISTRIBUTION.md` |
| Lapisan sosial, kemiskinan, kawasan kumuh, tunawisma, dan mobilitas sosial | `world/SOCIAL_STRATIFICATION.md` |
| Dunia, tokoh, tiga kekuasaan utama, fondasi lore | `world/WORLD.md` |
| Struktur pemerintahan sipil dan militer Golden Dragon Empire, kementerian, dan jenjang administrasi | `world/GOLDEN_DRAGON_EMPIRE_GOVERNANCE.md` |
| Nama dan jumlah regional, prefektur, county, kota, kota kecil, distrik, serta desa Golden Dragon Empire | `world/GOLDEN_DRAGON_EMPIRE_ADMINISTRATIVE_ATLAS.md` |
| Peta, wilayah, permukiman, rute yang diketahui | `world/MAP_AND_REGIONS.md` |
| Pelabuhan selatan Lawless, gugusan pulau hiburan kriminal, dan akses ke Guixu Canghai | `world/LAWLESS_SOUTHERN_PORT_AND_ISLES.md` |
| Tree navigasi terhubung tiga kekuasaan dan transit antarwilayah | `world/WORLD_NAVIGATION_TREE.md` |
| Peta garis tiga kekuasaan dari masing-masing perspektif, termasuk koridor darat dan laut | `world/THREE_POWER_PERSPECTIVE_MAPS.md` |
| Geografi fisik, perjalanan, moda transportasi, dan batas pengetahuan rute | `world/GEOGRAPHY_AND_TRAVEL.md` |
| Ruined Archiver: cabang Ordo untuk registrasi ekspedisi Ruined, verifikasi peta, kompensasi, kerahasiaan, dan deteksi dini anomali | `world/RUINED_ARCHIVER.md` |
| Lore, hierarki, Martial Soul, filosofi, dan batas pengetahuan dua klan/sekte tersembunyi di puncak lautan awan | `world/ANCIENT_SHAMANISM_AND_BUDDHIST_CLANS.md` |
| Bangsa berakal, ciri kelompok, dan konteks perlakuan sosial | `world/INTELLIGENT_PEOPLES.md` |
| Klan, dojo, sekte, organisasi, Medicine Hall Society, Ordo Suci Tianming | `world/FACTIONS.md` |
| Materi belajar tiap institusi, klasifikasi jalur Spirit Realm/Thinker/dual-path, tutor independen, dan encounter pengajar pengelana | `world/OPEN_LEARNING_PATHS_AND_WANDERING_INSTRUCTORS.md`; mekanik tetap mengikuti sumber resmi |
| Crimson Sovereign Court, hidden leader Ying Wuxin, and its shadow authority over Crimson Keel Brotherhood | `world/FACTIONS.md`; `world/REGION_BLACK_TIDE_EXPANSE.md`; `world/NPC_YING_WUXIN.md`; `world/LAWLESS_TERRITORIES.md` |
| Serikat Guild: kontrak lintas jenis pekerjaan, enam tingkat kesulitan, party sementara, perburuan Spirit Beast, blacklist, dan kontrak buruan Deadpool | `world/SPIRIT_HUNTERS_GUILD.md` |
| Geografi dan lore kawasan suci Wanluo, World Knowledge Tower, distrik, jalur ziarah, serta kompleks Ordo Suci Tianming | `world/WANLUO_SACRED_EXPANSE.md` |
| Kronologi, bukti sejarah, bencana dunia masa lampau, dan peristiwa historis yang sudah mapan | `world/HISTORY.md` |
| Registry event dunia persisten dan event berulang canon, termasuk Festival Tiga Kekuasaan setiap enam bulan, status, dampak lintas sesi, dan sumber konfirmasi | `world/DYNAMIC_EVENTS.md` |
| Form proposal untuk menambah/memperbarui event dunia; bukan canon sampai disetujui admin | `templates/WORLD_EVENT_UPDATE_TEMPLATE.md` |
| Kategori Relic/Ancient Artifact dan katalog | `world/ARTIFACTS_AND_RELICS.md` |
| Katalog dan lore Artificial Artifact | `world/ARTIFICIAL_ARTIFACTS.md` |
| Penjara, bound items, rantai pengekang Martial Soul/fisik, collar penyegelan, batas area, dan tahanan salah tuduh | `world/PRISON_AND_BOUND_ITEMS.md` |
| Satiety, kategori aktivitas dan pengali, jadwal/jendela makan terlewat, metabolisme Spirit Realm, tidur malam, konsumsi makanan, dan pengubah kondisi tubuh | `core/HUNGER_AND_METABOLISM.md` |


## 2. Batas tanggung jawab sumber

`backups/` adalah arsip historis, bukan sumber aktif: jangan gunakan file di dalamnya untuk bootstrap, canon, aturan, template, versi Nightly, atau state gameplay. Buka arsip hanya jika tugasnya secara eksplisit meminta perbandingan atau riwayat; untuk gameplay dan keputusan saat ini, gunakan file aktif yang dirujuk oleh INDEX pada `ACTIVE_SHA` yang sama.

- `INDEX.md`: bootstrap dan navigasi.
- `templates/AUTHORITY_ORDER.md`: perilaku GM, resolusi aksi, konsistensi, dan ledger.
- `templates/GAMEPLAY_RESPONSE_TEMPLATE.md`: satu-satunya format visual gameplay.\n- `templates/NARRATIVE_DYNAMICS.md`: modul wajib untuk kedalaman narasi, dinamika adegan, otonomi dunia, konsekuensi, dan kontinuitas naratif.
- `templates/ANTI_CHEAT_HARD_GATE.md`: hard gate tertinggi untuk penegakan anti-cheat; wajib dipakai sebelum resolusi dan output ketika ada klaim bypass/kecurangan.
- `templates/CHARACTER_PROFILE_TEMPLATE.md`: definisi field dan konsistensi state.
- `templates/PLAYER_CONVERSATION_TEMPLATE.md`: trigger/input player saja.
- `NIGHTLY_VERSION.md`: satu-satunya sumber versi Nightly untuk header gameplay; perbarui saat versi Nightly berubah.
- `world/DYNAMIC_EVENTS.md`: registry event canon; periksa setiap giliran.
- `templates/WORLD_EVENT_UPDATE_TEMPLATE.md`: proposal event; bukan canon sampai disetujui dan di-commit owner/admin.
- **HARD GATE THINKER:** bila aksi, karakter, NPC, ujian, pembelajaran, formulasi, produksi, appraisal kondisi Artificial Artifact, engraver, token, atau kontribusi menyentuh jalur Thinker, baca `core/THINKER_AND_FORMULATION.md` terlebih dahulu dan terapkan seluruh urutan mandatory-nya. Baca `world/TIANHAI_ACADEMIES_AND_THINKER_INSTITUTE.md` hanya untuk detail administrasi/regional yang relevan; file itu bukan jalur alternatif dan tidak boleh menimpa mekanik core. Untuk waktu/Satiety, uang, katalog fungsi artefak, dan anti-cheat, baca sumber domain masing-masing juga.
- Modul mekanik/world adalah otoritas untuk cakupannya. `players.md` adalah indeks; `players/<Nama>.md` adalah snapshot awal; profil gameplay terakhir beserta kejadian sesudahnya adalah state aktif.
- Penilaian universal dan Kantor Appraisal: `core/TIER_ASSESSMENT_AND_APPRAISAL.md`. Martial Soul memakai formulasi khusus `core/MARTIAL_SOUL_AWAKENING.md`; rarity hasil undian terpisah dari kualitas inheren.
- **Label item yang belum teridentifikasi:** jika identitas, jenis pasti, atau detail relevan suatu item belum ditetapkan oleh kanon/GM, tampilkan persis ``Unknown`` **membutuhkan appraisal untuk lebih pastinya** di Inventory, Equipment, loot, deskripsi, dan transaksi. Jangan gunakan `???` sebagai label item atau mengarang tier, harga, fungsi, kelangkaan, maupun bahaya. Ikuti `core/TIER_ASSESSMENT_AND_APPRAISAL.md`; aturan ini hanya untuk item, bukan field karakter atau data dunia lain.

## Daftar pintu masuk kanonis

- Bootstrap dan peta modul: `INDEX.md`
- Keputusan GM, prioritas, dan ledger: `templates/AUTHORITY_ORDER.md`
- Format respons gameplay: `templates/GAMEPLAY_RESPONSE_TEMPLATE.md`\n- Dinamika narasi dan konsekuensi: `templates/NARRATIVE_DYNAMICS.md`
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
- Format dan urutan modul regional mengikuti `templates/REGIONAL_MODULE_TEMPLATE.md`; tanggung jawab folder dan kepemilikan sumber mengikuti `world/REGIONAL_REPOSITORY_ARCHITECTURE.md`. Referensikan sumber bersama, jangan menduplikasi data.
- Jangan mengklaim event/proposal telah menjadi canon atau tersimpan tanpa persetujuan dan perubahan repo terverifikasi.

## 5. NPC navigation

**Mandatory NPC display rule:** wrap every NPC reference in double backticks. Use established context for named meetings/referrals and do not reset known identities to ``npc ???``. Reserve ``npc ???`` for significant/story-relevant or potentially recurring people whose identity is genuinely unknown; proactively introduce them when conversation naturally allows, without waiting for the player to ask. Ordinary background/service NPCs use role labels such as ``NPC: Penjaga gerbang``; once named, retain role plus name, e.g. ``Penjaga Gerbang: Wang Lan``. Full rules are owned by `templates/AUTHORITY_ORDER.md`, `templates/GAMEPLAY_RESPONSE_TEMPLATE.md`, and `world/NPC_MANAGEMENT.md`.

**One connected path, used in either direction: NPC ↔ Map.** After the normal `INDEX.md` → `templates/AUTHORITY_ORDER.md` bootstrap, choose the starting point from the scene:

- **NPC → Map:** when a named NPC is central, open their canonical profile (use the regional registry only to locate it), follow home/base/last-confirmed whereabouts to the matching map module, then use established local context.
- **Map → NPC:** when the player enters, crosses, or spends time in an area, open that area's map module first. Proactively inspect its established local NPC entries and relevant institutions/factions, then open the canonical profiles of plausible NPC candidates to verify role, behavior, relationships, whereabouts, and continuity before bringing them into the scene. If no established NPC fits, use a situational background NPC only within `world/NPC_MANAGEMENT.md`.

Regional map sources: Golden Dragon Empire uses the relevant `world/REGION_*.md` (imperial family scenes use `world/REGION_LONGYUAN.md`); Tianhai Yunzhou uses `world/REGION_TIANHAI_YUNZHOU.md`; Beiming Gu uses `world/REGION_BEIMING_GU.md` for all seven districts.

The profile establishes **who the NPC is and what is known about them**; the map establishes **local place context and candidate leads**. For presence checks, player-knowledge boundaries, and temporary NPC/activity limits, follow `templates/AUTHORITY_ORDER.md` and `world/NPC_MANAGEMENT.md`. A home, regional affiliation, or roster entry alone does not prove physical presence. Check office/faction rosters when authority or membership matters, and route/geography/time sources when travel matters. Never invent finer map details or concealed facts.

| Half-beast enslavement ban, corrupt restraint abuse, and regional safety pattern | `world/PRISON_AND_BOUND_ITEMS.md`; `world/MAP_AND_REGIONS.md` |
| Lawless organizations as largest suppliers in the half-beast slave trade; public-secret corruption among buyers tied to the three powers | `world/LAWLESS_TERRITORIES.md`; `world/PRISON_AND_BOUND_ITEMS.md`; `world/MAP_AND_REGIONS.md` |
| Inner Azerion hidden city and Azerion Forest map relationships | `world/THREE_POWER_PERSPECTIVE_MAPS.md`; `world/WORLD_NAVIGATION_TREE.md`; `world/LOCATION_AND_ROUTE_NETWORK.md` |
