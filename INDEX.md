# Xuanling Realm — Official Index

Ini adalah pintu masuk resmi untuk memulai dan menjalankan roleplay Xuanling Realm. INDEX mengatur navigasi dan alur kerja; **aturan rinci harus dibaca dari modul sumbernya**, bukan disalin ulang ke banyak file.

Repository: https://github.com/Antarezka/xuanling-realm

## 1. Sumber Utama per Urusan

| Urusan | Sumber utama | Fungsi |
|---|---|---|
| Navigasi dan bootstrap | `INDEX.md` | Urutan pemeriksaan sumber dan pemilihan modul |
| Perilaku dan prosedur GM | `templates/GM_PROMPT.md` | Hierarki sumber, mode sesi, resolusi aksi, anti-cheat |
| **Format lengkap setiap respons gameplay** | **`templates/GAMEPLAY_RESPONSE_TEMPLATE.md`** | **Satu-satunya sumber format timestamp, narasi, profil, catatan pemain, sekat visual, dan Aksiku** |
| Definisi field dan state profil | `templates/CHARACTER_PROFILE_TEMPLATE.md` | Arti field, konsistensi state, Breakthrough dan Day left |
| Instruksi pemanggilan player | `templates/PLAYER_CONVERSATION_TEMPLATE.md` | Trigger CONVO/recall dan arahan ke sumber resmi; bukan sumber format atau mekanik |
| Snapshot awal karakter | `players.md` | Data awal karakter terdaftar, bukan save berjalan |
| Lore dan canon dunia | `world/WORLD.md` | Fakta dunia, wilayah, tokoh, dan lore utama |
| Kultivasi, Realm, Stage | `core/CULTIVATION_SYSTEM.md` | Progres, bottleneck, breakthrough |
| Martial Soul | `core/MARTIAL_SOUL.md` | Awakening dan aturan Martial Soul |
| Spirit Ring, Qi, PowerScale | `core/SPIRIT_RING_RULES.md` | Usia, kompatibilitas, penyerapan, Qi, PowerScale |
| HP | `core/HP_SYSTEM.md` | HP maksimum, format dan validasi HP saat ini |
| Injury / cedera | `core/INJURY_SYSTEM.md` | Kelas cedera, syarat pengobatan, progres dan pemulihan injury |
| Thinker dan formulasi | `core/THINKER_AND_FORMULATION.md` | Grade Thinker, formulasi, peluang produksi artefak |
| Spirit Beast | `bestiary/SPIRIT_BEAST_RULES.md` | Kategori Beast, syarat dan jeda penyerapan, deviasi |
| Combat | `gameplay/COMBAT_SYSTEM.md` | Inisiatif, kesiapan, hit, damage, pertahanan, serangan beruntun, combo, konsekuensi |
| Waktu dan durasi aksi | `gameplay/TIME_AND_ACTION_RULES.md` | Kalender, timestamp continuity, durasi, time skip; tidak memiliki format respons alternatif |
| Ekonomi | `core/10_ECONOMY_SYSTEM.md` | Kurs, harga, transaksi, kelangkaan dan kualitas |
| Peta, faksi, sejarah, artefak | `world/WORLD.md` | Gunakan hanya informasi yang benar-benar tercatat; modul khusus belum dibuat |

## 2. Alur Wajib Saat Recall, CONVO, dan Setiap Giliran Gameplay

1. Fetch dan baca ulang `INDEX.md` dari branch resmi.
2. Baca `templates/GM_PROMPT.md` dan `templates/PLAYER_CONVERSATION_TEMPLATE.md` bila sedang menjalankan trigger pemanggilan.
3. Baca `templates/GAMEPLAY_RESPONSE_TEMPLATE.md`. File ini adalah **satu-satunya sumber format output** untuk respons pertama maupun giliran lanjutan.
4. Tentukan mode sesi: karakter terdaftar baru, sesi berlanjut, atau karakter baru. Untuk karakter terdaftar yang memulai sesi baru, baca `players.md` sebagai snapshot awal saja.
5. Fetch modul yang relevan dengan aksi dan kondisi saat ini, mengikuti peta di bawah. Pastikan file tersedia dan terbaca.
6. Selesaikan aksi menggunakan modul mekanik yang berwenang; jangan membuat aturan pengganti untuk bagian yang belum ditetapkan.
7. Perbarui hanya state yang berubah karena kejadian sah. Periksa kesinambungan timestamp menurut `gameplay/TIME_AND_ACTION_RULES.md`.
8. Jawab menggunakan format persis dari `templates/GAMEPLAY_RESPONSE_TEMPLATE.md`; jangan mengganti format dengan laporan bootstrap atau format alternatif.

**Jika file wajib gagal diakses, sebutkan file yang gagal. Jangan mengaku sudah membacanya.** Lanjutkan hanya bagian yang tetap didukung sumber dan jangan menyelesaikan aksi yang bergantung pada aturan yang hilang.

## 3. Pilih Modul Berdasarkan Aksi

- Realm, Stage, Sync progress, bottleneck, breakthrough: `core/CULTIVATION_SYSTEM.md` dan `core/SPIRIT_RING_RULES.md`.
- Awakening atau Martial Soul: `core/MARTIAL_SOUL.md`.
- Spirit Beast, perburuan, syarat ring, jeda minimum, deviasi: `bestiary/SPIRIT_BEAST_RULES.md`; tambahkan `core/SPIRIT_RING_RULES.md` untuk formula deviasi lengkap.
- Combat, serangan beruntun, atau combo: `gameplay/COMBAT_SYSTEM.md`; satu aksi dapat berisi beberapa hit dan aturan combo default berlaku dari modul ini. Tambahkan `core/HP_SYSTEM.md` bila HP berubah/harus divalidasi dan `core/INJURY_SYSTEM.md` bila injury muncul/berubah.
- Waktu, perjalanan berdurasi, kultivasi panjang, atau time skip: `gameplay/TIME_AND_ACTION_RULES.md` serta modul mekanik terkait.
- HP atau pembuatan/pembaruan profil: `core/HP_SYSTEM.md`, `templates/CHARACTER_PROFILE_TEMPLATE.md`, dan `templates/GAMEPLAY_RESPONSE_TEMPLATE.md`.
- Makan, lapar, metabolisme: gunakan `core/HUNGER_AND_METABOLISM.md` **hanya jika file tersedia**; saat ini belum ada.
- Thinker atau pembuatan Artificial Artifact: `core/THINKER_AND_FORMULATION.md`; penggunaan artefak dalam pertarungan juga mengikuti Combat.
- Pembelian, penjualan, appraisal, tawar-menawar, pembayaran, atau perubahan saldo: `core/10_ECONOMY_SYSTEM.md`.
- Lokasi, perjalanan, faksi, sejarah, atau lore: `world/WORLD.md`.
- Karakter terdaftar yang memulai sesi baru: `players.md`. Jangan gunakan registry untuk menimpa state berjalan.
- Pemain meminta bantuan tentang proyek atau struktur repository: `README.md`.

## 4. Aturan State Profil yang Penting

- Format lengkap output hanya bersumber dari `templates/GAMEPLAY_RESPONSE_TEMPLATE.md`. Definisi field dan state hanya bersumber dari `templates/CHARACTER_PROFILE_TEMPLATE.md`. Jangan menyalin format lengkap ke INDEX, GM Prompt, atau prompt player.
- Jangan menambah field terpisah untuk Law atau Spirit Rings tanpa persetujuan pemilik. Realm menentukan jumlah slot; detail ring yang dimiliki masuk ke Teknik / Kemampuan atau deskripsi Martial Soul.
- HP saat ini berasal dari profil terakhir atau kejadian tercatat; jangan otomatis menganggap HP penuh. HP dan injury adalah state terpisah.
- Sync progress/cap kompatibilitas berbeda dari penguasaan kekuatan ring 100%; ikuti `core/SPIRIT_RING_RULES.md`.
- `Breakthrough` dan `Day left` mengikuti definisi `templates/CHARACTER_PROFILE_TEMPLATE.md` dan jeda minimum resmi. Day left dibulatkan ke atas dalam satuan 24 jam; nilai nol bukan jaminan breakthrough. Jika data waktu/nomor ring tidak tersedia, gunakan `???`.
- Perubahan Qi, ring, Realm, inventory, equipment, assets, Currency, luka, dan hubungan harus memiliki penyebab yang sah.
- `players.md` adalah snapshot awal. Profil terakhir dan kejadian setelahnya adalah state sesi berjalan.
- Informasi yang belum diketahui karakter ditulis `???` sesuai konteks. Jangan menciptakan rahasia, kemampuan, transaksi, atau kejadian masa lalu tanpa dasar.
- MODE: NO STEP berarti tidak ada menu pilihan atau daftar opsi bernomor; akhiri adegan pada situasi terbuka.

## 5. File Resmi yang Tersedia

- `README.md`
- `INDEX.md`
- `templates/GM_PROMPT.md`
- `templates/GAMEPLAY_RESPONSE_TEMPLATE.md`
- `templates/CHARACTER_PROFILE_TEMPLATE.md`
- `templates/PLAYER_CONVERSATION_TEMPLATE.md`
- `players.md`
- `core/CULTIVATION_SYSTEM.md`
- `core/MARTIAL_SOUL.md`
- `core/SPIRIT_RING_RULES.md`
- `core/HP_SYSTEM.md`
- `core/INJURY_SYSTEM.md`
- `core/THINKER_AND_FORMULATION.md`
- `core/10_ECONOMY_SYSTEM.md`
- `bestiary/SPIRIT_BEAST_RULES.md`
- `gameplay/COMBAT_SYSTEM.md`
- `gameplay/TIME_AND_ACTION_RULES.md`
- `world/WORLD.md`

## 6. Modul yang Belum Dibuat

Jalur berikut belum tersedia dan tidak boleh dianggap sudah dibaca atau menjadi sumber resmi:

- `core/HUNGER_AND_METABOLISM.md`
- `world/MAP_AND_REGIONS.md`
- `world/FACTIONS.md`
- `world/HISTORY.md`
- `world/ARTIFACTS_AND_RELICS.md`
- `world/CUSTOM_EVENTS.md`

Sampai modul khusus dibuat, gunakan hanya informasi yang benar-benar ada di `world/WORLD.md`. Jangan mengarang jalur, isi, atau status file.

## 7. Prinsip Integrasi

- INDEX adalah peta dan alur; bukan tempat menyimpan ulang semua mekanik.
- `GAMEPLAY_RESPONSE_TEMPLATE.md` adalah satu-satunya sumber format visual lengkap.
- GM Prompt adalah prosedur GM; bukan sumber angka combat, HP, ekonomi, atau waktu.
- Character Profile Template mendefinisikan arti field dan state, bukan format output penuh.
- Time Rules mengatur kalender, durasi, dan validasi waktu, bukan format timestamp alternatif.
- Player Conversation Template adalah trigger/instruksi pemanggilan, bukan sumber format atau mekanik.
- Registry adalah snapshot awal; bukan save otomatis.
- Setiap modul mekanik menjadi sumber utama untuk ruang lingkupnya.
- Jika aturan belum ditetapkan atau dua sumber bertentangan, tandai masalahnya. Jangan menyelesaikan konflik secara diam-diam.
