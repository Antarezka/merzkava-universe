# Xuanling Realm

**Eastern Fantasy roleplay world and game mechanics.**

## Mulai di sini
- **[INDEX.md](INDEX.md)** — entry point resmi, alur bootstrap, dan peta modul.
- **[templates/PLAYER_CONVERSATION_TEMPLATE.md](templates/PLAYER_CONVERSATION_TEMPLATE.md)** — prompt pemanggilan roleplay.
- **[world/WORLD.md](world/WORLD.md)** — fondasi lore dunia dan tiga kekuasaan utama.
- **[world/MAP_AND_REGIONS.md](world/MAP_AND_REGIONS.md)** — regional index dan batas pengetahuan geografis.
- **[world/GEOGRAPHY_AND_TRAVEL.md](world/GEOGRAPHY_AND_TRAVEL.md)** — geografi fisik, moda transportasi, perjalanan, dan batas informasi rute.
- **[world/INTELLIGENT_PEOPLES.md](world/INTELLIGENT_PEOPLES.md)** — bangsa berakal, ciri kelompok, dan konteks sosial.
- **[world/FACTIONS.md](world/FACTIONS.md)** — klan, dojo, sekte, dan organisasi yang tercatat.
- **[world/HISTORY.md](world/HISTORY.md)** — kronologi dan pencatatan bukti sejarah.
- **[world/ARTIFACTS_AND_RELICS.md](world/ARTIFACTS_AND_RELICS.md)** — kategori Relic/Ancient Artifact dan provenance.
- **[world/ARTIFICIAL_ARTIFACTS.md](world/ARTIFICIAL_ARTIFACTS.md)** — katalog Artificial Artifact; aturan produksi tetap berada di core system.
- **[world/WEALTH_DISTRIBUTION.md](world/WEALTH_DISTRIBUTION.md)** — total kekayaan global dan konsentrasi kepemilikan.
- **[world/SOCIAL_STRATIFICATION.md](world/SOCIAL_STRATIFICATION.md)** — elite, kelas menengah, rakyat miskin, slum, tunawisma, dan mobilitas sosial.
- **[players.md](players.md)** — indeks karakter terdaftar.
- **[players/Yuha.md](players/Yuha.md)** — snapshot awal karakter Yuha.
- **[templates/GM_PROMPT.md](templates/GM_PROMPT.md)** — perilaku operasional AI Game Master.
- **[templates/GAMEPLAY_RESPONSE_TEMPLATE.md](templates/GAMEPLAY_RESPONSE_TEMPLATE.md)** — satu-satunya format visual lengkap untuk respons gameplay.
- **[templates/CHARACTER_PROFILE_TEMPLATE.md](templates/CHARACTER_PROFILE_TEMPLATE.md)** — definisi field dan konsistensi profil.
- **[gameplay/TIME_AND_ACTION_RULES.md](gameplay/TIME_AND_ACTION_RULES.md)** — timestamp, batas aksi, tidur malam, dan time skip.
- **[gameplay/COMBAT_SYSTEM.md](gameplay/COMBAT_SYSTEM.md)** — resolusi combat, multi-hit, combo, damage, dan pertahanan.
- **[core/HUNGER_AND_METABOLISM.md](core/HUNGER_AND_METABOLISM.md)** — Satiety, jadwal makan, metabolisme Realm, dan pengaruh kondisi tubuh.
- **[core/HP_SYSTEM.md](core/HP_SYSTEM.md)** dan **[core/INJURY_SYSTEM.md](core/INJURY_SYSTEM.md)** — HP, klasifikasi cedera, dan pemulihan.
- **[core/CULTIVATION_SYSTEM.md](core/CULTIVATION_SYSTEM.md)** — Realm, Stage, Sync, bottleneck, breakthrough.
- **[core/MARTIAL_SOUL.md](core/MARTIAL_SOUL.md)** — awakening dan Martial Soul.
- **[core/SPIRIT_RING_RULES.md](core/SPIRIT_RING_RULES.md)** — Spirit Ring, kompatibilitas, penyerapan, Qi, PowerScale.
- **[core/THINKER_AND_FORMULATION.md](core/THINKER_AND_FORMULATION.md)** — Thinker Grade dan aturan produksi Artificial Artifact.

## Alur memulai roleplay
1. Gunakan `templates/PLAYER_CONVERSATION_TEMPLATE.md` dan trigger `CONVO — [Nama Karakter]`.
2. Untuk karakter terdaftar dalam sesi baru, baca `players.md`, lalu file individual karakter yang tertaut.
3. Untuk sesi berlanjut, gunakan profil terakhir dan kejadian setelahnya; jangan menimpa state dengan snapshot awal.
4. Pada setiap giliran, periksa INDEX dan muat modul relevan. Jika sumber gagal diakses, jangan mengaku telah membacanya.
5. Respons gameplay langsung menggunakan timestamp, narasi, profil, catatan konsistensi, dan `Aksiku : --` sesuai template. MODE: NO STEP berarti tanpa menu pilihan.

Untuk transaksi, kurs, penilaian harga, atau perubahan saldo, gunakan `core/10_ECONOMY_SYSTEM.md` dan catat perubahan yang sah.

## Prinsip proyek
- Jangan mengarang aturan atau mengklaim membaca file yang tidak tersedia.
- Bedakan fakta canon, usulan provisional, rumor, dan informasi yang belum diketahui.
- Tidak ada plot armor; kematian permanen kecuali mekanik resmi menyatakan sebaliknya.
- Modul lore tidak menggantikan modul mekanik. Aturan produksi Artificial Artifact tetap berada di `core/THINKER_AND_FORMULATION.md`.
- File karakter dan registry adalah snapshot awal, bukan sistem save berjalan.
