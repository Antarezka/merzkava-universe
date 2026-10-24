# Merzkava Universe — Hunger and Metabolism

**Status:** Modul mekanik resmi.  
**Cakupan:** Satiety, jadwal makan, pengurangan karena waktu aktif, tidur malam, Spirit Realm, kondisi tubuh, dan pengubah biologis/supranatural.

Modul ini adalah satu-satunya sumber angka untuk Hunger dan Metabolism. Jangan membuat rumus hunger tandingan di modul lain.

## 1. Stat Satiety

Format stat wajib:

`Satiety: nilai/100`

- Satiety adalah ukuran rasa kenyang dan cadangan makan jangka pendek untuk gameplay, bukan HP atau Qi.
- Nilainya berada pada rentang 0–100. Jangan melebihi 100 atau mengurangi di bawah 0.
- Makanan menambah Satiety; waktu aktif menguranginya menurut rumus modul ini.
- Satiety 0 berarti karakter kehabisan rasa kenyang dan perlu makan. Itu **tidak otomatis** berarti pingsan, kehilangan HP, atau mati. Konsekuensi tambahan harus memiliki aturan atau sebab yang sah.
- Jangan mengubah Satiety tanpa waktu aktif yang berlalu, konsumsi makanan/minuman yang memang memberi nutrisi, atau pengubah kondisi yang sah.

## 2. Jadwal Makan Normal

Tiga jendela makan harian:

| Waktu lokal dunia | Jendela makan |
|---|---|
| 06.00–11.00 | Pagi |
| 12.00–18.00 | Siang |
| 19.00–01.00 | Malam |

- Karakter normal umumnya makan tiga kali sehari.
- Satu **porsi makan standar** memulihkan **34 Satiety**. Cukup untuk membuat tiga porsi sehari secara teori memulihkan 102 poin sebelum batas maksimum 100 diterapkan.
- Porsi kecil/camilan memulihkan 10 poin; porsi besar memulihkan 50 poin. Gunakan nilai ini hanya bila jenis dan jumlah makanan mendukung kategori tersebut.
- Satiety dari makanan ditambahkan ke nilai sekarang dan dibatasi maksimum 100. Makan tidak otomatis mengisi ke 100 jika porsinya tidak cukup.
- Makan di luar jendela tetap memulihkan Satiety sesuai porsi. Setelah makanan yang layak benar-benar dikonsumsi, hitungan beruntun jam makan terlewat direset; riwayat jendela yang sebelumnya terlewat tidak dihapus dari catatan kejadian.
- Jam makan yang terlewat dihitung saat jendela berakhir tanpa karakter makan, **hanya jika karakter terjaga dan punya kesempatan wajar untuk makan**. Jendela yang berlalu saat tidur tidak dihitung sebagai jam makan terlewat.
- Jika karakter tidak punya akses makanan atau tidak bisa makan karena situasi, jangan menganggap ia sengaja melewatkan makan; catat keadaan itu dan terapkan pengali jam makan terlewat hanya sesuai ketentuan di §5.

## 3. Laju Dasar Menurut Tingkat

Laju dasar menunjukkan waktu aktif yang diperlukan untuk mengurangi 100 Satiety dari penuh ke 0, sebelum pengubah kondisi tubuh, jam makan terlewat, dan efek khusus yang sah diterapkan.

| Tingkat tubuh/kultivasi | Waktu aktif per 100 Satiety |
|---|---:|
| Mortal (belum memasuki sembilan Spirit Realm) | 24 jam |
| Spirit Initiate | 2 hari |
| Spirit Adept | 4 hari |
| Spirit Elder | 8 hari |
| Spirit Monarch | 16 hari |
| Spirit King | 32 hari |
| Spirit Ancestor | 64 hari |
| Spirit Emperor | 128 hari |
| Spirit Sovereign | 256 hari |
| Spirit Primordial | 365 hari |

Gunakan Spirit Realm yang benar-benar tercatat dan jangan menyingkat tingkat kultivasi menjadi `Realm`. Mortal adalah status dasar sebelum sembilan Spirit Realm. Jangan menaikkan tingkat metabolisme hanya karena karakter memiliki Martial Soul langka, ring berusia tinggi, kekayaan, status sosial, atau kekuatan yang belum ditetapkan. Pengaruh khusus harus memenuhi §7.

## 4. Rumus Pengurangan Satiety

Gunakan satu rumus:

`Pengurangan = (Jam aktif berlalu / Waktu dasar per 100 Satiety dalam jam) × 100 × M`

- `Jam aktif berlalu`: waktu dunia yang benar-benar berlalu saat karakter terjaga, bukan waktu nyata dan bukan durasi tidur malam yang dilindungi §6.
- `Waktu dasar`: nilai dari tabel §3 yang dikonversi ke jam.
- `M`: hasil perkalian pengubah kondisi tubuh yang tercantum di §7, pengali jam makan terlewat di §5, dan pengubah khusus yang sudah ditetapkan secara sah. Aktivitas tidak memiliki pengali terpisah; aktivitas hanya memengaruhi Satiety melalui kondisi tubuh yang benar-benar ditimbulkannya atau efek khusus resmi.
- Hitung pengurangan secara presisi dan bulatkan hasil akhir ke **0,1 Satiety**. Simpan nilai presisi tersebut untuk perhitungan berikutnya; jangan membulatkan berulang kali setiap menit.
- Pengurangan aktual dibatasi pada Satiety yang tersedia. Satiety tidak pernah kurang dari 0.
- Jika tidak ada waktu aktif yang berlalu, tidak ada pengurangan karena waktu.

**Contoh mortal:** 6 jam aktif pada kondisi normal tanpa jam makan terlewat mengurangi (6/24 × 100 = 25) Satiety.

**Contoh Spirit Primordial:** 24 jam aktif pada kondisi normal tanpa pengubah mengurangi (24/(365×24) × 100 ≈ 0,0114) Satiety.

## 5. Jam Makan Terlewat

Hitung jumlah jendela makan yang terlewat secara beruntun saat karakter terjaga dan berkesempatan makan. Terapkan satu pengali berikut, bukan menumpuk pengali setiap jendela:

| Jendela makan terlewat berturut-turut | Pengali hunger |
|---|---:|
| 0 | ×1,00 |
| 1 | ×1,25 |
| 2 | ×1,50 |
| 3 atau lebih | ×2,00 |

- Pengali ini berlaku selama karakter belum makan lagi. Setelah karakter mengonsumsi makanan yang layak, reset hitungan jendela makan terlewat menjadi 0 untuk perhitungan berikutnya.
- Jika karakter makan setelah satu atau lebih jendela terlewat, makanan tetap menambah Satiety sesuai porsi; pengali jam makan terlewat direset setelah makan.
- Jendela yang berlalu ketika karakter sedang tidur malam tidak menambah hitungan.
- Jika karakter tidak bisa makan karena dikurung, tidak sadar, terikat, atau situasi lain yang benar-benar menghalangi makan, jam makan yang lewat tetap tercatat sebagai kesempatan makan yang hilang hanya jika karakter terjaga. Jangan menggambarkan pilihan sengaja ketika tidak ada pilihan yang masuk akal.

## 6. Tidur Malam dan Penguncian Satiety

Tidur malam normal adalah kebutuhan biologis dan pengecualian resmi dari batas durasi aksi biasa.

- Ketika karakter mulai tidur malam, catat nilai Satiety terakhir sebagai nilai terkunci.
- Selama tidur malam normal, **Satiety tidak berkurang**. Jangan menerapkan pengurangan waktu aktif, pengali kondisi tubuh, atau jam makan terlewat selama periode tidur yang dilindungi.
- Ketika karakter bangun, lanjutkan perhitungan dari nilai Satiety yang terkunci dan mulai menghitung waktu aktif kembali dari waktu bangun.
- Tidur malam boleh melewati batas aksi biasa 3 jam dalam `gameplay/TIME_AND_ACTION_RULES.md`; jangan memaksa pemain membagi tidur normal menjadi aksi tiga jam.
- Tidur tidak otomatis memulihkan Satiety, HP, Qi, atau injury. Tidur hanya mengunci pengurangan Satiety selama periode tidur normal; pemulihan sistem lain mengikuti aturan masing-masing.
- Jika tidur terganggu dan karakter benar-benar terjaga untuk periode tertentu, hitung pengurangan hanya selama waktu terjaga tersebut. Jangan menghukum waktu tidur yang benar-benar terjadi.
- Tidur siang atau pingsan tidak otomatis dianggap tidur malam yang dilindungi. Perlakukan sesuai fakta kejadian; jangan gunakan tidur sebagai alasan untuk mengabaikan kebutuhan darurat atau konsekuensi yang telah ditetapkan.

## 7. Kondisi Tubuh dan Pengubah Khusus

Kondisi tubuh mengubah laju pengurangan Satiety dengan mengalikan nilai dasar. Gunakan pengali kondisi paling sesuai yang didukung kejadian; kategori yang saling tumpang tindih tidak boleh ditumpuk satu sama lain.

| Kondisi tubuh | Pengali |
|---|---:|
| Normal / lelah ringan | ×1,00 |
| Kelelahan nyata | ×1,10 |
| Kelelahan berat | ×1,25 |
| Kelelahan ekstrem | ×1,50 |

- Kelelahan harus memiliki dasar, misalnya aktivitas berkepanjangan, perjalanan berat, latihan, kurang istirahat, atau kejadian lain yang masuk akal. Jangan memberikan kelelahan otomatis hanya karena giliran berlalu.
- Kategori kelelahan di atas adalah pengali alternatif, bukan bonus yang ditumpuk. Jika karakter mengalami kelelahan ekstrem, gunakan ×1,50, bukan ×1,10 ×1,25 ×1,50.
- Cedera, penyakit, racun, demam, kehamilan, perubahan usia, cuaca, atau keadaan khusus tidak mendapat pengali default dari modul ini. Terapkan pengali hanya jika ada aturan resmi lain atau dampak spesifik yang sudah ditetapkan dalam riwayat.
- Aktivitas yang menguras tenaga boleh menggunakan kategori kelelahan yang sesuai bila kondisi itu benar-benar timbul. Jangan menambahkan pengali aktivitas terpisah jika dampaknya sudah terwakili oleh kondisi kelelahan yang sama.

### Keunggulan atau kelemahan biologis/supranatural

Genetik, garis keturunan, kutukan, berkah langit, konstitusi khusus, Martial Soul, obat, teknik, relik, atau efek supernatural **boleh** mengubah metabolisme, tetapi tidak otomatis melakukannya.

1. Pastikan sifat atau efek tersebut benar-benar tercatat atau diperoleh melalui kejadian yang sah.
2. Tentukan apakah efek memengaruhi kebutuhan makan/metabolisme secara eksplisit.
3. Jika efek menyatakan besaran numerik, gunakan nilai resmi tersebut sebagai pengali `M`.
4. Jika efek menyatakan dampak tetapi belum memberi angka, catat sebagai efek kualitatif dan jangan menciptakan persentase. Tandai nilai numeriknya sebagai belum ditentukan sampai aturan atau pemilik proyek menetapkannya. Sifat bawaan tubuh yang tercatat dapat mengubah cara lapar atau kelelahan terlihat dan ditoleransi dalam narasi, tetapi tidak otomatis mengurangi laju numerik Satiety. Jangan menghapus kebutuhan biologis atau memberi kekebalan penuh tanpa aturan resmi; jangan pula memaksakan gejala yang bertentangan dengan sifat yang sudah ditetapkan.
5. Jangan menyimpulkan bahwa keturunan kuat otomatis tidak lapar, kutukan otomatis meningkatkan hunger, atau berkah otomatis menurunkan hunger tanpa bukti.

Semua pengubah yang benar-benar independen dapat dikalikan, tetapi:
- Jangan menghitung efek yang sama dua kali.
- Jangan menumpuk kategori kelelahan.
- Jangan mengarang angka untuk pengubah yang belum ditetapkan.
- Catat sumber setiap pengubah yang aktif agar dapat diaudit.

## 8. Urutan Resolusi Wajib GM

Setiap kali waktu berlalu, makan terjadi, atau kondisi tubuh berubah:

1. Baca timestamp sebelumnya dan tentukan berapa lama karakter benar-benar terjaga.
2. Kecualikan periode tidur malam yang dilindungi §6; Satiety tetap terkunci selama periode itu.
3. Tentukan tingkat/Spirit Realm yang tercatat dan waktu dasar dari §3.
4. Tentukan kondisi tubuh saat periode aktif itu, termasuk kategori kelelahan yang didukung.
5. Perbarui jumlah jendela makan terlewat jika jendela berakhir saat karakter terjaga dan punya kesempatan makan.
6. Tentukan pengubah khusus hanya dari aturan resmi atau kejadian yang tercatat.
7. Hitung pengurangan menggunakan §4 dan semua pengali yang sah.
8. Terapkan perubahan Satiety dari makanan yang benar-benar dikonsumsi, sesuai porsi.
9. Batasi Satiety pada 0–100 dan catat hasil akhirnya di profil.
10. Jangan mengubah HP, Qi, injury, atau kondisi lain hanya karena Satiety berubah, kecuali sumber resmi lain atau kejadian yang sah menetapkan hubungan itu.

Jika timestamp, Spirit Realm, periode tidur, atau kondisi penting tidak diketahui, jangan menebak angka secara diam-diam. Gunakan informasi yang tersedia, tandai nilai yang belum dapat ditentukan, dan minta klarifikasi hanya bila diperlukan untuk menyelesaikan hasil.

## 9. Format Profil

Tambahkan field berikut ke profil gameplay:

`Satiety: nilai/100`

Nilai harus berasal dari profil terakhir dan perubahan yang benar-benar terjadi. Jika state awal Satiety belum pernah ditetapkan, GM dapat menetapkan nilai awal yang masuk akal untuk karakter baru dan menandainya sebagai estimasi awal; jangan menganggap semua karakter yang sudah berjalan otomatis berada di 100.
