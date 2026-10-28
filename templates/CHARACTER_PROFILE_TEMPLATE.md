# Merzkava Universe — Character Profile Field Definitions

**File ini mendefinisikan arti field dan konsistensi state. Bentuk visual lengkap, urutan field, ornamen, dan penutup setiap balasan gameplay hanya ditentukan oleh `templates/GAMEPLAY_RESPONSE_TEMPLATE.md`.**

## Field Profil Resmi

Pertahankan nama dan urutan field sesuai `templates/GAMEPLAY_RESPONSE_TEMPLATE.md`:

1. `Nama`: nama karakter yang tercatat.
2. `Usia`: usia karakter yang tercatat.
3. `Spirit Realm`: selalu tulis nama field dan tingkat kultivasi sebagai `Spirit Realm` (bukan `Realm` atau `Cultivation Realm`), beserta Stage dan progres sesuai sistem resmi. Mortal ditulis `Mortal` sebagai status dasar sebelum Spirit Realm 1; jangan menuliskannya sebagai `Mortal/0` atau `Spirit Realm 0`.
4. `Sync progress`: progres saat ini dibandingkan dengan cap kompatibilitas ring saat ini. Cap tidak selalu 100%; misalnya `45%/45%` berarti cap telah tercapai. Ini bukan penguasaan penuh atas kekuatan ring. Jika karakter belum memiliki Spirit Ring yang sedang diproses, tampilkan `0%/0%` dan jelaskan bahwa belum ada cap kompatibilitas aktif; jangan gunakan `???`.
5. `Spirit Ring Absorption`: status tunggal dan format `status | Day left` wajib mengikuti bagian **Status Kanonis Spirit Ring Absorption** di bawah. Nilai `Day left` merupakan bagian dari field ini, bukan field profil terpisah. Saat ditampilkan dalam gameplay, format token status sebagai label klasifikasi persis ``*<status>*`` (misalnya ``*not eligible yet*``), lalu tulis `| Day left` sesuai nilai kanonis. Jangan menambahkan alasan atau label lain ke dalam field.
6. `Martial Soul`: jika karakter belum menjalani Martial Soul Awakening, tampilkan hanya `???` sebagai satu-satunya nilai field. Jangan menambahkan `Unknown`, keterangan appraisal, atau status Awakening di field ini. Awakening mengungkap Martial Soul; appraisal adalah proses penilaian terpisah dan tidak menggantikan Awakening. Setelah Awakening, tampilkan nama/identitas Martial Soul yang benar-benar ditetapkan oleh hasil dan riwayat resmi.
7. `Thinker Grade`: grade yang sudah ditetapkan oleh mekanik/riwayat.
8. `HP`: current HP dan maksimum HP mengikuti `core/HP_SYSTEM.md`.
9. `Satiety`: nilai kenyang 0–100 mengikuti `core/HUNGER_AND_METABOLISM.md`; bukan HP atau Qi. Format tampilan wajib `Satiety: nilai/100`. Setiap aktivitas terbaru wajib menyebutkan Satiety dalam narasi/laporan, termasuk nilai sebelum → perubahan → sesudah bila berubah atau nilai tetap beserta alasannya jika tidak berubah. Konsumsi wajib menyebut nama item dan tier jika diketahui, jumlah, serta efek aktual; tier tidak otomatis menentukan efek nutrisi. Jika snapshot awal dibuat sebelum field ini ditambahkan, tetapkan estimasi awal GM yang wajar saat bootstrap sesi baru berdasarkan modul tersebut; jangan otomatis memakai 0 atau 100, jangan menyimpulkan kekebalan/metabolisme khusus tanpa sumber, dan jangan mengubah snapshot hanya untuk mengisi state sesi.
10. `Qi`: nilai/state Qi yang benar-benar ditetapkan oleh sumber resmi dan riwayat; jangan mengarang batas atau pemulihan.
11. `Kondisi Tubuh`: kondisi fisik yang didukung kejadian dan mekanik, termasuk cedera yang relevan.
12. `Equipment`: perlengkapan yang sedang dimiliki/digunakan sesuai state.
13. `Inventory`: barang bawaan yang tercatat. Untuk item yang identitas, jenis pasti, atau detail relevannya belum ditetapkan oleh kanon/GM, tampilkan item tersebut dengan label persis `*Unknown* *membutuhkan appraisal untuk lebih pastinya*`; jangan menggantinya dengan `???` atau mengarang detail. Terapkan konsisten juga pada Equipment dan loot.
14. `Assets Bangunan`: hanya bangunan atau properti yang benar-benar dimiliki karakter dan tercatat sebagai aset. Penghasilan, tabungan, uang tunai, dan barang bawaan bukan Assets Bangunan; uang hanya dicatat pada `Wallet (wealth)`, sedangkan barang bawaan dicatat pada `Inventory`.
15. `Wallet (wealth)`: saldo mata uang sesuai sistem ekonomi dan transaksi tercatat. Pertahankan format canonical: `... xc | ... xs | ... xg | ... zj | ... az`; jangan mengarang kurs atau saldo.
16. `Teknik / Kemampuan`: kemampuan serta rincian Spirit Ring yang dimiliki, dengan fungsi jelas dan sumber yang sah.
17. `Tujuan Saat Ini`: tujuan karakter yang dinyatakan pemain atau sudah tercatat; jangan mengambil alih keputusan pemain.

## Sumber Currency dan Konsistensi Saldo

- Untuk sesi baru, cocokkan nama karakter melalui `players.md`, lalu ambil saldo Wallet dari file individual yang tepat `players/<Nama>.md`. Jangan menggunakan file karakter lain. Jika Authority secara eksplisit menyediakan saldo yang sah untuk karakter/sesi tersebut, gunakan saldo Authority dan abaikan pencarian saldo awal di snapshot. Untuk sesi berjalan/recall, gunakan Wallet pada profil gameplay terakhir lalu terapkan transaksi sah yang terjadi setelahnya.
- `core/10_ECONOMY_SYSTEM.md` adalah sumber aturan kurs, harga, valuasi, dan transaksi; file itu bukan sumber saldo individual.
- Salin saldo secara persis ke field `Wallet (wealth)` dengan urutan denominasi yang tidak boleh diubah: `... xc | ... xs | ... xg | ... zj | ... az`. Pindahkan hanya nominal ke posisi denominasi kanonis yang sesuai; jangan menukar urutan berdasarkan besar-kecil nilai, jangan menyalin urutan yang salah dari respons terdahulu, dan jangan mengubah total saldo. Jangan memakai deskripsi penghasilan atau Assets untuk menebak saldo bila saldo sudah tercatat.
- Jika saldo awal tidak tercatat di snapshot atau riwayat, lakukan **undian bootstrap satu kali** untuk menentukan saldo awal konkret, lalu tampilkan angka yang dipilih sebagai saldo awal tetap. Jangan menghitung saldo dari latar, pekerjaan, Assets, atau penghasilan masa lalu, dan jangan mengarang transaksi lampau. Jika snapshot sudah mencatat saldo, snapshot menjadi sumber utama dan tidak boleh diundi ulang.
- Setelah saldo awal ditetapkan, jangan mengundi ulang atau mengubahnya hanya karena giliran baru. Setiap perubahan harus memiliki sebab dan waktu yang jelas, jumlah masuk/keluar yang sesuai dengan aturan ekonomi, serta saldo akhir yang konsisten dengan riwayat gameplay. Profil akhir giliran menampilkan saldo setelah transaksi sah. Tidak perlu membuat file GitHub atau modul profil terpisah khusus ledger; setiap perubahan Satiety, uang, item, equipment, loot, atau aset tetap wajib memiliki catatan ledger berkelanjutan di riwayat sesi. Jika perubahan state benar-benar terjadi, laporan sebelum → perubahan → sesudah harus menjadi bagian dari kalimat laporan perubahan di seksi `NARASI`, bukan seksi/heading tambahan. Akhiri kalimat laporan perubahan terverifikasi dengan `Log tercatat!` tepat satu kali, lalu tampilkan satu blok `LEDGER LOG` gabungan sebelum profil. Tampilkan penanda dan ledger hanya jika perubahan relevan benar-benar terjadi; jangan mengganti penanda itu dengan konfirmasi terpisah atau penegasan transaksi lain.

## Aturan Pengisian

- Jangan menambah field terpisah untuk **Spirit Rings** atau **Law** tanpa persetujuan pemilik. Jumlah slot mengikuti Spirit Realm; rincian ring masuk ke **Teknik / Kemampuan** atau deskripsi Martial Soul.
- Gunakan profil gameplay terakhir ditambah kejadian yang benar-benar terjadi. Jangan menganggap HP penuh, mengisi ulang sumber daya, mengubah saldo, atau menghapus konsekuensi tanpa sebab yang sah.
- Estimasi praktis untuk karakter baru hanya boleh digunakan bila wajar dan harus diberi label estimasi GM. Jangan mengarang rahasia besar, garis keturunan, artefak langka, atau teknik formal.
- `???` digunakan untuk **identitas karakter yang benar-benar tidak dikenal**, **nama Martial Soul yang belum diketahui**, dan `Day left` jika karakter belum pernah berhasil menyerap Spirit Ring karena jeda antarpenyerapan belum dimulai. Pada semua tahap sebelum penyerapan pertama, `??? Day left` tetap dipasangkan dengan status tahap yang tepat (`not eligible yet` atau `pending`, atau `eligible` bila syarat ring pertama terpenuhi). `???` tidak berarti riwayat cooldown hilang. Dalam tampilan gameplay, format status Spirit Ring sebagai label klasifikasi ``*<status>*``; jangan biarkan token status polos ketika template mewajibkan format klasifikasi.
- Field numerik yang belum tercatat diisi `0`, kecuali jika angka tersebut punya makna mekanik khusus yang akan menjadi klaim palsu bila dipaksa menjadi nol. Untuk `Day left`, bedakan dua keadaan: gunakan `??? Day left` jika belum pernah ada penyerapan Spirit Ring yang berhasil (jeda belum berlaku); gunakan `Belum ditetapkan Day left` hanya jika karakter pernah menyerap ring tetapi data waktu/riwayat yang dibutuhkan untuk menghitung cooldown tidak tersedia.
- Field nonnumerik lain yang belum ditetapkan ditulis `Belum ditetapkan`; gunakan `Tidak ada` hanya jika memang diketahui tidak ada. Jangan menebak atau menciptakan fakta.
- HP dan injury adalah state terpisah: `core/HP_SYSTEM.md` mengatur HP, sedangkan `core/INJURY_SYSTEM.md` mengatur klasifikasi dan progres pemulihan cedera.
- Satiety dan metabolisme hanya mengikuti `core/HUNGER_AND_METABOLISM.md`. Tidur malam yang dilindungi mengunci Satiety, tetapi tidak otomatis memulihkan HP, Qi, atau injury.
- Profil adalah snapshot state setelah giliran, bukan pengganti narasi kejadian atau riwayat transaksi.
- Jangan mengubah, menghilangkan, atau memindahkan field maupun mengubah ornamen visual yang ditetapkan oleh `templates/GAMEPLAY_RESPONSE_TEMPLATE.md` tanpa persetujuan pemilik repository.

## Status Kanonis Spirit Ring Absorption

Status ditentukan oleh tahap karakter terlebih dahulu, lalu kelayakan proses penyerapan berikutnya. Tampilkan **tepat satu status**, jangan menampilkan alternatif sekaligus, dan jangan menambahkan alasan/label lain di dalam field profil.

- **Mortal, tidak sedang menjalani Awakening:** Spirit Ring Absorption: ``*not eligible yet*`` | ??? Day left
- **Proses Martial Soul Awakening sedang berlangsung:** Spirit Ring Absorption: ``*pending*`` | ??? Day left
- **Awakening selesai, belum pernah menyerap ring pertama, syarat ring pertama terpenuhi:** Spirit Ring Absorption: ``*eligible*`` | ??? Day left
- **Awakening selesai, belum pernah menyerap ring pertama, syarat ring pertama belum terpenuhi:** Spirit Ring Absorption: ``*not eligible yet*`` | ??? Day left
- **Spirit Realm 1–8, syarat penyerapan berikutnya belum lengkap:** Spirit Ring Absorption: ``*not eligible yet*`` | N Day left
- **Spirit Realm 1–8, seluruh syarat karakter/proses penyerapan berikutnya terpenuhi:** Spirit Ring Absorption: ``*eligible*`` | 0 Day left
- **Spirit Realm 9 (Spirit Primordial), batas puncak sistem:** Spirit Ring Absorption: ``*max*`` | ∞ Day left

Aturan:
- `pending` hanya digunakan selama proses Awakening benar-benar berlangsung, bukan sekadar karena karakter belum Awakening.
- Untuk Mortal yang tidak sedang menjalani Awakening, tampilkan persis Spirit Ring Absorption: ``*not eligible yet*`` | ??? Day left. Jangan menggantinya dengan `Tidak ada | 0 Day left`, karena belum adanya Awakening berarti cooldown penyerapan pertama belum dimulai, bukan cooldown nol.
- Setelah Awakening selesai tetapi sebelum penyerapan pertama berhasil, `Day left` adalah `???` karena jeda belum dimulai. Awakening sendiri tidak otomatis memberikan ring atau membuat status `eligible`.
- Pada Spirit Realm 1–8, cooldown positif berarti `not eligible yet`. Cooldown nol hanyalah satu gerbang; status `eligible` hanya jika seluruh syarat resmi lain terpenuhi. Ketersediaan ring fisik tetap terpisah dari kelayakan karakter/proses.
- Spirit Realm 9 selalu `max | ∞ Day left`. Sembilan slot adalah batas sistem; jangan hitung cooldown ke ring kesepuluh, jangan tampilkan `eligible`, dan jangan menambahkan Spirit Realm atau slot kesepuluh tanpa revisi canon eksplisit pemilik.
- `Belum ditetapkan Day left` hanya untuk save lama yang diketahui pernah menyerap ring tetapi riwayat waktunya tidak cukup untuk merekonstruksi cooldown. Jangan gunakan untuk Mortal, Awakening, karakter yang belum pernah menyerap ring, atau Spirit Realm 9.

## Rujukan Perhitungan Day left

Template ini hanya menetapkan format field dan pemetaan status `Spirit Ring Absorption`. Rumus, akumulasi waktu yang memenuhi syarat, konversi durasi, dan perhitungan `Day left` hanya ditetapkan di `gameplay/TIME_AND_ACTION_RULES.md` §7; interval minimum `T_min` hanya ditetapkan di `bestiary/SPIRIT_BEAST_RULES.md` §3. Jangan menyalin atau membuat formulasi hitung alternatif di template ini.
