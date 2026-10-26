## 0. Bootstrap wajib

Trigger awal yang merujuk `INDEX.md` dan `players.md` berarti mulai gameplay, bukan membuat laporan.

1. Baca penuh `templates/GAMEPLAY_RESPONSE_TEMPLATE.md`, lalu `templates/CHARACTER_PROFILE_TEMPLATE.md`.
2. Pilih state: sesi baru memakai `players.md` lalu seluruh `players/<Nama>.md`; sesi berlanjut memakai profil gameplay terakhir dan kejadian sesudahnya; karakter baru memakai template tanpa mengarang rahasia atau kemampuan formal.
3. Verifikasi Wallet dari Authority yang eksplisit; jika tidak ada, gunakan snapshot karakter (sesi baru) atau profil aktif (sesi berlanjut). Jika saldo tidak ditetapkan, lakukan satu undian bootstrap menurut `core/10_ECONOMY_SYSTEM.md`, catat, dan jangan undi ulang.
4. Periksa `world/DYNAMIC_EVENTS.md` dan baca modul yang relevan dengan lokasi, waktu, kondisi, serta aksi. Jika sumber wajib gagal diakses, sebutkan path dan jangan mengaku pemeriksaan selesai.
5. Validasi state, ledger, field, dan format sebelum respons. Mulai adegan langsung; jangan tampilkan laporan bootstrap.

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

## 3. Regional Modules and NPC References

The three major powers are **Golden Dragon Empire, Tianhai Yunzhou, and Beiming Gu**. They are represented by regional folders/modules inside this one repository, not separate GitHub repositories. Canonical full NPC profiles and registries are maintained under `regions/<power>/npcs/`; the regional INDEX and registry guide NPC lookup, while the relevant `world/REGION_*.md` module remains the source for established regional/location context unless another canonical source is explicitly linked. Legacy `world/NPC_*.md` files must be inspected individually: treat each as a legacy source until its actual contents confirm that it is a compatibility pointer. Do not invent missing canon from scaffold headings. For NPC handling, use `world/NPC_MANAGEMENT.md`, the relevant regional module, the regional NPC registry, and `templates/NPC_PROFILE_TEMPLATE.md`.

### Golden Dragon Empire
- civil and military governance across the Golden Dragon Empire — `world/GOLDEN_DRAGON_EMPIRE_GOVERNANCE.md`
- Named central ministers, seven regional governors, twelve active prefectural offices, and retained former prefects/county magistrates — `world/GOLDEN_DRAGON_EMPIRE_OFFICIALS.md`
- Population-facing services, bank and information-exchange offices, Medicine Hall Society locations, two central dormitory-based academies, and selected Ordo Suci Tianming public libraries — `world/GOLDEN_DRAGON_EMPIRE_POPULATION_SERVICES.md`
- Seven-region, twelve-prefecture, six-county-circuit register and thirteen named rural villages — `world/GOLDEN_DRAGON_EMPIRE_ADMINISTRATIVE_ATLAS.md`

**Canon lock — official villages vs. local settlements (Golden Dragon Empire):**
- The Golden Dragon Empire has exactly **13 officially registered named villages**. The canonical names and regional distribution must be taken from `world/GOLDEN_DRAGON_EMPIRE_ADMINISTRATIVE_ATLAS.md`; the seven `world/REGION_*.md` files must agree with that register.
- The atlas also lists **21 named hamlets/local settlements** for exploration and local route continuity. These are not official villages and must never be added to the official village count.
- When counting, use only entries explicitly classified as `Village` in the canonical atlas. Entries classified as `Hamlet` or another local-settlement status are separate categories, even if an older revision or regional table used the word “Village.”
- If a regional file, atlas heading/table, summary, or other document gives a conflicting number or classification, do not average, infer, or silently choose the larger list. Follow the canonical atlas and the owner’s recorded canon decisions; correct the inconsistent newer/secondary material and preserve useful extra locations under their correct local-settlement status.
- Before adding a settlement or editing a regional roster, cross-check the atlas and all seven regional village counts. Do not promote a hamlet to an official village unless the owner explicitly approves a canon change and the atlas plus every affected reference are updated together.

- Longyuan — `world/REGION_LONGYUAN.md`
- Canglan — `world/REGION_CANGLAN.md`
- Jinyue — `world/REGION_JINYUE.md`
- Tianfeng — `world/REGION_TIANFENG.md`
- Yanling — `world/REGION_YANLING.md`
- Baiyue — `world/REGION_BAIYUE.md`
- Xingluo — `world/REGION_XINGLUO.md`

### Tianhai Yunzhou
- Tianhai Yunzhou — `world/REGION_TIANHAI_YUNZHOU.md`
- Tianhai Yunzhou Spirit Hunters Guild offices, independent trade associations, and Medicine Hall Society service points — `world/REGION_TIANHAI_YUNZHOU.md` and `world/FACTIONS.md`
- Four cardinal areas, twelve clan placements, four Cultivator Academies, and the exclusive high-level Thinker Institute — `world/TIANHAI_ACADEMIES_AND_THINKER_INSTITUTE.md`
- Tianhai Yunzhou court, civil/military officials, district administrators, clan heads, dojo masters, Thinker institutions — `regions/tianhai-yunzhou/npcs/POWER_STRUCTURE.md`
- Maharaja Ji Haoyuan — `regions/tianhai-yunzhou/npcs/JI_HAOYUAN.md`
- Bai Xuanyin, revered Tianhai Yunzhou heroine — `regions/tianhai-yunzhou/npcs/BAI_XUANYIN.md`
- Ji Zhaoning, elder twin princess — `regions/tianhai-yunzhou/npcs/JI_ZHAONING.md`
- Ji Ningzhao, younger twin princess — `regions/tianhai-yunzhou/npcs/JI_NINGZHAO.md`

### Beiming Gu
- Beiming Heartland — `world/REGION_BEIMING_HEARTLAND.md`
- Frostveil Range — `world/REGION_FROSTVEIL_RANGE.md`
- Azureflame Basin — `world/REGION_AZUREFLAME_BASIN.md`
- Silverpine Wilds — `world/REGION_SILVERPINE_WILDS.md`
- Stonegate March — `world/REGION_STONEGATE_MARCH.md`
- Hollowmoon Valley — `world/REGION_HOLLOWMOON_VALLEY.md`
- Ironroot Reach — `world/REGION_IRONROOT_REACH.md`
- Beiming Gu NPC registry and full roster — `regions/beiming-gu/npcs/REGISTRY.md`; established profiles: `regions/beiming-gu/npcs/BEIMING_HAN.md`, `regions/beiming-gu/npcs/BEIMING_XENHWA.md`, `regions/beiming-gu/npcs/BEIMING_JINGHENG.md`, `regions/beiming-gu/npcs/BEIMING_NERVA.md`; clan/dojo roster profiles are linked from the registry.

### Lawless Territories
- Ashen Borderlands — `world/REGION_ASHEN_BORDERLANDS.md`
- Black Tide Expanse — `world/REGION_BLACK_TIDE_EXPANSE.md`
- Nine Frost Wastes — `world/REGION_NINE_FROST_WASTES.md`
- **Lawless Territories master reference** (underground economy, organizations' service roles, neutral refuge, Azerion Forest, Dead Zone as the deepest core only, central lake and Mega Colossal Labyrinth, unexplored-ruin map/hidden-treasure rules, hidden Inner Azerion city and half-beast economy, illusion fog, human access risks, slave market, food scarcity, elite auctions) — `world/LAWLESS_TERRITORIES.md`

### NPC modules and templates
- NPC management rules — `world/NPC_MANAGEMENT.md`
- Regional module template — `templates/REGIONAL_MODULE_TEMPLATE.md`
- NPC profile template — `templates/NPC_PROFILE_TEMPLATE.md`

### Established Imperial Family NPC Profiles
- Emperor Jun Haotian — `regions/golden-dragon-empire/npcs/JUN_HAOTIAN.md`
- Empress Shen Yuehua — `regions/golden-dragon-empire/npcs/SHEN_YUEHUA.md`
- Crown Prince Jun Ruiyuan — `regions/golden-dragon-empire/npcs/JUN_RUIYUAN.md`
- Princess Jun Yuejin — `regions/golden-dragon-empire/npcs/JUN_YUEJIN.md`



### Regional structure, NPCs, and route network
- Golden Dragon Empire regional INDEX and NPC registry — `regions/golden-dragon-empire/INDEX.md` and `regions/golden-dragon-empire/npcs/REGISTRY.md`
- Tianhai Yunzhou regional INDEX and NPC registry — `regions/tianhai-yunzhou/INDEX.md` and `regions/tianhai-yunzhou/npcs/REGISTRY.md`
- Beiming Gu regional INDEX and NPC registry — `regions/beiming-gu/INDEX.md` and `regions/beiming-gu/npcs/REGISTRY.md`

- Location and route network rules — `world/LOCATION_AND_ROUTE_NETWORK.md`
- NPC agency, regional placement, and continuity — `world/NPC_MANAGEMENT.md`
- Regional module standard — `templates/REGIONAL_MODULE_TEMPLATE.md`
- Canonical full NPC profile standard — `templates/NPC_PROFILE_TEMPLATE.md`

**Required regional workflow:** when a scene involves a named region, first perform the applicable global canon/precedence checks in the `Mandatory Territorial Canon Load Path — All Major Powers` below, then load the exact regional module from `world/REGION_*.md` for local context. Check the NPC table beside the relevant settlement, institution, or faction heading; use the regional NPC registry for broader roster audits, then consult only the canonical profile of an established recurring/major NPC relevant to the scene. When travel is involved, verify the route through `world/LOCATION_AND_ROUTE_NETWORK.md`, the relevant origin/destination regional modules, and `world/GEOGRAPHY_AND_TRAVEL.md`; resolve duration only through `gameplay/TIME_AND_ACTION_RULES.md`. Do not assume direct connections between all locations.

**Regional data format:** regional modules should keep the same conceptual order: identity → geography → settlements and local life → economy/resources → cultivation/Spirit Beasts/Thinkers → factions/authority → NPC registry → conflicts/events → route network and GM guidance. Existing canon may remain in its established subsection when moving it would risk loss, but new and revised regional content should follow this order and cross-reference rather than duplicate shared records.

**NPC placement:** follow the path: central INDEX → relevant regional/settlement module → NPC table grouped beside the matching location or faction → canonical full profile when needed. Ordinary residents and temporary scene characters may be portrayed situationally under `world/NPC_MANAGEMENT.md`. Recurring and major NPCs belong in the regional registry for discoverability and should link to one canonical full profile. Check official and faction rosters before creating an officeholder or faction member. Separate public knowledge, NPC knowledge, beliefs, and GM-only secrets.

**Route and economy realism:** routes must reflect confirmed geography and transport. Some settlements require an intermediate village, bridge, ferry, pass, port, or gate. Local resources, crafts, labor, demand, and services should create plausible trade relationships, but proposals remain non-canon until owner-approved.

## 3. Canon wilayah — jalur wajib

### Semua kekuasaan besar dan Lawless Territories

Untuk gameplay, lore, audit, atau edit yang melibatkan Golden Dragon Empire, Tianhai Yunzhou, Beiming Gu, atau Lawless Territories:
1. Baca `world/CANON_DECISIONS_AND_PRECEDENCE.md`; baca `world/WORLD.md` dan `world/MAP_AND_REGIONS.md` bila konteks global/lintas wilayah relevan.
2. Baca modul `world/REGION_*.md` yang sesuai; untuk Lawless Territories baca `world/LAWLESS_TERRITORIES.md`.
3. Ikuti INDEX ke sumber khusus pemerintahan, faksi, institusi, layanan, ekonomi, atau NPC. Untuk NPC, gunakan `regions/<power>/INDEX.md` dan `regions/<power>/npcs/REGISTRY.md`, lalu baca profil canonical yang relevan.
4. Untuk perjalanan, verifikasi rute melalui `world/LOCATION_AND_ROUTE_NETWORK.md`, modul wilayah asal/tujuan, dan `world/GEOGRAPHY_AND_TRAVEL.md`; durasi hanya dari `gameplay/TIME_AND_ACTION_RULES.md`.
5. Untuk audit lintas wilayah, baca semua roster/register yang terdampak. Jangan mengasumsikan koneksi langsung atau memindahkan hitungan, pemerintahan, harga, institusi, dan norma sosial antar-kekuasaan.
6. Perlakukan scaffold dan detail yang belum ditetapkan sebagai belum diketahui. Pisahkan canon, proposal, estimasi, rumor, dan rahasia.

### Golden Dragon Empire — permukiman

Untuk menghitung, mengubah nama/klasifikasi, atau mengedit permukiman, baca `world/CANON_DECISIONS_AND_PRECEDENCE.md`, `world/GOLDEN_DRAGON_EMPIRE_ADMINISTRATIVE_ATLAS.md`, dan modul regional terkait. Untuk audit total, perbandingan lintas wilayah, atau edit roster, baca ketujuh modul regional Golden Dragon Empire; tambahkan peta/rute/geografi bila relevan.

Canon tetap: **13 desa resmi bernama** dan **21 hamlet/permukiman lokal bernama yang terpisah**. Hanya entri `Village` dalam atlas dihitung sebagai desa resmi. Perubahan status memerlukan persetujuan eksplisit owner dan sinkronisasi seluruh referensi terkait.

### Pemicu navigasi cepat

| Situasi | Sumber tambahan |
|---|---|
| Wilayah/permukiman atau perjalanan | Modul regional; `world/MAP_AND_REGIONS.md`, `world/LOCATION_AND_ROUTE_NETWORK.md`, `world/GEOGRAPHY_AND_TRAVEL.md` sesuai kebutuhan; Lawless: `world/LAWLESS_TERRITORIES.md` |
| NPC utama/berulang | Registry regional dan profil canonical NPC |
| NPC minor baru | `world/NPC_MANAGEMENT.md`, `templates/NPC_PROFILE_TEMPLATE.md` |
| Ruin, peta, kredit ekspedisi, kompensasi, anomali | `world/RUINED_ARCHIVER.md`, `world/GEOGRAPHY_AND_TRAVEL.md`, `world/HISTORY.md`, modul regional terkait |
| Faksi/keanggotaan/kewenangan | `world/FACTIONS.md` dan modul regional |
| Guild, kontrak, party, bounty, perburuan | `world/SPIRIT_HUNTERS_GUILD.md`; modul ring/beast/combat bila relevan |
| Awakening/Martial Soul Awakening Hall | `world/CANON_DECISIONS_AND_PRECEDENCE.md`, `core/MARTIAL_SOUL.md`, `core/MARTIAL_SOUL_AWAKENING.md`, sumber regional/pemerintahan |
| Spirit Ring Absorption | `core/SPIRIT_RING_RULES.md`, `core/CULTIVATION_SYSTEM.md`, `bestiary/SPIRIT_BEAST_RULES.md`, modul HP/injury/time/rute/combat yang relevan |
| Pemerintahan/administrasi Golden Dragon Empire | `world/GOLDEN_DRAGON_EMPIRE_GOVERNANCE.md`, `world/GOLDEN_DRAGON_EMPIRE_ADMINISTRATIVE_ATLAS.md`, modul regional/NPC |
| Bank, informasi, medis, pendidikan dasar, perpustakaan Golden Dragon Empire | `world/GOLDEN_DRAGON_EMPIRE_POPULATION_SERVICES.md` dan modul regional |
| Guild/layanan medis di Tianhai Yunzhou | `world/REGION_TIANHAI_YUNZHOU.md`, `world/FACTIONS.md`, `world/SPIRIT_HUNTERS_GUILD.md`; ekonomi untuk harga |
| Dampak NPC persisten pada dunia | `world/DYNAMIC_EVENTS.md` dan alur proposal event yang disetujui; jangan klaim persistensi tanpa commit terverifikasi |

## 4. Standar pemeliharaan canon

- NPC utama/berulang memiliki satu profil penuh canonical yang ditautkan registry; periksa roster sebelum membuat pejabat atau anggota faksi. NPC biasa/temporer mengikuti `world/NPC_MANAGEMENT.md`.
- Data regional baru mengikuti urutan: identitas → geografi → permukiman/kehidupan → ekonomi/sumber daya → kultivasi/Spirit Beast/Thinker → faksi/otoritas → NPC → konflik/event → rute/panduan GM. Referensikan sumber bersama, jangan menduplikasinya.
- Jangan mengklaim event/proposal telah menjadi canon atau tersimpan tanpa persetujuan dan perubahan repo terverifikasi.