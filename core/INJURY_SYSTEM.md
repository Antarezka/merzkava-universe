# Merzkava Universe — Injury System

**Status:** Mekanik resmi injury v1.  
**Cakupan:** klasifikasi cedera, syarat pemulihan, progres pemulihan, dan hubungan injury dengan HP.

## 1. Prinsip Dasar

- **HP dan injury adalah dua hal berbeda.** HP mengukur kondisi keseluruhan; injury mencatat kerusakan tertentu pada tubuh.
- HP yang pulih tidak otomatis menyembuhkan injury. Injury yang sembuh juga tidak otomatis mengisi HP sampai penuh.
- Setiap injury yang berdampak pada gameplay harus dicatat dengan: nama/jenis, bagian tubuh jika diketahui, kelas injury, kondisi pemicu, metode pemulihan yang dibutuhkan, progres pemulihan, serta efek atau komplikasi yang benar-benar terjadi.
- Gunakan hanya cedera yang didukung kejadian. Jangan memberi cedera baru hanya untuk menghukum karakter, dan jangan menghapus cedera tanpa alasan pemulihan yang sah.
- Tingkat keparahan tidak ditentukan dari nama luka saja. Pertimbangkan mekanisme cedera, lokasi, damage yang diterima, kondisi karakter, dan hasil pemeriksaan atau penanganan yang tercatat. **Jumlah HP yang hilang saja tidak cukup untuk menentukan kelas injury**: HP adalah dampak umum, sedangkan injury adalah kerusakan tubuh tertentu.
- Satu kejadian dapat menimbulkan beberapa injury berbeda. Jangan menggabungkan, menggandakan, atau menganggap satu cedera sebagai cedera lain tanpa dasar.
- Persentase progres adalah **kemajuan pemulihan injury**, bukan HP. Progres 100% berarti injury itu pulih; efek sisa hanya boleh dipertahankan bila sudah tercatat dan memiliki dasar.

## 2. Empat Kelas Injury

| Kelas | Nama | Contoh umum | Pemulihan alami | Pengobatan |
|---|---|---|---|---|
| I | Ringan | Memar ringan, lecet, luka dangkal, ketegangan otot ringan | Bisa pulih dengan istirahat dan perawatan dasar | Membantu mempercepat pemulihan |
| II | Membutuhkan Perawatan | Luka dalam yang belum kritis, keseleo sedang, luka bakar sedang, robekan jaringan ringan | Bisa pulih lambat jika kondisi memungkinkan; risiko komplikasi tetap ada | Perawatan yang tepat mempercepat pemulihan secara signifikan |
| III | Struktural | Patah tulang, dislokasi, robekan tendon/ligamen berat, kerusakan struktur tubuh | Istirahat saja tidak cukup untuk pemulihan yang benar; fungsi dapat tetap terganggu atau cedera memburuk | Wajib ada penanganan yang sesuai, misalnya reposisi, bidai, imobilisasi, atau teknik penyembuhan yang terbukti |
| IV | Kritis | Pendarahan internal berat, kerusakan organ, luka yang mengancam nyawa, keracunan berat | Tidak dianggap pulih secara alami; dapat memburuk atau menyebabkan kematian | Perlu penanganan mendesak yang sesuai. Pemulihan baru berjalan setelah kondisi cukup stabil |

Contoh di atas adalah panduan klasifikasi, bukan diagnosis otomatis. Jika tingkat keparahan belum dapat diketahui, catat sebagai **injury belum terklasifikasi** sampai ada bukti yang cukup.

## 3. Progres Pemulihan

Setiap injury memiliki progres tersendiri dari **0% sampai 100%**. Gunakan tabel berikut sebagai laju dasar per 24 jam waktu dalam dunia game, bukan waktu nyata.

| Kelas injury | Pemulihan alami saat istirahat penuh | Dengan perawatan tepat |
|---|---:|---:|
| I — Ringan | +10 poin progres | +20 poin progres |
| II — Membutuhkan Perawatan | +2 poin progres | +10 poin progres |
| III — Struktural | Tidak ada progres pemulihan fungsional | +5 poin progres setelah penanganan yang diperlukan selesai |
| IV — Kritis | Tidak ada progres sebelum kondisi distabilkan | +2 poin progres setelah stabil dan selama penanganan berkelanjutan |

- Maksimum progres adalah 100%; jangan melampauinya.
- Terapkan laju berdasarkan waktu pemulihan yang benar-benar berlalu. Jika waktu berlalu kurang dari 24 jam, hitung secara proporsional.
- Angka pada tabel adalah laju dasar saat istirahat penuh dan tanpa komplikasi. Jika karakter beraktivitas, kembali bertarung, atau menggunakan bagian tubuh yang cedera, GM dapat mengurangi progres atau memperburuk injury **hanya jika aktivitas tersebut secara masuk akal mengganggu penyembuhan**. Jangan memberi penalti otomatis tanpa kaitan dengan cedera.
- Perawatan harus sesuai dengan jenis injury dan benar-benar tersedia serta digunakan. Salep tidak otomatis menyembuhkan patah tulang; tabib tidak otomatis berhasil; pil, teknik, artefak, dan kemampuan penyembuhan hanya berpengaruh sesuai fungsi yang telah ditetapkan.
- Untuk injury kelas III, progres dihitung setelah penanganan struktural yang diperlukan—misalnya tulang diposisikan dan diimobilisasi—benar-benar dilakukan. Tanpa penanganan itu, istirahat saja tidak menambah progres pemulihan fungsional.
- Untuk injury kelas IV, penanganan awal harus menstabilkan kondisi terlebih dahulu. Jika belum stabil, jangan menambahkan progres pemulihan dan selesaikan konsekuensi sesuai kondisi yang tercatat.
- Jika metode pengobatan, kualitas obat, kemampuan tabib, atau efektivitas teknik belum memiliki aturan khusus, gunakan laju dasar di atas dan jelaskan keterbatasannya; jangan mengarang bonus angka.

## 4. Syarat dan Efek Pengobatan

Pengobatan hanya dihitung bila semua syarat yang relevan terpenuhi:

1. **Kecocokan:** metode atau obat memang dapat menangani jenis injury tersebut.
2. **Akses:** karakter benar-benar memiliki, memperoleh, atau sedang ditangani dengan metode itu.
3. **Penerapan:** obat digunakan dengan benar, atau tabib/teknik melakukan penanganan yang diperlukan.
4. **Kebutuhan khusus:** cedera struktural sudah ditangani secara struktural; cedera kritis sudah distabilkan sebelum pemulihan rutin dimulai.

Jika seluruh syarat terpenuhi, gunakan laju kolom **Dengan perawatan tepat**. Jika hanya sebagian terpenuhi, jangan otomatis memberikan bonus penuh. Jika pengobatan salah atau berbahaya, efeknya ditentukan oleh fakta dan konsekuensi yang didukung situasi; jangan mengarang efek pasti.

## 5. Istirahat, Aktivitas, dan Komplikasi

- Istirahat penuh berarti karakter tidak melakukan aktivitas yang mengganggu pemulihan dan mendapat kesempatan memulihkan diri.
- Aktivitas ringan, perjalanan, latihan, pertarungan, atau penggunaan bagian tubuh yang cedera harus dinilai berdasarkan injury yang tercatat. Aktivitas tidak selalu memperburuk semua cedera.
- Komplikasi seperti infeksi, pendarahan berulang, tulang bergeser, atau cedera memburuk hanya boleh terjadi jika didukung oleh jenis injury, penanganan, kondisi, atau kejadian yang tercatat.
- Jika komplikasi terjadi, catat sebagai perubahan kondisi yang jelas. Jangan diam-diam mengatur ulang progres tanpa menjelaskan penyebabnya.
- Untuk injury yang mengancam nyawa, jangan memperlakukan tidur atau time skip sebagai pengganti penanganan darurat.

## 6. Hubungan dengan HP dan Sistem Lain

### Panduan konsekuensi injury dari Combat

Combat menentukan apakah kejadian benar-benar menimbulkan cedera; bagian ini membantu memilih konsekuensi tanpa membuat ambang damage kaku:

- **Benturan atau serangan ringan yang tertahan/teralihkan:** tidak wajib menghasilkan injury. Jika ada cedera yang tampak, gunakan Kelas I bila bukti mendukung.
- **Serangan bersih yang menembus pertahanan, luka sayat/tusuk yang jelas, atau benturan kuat:** pertimbangkan Kelas I atau II berdasarkan kedalaman, lokasi, dan mekanisme. Jangan otomatis memilih Kelas II hanya karena serangan mengenai target.
- **Patah tulang, dislokasi, tendon/ligamen rusak, atau kerusakan struktur yang jelas:** Kelas III. Jangan menyimpulkan cedera struktural dari angka damage saja.
- **Pendarahan internal berat, kerusakan organ, keracunan berat, atau kondisi yang mengancam nyawa:** Kelas IV hanya jika kejadian dan bukti mendukungnya; jangan membuat diagnosis internal hanya karena HP rendah.
- **Serangan beruntun/combo:** evaluasi tiap hit dan dampak gabungannya. Hit berikutnya dapat memperparah injury yang sudah ada atau menimbulkan injury berbeda jika mekanismenya mendukung; jangan menggandakan injury identik tanpa alasan.
- **Beda satu Spirit Realm:** terapkan aturan khusus di `gameplay/COMBAT_SYSTEM.md`. Itu menetapkan ekspektasi adanya injury setelah hit yang merusak, bukan izin untuk mengarang jenis cedera berat. Jika bukti hanya mendukung cedera ringan, catat Kelas I.
- **Deviasi penyerapan Spirit Ring:** catat cedera yang ditetapkan dari peristiwa deviasi. Jangan mengubah kategori risiko HP langsung menjadi diagnosis injury tertentu.

Jika bukti belum cukup untuk memilih kelas, catat `injury belum terklasifikasi` dan efek fungsional yang benar-benar terlihat. Klasifikasi dapat diperbarui ketika ada pemeriksaan atau bukti baru.

- Gunakan `core/HP_SYSTEM.md` untuk HP maksimum dan validasi HP.
- Gunakan `gameplay/COMBAT_SYSTEM.md` untuk damage dan penentuan konsekuensi serangan yang didukung situasi. Combat menentukan kejadian cedera; modul ini menentukan klasifikasi dan pemulihannya.
- Gunakan `core/SPIRIT_RING_RULES.md` untuk damage HP dan konsekuensi deviasi saat penyerapan Spirit Ring. Jika proses itu menghasilkan cedera, catat jenis cedera hanya berdasarkan hasil yang benar-benar ditetapkan; jangan mengarang diagnosis dari angka HP saja.
- Gunakan `gameplay/TIME_AND_ACTION_RULES.md` untuk waktu yang berlalu. Progres injury hanya bertambah selama waktu pemulihan yang benar-benar berlalu.
- Pemulihan HP dari modul lain tidak mengubah progres injury kecuali aturan khusus menyatakan demikian.
- Kemampuan penyembuhan, obat khusus, salep, tabib, atau artefak dapat mengganti atau meningkatkan laju dasar hanya jika efeknya terdokumentasi dan syaratnya terpenuhi.

## 7. Pencatatan dan Alur GM

Saat injury muncul atau berubah:

1. Catat cedera yang didukung oleh kejadian dan bagian tubuh jika diketahui.
2. Tentukan kelas injury berdasarkan bukti. Jika tidak cukup, tandai belum terklasifikasi.
3. Catat progres awal, biasanya 0% ketika injury baru terjadi.
4. Nyatakan apakah pemulihan alami memungkinkan atau pengobatan wajib.
5. Saat waktu berlalu, pilih laju yang sesuai dengan kondisi istirahat dan perawatan aktual.
6. Perbarui progres, kondisi, dan efek fungsional yang benar-benar berubah.
7. Pada 100%, tandai injury pulih dan hapus pembatasan yang berasal dari injury tersebut, kecuali efek sisa yang telah ditetapkan masih berlaku.

**Format pencatatan ringkas:**

`Injury: [jenis/lokasi] | Kelas: [I–IV/belum terklasifikasi] | Progres: [0–100]% | Syarat: [istirahat/perawatan khusus/stabilisasi] | Penanganan: [yang benar-benar dilakukan] | Efek: [yang masih berlaku]`

## 8. Batas Aturan

Kelas dan laju dalam modul ini adalah baseline umum. Modul ini belum menetapkan diagnosis medis terperinci, daftar obat khusus, tingkat kemampuan setiap tabib, atau efek numerik setiap teknik penyembuhan. Jangan mengarang angka atau menjadikan contoh umum sebagai kepastian. Aturan khusus yang kelak dibuat harus merujuk ke modul ini, bukan menduplikasi sistem progres injury di tempat lain.
