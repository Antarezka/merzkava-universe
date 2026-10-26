# Merzkava Universe — Official Index

INDEX ini adalah **router** untuk memulai, melanjutkan, dan menjalankan roleplay Merzkava Universe. Aturan mekanik dan format berada di modul masing-masing. INDEX hanya menunjuk ke sana, jadi jangan menyalin aturan dari modul ke file ini.

Repository resmi: https://github.com/Antarezka/merzkava-universe

## 1. Bootstrap (urutan tetap)

1. Baca INDEX.md dan `templates/AUTHORITY_ORDER.md`.
2. Pilih mode sesi (AUTHORITY_ORDER §3):
   - Sesi baru: pakai snapshot `players/<Nama>.md`.
   - Sesi berlanjut: pakai profil gameplay terakhir dan kejadian sesudahnya. Jangan menimpa state dengan snapshot.
3. Muat sumber berikut sebelum respons pertama, sesuai urutan:
   a. `templates/GAMEPLAY_RESPONSE_TEMPLATE.md` — satu-satunya format visual.
   b. `templates/CHARACTER_PROFILE_TEMPLATE.md` — definisi field profil.
   c. Profil karakter: `players.md`, lalu `players/<Nama>.md` untuk sesi baru.
   d. Saldo Wallet: ambil dari file karakter yang cocok. Aturan transaksi ada di `core/10_ECONOMY_SYSTEM.md`.
4. Periksa `world/DYNAMIC_EVENTS.md` sebelum adegan pertama dan setiap giliran.
5. Baca modul yang relevan dengan lokasi, waktu, karakter, dan aksi (lihat §3). Jangan membaca seluruh repo sekaligus.
6. Mulai gameplay langsung. Jangan tampilkan laporan bootstrap atau daftar file yang dibaca.

Jika sumber wajib gagal diakses, sebutkan file yang gagal dan jangan mengaku sudah membacanya.

## 2. Format respons GM

- Format visual gameplay hanya diatur oleh `templates/GAMEPLAY_RESPONSE_TEMPLATE.md`.
- Penutup setiap respons gameplay ditulis persis: `••• Tentukan Aksimu (⁠｡⁠•̀⁠ᴗ⁠-⁠)⁠✧`
- `Aksiku:` adalah label input player (`templates/PLAYER_CONVERSATION_TEMPLATE.md`). Label itu bukan penutup GM.

## 3. Navigasi modul

| Kebutuhan | Sumber resmi |
|---|---|
| Aturan GM, hierarki sumber, mode sesi | `templates/AUTHORITY_ORDER.md` |
| Definisi field profil dan status Spirit Ring Absorption | `templates/CHARACTER_PROFILE_TEMPLATE.md` |
| Kalender, timestamp, durasi aksi, time skip, rumus Day left (§7) | `gameplay/TIME_AND_ACTION_RULES.md` |
| Encounter perjalanan, ambush, pertolongan darurat | `gameplay/TRAVEL_ENCOUNTER_AMBUSH_RESCUE.md` |
| Combat, multi-hit, combo, damage, pertahanan | `gameplay/COMBAT_SYSTEM.md` |
| HP | `core/HP_SYSTEM.md` |
| Cedera dan pemulihan | `core/INJURY_SYSTEM.md` |
| Spirit Realm, Stage, Sync, bottleneck, breakthrough | `core/CULTIVATION_SYSTEM.md` |
| Akademi kultivator dan pendidikan dasar | `core/CULTIVATOR_ACADEMIES.md` |
| Spirit Ring, kompatibilitas, penyerapan, deviasi | `core/SPIRIT_RING_RULES.md` |
| Spirit Beast, syarat ring, jeda minimum | `bestiary/SPIRIT_BEAST_RULES.md` |
| Martial Soul: lore dan karakteristik | `core/MARTIAL_SOUL.md` |
| Martial Soul: awakening, undian rarity, mutasi | `core/MARTIAL_SOUL_AWAKENING.md` |
| Thinker Grade, formulasi, Artificial Artifact | `core/THINKER_AND_FORMULATION.md` |
| Penilaian tier dan Kantor Appraisal (MAA) | `core/TIER_ASSESSMENT_AND_APPRAISAL.md` |
| Satiety, aktivitas, makan, tidur, kondisi tubuh | `core/HUNGER_AND_METABOLISM.md` |
| Harga, transaksi, kurs, Currency, ledger uang dan item | `core/10_ECONOMY_SYSTEM.md` |
| Keputusan canon owner dan prioritas sumber | `world/CANON_DECISIONS_AND_PRECEDENCE.md` |
| Registry event dunia persisten | `world/DYNAMIC_EVENTS.md` |
| Form proposal event (bukan canon sampai disetujui) | `templates/WORLD_EVENT_UPDATE_TEMPLATE.md` |
| Dunia, tokoh, tiga kekuasaan utama | `world/WORLD.md` |
| Peta, wilayah, permukiman, rute yang diketahui | `world/MAP_AND_REGIONS.md` |
| Rute dan jaringan lokasi | `world/LOCATION_AND_ROUTE_NETWORK.md` |
| Geografi fisik, moda transportasi, batas pengetahuan rute | `world/GEOGRAPHY_AND_TRAVEL.md` |
| Sejarah dan bukti sejarah | `world/HISTORY.md` |
| Faksi, klan, dojo, sekte, organisasi | `world/FACTIONS.md` |
| Serikat Guild dan kontrak | `world/SPIRIT_HUNTERS_GUILD.md` |
| Pemerintahan Golden Dragon Empire | `world/GOLDEN_DRAGON_EMPIRE_GOVERNANCE.md` |
| Pejabat Golden Dragon Empire | `world/GOLDEN_DRAGON_EMPIRE_OFFICIALS.md` |
| Layanan publik Golden Dragon Empire | `world/GOLDEN_DRAGON_EMPIRE_POPULATION_SERVICES.md` |
| Atlas wilayah dan desa Golden Dragon Empire | `world/GOLDEN_DRAGON_EMPIRE_ADMINISTRATIVE_ATLAS.md` |
| Lawless Territories | `world/LAWLESS_TERRITORIES.md` |
| Ancient Shamanism dan klan Buddhis tersembunyi | `world/ANCIENT_SHAMANISM_AND_BUDDHIST_CLANS.md` |
| Bangsa berakal | `world/INTELLIGENT_PEOPLES.md` |
| Kelas sosial dan kemiskinan | `world/SOCIAL_STRATIFICATION.md` |
| Distribusi kekayaan | `world/WEALTH_DISTRIBUTION.md` |
| Relic dan Ancient Artifact | `world/ARTIFACTS_AND_RELICS.md` |
| Artificial Artifact | `world/ARTIFICIAL_ARTIFACTS.md` |
| Ruined Archiver | `world/RUINED_ARCHIVER.md` |
| Kawasan suci Wanluo | `world/WANLUO_SACRED_EXPANSE.md` |
| Akademi Tianhai dan Thinker Institute | `world/TIANHAI_ACADEMIES_AND_THINKER_INSTITUTE.md` |
| Aturan NPC | `world/NPC_MANAGEMENT.md` |

Untuk aksi yang menyentuh beberapa sistem, baca semua modul yang relevan. Contoh: combat yang mengubah HP dan menimbulkan luka memerlukan Combat, HP, Injury, Time, dan Hunger/Metabolism.

## 4. Wilayah, NPC, dan struktur repo

- Semua canon berada dalam satu repo ini. Golden Dragon Empire, Tianhai Yunzhou, dan Beiming Gu adalah tiga folder regional di dalamnya, bukan repo terpisah. Jangan membuat atau menyarankan repo regional baru atau migrasi.
- Struktur kanonis: `world/` untuk canon global, `regions/<power>/` untuk indeks dan NPC regional, dan `world/REGION_*.md` untuk modul lokasi. Susunan lengkap ada di `world/REGIONAL_REPOSITORY_ARCHITECTURE.md`.
- Registry NPC: `regions/golden-dragon-empire/npcs/REGISTRY.md`, `regions/tianhai-yunzhou/npcs/REGISTRY.md`, `regions/beiming-gu/npcs/REGISTRY.md`.
- Modul regional Golden Dragon Empire: `world/REGION_LONGYUAN.md`, `REGION_CANGLAN.md`, `REGION_JINYUE.md`, `REGION_TIANFENG.md`, `REGION_YANLING.md`, `REGION_BAIYUE.md`, `REGION_XINGLUO.md`.
- Modul regional Tianhai Yunzhou: `world/REGION_TIANHAI_YUNZHOU.md`.
- Modul regional Beiming Gu: `world/REGION_BEIMING_HEARTLAND.md`, `REGION_FROSTVEIL_RANGE.md`, `REGION_AZUREFLAME_BASIN.md`, `REGION_SILVERPINE_WILDS.md`, `REGION_STONEGATE_MARCH.md`, `REGION_HOLLOWMOON_VALLEY.md`, `REGION_IRONROOT_REACH.md`.
- Modul Lawless Territories: `world/REGION_ASHEN_BORDERLANDS.md`, `REGION_BLACK_TIDE_EXPANSE.md`, `REGION_NINE_FROST_WASTES.md`.
- Beiming Gu masih berstatus scaffold. Detail yang belum tercatat tetap belum ditetapkan dan tidak boleh diisi sebagai canon tetap.
- Mengubah atau menghapus `world/NPC_*.md` harus diperiksa per file dulu. Pastikan referensinya ikut disinkronkan.
- Aturan wajib pemuatan canon per kekuasaan ada di `templates/AUTHORITY_ORDER.md` §2A dan §2B.

## 5. Istilah kultivasi

- Untuk tingkat 1–9 gunakan **Spirit Realm**. Jangan menyingkatnya menjadi `Realm` atau `Cultivation Realm`.
- Nama tingkat resmi: Spirit Initiate, Spirit Adept, Spirit Elder, Spirit Monarch, Spirit King, Spirit Ancestor, Spirit Emperor, Spirit Sovereign, Spirit Primordial.
- **Mortal** adalah status dasar sebelum Spirit Realm 1, bukan Spirit Realm 0.
- Nama proper yang memakai kata "Realm" dengan arti lain, seperti Heaven Realm dalam sejarah, tidak diubah.

## 6. Aturan yang berlaku lintas dokumen

Aturan berikut ditulis lengkap di sumber masing-masing. INDEX hanya mengingatkan:

- Satiety, Wallet, Inventory, dan Equipment hanya berubah karena kejadian sah. Lihat `core/HUNGER_AND_METABOLISM.md` dan `core/10_ECONOMY_SYSTEM.md`.
- Penggunaan `???` sangat terbatas. Lihat `templates/CHARACTER_PROFILE_TEMPLATE.md`.
- Event dunia hanya menjadi canon setelah disetujui dan di-commit oleh owner atau admin. Lihat `templates/AUTHORITY_ORDER.md` §5.
- Snapshot karakter dan registry tidak diubah selama gameplay tanpa permintaan eksplisit pemilik repo.
- Jangan mengklaim perubahan tersimpan di GitHub sebelum penulisan dilakukan dan diverifikasi.
- Jangan memberi menu pilihan atau daftar opsi bernomor. Akhiri adegan dengan situasi terbuka.

## 7. Batas canon

Angka desa dan wilayah Golden Dragon Empire hanya berlaku untuk Golden Dragon Empire. Lihat `world/GOLDEN_DRAGON_EMPIRE_ADMINISTRATIVE_ATLAS.md`. Jangan menerapkan angka itu ke Tianhai Yunzhou atau Beiming Gu. Modul yang disebut tetapi belum tersedia bukan sumber resmi.
