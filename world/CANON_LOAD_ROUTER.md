# Merzkava Universe — Regional Canon Load Router

This specialist router is loaded only when regional, NPC, settlement, or territorial canon is relevant. The central `INDEX.md` remains the bootstrap and general navigation entry point.

## 1. Connected Tree and Transit Entry

For the full connected navigation tree across all three major powers, their established regional branches, canonical source paths, and the inter-power transit graph, start at [`world/WORLD_NAVIGATION_TREE.md`](WORLD_NAVIGATION_TREE.md). It is a navigation index, not a replacement for source files. For travel, verify each edge in `world/LOCATION_AND_ROUTE_NETWORK.md`, `world/GEOGRAPHY_AND_TRAVEL.md`, both endpoint regional modules, and `gameplay/TIME_AND_ACTION_RULES.md`. Three dedicated direct air corridors are established, including Longyuan Sky Transit Terminal (Golden Dragon Empire) ↔ Beiming Heartland Sky Transit Terminal (Beiming Gu); do not force a transfer through Tianhai Yunzhou. Check current access conditions and disruptions in the authoritative route and regional sources.

## 2. Regional Modules and NPC References

The three major powers are **Golden Dragon Empire, Tianhai Yunzhou, and Beiming Gu**. They are represented by regional folders/modules inside this one repository, not separate GitHub repositories. Canonical full NPC profiles and registries are maintained under `regions/<power>/npcs/`; the regional INDEX and registry guide NPC lookup, while the relevant regional module remains the source for established regional/location context unless another canonical source is explicitly linked. For Beiming Gu, the single canonical module is `world/REGION_BEIMING_GU.md`. Legacy `world/NPC_*.md` files must be inspected individually: treat each as a legacy source until its actual contents confirm that it is a compatibility pointer. Do not invent missing canon from scaffold headings. For NPC handling, use `world/NPC_MANAGEMENT.md`, the relevant regional module, the regional NPC registry, and `templates/NPC_PROFILE_TEMPLATE.md`.

### Golden Dragon Empire
- civil and military governance across the Golden Dragon Empire — `world/GOLDEN_DRAGON_EMPIRE_GOVERNANCE.md`
- Named central ministers, seven regional governors, twelve active prefectural offices, and retained former prefects/county magistrates — `world/GOLDEN_DRAGON_EMPIRE_OFFICIALS.md`
- Population-facing services, bank and information-exchange offices, Medicine Hall Society locations, two central dormitory-based academies, and selected Ordo Suci Tianming public libraries — `world/GOLDEN_DRAGON_EMPIRE_POPULATION_SERVICES.md`
- Seven-region, twelve-prefecture, six-county-circuit register and thirteen named rural villages — `world/GOLDEN_DRAGON_EMPIRE_ADMINISTRATIVE_ATLAS.md`
- Ying Wuxin's public civilian life in Huanglongcheng, Longyuan, and the restricted GM canon separating it from his concealed criminal identity — `world/NPC_YING_WUXIN.md`; `world/REGION_LONGYUAN.md`; `regions/golden-dragon-empire/npcs/REGISTRY.md`

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
- **Single canonical regional reference for all seven districts** — `world/REGION_BEIMING_GU.md`
- Compatibility pointers retained for old district paths: `world/REGION_BEIMING_HEARTLAND.md`, `world/REGION_FROSTVEIL_RANGE.md`, `world/REGION_AZUREFLAME_BASIN.md`, `world/REGION_SILVERPINE_WILDS.md`, `world/REGION_STONEGATE_MARCH.md`, `world/REGION_HOLLOWMOON_VALLEY.md`, and `world/REGION_IRONROOT_REACH.md`. These are navigation redirects, not separate canon sources.
- Beiming Gu NPC registry and full roster — `regions/beiming-gu/npcs/REGISTRY.md`; established profiles: `regions/beiming-gu/npcs/BEIMING_HAN.md`, `regions/beiming-gu/npcs/BEIMING_XENHWA.md`, `regions/beiming-gu/npcs/BEIMING_JINGHENG.md`, `regions/beiming-gu/npcs/BEIMING_NERVA.md`; clan/dojo roster profiles are linked from the registry.

### Lawless Territories
- Ashen Borderlands — `world/REGION_ASHEN_BORDERLANDS.md`
- Black Tide Expanse — `world/REGION_BLACK_TIDE_EXPANSE.md`
- Nine Frost Wastes — `world/REGION_NINE_FROST_WASTES.md`
- **Lawless Territories master reference** (underground economy, organizations' service roles, neutral refuge, Azerion Forest, Dead Zone as the deepest core only, central lake and Mega Colossal Labyrinth, unexplored-ruin map/hidden-treasure rules, hidden Inner Azerion city and half-beast economy, illusion fog, human access risks, slave market, food scarcity, elite auctions) — `world/LAWLESS_TERRITORIES.md`
- **Crimson Sovereign Court and Ying Wuxin:** `world/REGION_BLACK_TIDE_EXPANSE.md`, `world/FACTIONS.md`, and canonical profile `world/NPC_YING_WUXIN.md`.

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

**One connected NPC ↔ Map path:** use the scene's starting point. For a named NPC, follow **profile → location → matching map → local context**. When the player enters or explores an area, follow **map → local NPC entries/institutions → plausible NPC profiles → scene**. Proactively check which established NPCs or everyday local roles fit the location; verify profiles, whereabouts, duties, relationships, and knowledge boundaries before using candidates. The registry only locates profiles, not another mandatory reading chain. For Beiming Gu, the map source is always `world/REGION_BEIMING_GU.md`. If travel matters, verify route and duration through route/geography/time sources. Never invent finer map details or assume physical presence from regional affiliation alone.

**Regional data format:** use `templates/REGIONAL_MODULE_TEMPLATE.md` as the single structural standard. This router owns source discovery, not a second regional-content template. Preserve existing canon when relocation risks losing facts, and cross-reference shared records rather than duplicating them.

**NPC placement:** follow the single `NPC profile → matching map/regional module → relevant local entry` path above. Ordinary residents and temporary scene characters may be portrayed situationally under `world/NPC_MANAGEMENT.md`. Recurring and major NPCs belong in the regional registry for discoverability and should link to one canonical full profile. Check official and faction rosters when establishing an officeholder or faction member. Separate public knowledge, NPC knowledge, beliefs, and GM-only secrets.

**Route and economy realism:** routes must reflect confirmed geography and transport. Some settlements require an intermediate village, bridge, ferry, pass, port, or gate. Local resources, crafts, labor, demand, and services should create plausible trade relationships, but proposals remain non-canon until owner-approved.

## 3. Canon wilayah — jalur wajib

### Semua kekuasaan besar dan Lawless Territories

Untuk gameplay, lore, audit, atau edit yang melibatkan Golden Dragon Empire, Tianhai Yunzhou, Beiming Gu, atau Lawless Territories:
1. Baca `world/CANON_DECISIONS_AND_PRECEDENCE.md`; baca `world/WORLD.md` dan `world/MAP_AND_REGIONS.md` bila konteks global/lintas wilayah relevan.
2. Baca modul regional kanonis yang sesuai; untuk seluruh tujuh distrik Beiming Gu gunakan `world/REGION_BEIMING_GU.md`, dan untuk Lawless Territories baca `world/LAWLESS_TERRITORIES.md`.
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