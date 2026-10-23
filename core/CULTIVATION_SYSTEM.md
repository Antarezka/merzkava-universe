# Xuanling Realm — Cultivation System

Status: Modul mekanik resmi.
Cakupan: Realm, Stage, Sync progress, bottleneck, breakthrough, dan slot Spirit Ring.

Modul ini hanya menetapkan aturan yang telah disepakati. Angka pertumbuhan kekuatan, biaya Qi, durasi latihan, dan rumus kompatibilitas yang belum ditetapkan tidak boleh dibuat seolah-olah merupakan aturan resmi.

---

## 1. Sembilan Realm Kultivasi

Setiap Realm memiliki empat Stage: Early (Awal), Middle (Menengah), Late (Akhir), dan Peak (Puncak).

| Urutan | Realm | Jumlah slot Spirit Ring setelah slot Realm itu terbuka |
|---:|---|---:|
| 1 | Spirit Initiate | 1 |
| 2 | Spirit Adept | 2 |
| 3 | Spirit Elder | 3 |
| 4 | Spirit Monarch | 4 |
| 5 | Spirit King | 5 |
| 6 | Spirit Ancestor | 6 |
| 7 | Spirit Emperor | 7 |
| 8 | Spirit Sovereign | 8 |
| 9 | Spirit Primordial | 9 |

Satu Realm memberikan satu slot Spirit Ring, sehingga batas normal sistem ini adalah sembilan slot pada Realm kesembilan. Urutan Realm 1–9 yang kanonis adalah Spirit Initiate, Spirit Adept, Spirit Elder, Spirit Monarch, Spirit King, Spirit Ancestor, Spirit Emperor, Spirit Sovereign, dan Spirit Primordial. Nama ini harus dipertahankan secara konsisten di seluruh repository. Jangan menambahkan Realm kesepuluh atau slot tambahan tanpa revisi canon oleh pemilik.

Nama dan jumlah slot menunjukkan struktur kultivasi, bukan jaminan bahwa dua orang dalam Realm yang sama memiliki kekuatan tempur identik.

## 2. Martial Soul dan Awakening

Martial Soul adalah bentuk kekuatan utama seseorang. Bentuknya dapat berupa, misalnya, senjata, tumbuhan, atau hewan; kategori dan kemampuan spesifik harus mengikuti modul Martial Soul ketika tersedia.

Awakening Martial Soul berlangsung pada usia empat tahun atau lebih. Awakening mengungkap Martial Soul, tetapi tidak otomatis memberikan Spirit Ring pertama.

Spirit Ring pertama harus diperoleh melalui proses tersendiri yang sah. Jangan memberikan Spirit Ring, kemampuan ring, atau slot yang telah terisi hanya karena karakter sudah mengalami awakening.

## 3. Progres dan Empat Stage

Gunakan urutan Stage berikut di dalam setiap Realm:

1. Early (Awal)
2. Middle (Menengah)
3. Late (Akhir)
4. Peak (Puncak)

Istilah proses mekanik yang digunakan hanya:
- **Penyerapan Spirit Ring:** proses memperoleh dan menambahkan satu Spirit Ring ke jumlah ring yang dimiliki.
- **Kultivasi:** proses meningkatkan Sync progress menuju cap kompatibilitas maksimum ring yang sedang diproses.
- **Menerobos:** proses terpisah yang mensyaratkan seluruh ketentuan resmi.

Sync progress wajib ditulis sebagai `Sync progress: [progres saat ini]%/[cap kompatibilitas maksimum]%`. Cap berbeda menurut ring dan dihitung sesuai `core/SPIRIT_RING_RULES.md`; jangan menganggap cap selalu 100%.

Meditasi biasa tidak otomatis menjadi Kultivasi dan tidak mengubah Sync progress. Hanya aktivitas yang secara jelas dijalankan sebagai **Kultivasi** menurut aturan ini yang dapat meningkatkan Sync progress; Kultivasi tetap bukan Penyerapan Spirit Ring atau breakthrough.

Mencapai cap berarti mencapai bottleneck, bukan breakthrough otomatis. Untuk percobaan menerobos, jarak antara Sync progress dan cap harus **kurang dari 10 poin persentase**. Jika jaraknya 10 poin atau lebih, syarat bottleneck belum terpenuhi.

Makin besar jarak Sync progress dari cap dalam rentang yang diizinkan, makin tinggi deviasi yang harus dipertimbangkan. Persentase paparan deviasi mengikuti nomor ring: Ring 1 = 100%, lalu menurun untuk setiap nomor ring berikutnya; nilai persis Ring 2–9 belum ditetapkan. Tingkat risiko ditentukan berdasarkan jumlah poin status yang benar-benar hilang, bukan persentase paparan; kehilangan 15–19 poin termasuk Menengah Rendah. Rentang kategori risiko lainnya belum ditetapkan. Deviasi wajib dicatat sebagai pengurangan cap kompatibilitas maksimum ring berikutnya, damage HP, dan cedera/kondisi tubuh. Terapkan rincian di `core/SPIRIT_RING_RULES.md`; jangan mengarang angka numerik yang belum disahkan.
## 4. Bottleneck dan Breakthrough

Menerobos hanya dapat dilakukan jika semua syarat berikut terpenuhi:

1. **Bottleneck:** Sync progress berada kurang dari 10 poin persentase di bawah cap kompatibilitas ring aktif.
2. **Spirit Ring tersedia:** ring berikutnya benar-benar tersedia untuk diserap melalui proses yang sah.
3. **Item wajib tersedia:** karakter memenuhi persyaratan item yang berlaku untuk Spirit Beast target sesuai `bestiary/SPIRIT_BEAST_RULES.md`. Jika persyaratan item Beast belum ditetapkan, jangan mengarangnya atau menganggapnya tidak ada.
4. **Jeda minimum terpenuhi:** waktu sejak Penyerapan Spirit Ring sebelumnya yang berhasil telah mencapai jeda minimum sesuai `bestiary/SPIRIT_BEAST_RULES.md`.

Jeda minimum antar-ring: Ring 1→2 = 2 minggu; Ring 2→3 = 1 bulan; Ring 3→4 = 3 bulan; Ring 4→5 = 6 bulan; Ring 5→6 = 1 tahun; Ring 6→7 = 2 tahun; Ring 7→8 = 3 tahun; Ring 8→9 = 4 tahun.

Jika percobaan dilakukan terlalu jauh dari cap atau sebelum jeda minimum, terapkan deviasi sesuai modul resmi: cap kompatibilitas ring berikutnya berkurang, HP menerima damage, dan kondisi tubuh mengalami cedera. Tingkat deviasi meningkat seiring jarak dari cap atau besarnya pelanggaran jeda. Jika rumus numerik belum tersedia, nyatakan dampak dan tingkat deviasi tanpa mengarang angka damage atau persentase pengurangan cap.

Penyerapan Spirit Ring, Kultivasi, dan menerobos adalah proses berbeda. Realm dan slot baru hanya diperbarui setelah seluruh syarat dan proses resmi benar-benar berhasil. Jika aturan tambahan seperti durasi, biaya, atau hasil parsial belum ditetapkan, jangan mengarangnya.
## 5. Spirit Ring dan Slot

- Jumlah slot mengikuti Realm: Realm 1 menyediakan satu slot, Realm 2 dua slot, dan seterusnya hingga sembilan slot pada Realm 9.
- Slot yang tersedia tidak berarti slot tersebut sudah terisi.
- Setiap Spirit Ring harus memiliki asal-usul dan proses perolehan yang sah.
- Kemampuan yang diberikan oleh sebuah Spirit Ring harus memiliki dasar dari Beast yang bersangkutan dan aturan resmi yang tersedia.
- Jangan membuat kemampuan, evolusi, mutasi, atau efek ring tanpa dasar yang sah.

Rentang warna Spirit Ring yang telah ditetapkan:

| Warna | Usia Spirit Ring |
|---|---:|
| Putih | 10–99 tahun |
| Kuning | 100–999 tahun |
| Ungu | 1.000–9.999 tahun |
| Hitam | 10.000–49.999 tahun |
| Merah | 50.000–99.999 tahun |
| Emas | 100.000–499.999 tahun |

Warna untuk Spirit Ring berusia 500.000 tahun atau lebih belum ditetapkan. Jangan menciptakan warna atau kategori baru.

Tidak ada batas usia Spirit Ring yang mutlak hanya berdasarkan angka usia. Kesesuaian tetap mempertimbangkan toleransi tubuh, kompatibilitas, dan aturan penyerapan yang berlaku. Usia tinggi bukan jaminan bahwa karakter mampu menyerap ring tersebut dengan aman atau berhasil.

## 6. Penaklukan Beast, Penyerapan, dan Sinkronisasi

Penaklukan Spirit Beast dan proses penyerapan Spirit Ring adalah bagian yang berbeda:

- Perburuan Spirit Beast dapat berlangsung di hutan atau lokasi berbahaya. Jangan mewajibkan karakter membawa Beast ke lokasi meditasi aman sebelum menyelesaikan perburuan.
- Setelah Spirit Beast dikalahkan, Spirit Ring muncul mengambang di atas tubuh Beast.
- Aktivitas Kultivasi untuk meningkatkan Sync progress dilakukan di tempat aman dan stasioner. Meditasi biasa tanpa tujuan/proses Kultivasi yang jelas tidak mengubah Sync progress.
- Saat progres mencapai 100% dan karakter berada di bottleneck, Spirit Ring berikutnya menjadi bagian dari proses penyerapan dan breakthrough.
- Sinkronisasi 100% nyaris mustahil melalui penyerapan paksa. Jika Spirit Beast secara sukarela menyerahkan ringnya, sinkronisasi 100% lebih mungkin dicapai, tetapi tidak dijamin.
- Usia Spirit Ring tidak memiliki batas mutlak hanya berdasarkan angka; toleransi tubuh dan kompatibilitas tetap menentukan. Rentang warna ring tetap mengikuti tabel di atas, sementara warna untuk usia 500.000 tahun ke atas belum ditetapkan.
- Gunakan formula kompatibilitas, PowerScale, dan Qi yang tercantum di `core/SPIRIT_RING_RULES.md`. Jangan mengganti rumus atau mengarang nilai input yang belum diketahui.

## 7. Konsistensi dengan WORLD.md

- WORLD.md adalah acuan utama untuk lore dan fakta dunia yang sudah ditetapkan.
- Tiga penguasa utama yang tercatat di WORLD.md berada di Realm 9 — Spirit Primordial; Stage masing-masing harus mengikuti WORLD.md: Emperor berada di Middle, sedangkan Maharaja dan Leluhur Utara berada di Early.
- Konfigurasi Spirit Ring para penguasa di WORLD.md berstatus rancangan kanon awal. Pertahankan usia ring dan status warna yang tertulis; jangan mengubah `Undefined` menjadi warna baru.
- Warna Spirit Ring untuk usia 500.000 tahun ke atas belum ditetapkan, walaupun WORLD.md mencantumkan ring dengan usia tersebut.
- Jika tabel umum sistem dan konfigurasi karakter spesifik tampak berbeda, pertahankan fakta spesifik yang tercatat di WORLD.md dan tandai konflik untuk ditinjau; jangan diam-diam mengubah lore.

## 8. Batas Informasi dan Konsistensi

1. Gunakan `world/WORLD.md` sebagai acuan lore dan modul ini untuk mekanik kultivasi yang sudah disepakati.
2. Gunakan modul ini bersama `core/MARTIAL_SOUL.md` dan `core/SPIRIT_RING_RULES.md`; gunakan `bestiary/SPIRIT_BEAST_RULES.md` ketika file tersebut tersedia.
3. Gunakan `gameplay/TIME_AND_ACTION_RULES.md` untuk durasi aksi dan Kultivasi; modul tersebut sudah tersedia.
4. Jangan mengklaim membaca modul yang belum tersedia.
5. Jangan menciptakan rumus, statistik, peluang, bonus, atau pengecualian baru sebagai canon.
6. Jika suatu aksi memerlukan aturan rinci yang belum ditetapkan, jelaskan keterbatasannya dan selesaikan hanya bagian yang didukung sumber.
7. Profil karakter harus mencerminkan Realm, Stage, dan progres. Jangan menambahkan field terpisah untuk Spirit Ring; jumlah slot mengikuti Realm, sementara informasi ring yang telah diperoleh—sumber, usia, warna, kemampuan, dan hasil proses yang diketahui—dicatat dalam bagian Teknik / Kemampuan atau deskripsi Martial Soul yang sudah ada. Jangan mengisi slot atau menaikkan Realm tanpa proses yang sah.
