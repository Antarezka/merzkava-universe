🧭 Xuanling Realm — OFFICIAL INDEX

«Ini adalah SATU-SATUNYA link yang perlu ditempel pemain untuk memulai sesi roleplay Xuanling Realm.

Semua modul aturan, sistem kekuatan, wilayah, faksi, bestiary, dan data karakter diakses AI GM dari repository ini sesuai kondisi gameplay.

Untuk AI GM: pada SETIAP giliran gameplay, fetch dan baca ulang INDEX ini terlebih dahulu, lalu periksa templates/GM_PROMPT.md dan fetch modul relevan sesuai kondisi serta aksi sebelum menulis respons gameplay. Jangan menganggap ingatan atau cache percakapan menggantikan pemeriksaan INDEX terbaru. Gunakan modul resmi dan riwayat percakapan sebagai sumber kebenaran. Jangan mengarang isi file yang belum tersedia, dan jangan mengaku telah membaca file yang gagal diakses.»

Repository: https://github.com/Antarezka/xuanling-realm

---

0. Prosedur Bootstrap (WAJIB, SETIAP GILIRAN GAMEPLAY)

1. Pada setiap giliran gameplay, fetch dan baca versi terbaru "INDEX.md" dari branch resmi repository. Jangan hanya mengandalkan salinan yang dibaca pada giliran sebelumnya.
2. Fetch "templates/GM_PROMPT.md" melalui tautan di §1. File ini sudah ada di repository dan berisi prosedur GM, anti-cheat, serta format respons. Jika fetch gagal, jangan berpura-pura telah membacanya.

3. Inisialisasi format gameplay:
   
   - Ikuti format waktu, narasi, profil karakter, dan deklarasi aksi yang ditentukan dalam "templates/GM_PROMPT.md".
   - Terapkan batas waktu aksi dan aturan gameplay resmi.
   - Jangan menciptakan indikator, sistem step, atau format profil baru tanpa dasar resmi.

4. Periksa pesan pemain untuk menentukan kondisi karakter:
   
   - (a) Karakter terdaftar, memulai sesi baru: jika "players.md" dan data karakter terkait tersedia, fetch data tersebut dan gunakan sebagai titik awal.
   - (b) Melanjutkan karakter dalam chat yang sama: gunakan profil karakter terakhir dan riwayat kejadian yang tersedia sebagai kondisi terkini. Jangan mengganti status dengan data awal lama.
   - (c) Karakter baru: jika tidak ditemukan data karakter atau riwayat sebelumnya, minta nama karakter dan lokasi awal jika belum diberikan.

5. Tentukan lokasi karakter berdasarkan data karakter atau input pemain. Fetch "world/WORLD.md" dan "world/MAP_AND_REGIONS.md" jika tersedia dan relevan. Jangan mengarang lokasi, jarak, atau fasilitas yang belum ditetapkan.

6. Periksa "world/CUSTOM_EVENTS.md" jika file tersebut telah dibuat dan dapat diakses. Gunakan event yang benar-benar tercatat; jangan mengarang event resmi.

7. Fetch modul mekanik yang dibutuhkan berdasarkan kondisi karakter dan aksi yang hendak dilakukan. Jangan memulai penyelesaian aksi yang bergantung pada aturan penting sebelum aturan tersebut diperiksa jika sumbernya tersedia.

8. Mulai gameplay dengan mengikuti format wajib AI GM dan kondisi karakter yang sah.

9. Selama sesi berlangsung, fetch modul tambahan secara dinamis berdasarkan tabel pemicu di §2. Jangan mengambil semua modul sekaligus tanpa kebutuhan.

10. Jika sebuah tautan gagal diakses atau file belum tersedia, beri tahu pemain. Jangan mengarang isinya atau mengklaim sudah membacanya.

---

1. Direktori Lengkap Seluruh Modul

Status repository harus diverifikasi dari branch yang sedang digunakan. Pada saat dokumen ini diperiksa, "INDEX.md", "README.md", "templates/GM_PROMPT.md", "templates/CHARACTER_PROFILE_TEMPLATE.md", "core/HP_SYSTEM.md", "core/CULTIVATION_SYSTEM.md", "core/MARTIAL_SOUL.md", "core/SPIRIT_RING_RULES.md", "core/THINKER_AND_FORMULATION.md", "bestiary/SPIRIT_BEAST_RULES.md", dan "world/WORLD.md" tersedia. Jalur modul lain di bawah adalah rencana hingga file benar-benar dibuat dan dapat dibaca.

A. Aturan Inti dan Sistem Kekuatan

Kode| File| Link Raw| Isi
CORE| "templates/GM_PROMPT.md"| "GM Prompt" (https://raw.githubusercontent.com/Antarezka/xuanling-realm/refs/heads/main/templates/GM_PROMPT.md)| Instruksi operasional AI GM, anti-cheat, format respons, batas waktu, konsistensi profil
C01| "core/CULTIVATION_SYSTEM.md"| "Cultivation System" (https://raw.githubusercontent.com/Antarezka/xuanling-realm/refs/heads/main/core/CULTIVATION_SYSTEM.md)| Sembilan Realm, empat Stage, progres, bottleneck, breakthrough
C02| "core/MARTIAL_SOUL.md"| "Martial Soul" (https://raw.githubusercontent.com/Antarezka/xuanling-realm/refs/heads/main/core/MARTIAL_SOUL.md)| Sistem kekuatan Martial Soul dan karakteristiknya
C03| "core/SPIRIT_RING_RULES.md"| "Spirit Ring Rules" (https://raw.githubusercontent.com/Antarezka/xuanling-realm/refs/heads/main/core/SPIRIT_RING_RULES.md)| Perolehan Spirit Ring, usia, penyerapan, sinkronisasi, hubungan dengan breakthrough
C04| "core/HUNGER_AND_METABOLISM.md"| "Hunger and Metabolism" (https://raw.githubusercontent.com/Antarezka/xuanling-realm/refs/heads/main/core/HUNGER_AND_METABOLISM.md)| Nutrisi, kelaparan, kebutuhan energi, dan pemulihan
C05| "core/HP_SYSTEM.md"| "HP System" (https://raw.githubusercontent.com/Antarezka/xuanling-realm/refs/heads/main/core/HP_SYSTEM.md)| HP maksimum berdasarkan Realm/Stage, formula interpolasi, dan format pencatatan HP
C06| "core/10_ECONOMY_SYSTEM.md"| "Economy System" (https://raw.githubusercontent.com/Antarezka/xuanling-realm/refs/heads/main/core/10_ECONOMY_SYSTEM.md)| Mata uang resmi, kurs, sembilan tier kualitas item, harga regional, distribusi, kelangkaan musiman, dan penyesuaian pasar

B. Gameplay

Kode| File| Link Raw| Isi
G01| "gameplay/COMBAT_SYSTEM.md"| "Combat System" (https://raw.githubusercontent.com/Antarezka/xuanling-realm/refs/heads/main/gameplay/COMBAT_SYSTEM.md)| Giliran, aksi, posisi, damage, pertahanan, konsekuensi
G02| "gameplay/TIME_AND_ACTION_RULES.md"| "Time and Action Rules" (https://raw.githubusercontent.com/Antarezka/xuanling-realm/refs/heads/main/gameplay/TIME_AND_ACTION_RULES.md)| Durasi aksi, meditasi, time skip, checkpoint

C. Bestiary

Kode| File| Link Raw| Isi
B01| "bestiary/SPIRIT_BEAST_RULES.md"| "Spirit Beast Rules" (https://raw.githubusercontent.com/Antarezka/xuanling-realm/refs/heads/main/bestiary/SPIRIT_BEAST_RULES.md)| Kategori Beast, persyaratan item penyerapan per Beast, jeda minimum antar-ring, dan deviasi

D. Dunia dan Lore

Kode| File| Link Raw| Isi
W01| "world/WORLD.md"| "World" (https://raw.githubusercontent.com/Antarezka/xuanling-realm/refs/heads/main/world/WORLD.md)| Gambaran umum dunia dan geografi
W02| "world/MAP_AND_REGIONS.md"| "Map and Regions" (https://raw.githubusercontent.com/Antarezka/xuanling-realm/refs/heads/main/world/MAP_AND_REGIONS.md)| Peta, wilayah, lokasi, dan hubungan geografis
W03| "world/FACTIONS.md"| "Factions" (https://raw.githubusercontent.com/Antarezka/xuanling-realm/refs/heads/main/world/FACTIONS.md)| Kekaisaran, organisasi, kekuatan politik, dan hubungan antarfaksi
W04| "world/HISTORY.md"| "History" (https://raw.githubusercontent.com/Antarezka/xuanling-realm/refs/heads/main/world/HISTORY.md)| Sejarah dan peristiwa yang sudah ditetapkan
W05| "world/ARTIFACTS_AND_RELICS.md"| "Artifacts and Relics" (https://raw.githubusercontent.com/Antarezka/xuanling-realm/refs/heads/main/world/ARTIFACTS_AND_RELICS.md)| Artefak buatan, relik kuno, dan sifat yang sudah ditetapkan
W06| "world/CUSTOM_EVENTS.md"| "Custom Events" (https://raw.githubusercontent.com/Antarezka/xuanling-realm/refs/heads/main/world/CUSTOM_EVENTS.md)| Event dunia yang dicatat dan dikelola pemilik repository

E. Karakter dan Template

Kode| File| Link Raw| Isi
P01| "players.md"| "Players" (https://raw.githubusercontent.com/Antarezka/xuanling-realm/refs/heads/main/players.md)| Katalog karakter awal yang wajib dibaca saat sesi baru untuk karakter terdaftar; bukan save otomatis
T01| "templates/CHARACTER_PROFILE_TEMPLATE.md"| "Character Profile Template" (https://raw.githubusercontent.com/Antarezka/xuanling-realm/refs/heads/main/templates/CHARACTER_PROFILE_TEMPLATE.md)| Format wajib profil karakter
T02| "templates/GM_PROMPT.md"| "GM Prompt" (https://raw.githubusercontent.com/Antarezka/xuanling-realm/refs/heads/main/templates/GM_PROMPT.md)| Template instruksi AI GM untuk gameplay

F. Dokumentasi Proyek

File| Link| Isi
"README.md"| "README" (https://github.com/Antarezka/xuanling-realm/blob/main/README.md)| Dokumentasi proyek dan petunjuk penggunaan repository

---

1a. Direktori Faksi dan Organisasi

«Faksi utama sudah ditetapkan dalam canon Xuanling Realm. File individual per faksi belum ditetapkan sebagai struktur wajib. Untuk saat ini, gunakan "world/FACTIONS.md" sebagai sumber utama.

Jika sebuah faksi kelak membutuhkan detail internal yang besar, pemilik repository dapat membuat file tersendiri dan menambahkan tautannya ke INDEX ini. Jangan membuat nama file atau menganggap detail faksi sudah resmi sebelum ditetapkan.»

Faksi| Identitas yang sudah ditetapkan
Golden Dragon Empire (Kekaisaran Naga Emas)| Kekuatan besar di timur, dipimpin Emperor
Tianhai Yunzhou (天海云洲)| Kekuatan maritim dan kepulauan, dipimpin Maharaja
Beiming Gu (北冥谷)| Lembah utara yang terisolasi, dipimpin Leluhur Utara

Tujuh wilayah Kekaisaran Naga Emas yang sudah ditetapkan:

- Longyuan: pusat kekaisaran dan pemerintahan.
- Canglan: sungai, pertanian, dan perdagangan darat.
- Jinyue: mineral, logam spiritual, artefak, dan kerajinan.
- Tianfeng: akademi, sekte, dan pendidikan kultivasi.
- Yanling: pegunungan vulkanik dan pandai besi.
- Baiyue: pertahanan perbatasan dan jalur pegunungan.
- Xingluo: pelabuhan timur, perdagangan laut, dan diplomasi.

Detail yang belum ditetapkan harus tetap dianggap belum diketahui.

---

2. Alur Navigasi Otomatis (Trigger → Modul yang Difetch)

Trigger dalam Roleplay| Modul yang Difetch| Catatan
Awal sesi baru| "templates/GM_PROMPT.md"| Instruksi operasional AI GM; wajib diperiksa terlebih dahulu
Karakter terdaftar dan memulai sesi baru| "players.md"| Hanya jika katalog telah tersedia
Membuka file karakter tertentu| Data karakter yang relevan| Jangan mengarang file karakter yang belum dibuat
Melanjutkan karakter di chat yang sama| Profil terakhir dan riwayat percakapan| Pertahankan status terkini
Karakter baru| "templates/CHARACTER_PROFILE_TEMPLATE.md"| Gunakan template wajib; minta nama dan lokasi awal jika belum diberikan
Realm, Stage, Sync progress, bottleneck, atau breakthrough| "core/CULTIVATION_SYSTEM.md" dan "core/SPIRIT_RING_RULES.md"| Sync progress dibanding cap ring; cek semua syarat menerobos dan countdown jeda
Pembuatan atau pembaruan profil HP| "core/HP_SYSTEM.md" dan "core/CULTIVATION_SYSTEM.md"| Cocokkan HP maksimum dengan Realm/Stage; gunakan format HP saat ini/maksimum
Martial Soul atau karakteristik kekuatan| "core/MARTIAL_SOUL.md"| Jangan menyimpulkan kemampuan tanpa dasar
Memburu atau menghadapi Spirit Beast| "bestiary/SPIRIT_BEAST_RULES.md"| Gunakan bersama aturan pertarungan jika diperlukan
Mengalahkan Spirit Beast dan memperoleh Spirit Ring| "bestiary/SPIRIT_BEAST_RULES.md" dan "core/SPIRIT_RING_RULES.md"| Terapkan aturan perolehan yang resmi
Penyerapan Spirit Ring atau menerobos| "core/SPIRIT_RING_RULES.md", "core/CULTIVATION_SYSTEM.md", dan "bestiary/SPIRIT_BEAST_RULES.md"| Periksa cap sinkronisasi, ring tersedia, item wajib Beast, jeda minimum, dan deviasi
Pertarungan resmi dimulai| "gameplay/COMBAT_SYSTEM.md"| Periksa aksi, posisi, damage, dan konsekuensi
Kultivasi, time skip, atau durasi aksi| "gameplay/TIME_AND_ACTION_RULES.md" jika tersedia dan modul mekanik terkait| Meditasi bukan sinonim Kultivasi atau Penyerapan Spirit Ring
Kelaparan, kebutuhan makan, atau pemulihan| "core/HUNGER_AND_METABOLISM.md"| Perhitungkan kondisi dan aktivitas
Perjalanan atau penentuan lokasi| "world/WORLD.md" dan "world/MAP_AND_REGIONS.md"| Jangan mengarang jarak atau rute
Bertemu kekaisaran, sekte, atau organisasi| "world/FACTIONS.md"| Gunakan detail yang benar-benar tersedia
Memeriksa sejarah dunia| "world/HISTORY.md"| Jangan mengubah sejarah yang sudah ditetapkan
Membuat Artificial Artifact, menyusun formulasi, atau memakai kemampuan Thinker| "core/THINKER_AND_FORMULATION.md"| Periksa tier Thinker, matriks peluang, material, fokus, bakat, dan batas resolusi
Menggunakan artefak atau relik| "world/ARTIFACTS_AND_RELICS.md"| Periksa asal-usul dan fungsi yang tercatat
Memeriksa event dunia| "world/CUSTOM_EVENTS.md"| Hanya jika file tersedia
Membutuhkan format profil| "templates/CHARACTER_PROFILE_TEMPLATE.md"| Pertahankan field yang telah disepakati
Membeli, menjual, menilai harga, menawar, atau mengubah saldo uang| "core/10_ECONOMY_SYSTEM.md" dan "templates/CHARACTER_PROFILE_TEMPLATE.md"| Terapkan tier kualitas, harga regional, distribusi, kelangkaan, dan catat saldo mata uang
Pemain meminta bantuan menggunakan repository| "README.md"| Jelaskan penggunaan GitHub, bukan narasi gameplay

Efisiensi konteks: jika modul sudah dibaca dalam percakapan yang sama dan informasi relevannya masih tersedia, tidak perlu fetch ulang tanpa alasan. Fetch ulang jika informasi terbaru dari repository dibutuhkan dan akses memungkinkan.

---

3. Cara Kerja Data Karakter dan Profil Gameplay

File "players.md" adalah katalog data awal karakter, bukan save file yang otomatis diperbarui.

1. Pemain menyebut nama karakter ketika memulai sesi baru.
2. AI GM memeriksa apakah karakter terdaftar dan apakah data awalnya tersedia.
3. Jika karakter ditemukan di "players.md", data awal digunakan sebagai titik mulai sesi.
4. Jika tidak tersedia, AI GM meminta informasi yang diperlukan untuk karakter baru.
5. Selama gameplay, perkembangan dicatat melalui blok Profil Karakter dalam percakapan.
6. AI GM tidak boleh mengedit "players.md" atau file data awal karakter selama gameplay.

Profil karakter

Format profil wajib mengikuti "templates/CHARACTER_PROFILE_TEMPLATE.md". File template profil resmi tersedia dan harus digunakan.

Field yang sudah disepakati mencakup:

- Nama
- Usia
- Spirit Realm (format Nama Realm/angka Stage; Mortal/0)
- Martial Soul
- HP (format saat ini/maksimum; maksimum mengikuti core/HP_SYSTEM.md)
- Qi (format saat ini/maksimum setelah ring pertama; sebelum ring pertama tulis "...")
- Kondisi Tubuh
- Equipment
- Inventory
- Assets
- Currency (xuan/zun)
- Teknik / Kemampuan
- Tujuan Saat Ini

Jangan menambahkan field terpisah untuk Law atau Spirit Ring. Informasi ring yang telah diperoleh—sumber, usia, warna, kemampuan, dan hasil proses yang diketahui—dicatat dalam Teknik / Kemampuan atau deskripsi Martial Soul yang sudah ada. Jangan menghilangkan kemampuan yang telah diperoleh, tetapi jangan membuat field profil baru tanpa persetujuan pemilik.


---

4. Batasan Penting dan Anti-Cheat

- Tidak ada plot armor. Kematian bersifat permanen kecuali terdapat pengecualian resmi.
- NPC memiliki agenda sendiri dan tidak selalu kooperatif.
- Informasi yang belum diketahui karakter ditulis "???".
- Teknik, kemampuan, dan item tidak boleh muncul tanpa dasar perolehan atau mekanik yang sah.
- Luka, efek, kerusakan equipment, dan penggunaan sumber daya tidak boleh dihapus begitu saja.
- Meta-gaming harus ditangani sesuai aturan resmi.
- Dalam situasi kritis, pemain memilih satu aksi utama ketika beberapa aksi independen tidak dapat dilakukan sekaligus.
- Sync progress harus ditulis sebagai progres saat ini/cap kompatibilitas maksimum; cap berbeda pada tiap ring dan bukan otomatis 100%.
- Menerobos memerlukan Sync progress kurang dari 10 poin persentase di bawah cap, ring berikutnya tersedia, item wajib Beast target tersedia, dan jeda minimum antar-ring terpenuhi.
- Jeda minimum: ring 1→2 = 2 minggu; 2→3 = 1 bulan; 3→4 = 3 bulan; 4→5 = 6 bulan; 5→6 = 1 tahun; 6→7 = 2 tahun; 7→8 = 3 tahun; 8→9 = 4 tahun.
- Deviasi wajib mencatat pengurangan cap ring berikutnya, damage HP, dan cedera/kondisi tubuh. Jangan mengarang angka numerik tanpa formula resmi.
- Aksi biasa maksimal 3 jam per giliran.
- Kultivasi murni dapat berlangsung maksimal 1 bulan hanya jika seluruh syarat waktu resmi terpenuhi. Meditasi bukan Kultivasi dan tidak otomatis mengubah Sync progress.
- Jika syarat meditasi panjang tidak terpenuhi, gunakan batas aksi biasa.
- Perburuan Spirit Beast boleh terjadi di lokasi berbahaya. Setelah Beast dikalahkan, ring muncul mengambang di atas tubuhnya, tetapi tidak otomatis terserap. Penyerapan Spirit Ring, Kultivasi, dan menerobos adalah proses berbeda.
- WORLD.md adalah acuan utama untuk lore dunia. Modul mekanik mengatur mekanik yang secara eksplisit ditetapkan. INDEX adalah navigasi, bukan pengganti dokumen sumber.
- Semua kemampuan dan mekanik harus mengikuti sumber resmi yang tersedia.
- Jika aturan belum ditetapkan atau sumber bertentangan, nyatakan masalah dan minta klarifikasi jika diperlukan.

Konsistensi Spirit Ring

Rentang warna Spirit Ring yang sudah ditetapkan:

Warna| Rentang Usia
Putih| 10–99 tahun
Kuning| 100–999 tahun
Ungu| 1.000–9.999 tahun
Hitam| 10.000–49.999 tahun
Merah| 50.000–99.999 tahun
Emas| 100.000–499.999 tahun

Warna untuk usia 500.000 tahun ke atas belum diputuskan. Jangan mengarang kategori baru. Usia Spirit Ring tidak memiliki batas mutlak hanya berdasarkan angka atau Realm; rekomendasi usia harus mempertimbangkan toleransi tubuh dan kompatibilitas. Jangan membuat batas maksimum universal.

---

5. Ringkasan Dunia

Xuanling Realm — Eastern Fantasy · Martial Soul · Spirit Beast · Spirit Ring · Cultivation.

Dunia ini memiliki tiga kekuatan utama yang sudah ditetapkan: Golden Dragon Empire di timur, Tianhai Yunzhou di wilayah maritim, dan Beiming Gu di utara. Kekaisaran Naga Emas memiliki tujuh wilayah utama. Dunia juga mencakup hutan, reruntuhan kuno, sekte, akademi, jalur perdagangan, dan kawasan Spirit Beast.

Sistem kultivasi terdiri dari 9 Realm, masing-masing dengan tahap Early, Middle, Late, dan Peak. Satu Realm membuka satu slot Spirit Ring tambahan. Urutan Realm: Spirit Initiate, Spirit Adept, Spirit Elder, Spirit Monarch, Spirit King, Spirit Ancestor, Spirit Emperor, Spirit Sovereign, dan Spirit Primordial. Martial Soul mengalami awakening pada usia empat tahun atau lebih, tetapi awakening tidak otomatis memberikan ring pertama. Setelah Spirit Beast dikalahkan, ring muncul mengambang di atas tubuhnya. Sync progress dicatat sebagai progres saat ini/cap kompatibilitas maksimum ring aktif. Mencapai bottleneck bukan breakthrough otomatis; Kultivasi, Penyerapan Spirit Ring, dan menerobos adalah proses berbeda. Setelah setiap penyerapan berhasil, sebutkan nomor ring dan jumlah total ring yang dimiliki, usia, warna, tier/sumber Beast, kemampuan, kompatibilitas ring terbaru, kompatibilitas keseluruhan, AgeTotal, PowerScale, dan Qi. Terapkan formula dan tabel Qi dalam `core/SPIRIT_RING_RULES.md`: usia total ring menjadi faktor dominan PowerScale, tier Beast terutama memengaruhi kompatibilitas, dan Qi dasar sembilan ring adalah 45.234.100. Mortal sebelum awakening memiliki Qi 0; setelah awakening tetapi sebelum ring pertama, Qi belum terbentuk.

Prinsip utama: tidak ada plot armor, profil harus konsisten, aturan bersumber dari modul resmi, dan informasi yang belum ditetapkan tidak boleh dikarang.

---

6. Status Repository

Struktur di INDEX ini adalah peta pengembangan proyek, bukan bukti bahwa semua modul telah dibuat.

Sebelum AI GM menggunakan suatu modul sebagai sumber resmi, modul tersebut harus:

1. Sudah dibuat pada jalur yang benar.
2. Sudah tersedia pada branch repository yang digunakan.
3. Dapat diakses dan dibaca.
4. Memuat aturan yang benar-benar telah ditetapkan.

Jika file belum tersedia, AI GM harus menyatakan keterbatasannya dan tidak boleh berpura-pura telah memuat isinya.
