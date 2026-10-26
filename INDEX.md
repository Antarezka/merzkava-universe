## 0. Bootstrap wajib

Trigger awal yang merujuk `INDEX.md` dan `players.md` berarti mulai gameplay, bukan membuat laporan.

1. Baca `README.md` untuk memperoleh **Latest pinned source**. Gunakan SHA tersebut untuk membaca ulang `INDEX.md` dan semua file sumber dari snapshot yang sama; jangan mencampur isi dari `main` dengan snapshot gameplay.
2. Baca penuh `templates/AUTHORITY_ORDER.md`, `templates/GAMEPLAY_RESPONSE_TEMPLATE.md`, lalu `templates/CHARACTER_PROFILE_TEMPLATE.md`.
3. Pilih state: sesi baru memakai `players.md` lalu seluruh `players/<Nama>.md`; sesi berlanjut memakai profil gameplay terakhir dan kejadian sesudahnya; karakter baru memakai template tanpa mengarang rahasia atau kemampuan formal.
4. Verifikasi Wallet dari Authority yang eksplisit; jika tidak ada, gunakan snapshot karakter (sesi baru) atau profil aktif (sesi berlanjut). Jika saldo tidak ditetapkan, lakukan satu undian bootstrap menurut `core/10_ECONOMY_SYSTEM.md`, catat, dan jangan undi ulang.
5. Periksa `world/DYNAMIC_EVENTS.md` dan baca modul yang relevan dengan lokasi, waktu, kondisi, serta aksi. Jika sumber wajib gagal diakses, sebutkan path dan jangan mengaku pemeriksaan selesai.
6. Validasi state, ledger, field, dan format sebelum respons. Mulai adegan langsung; jangan tampilkan laporan bootstrap.

### State dan format

- `templates/GAMEPLAY_RESPONSE_TEMPLATE.md` adalah satu-satunya master visual respons GM; footer wajib persis `••• Tentukan Aksimu (⁠｡⁠•̀⁠ᴗ⁠-⁠)⁠✧`. Template player hanya untuk input, bukan format GM.
- Wallet menggunakan urutan `xc | xs | xg | zj | az`. Kurs/transaksi dari `core/10_ECONOMY_SYSTEM.md`; Satiety dari `core/HUNGER_AND_METABOLISM.md`. Setiap aktivitas terbaru menyebut Satiety.
- Jangan mengganti nilai tercatat, kehilangan item/aset, menebak saldo, atau membocorkan catatan GM sebagai pengetahuan karakter. Ledger perubahan state mengikuti Authority Order dan modul terkait; `Log tercatat!` bukan klaim bahwa GitHub telah diubah.
- Spirit Ring Absorption memakai satu field `status | Day left`. Definisi status: `templates/CHARACTER_PROFILE_TEMPLATE.md`; timer: `gameplay/TIME_AND_ACTION_RULES.md` §7; interval: `bestiary/SPIRIT_BEAST_RULES.md`; syarat penyerapan: `core/SPIRIT_RING_RULES.md`.
- Gunakan istilah **Spirit Realm** secara utuh untuk tingkat 1–9: Spirit Initiate, Spirit Adept, Spirit Elder, Spirit Monarch, Spirit King, Spirit Ancestor, Spirit Emperor, Spirit Sovereign, Spirit Primordial. **Mortal** adalah status dasar, bukan Spirit Realm 0.
- Jangan menambah field tanpa persetujuan owner. `???` hanya untuk identitas karakter yang benar-benar tidak diketahui atau nama Martial Soul yang belum diketahui; nilai lain mengikuti default resmi.

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
- `world/DYNAMIC_EVENTS.md`: registry event canon; periksa setiap giliran.
- `templates/WORLD_EVENT_UPDATE_TEMPLATE.md`: proposal event; bukan canon sampai disetujui dan di-commit owner/admin.
- Modul mekanik/world adalah otoritas untuk cakupannya. `players.md` adalah indeks; `players/<Nama>.md` adalah snapshot awal; profil gameplay terakhir beserta kejadian sesudahnya adalah state aktif.
- Penilaian universal dan Kantor Appraisal: `core/TIER_ASSESSMENT_AND_APPRAISAL.md`. Martial Soul memakai formulasi khusus `core/MARTIAL_SOUL_AWAKENING.md`; rarity hasil undian terpisah dari kualitas inheren.

## Daftar File Resmi

- `README.md`
- `INDEX.md`
- `players.md`
- `players/Yuha.md`
- `players/Nafila.md`
- `templates/AUTHORITY_ORDER.md`
- `templates/GAMEPLAY_RESPONSE_TEMPLATE.md`
- `templates/CHARACTER_PROFILE_TEMPLATE.md`
- `templates/PLAYER_CONVERSATION_TEMPLATE.md`
- `core/CULTIVATION_SYSTEM.md`
- `core/CULTIVATOR_ACADEMIES.md`
- `core/MARTIAL_SOUL.md`
- `core/MARTIAL_SOUL_AWAKENING.md`
- `core/SPIRIT_RING_RULES.md`
- `core/HP_SYSTEM.md`
- `core/HUNGER_AND_METABOLISM.md`
- `core/INJURY_SYSTEM.md`
- `core/THINKER_AND_FORMULATION.md`
- `core/10_ECONOMY_SYSTEM.md`
- `bestiary/SPIRIT_BEAST_RULES.md`
- `gameplay/COMBAT_SYSTEM.md`
- `gameplay/TIME_AND_ACTION_RULES.md`
- `gameplay/TRAVEL_ENCOUNTER_AMBUSH_RESCUE.md`
- `world/WORLD.md`
- `world/GOLDEN_DRAGON_EMPIRE_GOVERNANCE.md`
- `world/GOLDEN_DRAGON_EMPIRE_ADMINISTRATIVE_ATLAS.md`
- `world/MAP_AND_REGIONS.md`
- `world/LAWLESS_TERRITORIES.md`
- `world/GEOGRAPHY_AND_TRAVEL.md`
- `world/WANLUO_SACRED_EXPANSE.md`
- `world/INTELLIGENT_PEOPLES.md`
- `world/FACTIONS.md`
- `world/SPIRIT_HUNTERS_GUILD.md`
- `world/HISTORY.md`
- `world/RUINED_ARCHIVER.md`
- `world/DYNAMIC_EVENTS.md`
- `templates/WORLD_EVENT_UPDATE_TEMPLATE.md`
- `world/ARTIFACTS_AND_RELICS.md`
- `world/ARTIFICIAL_ARTIFACTS.md`
- `world/WEALTH_DISTRIBUTION.md`
- `world/SOCIAL_STRATIFICATION.md`

Modul yang disebut tetapi belum tersedia tidak otomatis menjadi sumber resmi. Jangan mengklaim membacanya atau menganggap isinya sudah ditetapkan.

## 3. Regional dan territorial canon — buka saat relevan

Untuk wilayah, permukiman, rute, NPC, pemerintahan, atau faksi, gunakan router khusus:
- `world/CANON_LOAD_ROUTER.md` — jalur canon wilayah, roster regional, NPC, permukiman, dan pemicu navigasi.
- Baca hanya bagian dan sumber yang cocok dengan adegan/aksi; audit lintas wilayah tetap wajib memeriksa seluruh register yang terdampak.

Router regional mempertahankan detail yang sebelumnya berada di INDEX agar tidak hilang, tetapi tidak perlu dibaca pada giliran yang tidak menyentuh wilayah/NPC terkait.

## 4. Standar pemeliharaan canon

- NPC utama/berulang memiliki satu profil penuh canonical yang ditautkan registry; periksa roster sebelum membuat pejabat atau anggota faksi. NPC biasa/temporer mengikuti `world/NPC_MANAGEMENT.md`.
- Data regional baru mengikuti urutan: identitas → geografi → permukiman/kehidupan → ekonomi/sumber daya → kultivasi/Spirit Beast/Thinker → faksi/otoritas → NPC → konflik/event → rute/panduan GM. Referensikan sumber bersama, jangan menduplikasinya.
- Jangan mengklaim event/proposal telah menjadi canon atau tersimpan tanpa persetujuan dan perubahan repo terverifikasi.
