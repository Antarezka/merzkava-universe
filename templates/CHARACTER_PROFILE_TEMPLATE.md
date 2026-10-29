# Merzkava Universe — Character Profile Field Definitions

**File ini mendefinisikan arti field dan konsistensi state. Bentuk visual lengkap, urutan field, ornamen, dan penutup setiap balasan gameplay hanya ditentukan oleh `templates/GAMEPLAY_RESPONSE_TEMPLATE.md`.**

## Field Profil Resmi

Pertahankan nama dan urutan field sesuai `templates/GAMEPLAY_RESPONSE_TEMPLATE.md`:

1. `Nama`: nama karakter yang tercatat.
2. `Usia`: usia karakter yang tercatat. Saat membuat karakter baru, jika usia tidak disebutkan atau ambigu, tetapkan estimasi GM terbaik berdasarkan latar, peran, pengalaman, tanggung jawab, dan kronologi karakter. Rentang 8–19 tahun adalah acuan umum untuk karakter muda, bukan batas minimum/maksimum dan bukan kewajiban; usia di luar rentang tetap sah bila latar mendukungnya. Tandai estimasi sebagai estimasi, jangan mengubahnya menjadi fakta biografis pasti tanpa dasar, dan jangan membiarkannya kosong hanya karena pemain tidak menyebut angka.
3. `Spirit Realm`: selalu tulis nama field dan tingkat kultivasi sebagai `Spirit Realm` (bukan `Realm` atau `Cultivation Realm`), beserta Stage dan progres sesuai sistem resmi. Mortal ditulis `Mortal` sebagai status dasar sebelum Spirit Realm 1; jangan menuliskannya sebagai `Mortal/0` atau `Spirit Realm 0`.
4. `Sync progress`: progres saat ini dibandingkan dengan cap kompatibilitas ring saat ini. Cap tidak selalu 100%; misalnya `45%/45%` berarti cap telah tercapai. Ini bukan penguasaan penuh atas kekuatan ring. Jika karakter belum memiliki Spirit Ring yang sedang diproses, tampilkan `0%/0%` dan jelaskan bahwa belum ada cap kompatibilitas aktif; jangan gunakan `???`.
5. `Spirit Ring Absorption`: status tunggal dan format `status | Day left` wajib mengikuti bagian **Status Kanonis Spirit Ring Absorption** di bawah. Nilai `Day left` merupakan bagian dari field ini, bukan field profil terpisah. Saat ditampilkan dalam gameplay, format token status sebagai label klasifikasi persis ``<status>`` (misalnya ``not eligible yet``), lalu tulis `| Day left` sesuai nilai kanonis. Jangan menambahkan alasan atau label lain ke dalam field.
6. `Martial Soul`: Martial Soul karakter sesuai sumber resmi dan riwayat.
7. `Thinker Grade`: Grade resmi yang sudah ditetapkan melalui mekanik dan riwayat sah. Jika Grade personal belum terverifikasi, tampilkan persis ``???``—jangan gunakan `Belum ditetapkan`, `Not established`, `Unknown`, atau menyimpulkan Grade dari T.Focus maupun Spirit Realm. Jika sudah terverifikasi, tampilkan Grade resmi yang tercatat.
8. `T.Focus`: field wajib dan selalu ditampilkan bersama `Thinker Grade`. Isinya adalah tahap fokus Thinker terakhir yang benar-benar lulus penilaian guru/institusi, mengikuti urutan `Pemula → Initiate → Beginner → Ordinary → Ahli → Expert` di `core/THINKER_AND_FORMULATION.md`. Format nilai sebagai label klasifikasi, misalnya ``Pemula`` atau ``Expert``; jika belum ada tahap yang terverifikasi, gunakan ``Belum ditetapkan``, kecuali sumber state memastikan karakter belum memulai latihan, yang ditulis ``Belum dimulai``. Latihan yang sedang berjalan tidak otomatis menaikkan tahap. Jangan menyimpulkan T.Focus dari Thinker Grade, menghapus field, membiarkannya kosong, atau mengganti status yang belum terverifikasi dengan dugaan. Validasi nilainya dari state aktif dan bukti penilaian yang sah.
9. `HP`: current HP dan maksimum HP mengikuti `core/HP_SYSTEM.md`.
10. `Satiety`: nilai kenyang 0–100 mengikuti `core/HUNGER_AND_METABOLISM.md`; bukan HP atau Qi. Format tampilan wajib `Satiety: nilai/100`. Setiap interval waktu terjaga harus dihitung dari timestamp dan satu kategori aktivitas yang sesuai; terapkan pengali sah dan simpan presisi internal sebelum pembulatan tampilan. Setiap aktivitas terbaru wajib menyebut Satiety: nilai sebelum → perubahan bertanda → sesudah bila berubah, atau nilai tetap beserta alasan mekanis jika tidak berubah. Konsumsi harus menyebut makanan yang benar-benar dimakan, jumlah/porsi yang dikonsumsi, efek Satiety aktual, dan tier hanya jika diketahui/relevan. Jangan menyamakan jumlah yang dibeli dengan jumlah yang dimakan; jangan memberi efek untuk sisa makanan; jangan menggandakan pemulihan Satiety. Jika snapshot awal dibuat sebelum field ini ditambahkan, tetapkan estimasi awal GM yang wajar saat bootstrap sesi baru sesuai modul; jangan otomatis memakai 0 atau 100, jangan menyimpulkan kekebalan/metabolisme khusus tanpa sumber, dan jangan mengubah snapshot hanya untuk mengisi state.
11. `Qi`: nilai/state Qi yang benar-benar ditetapkan oleh sumber resmi dan riwayat; jangan mengarang batas atau pemulihan.
12. `Kondisi Tubuh`: kondisi fisik yang didukung kejadian dan mekanik, termasuk cedera yang relevan.
13. `Equipment`: perlengkapan yang sedang dimiliki/digunakan sesuai state.
14. `Inventory`: barang bawaan yang tercatat. Untuk item yang identitas, jenis pasti, atau detail relevannya belum ditetapkan oleh kanon/GM, tampilkan item tersebut dengan label persis ``Unknown`` **membutuhkan appraisal untuk lebih pastinya**; jangan menggantinya dengan `???` atau mengarang detail. Terapkan konsisten juga pada Equipment dan loot.
15. `Assets Bangunan`: hanya bangunan atau properti yang benar-benar dimiliki karakter dan tercatat sebagai aset. Penghasilan, tabungan, uang tunai, dan barang bawaan bukan Assets Bangunan; uang hanya dicatat pada `Wallet (wealth)`, sedangkan barang bawaan dicatat pada `Inventory`.
16. `Wallet (wealth)`: saldo mata uang sesuai sistem ekonomi dan transaksi tercatat. Pertahankan format canonical: `... xc | ... xs | ... xg | ... zj | ... az`; jangan mengarang kurs atau saldo.
17. `Teknik / Kemampuan`: kemampuan serta rincian Spirit Ring yang dimiliki, dengan fungsi jelas dan sumber yang sah.
18. `Tujuan Saat Ini`: tujuan karakter yang dinyatakan pemain atau sudah tercatat; jangan mengambil alih keputusan pemain.

## Satu Jalur Bootstrap dan Save Karakter Baru

Gunakan satu proses terpadu untuk membuat, melengkapi, dan menyimpan snapshot karakter baru. Jangan membuat jalur bootstrap Wallet terpisah dari profil karakter, dan jangan mengulang proses yang sama di modul lain.

1. Baca latar yang diberikan pemain dan pertahankan seluruh fakta eksplisit. Jangan mengubah fixture atau snapshot karakter yang sudah terdaftar hanya untuk menerapkan aturan bootstrap baru.
2. Isi field ambigu dengan estimasi GM terbaik berdasarkan latar dan konteks yang tersedia. Untuk usia, gunakan 8–19 tahun sebagai acuan umum yang fleksibel, bukan batas minimum/maksimum; pilih usia di luar rentang bila paling masuk akal berdasarkan latar. Untuk field yang menyangkut mekanik, ikuti default resmi dan jangan mengarang hasil mekanik yang belum terjadi.
3. Tentukan kondisi awal yang masuk akal untuk kehidupan karakter—misalnya perlengkapan umum, kebutuhan sehari-hari, keterampilan biasa, dan keadaan ekonomi—hanya sejauh didukung latar. Bedakan estimasi awal GM dari fakta eksplisit, dan jangan menambahkan bakat rahasia, garis keturunan, Martial Soul, teknik formal, pusaka langka, atau sejarah yang tidak diberikan.
4. Tetapkan `Wallet (wealth)` sebagai bagian dari proses profil yang sama, berdasarkan latar belakang, asal/lingkungan, kondisi keluarga, pekerjaan atau sumber nafkah yang diketahui, aset, tanggung jawab, serta akses ekonomi yang masuk akal. Jangan mengundi saldo secara acak sebagai default dan jangan mengarang transaksi atau penghasilan masa lalu. Jika latar sangat tipis, pilih estimasi konservatif yang paling wajar, tandai sebagai estimasi GM pada catatan bootstrap, dan jadikan nominal konkret itu saldo awal tetap.
5. Normalisasi saldo ke urutan resmi `xc | xs | xg | zj | az` memakai kurs `core/10_ECONOMY_SYSTEM.md`. Jangan mengubah saldo eksplisit yang diberikan pemain atau sudah tersimpan di snapshot; sumber eksplisit selalu mengalahkan estimasi.
6. Setelah profil dan Wallet ditetapkan, simpan keduanya dalam satu file `players/<Nama>.md`, lalu tambahkan karakter ke `players.md`. File individual menjadi satu-satunya snapshot awal karakter; tidak perlu file, modul, atau jalur save uang yang terpisah. Ledger transaksi selama gameplay tetap merupakan riwayat perubahan setelah baseline, bukan bagian untuk mengarang sejarah sebelum sesi.
7. Untuk sesi baru karakter terdaftar, gunakan snapshot persis yang tersimpan. Untuk sesi berlanjut/recall, gunakan profil gameplay terakhir dan transaksi sah setelahnya; jangan mengestimasi ulang usia, perlengkapan, atau Wallet dan jangan menimpa state aktif dengan snapshot awal.

### Default Spirit Realm dan ras karakter baru

- Jika player tidak menetapkan Spirit Realm dan latar tidak memberi petunjuk tegas tentang tingkat kultivasi, tetapkan **Mortal**. Jangan menyimpulkan realm tinggi hanya dari bakat, status keluarga, atau tempat tinggal.
- Jika player tidak menetapkan ras dan latar tidak memberi petunjuk kuat, tentukan ras secara acak dari manusia atau bangsa setengah makhluk lain yang didukung `world/INTELLIGENT_PEOPLES.md`. Peluang manusia harus lebih besar daripada setiap pilihan nonmanusia; sesuaikan bobot dengan latar keluarga, asal/daerah, komunitas sekitar, dan persebaran yang didukung sumber wilayah.
- Jangan mengarang persentase atau mengklaim tabel peluang resmi bila canon belum menetapkannya. Jangan menganggap semua penghuni suatu wilayah memiliki ras yang sama. Jika player menyebut ras secara eksplisit atau latar memberi bukti kuat tentang keluarga/komunitas tertentu, pertahankan atau gunakan bukti itu.
- Mortal tidak berarti Martial Soul sudah Awakening. Jangan memberi Awakening, Spirit Ring, teknik formal, kekuatan rahasia, atau lineage khusus tanpa dasar canon dan proses yang sah.

## Sumber Currency dan Konsistensi Saldo

- Untuk sesi baru, cocokkan nama karakter melalui `players.md`, lalu baca file individual `players/<Nama>.md` sebagai snapshot awal lengkap, termasuk Wallet. Jika Authority secara eksplisit menetapkan state awal yang sah untuk sesi tersebut, ikuti Authority. Untuk sesi berjalan/recall, gunakan Wallet pada profil gameplay terakhir lalu terapkan transaksi sah yang terjadi setelahnya.
- `core/10_ECONOMY_SYSTEM.md` adalah sumber aturan kurs, harga, valuasi, dan transaksi; saldo individual berada di snapshot karakter atau state gameplay aktif.
- Salin saldo secara persis ke `Wallet (wealth)` dengan urutan tetap `... xc | ... xs | ... xg | ... zj | ... az`. Jangan menukar posisi denominasi, mengubah nominal, atau menebak saldo dari aset/penghasilan bila saldo sudah tercatat.
- Saldo awal baru yang belum tercatat harus ditentukan melalui langkah 4–5 pada **Satu Jalur Bootstrap dan Save Karakter Baru** di atas. Jangan lakukan undian uang terpisah. Jangan mengarang transaksi lampau untuk menjelaskan saldo awal.
- Setelah saldo awal ditetapkan, jangan mengestimasi ulang atau mengubahnya hanya karena giliran baru. Setiap perubahan harus memiliki sebab dan waktu yang jelas, jumlah masuk/keluar sesuai aturan ekonomi, serta saldo akhir konsisten dengan riwayat gameplay. Profil akhir giliran menampilkan saldo setelah transaksi sah. Tidak perlu membuat file GitHub atau modul profil terpisah khusus ledger; setiap perubahan Satiety, uang, item, equipment, loot, atau aset tetap wajib memiliki catatan ledger berkelanjutan di riwayat sesi. Jika perubahan state benar-benar terjadi, laporan sebelum → perubahan → sesudah harus menjadi bagian dari kalimat laporan perubahan di seksi `NARASI`, bukan seksi/heading tambahan. Akhiri kalimat laporan perubahan terverifikasi dengan `Log tercatat!` tepat satu kali, lalu tampilkan satu blok `LEDGER LOG` gabungan sebelum profil. Tampilkan penanda dan ledger hanya jika perubahan relevan benar-benar terjadi; jangan mengganti penanda itu dengan konfirmasi terpisah atau penegasan transaksi lain.

## Aturan Pengisian

- Jangan menambah field terpisah untuk **Spirit Rings** atau **Law** tanpa persetujuan pemilik. Jumlah slot mengikuti Spirit Realm; rincian ring masuk ke **Teknik / Kemampuan** atau deskripsi Martial Soul.
- Gunakan profil gameplay terakhir ditambah kejadian yang benar-benar terjadi. Jangan menganggap HP penuh, mengisi ulang sumber daya, mengubah saldo, atau menghapus konsekuensi tanpa sebab yang sah.
- Estimasi praktis untuk karakter baru hanya boleh digunakan bila wajar dan harus diberi label estimasi GM. Jangan mengarang rahasia besar, garis keturunan, artefak langka, atau teknik formal.
- `???` digunakan untuk **identitas karakter yang benar-benar tidak dikenal**, **nama Martial Soul yang belum diketahui**, dan `Day left` jika karakter belum pernah berhasil menyerap Spirit Ring karena jeda antarpenyerapan belum dimulai. Pada semua tahap sebelum penyerapan pertama, `??? Day left` tetap dipasangkan dengan status tahap yang tepat (`not eligible yet` atau `pending`, atau `eligible` bila syarat ring pertama terpenuhi). `???` tidak berarti riwayat cooldown hilang. Dalam tampilan gameplay, format status Spirit Ring sebagai label klasifikasi ``<status>``; jangan biarkan token status polos ketika template mewajibkan format klasifikasi.
- Field numerik yang belum tercatat diisi `0`, kecuali jika angka tersebut punya makna mekanik khusus yang akan menjadi klaim palsu bila dipaksa menjadi nol. Untuk `Day left`, bedakan dua keadaan: gunakan `??? Day left` jika belum pernah ada penyerapan Spirit Ring yang berhasil (jeda belum berlaku); gunakan `Belum ditetapkan Day left` hanya jika karakter pernah menyerap ring tetapi data waktu/riwayat yang dibutuhkan untuk menghitung cooldown tidak tersedia.
- Field nonnumerik lain yang belum ditetapkan ditulis `Belum ditetapkan`; gunakan `Tidak ada` hanya jika memang diketahui tidak ada. Jangan menebak atau menciptakan fakta.
- HP dan injury adalah state terpisah: `core/HP_SYSTEM.md` mengatur HP, sedangkan `core/INJURY_SYSTEM.md` mengatur klasifikasi dan progres pemulihan cedera.
- Satiety dan metabolisme hanya mengikuti `core/HUNGER_AND_METABOLISM.md`. Tidur malam yang dilindungi mengunci Satiety, tetapi tidak otomatis memulihkan HP, Qi, atau injury.
- Profil adalah snapshot state setelah giliran, bukan pengganti narasi kejadian atau riwayat transaksi.
- Jangan mengubah, menghilangkan, atau memindahkan field maupun mengubah ornamen visual yang ditetapkan oleh `templates/GAMEPLAY_RESPONSE_TEMPLATE.md` tanpa persetujuan pemilik repository.

## Status Kanonis Spirit Ring Absorption

Status ditentukan oleh tahap karakter terlebih dahulu, lalu kelayakan proses penyerapan berikutnya. Tampilkan **tepat satu status**, jangan menampilkan alternatif sekaligus, dan jangan menambahkan alasan/label lain di dalam field profil.

- **Mortal, tidak sedang menjalani Awakening:** Spirit Ring Absorption: ``not eligible yet`` | ??? Day left
- **Proses Martial Soul Awakening sedang berlangsung:** Spirit Ring Absorption: ``pending`` | ??? Day left
- **Awakening selesai, belum pernah menyerap ring pertama, syarat ring pertama terpenuhi:** Spirit Ring Absorption: ``eligible`` | ??? Day left
- **Awakening selesai, belum pernah menyerap ring pertama, syarat ring pertama belum terpenuhi:** Spirit Ring Absorption: ``not eligible yet`` | ??? Day left
- **Spirit Realm 1–8, syarat penyerapan berikutnya belum lengkap:** Spirit Ring Absorption: ``not eligible yet`` | N Day left
- **Spirit Realm 1–8, seluruh syarat karakter/proses penyerapan berikutnya terpenuhi:** Spirit Ring Absorption: ``eligible`` | 0 Day left
- **Spirit Realm 9 (Spirit Primordial), batas puncak sistem:** Spirit Ring Absorption: ``max`` | ∞ Day left

Aturan:
- `pending` hanya digunakan selama proses Awakening benar-benar berlangsung, bukan sekadar karena karakter belum Awakening.
- Untuk Mortal yang tidak sedang menjalani Awakening, tampilkan persis Spirit Ring Absorption: ``not eligible yet`` | ??? Day left. Jangan menggantinya dengan `Tidak ada | 0 Day left`, karena belum adanya Awakening berarti cooldown penyerapan pertama belum dimulai, bukan cooldown nol.
- Setelah Awakening selesai tetapi sebelum penyerapan pertama berhasil, `Day left` adalah `???` karena jeda belum dimulai. Awakening sendiri tidak otomatis memberikan ring atau membuat status `eligible`.
- Pada Spirit Realm 1–8, cooldown positif berarti `not eligible yet`. Cooldown nol hanyalah satu gerbang; status `eligible` hanya jika seluruh syarat resmi lain terpenuhi. Ketersediaan ring fisik tetap terpisah dari kelayakan karakter/proses.
- Spirit Realm 9 selalu `max | ∞ Day left`. Sembilan slot adalah batas sistem; jangan hitung cooldown ke ring kesepuluh, jangan tampilkan `eligible`, dan jangan menambahkan Spirit Realm atau slot kesepuluh tanpa revisi canon eksplisit pemilik.
- `Belum ditetapkan Day left` hanya untuk save lama yang diketahui pernah menyerap ring tetapi riwayat waktunya tidak cukup untuk merekonstruksi cooldown. Jangan gunakan untuk Mortal, Awakening, karakter yang belum pernah menyerap ring, atau Spirit Realm 9.

## Rujukan Perhitungan Day left

Template ini hanya menetapkan format field dan pemetaan status `Spirit Ring Absorption`. Rumus, akumulasi waktu yang memenuhi syarat, konversi durasi, dan perhitungan `Day left` hanya ditetapkan di `gameplay/TIME_AND_ACTION_RULES.md` §7; interval minimum `T_min` hanya ditetapkan di `bestiary/SPIRIT_BEAST_RULES.md` §3. Jangan menyalin atau membuat formulasi hitung alternatif di template ini.
