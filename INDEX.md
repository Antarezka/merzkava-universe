# Xuanling Realm — Official Index

INDEX ini adalah **pintu masuk tunggal** untuk memulai, melanjutkan, dan menjalankan roleplay Xuanling Realm. Ikuti prosedur bootstrap dan navigasi modul di bawah. Jangan menggandakan aturan mekanik atau format respons lengkap ke file lain.

Repository resmi: https://github.com/Antarezka/xuanling-realm

## 0. Prosedur Bootstrap (WAJIB)

Saat pemain memakai trigger awal yang merujuk INDEX.md dan players.md, perlakukan pesan itu sebagai perintah untuk menginisialisasi gameplay — bukan permintaan untuk sekadar menganalisis atau merangkum tautan.

1. **Baca seluruh INDEX.md ini terlebih dahulu.** Gunakan direktori dan aturan navigasi di bawah untuk menemukan sumber resmi; jangan mengandalkan ingatan bebas jika sumber repository dapat diakses.
2. **Fetch dan baca `templates/AUTHORITY_ORDER.md` sebelum memutuskan atau menarasikan hasil gameplay.** File ini menetapkan perilaku GM, anti-cheat, mode sesi, dan resolusi aksi.
3. **Kenali apakah sesi baru atau berlanjut dari pesan pemain dan riwayat chat yang tersedia.** Jangan menganggap semua penyebutan nama karakter sebagai jenis sesi yang sama:
   - **A. Sesi berlanjut / recall:** profil gameplay terakhir atau riwayat karakter masih tersedia di percakapan saat ini. Gunakan state terbaru itu; jangan fetch snapshot awal untuk menimpanya. Jika state terakhir tidak tersedia, minta pemain memberikan profil terakhir yang diperlukan.
   - **B. Calon sesi baru:** tidak ada profil gameplay berjalan untuk karakter itu di percakapan saat ini. Tunda pengecekan registry dan pemilihan snapshot sampai template canonical selesai dimuat pada langkah 4; setelah itu, cocokkan nama karakter dengan `players.md`.
4. **Muat template sebelum memuat snapshot karakter atau menulis respons gameplay.** Fetch dan baca seluruh `templates/GAMEPLAY_RESPONSE_TEMPLATE.md` terlebih dahulu, lalu seluruh `templates/CHARACTER_PROFILE_TEMPLATE.md`. Keduanya wajib; jangan mengganti format canonical dengan daftar bullet atau format buatan sendiri.
5. **Pilih dan inisialisasi state karakter dari sumber yang tepat.** Setelah langkah 4, baca `players.md` untuk memeriksa registry. Jika karakter terdaftar dan sesi baru, fetch tautan RAW file individualnya dan baca seluruh isi sebagai snapshot awal. Jika nama tidak terdaftar dan tidak ada state di riwayat, perlakukan sebagai karakter baru dengan mengikuti template profil dan Authority Order; jangan mengarang rahasia inti atau kemampuan formal. Pertahankan identitas, latar belakang, lokasi awal, hubungan, equipment, inventory, assets, Currency, kemampuan, catatan canon, estimasi awal, batas penafsiran, informasi khusus GM, serta Session Continuity. Bedakan fakta canon, estimasi GM, informasi khusus GM, dan pengetahuan karakter.
6. **Baca modul berdasarkan lokasi, state, dan kebutuhan gameplay.** Tentukan lokasi awal dari snapshot karakter atau input pemain, lalu baca modul world/lokasi yang relevan serta modul mekanik yang dibutuhkan untuk menghitung state awal dan aksi pertama. Jangan fetch seluruh repository sekaligus.
7. **Periksa `world/DYNAMIC_EVENTS.md` sebelum gameplay pertama dan setiap giliran gameplay.** Terapkan hanya event yang benar-benar terdaftar dan relevan. Jika file gagal diakses, ungkapkan kegagalan itu; jangan mengarang event.
8. **Validasi sebelum menjawab.** Cocokkan seluruh data karakter dengan template profil, pastikan field wajib tidak hilang, dan pastikan nilai tercatat tidak diganti dengan placeholder. `???` hanya boleh dipakai untuk identitas karakter yang benar-benar tidak dikenal atau nama Martial Soul yang belum diketahui. Field numerik yang belum memiliki nilai memakai `0`, kecuali HP awal yang diinisialisasi menurut aturan HP dan field hitung-mundur yang memiliki arti mekanik khusus. Gunakan timestamp yang konsisten sesuai modul waktu.
9. **Mulai gameplay langsung** menggunakan `templates/GAMEPLAY_RESPONSE_TEMPLATE.md`. Jangan membalas trigger dengan laporan bootstrap, daftar file yang dibaca, atau ringkasan analisis sebagai pengganti adegan.
10. **Selama permainan, navigasikan modul secara dinamis** memakai tabel pemicu di bawah. Jika modul sudah dibaca di percakapan yang sama dan belum berubah atau tidak ada alasan untuk mengambil ulang, gunakan konteks tersebut secara konsisten.

### Gerbang format → profil player → ekonomi (URUTAN MUTLAK)

Jangan mulai menulis narasi atau profil gameplay sampai tiga sumber ini selesai dimuat, dalam urutan berikut:

1. **Format visual percakapan:** baca seluruh `templates/GAMEPLAY_RESPONSE_TEMPLATE.md`. Format ini mengunci bentuk visual, garis/kotak, urutan field, nama field, catatan, dan penutup. Jangan membuat format sendiri.
2. **Definisi field profil:** baca seluruh `templates/CHARACTER_PROFILE_TEMPLATE.md` agar setiap nilai ditempatkan pada field yang benar.
3. **Profil player:** untuk sesi baru karakter terdaftar, baca `players.md`, lalu baca seluruh `players/<Nama>.md`. Untuk sesi berjalan, gunakan profil gameplay terakhir dan kejadian setelahnya sebagai state aktif; snapshot awal hanya referensi latar yang belum berubah.
4. **Sumber saldo Currency:** untuk sesi baru, gunakan saldo eksplisit di snapshot `players/<Nama>.md`. Untuk sesi berjalan/recall, gunakan saldo pada profil gameplay terakhir lalu terapkan hanya transaksi yang benar-benar terjadi setelahnya. `core/10_ECONOMY_SYSTEM.md` adalah sumber aturan kurs, harga, dan transaksi—bukan sumber saldo individual.
   - Jika saldo awal belum tercatat, isi semua denominasi Currency dengan `0` sampai saldo sah ditetapkan. Jangan menebak saldo dari latar, pekerjaan, aset, atau penghasilan; jangan mengarang transaksi masa lalu.
   - Setelah saldo awal ditetapkan, pertahankan di profil sesi dan jangan mengundi ulang atau mengubahnya hanya karena giliran baru. Setiap transaksi harus memiliki sebab, waktu, nilai masuk/keluar, dan saldo sesudah transaksi yang dapat diverifikasi dari kejadian/riwayat sesi.
5. **Pemetaan ke bagan:** baru setelah langkah 1–4, tempatkan setiap data pada field template visual. Currency harus disalin persis dari snapshot atau profil sesi aktif setelah menerapkan transaksi sah; aset non-uang tetap di Assets. Jangan mengubah nilai tercatat menjadi `???`, membulatkan saldo, atau mengganti format mata uang.
6. **Modul mekanik dan dunia:** setelah sumber state dimuat, baca modul yang diperlukan untuk timestamp, Satiety, HP, lokasi, event, dan aksi pertama. Jika sumber wajib gagal dibaca, jangan berpura-pura selesai.

**Gate sebelum respons:** pastikan format visual canonical sudah dimuat; profil/snapshot yang benar sudah dipilih; saldo Currency memiliki sumber yang jelas; Currency cocok dengan semua transaksi sah sejak saldo tersebut; seluruh field wajib dan ornamen visual dipertahankan. Jika satu gate belum terpenuhi, jangan kirim gameplay seolah-olah bootstrap lengkap.

### Protokol pemuatan karakter terdaftar

- `players.md` adalah **indeks karakter**, bukan file yang memuat seluruh ingatan karakter.
- File `players/<Nama>.md` adalah snapshot awal yang wajib dibaca penuh pada sesi baru untuk karakter terdaftar.
- Jangan menghilangkan data yang berada di bagian latar belakang, catatan khusus GM, aset, inventaris, relasi, atau batas penafsiran hanya karena field tersebut tidak tampil sebagai field terpisah di profil gameplay.
- Baca `core/10_ECONOMY_SYSTEM.md` saat menetapkan atau mengubah saldo, aset, transaksi, maupun harga. Pertahankan saldo yang tercatat di snapshot/profil sesi; jangan mengubah estimasi awal menjadi klaim bahwa transaksi masa lalu tertentu benar-benar terjadi.
- Baca `core/HUNGER_AND_METABOLISM.md` saat menetapkan Satiety atau menghitung perubahan karena waktu/makanan. Jangan otomatis menetapkan Satiety ke 100 jika sumber dan prosedur resmi tidak mendukungnya.
- Informasi khusus GM digunakan untuk konsistensi dunia, tetapi tidak otomatis diketahui karakter.
- Jika sumber wajib gagal diakses, sebutkan file yang gagal. Jangan mengklaim sudah membaca sumber yang tidak berhasil diambil.

### 1. Baca modul sesuai kebutuhan
Pilih modul berdasarkan aksi, kondisi, dan lokasi saat ini. Jangan membaca atau mengarang modul yang tidak tersedia hanya karena jalurnya tercantum di peta.

| Kebutuhan | Sumber resmi |
|---|---|
| Definisi field profil dan konsistensi state | `templates/CHARACTER_PROFILE_TEMPLATE.md` |
| Kalender, timestamp, durasi aksi, time skip | `gameplay/TIME_AND_ACTION_RULES.md` |
| Realm, Stage, Sync, bottleneck, breakthrough | `core/CULTIVATION_SYSTEM.md` |
| Akademi kultivator dan pendidikan dasar | `core/CULTIVATOR_ACADEMIES.md` |
| Prosedur awakening, tabel rarity, undian dan keputusan mutasi Martial Soul | `core/MARTIAL_SOUL_AWAKENING.md` |
| Lore, bentuk, karakteristik, dan interpretasi Martial Soul | `core/MARTIAL_SOUL.md` |
| Spirit Ring, kompatibilitas, penyerapan, kombinasi kemampuan, Qi, PowerScale | `core/SPIRIT_RING_RULES.md` |
| Spirit Beast, syarat ring, jeda minimum, deviasi | `bestiary/SPIRIT_BEAST_RULES.md` |
| Combat, serangan beruntun, multi-hit, combo, damage, pertahanan | `gameplay/COMBAT_SYSTEM.md` |
| HP | `core/HP_SYSTEM.md` |
| Cedera dan pemulihan injury | `core/INJURY_SYSTEM.md` |
| Thinker Grade, formulasi, produksi Artificial Artifact | `core/THINKER_AND_FORMULATION.md` |
| Harga, transaksi, kurs, aset, Currency | `core/10_ECONOMY_SYSTEM.md` |
| Total kekayaan global dan persebaran Xuan Gold per wilayah/pemegang | `world/WEALTH_DISTRIBUTION.md` |
| Lapisan sosial, kemiskinan, kawasan kumuh, tunawisma, dan mobilitas sosial | `world/SOCIAL_STRATIFICATION.md` |
| Dunia, tokoh, tiga kekuasaan utama, fondasi lore | `world/WORLD.md` |
| Peta, wilayah, permukiman, rute yang diketahui | `world/MAP_AND_REGIONS.md` |
| Geografi fisik, perjalanan, moda transportasi, dan batas pengetahuan rute | `world/GEOGRAPHY_AND_TRAVEL.md` |
| Bangsa berakal, ciri kelompok, dan konteks perlakuan sosial | `world/INTELLIGENT_PEOPLES.md` |
| Klan, dojo, sekte, organisasi, Medicine Hall Society | `world/FACTIONS.md` |
| Kronologi, bukti sejarah, peristiwa historis yang sudah mapan | `world/HISTORY.md` |
| Event dunia dinamis yang aktif/berakhir, status event, dampak lintas sesi, dan sumber konfirmasi | `world/DYNAMIC_EVENTS.md` |
| Form proposal untuk menambah/memperbarui event dunia; bukan canon sampai disetujui admin | `templates/WORLD_EVENT_UPDATE_TEMPLATE.md` |
| Kategori Relic/Ancient Artifact dan katalog | `world/ARTIFACTS_AND_RELICS.md` |
| Katalog dan lore Artificial Artifact | `world/ARTIFICIAL_ARTIFACTS.md` |
| Satiety, jadwal makan, metabolisme Realm, tidur malam, dan pengubah kondisi tubuh | `core/HUNGER_AND_METABOLISM.md` |

Untuk aksi yang menyentuh beberapa sistem, baca semua modul yang relevan. Contoh: combat yang mengubah HP dan menimbulkan luka memerlukan Combat, HP, Injury, Time, dan Hunger/Metabolism bila waktu aktif berlalu. Produksi Artificial Artifact menggunakan mekanik di `core/THINKER_AND_FORMULATION.md`; file lore artefak tidak menggantikan aturan produksi.

### 2. Jalankan giliran
1. Pahami niat player dan periksa lokasi, waktu, kemampuan, kondisi, sumber daya, serta pengetahuan karakter.
2. Resolusi aksi menggunakan modul resmi yang relevan. Satu aksi tidak otomatis berarti satu hit; ikuti Combat System untuk multi-hit dan combo.
3. Terapkan hanya konsekuensi yang didukung mekanik dan kejadian.
4. Perbarui state yang benar-benar berubah dan validasi kesinambungan waktu.
5. Kirim respons gameplay langsung dengan format canonical. Jangan tampilkan laporan bootstrap atau daftar file yang dibaca sebagai pengganti gameplay.

Jika sumber wajib gagal diakses, sebutkan file yang gagal dan jangan mengaku telah membacanya. Jangan menyelesaikan bagian aksi yang bergantung pada aturan yang tidak tersedia.

## Sumber Utama dan Batas Tanggung Jawab

- `INDEX.md`: alur dan navigasi.
- `templates/AUTHORITY_ORDER.md`: Authority Order: perilaku GM, prosedur, anti-cheat, dan resolusi aksi tingkat umum.
- `templates/GAMEPLAY_RESPONSE_TEMPLATE.md`: **satu-satunya sumber format visual lengkap setiap respons gameplay**.
- `templates/CHARACTER_PROFILE_TEMPLATE.md`: arti field dan aturan konsistensi state; bukan format output kedua.
- `templates/PLAYER_CONVERSATION_TEMPLATE.md`: prompt pemanggilan singkat; bukan sumber mekanik.
- `world/DYNAMIC_EVENTS.md`: registry canon event dunia persisten; wajib diperiksa setiap giliran gameplay.
- `templates/WORLD_EVENT_UPDATE_TEMPLATE.md`: format usulan perubahan event untuk ditinjau admin; bukan registry dan bukan bukti bahwa perubahan telah disimpan.
- `players.md`: indeks karakter terdaftar.
- `players/<Nama>.md`: snapshot awal karakter individual, bukan save berjalan.
- Modul mekanik: sumber resmi untuk aturan di ruang lingkupnya.
- Modul world: sumber resmi untuk lore, geografi/perjalanan, bangsa berakal, faksi, sejarah, katalog artefak, distribusi kekayaan, stratifikasi sosial, serta event dinamis sesuai cakupannya. Untuk perjalanan atau interaksi dengan kelompok masyarakat, baca modul world yang relevan; jangan menganggap `MAP_AND_REGIONS.md` menggantikan aturan transportasi atau lore bangsa berakal.
- Event dinamis: setelah hasil aksi ditetapkan, cek apakah konsekuensinya persisten dan berdampak pada dunia bersama. Jika ya, siapkan proposal melalui `templates/WORLD_EVENT_UPDATE_TEMPLATE.md`. Proposal pemain/GM bukan canon dan tidak boleh dianggap tersimpan sebelum ditinjau, disetujui, dan di-commit oleh owner/admin. Perubahan karakter pribadi tidak dimasukkan ke registry event dunia.
- Profil gameplay terakhir dan kejadian setelahnya: sumber state sesi berjalan.

## Konsistensi yang Wajib Dipertahankan

- Jangan menambah field terpisah untuk Law atau Spirit Rings tanpa persetujuan pemilik. Rincian ring masuk ke Teknik / Kemampuan atau deskripsi Martial Soul.
- HP dan injury adalah dua state berbeda; gunakan modul masing-masing.
- `Satiety: nilai/100` adalah field profil resmi dan hanya dihitung menurut `core/HUNGER_AND_METABOLISM.md`. Waktu tidur malam yang dilindungi mengunci Satiety; pengecualian tidur malam terhadap batas aksi ditetapkan di `gameplay/TIME_AND_ACTION_RULES.md`.
- Sync progress/cap kompatibilitas berbeda dari penguasaan kekuatan ring 100%; ikuti Spirit Ring Rules.
- Breakthrough dan Day left mengikuti definisi di Character Profile Template serta interval resmi Spirit Beast Rules. 0 Day left bukan jaminan breakthrough. Jika data waktu atau riwayat tidak tersedia, tulis `Belum ditetapkan Day left`; jangan gunakan `???` atau `0 Day left`.
- Jangan mengubah HP, Qi, Realm, ring, inventory, equipment, assets, Currency, luka, atau relasi tanpa penyebab yang sah.
- Penggunaan `???` sangat terbatas: hanya untuk karakter yang identitasnya benar-benar tidak dikenal dan nama Martial Soul yang belum diketahui. Jangan gunakan `???` untuk saldo, HP, Qi, Satiety, angka, atau field lain. Field numerik yang belum tercatat diisi `0`; field nonnumerik lain yang belum ditetapkan ditulis `Belum ditetapkan` atau `Tidak ada` sesuai makna. Jangan menciptakan rahasia, kemampuan, transaksi, atau kejadian masa lalu.
- Registry dan file karakter individual tidak boleh diubah selama gameplay tanpa permintaan eksplisit pemilik repository.
- **MODE: NO STEP** berarti tidak ada menu pilihan atau daftar opsi bernomor. Akhiri adegan pada situasi terbuka agar player menentukan tindakan sendiri.

## Daftar File Resmi

- `README.md`
- `INDEX.md`
- `players.md`
- `players/Yuha.md`
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
- `world/WORLD.md`
- `world/MAP_AND_REGIONS.md`
- `world/GEOGRAPHY_AND_TRAVEL.md`
- `world/INTELLIGENT_PEOPLES.md`
- `world/FACTIONS.md`
- `world/HISTORY.md`
- `world/DYNAMIC_EVENTS.md`
- `templates/WORLD_EVENT_UPDATE_TEMPLATE.md`
- `world/ARTIFACTS_AND_RELICS.md`
- `world/ARTIFICIAL_ARTIFACTS.md`
- `world/WEALTH_DISTRIBUTION.md`
- `world/SOCIAL_STRATIFICATION.md`

Modul yang disebut tetapi belum tersedia tidak otomatis menjadi sumber resmi. Jangan mengklaim membacanya atau menganggap isinya sudah ditetapkan.
