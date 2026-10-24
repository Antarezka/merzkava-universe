# Xuanling Realm — Character Profile Field Definitions

**File ini mendefinisikan arti field dan konsistensi state. Bentuk visual lengkap, urutan field, ornamen, dan penutup setiap balasan gameplay hanya ditentukan oleh `templates/GAMEPLAY_RESPONSE_TEMPLATE.md`.**

## Field Profil Resmi

Pertahankan nama dan urutan field sesuai `templates/GAMEPLAY_RESPONSE_TEMPLATE.md`:

1. `Nama`: nama karakter yang tercatat.
2. `Usia`: usia karakter yang tercatat.
3. `Spirit Realm`: Realm/Stage dan progres sesuai sistem resmi.
4. `Sync progress`: progres saat ini dibandingkan dengan cap kompatibilitas ring saat ini. Cap tidak selalu 100%; misalnya `45%/45%` berarti cap telah tercapai. Ini bukan penguasaan penuh atas kekuatan ring.
5. `Breakthrough`: status bottleneck/proses menerobos berdasarkan Realm/Stage, Sync progress terhadap cap, ketersediaan ring berikutnya, item wajib, jeda minimum, dan seluruh syarat resmi lainnya.
6. `Day left`: sisa durasi sampai jeda minimum antarpenyerapan Spirit Ring berikutnya terpenuhi. Pilih interval berdasarkan jumlah ring yang telah berhasil diserap, lalu hitung dari timestamp dunia penyerapan terakhir yang berhasil menurut `bestiary/SPIRIT_BEAST_RULES.md`.
7. `Martial Soul`: Martial Soul karakter sesuai sumber resmi dan riwayat.
8. `Thinker Grade`: grade yang sudah ditetapkan oleh mekanik/riwayat.
9. `HP`: current HP dan maksimum HP mengikuti `core/HP_SYSTEM.md`.
10. `Satiety`: nilai kenyang 0–100 mengikuti `core/HUNGER_AND_METABOLISM.md`; bukan HP atau Qi. Format tampilan wajib `Satiety: nilai/100`.
11. `Qi`: nilai/state Qi yang benar-benar ditetapkan oleh sumber resmi dan riwayat; jangan mengarang batas atau pemulihan.
12. `Kondisi Tubuh`: kondisi fisik yang didukung kejadian dan mekanik, termasuk cedera yang relevan.
13. `Equipment`: perlengkapan yang sedang dimiliki/digunakan sesuai state.
14. `Inventory`: barang bawaan yang tercatat.
15. `Assets`: aset yang tercatat selain rincian mata uang yang ditampilkan pada field Currency.
16. `Currency (xuan/zun)`: saldo mata uang sesuai sistem ekonomi dan transaksi tercatat. Pertahankan format canonical: `...xc | ...xs | ...xg | ...zj | ...az`; jangan mengarang kurs atau saldo.
17. `Teknik / Kemampuan`: kemampuan serta rincian Spirit Ring yang dimiliki, dengan fungsi jelas dan sumber yang sah.
18. `Tujuan Saat Ini`: tujuan karakter yang dinyatakan pemain atau sudah tercatat; jangan mengambil alih keputusan pemain.

## Sumber Currency dan Konsistensi Saldo

- Untuk sesi baru, gunakan saldo eksplisit pada snapshot `players/<Nama>.md`. Untuk sesi berjalan/recall, gunakan Currency pada profil gameplay terakhir lalu terapkan transaksi sah yang terjadi setelahnya.
- `core/10_ECONOMY_SYSTEM.md` adalah sumber aturan kurs, harga, valuasi, dan transaksi; file itu bukan sumber saldo individual.
- Salin saldo secara persis ke field `Currency (xuan/zun)` dengan format `...xc | ...xs | ...xg | ...zj | ...az`. Jangan memakai deskripsi penghasilan atau Assets untuk menebak saldo bila saldo sudah tercatat.
- Jika saldo awal tidak tercatat di snapshot atau riwayat, lakukan **undian bootstrap satu kali** untuk menentukan saldo awal konkret, lalu tampilkan angka yang dipilih sebagai saldo awal tetap. Jangan menghitung saldo dari latar, pekerjaan, Assets, atau penghasilan masa lalu, dan jangan mengarang transaksi lampau. Jika snapshot sudah mencatat saldo, snapshot menjadi sumber utama dan tidak boleh diundi ulang.
- Setelah saldo awal ditetapkan, jangan mengundi ulang atau mengubahnya hanya karena giliran baru. Setiap perubahan harus memiliki sebab dan waktu yang jelas, jumlah masuk/keluar yang sesuai dengan aturan ekonomi, serta saldo akhir yang konsisten dengan riwayat gameplay. Profil akhir giliran menampilkan saldo setelah transaksi sah; tidak ada file ledger terpisah yang wajib dibuat.

## Aturan Pengisian

- Jangan menambah field terpisah untuk **Spirit Rings** atau **Law** tanpa persetujuan pemilik. Jumlah slot mengikuti Realm; rincian ring masuk ke **Teknik / Kemampuan** atau deskripsi Martial Soul.
- Gunakan profil gameplay terakhir ditambah kejadian yang benar-benar terjadi. Jangan menganggap HP penuh, mengisi ulang sumber daya, mengubah saldo, atau menghapus konsekuensi tanpa sebab yang sah.
- Estimasi praktis untuk karakter baru hanya boleh digunakan bila wajar dan harus diberi label estimasi GM. Jangan mengarang rahasia besar, garis keturunan, artefak langka, atau teknik formal.
- `???` hanya boleh digunakan untuk **identitas karakter yang benar-benar tidak dikenal** atau **nama Martial Soul yang belum diketahui**. Jangan gunakan `???` pada field lain.
- Field numerik yang belum tercatat diisi `0`, bukan `???`. Pengecualian hanya bila angka tersebut punya makna mekanik khusus yang akan menjadi klaim palsu jika dipaksa menjadi nol; gunakan `Belum ditetapkan` untuk field seperti `Day left` jika timestamp/riwayat yang dibutuhkan tidak tersedia.
- Field nonnumerik lain yang belum ditetapkan ditulis `Belum ditetapkan`; gunakan `Tidak ada` hanya jika memang diketahui tidak ada. Jangan menebak atau menciptakan fakta.
- HP dan injury adalah state terpisah: `core/HP_SYSTEM.md` mengatur HP, sedangkan `core/INJURY_SYSTEM.md` mengatur klasifikasi dan progres pemulihan cedera.
- Satiety dan metabolisme hanya mengikuti `core/HUNGER_AND_METABOLISM.md`. Tidur malam yang dilindungi mengunci Satiety, tetapi tidak otomatis memulihkan HP, Qi, atau injury.
- Profil adalah snapshot state setelah giliran, bukan pengganti narasi kejadian atau riwayat transaksi.
- Jangan mengubah, menghilangkan, atau memindahkan field maupun mengubah ornamen visual yang ditetapkan oleh `templates/GAMEPLAY_RESPONSE_TEMPLATE.md` tanpa persetujuan pemilik repository.

## Perhitungan Day left

- Gunakan selisih waktu dunia yang tercatat, bukan jumlah giliran atau waktu nyata.
- Bulatkan sisa durasi positif ke atas dalam satuan 24 jam: 1 jam tersisa = `1 Day left`, 24 jam = `1 Day left`, 25 jam = `2 Day left`. Ini hitung mundur durasi, bukan hitungan pergantian tanggal kalender.
- Tulis `0 Day left` hanya ketika jeda minimum benar-benar terpenuhi. Nilai nol bukan jaminan breakthrough atau penyerapan ring sah/berhasil.
- Jika timestamp, jumlah ring, atau riwayat penyerapan tidak diketahui atau bertentangan, tulis `Belum ditetapkan Day left`; jangan tulis `??? Day left`, dan jangan menulis `0 Day left` karena nol berarti jeda minimum benar-benar terpenuhi.
- Hitung ulang hanya ketika timestamp dunia atau informasi riwayat yang sah berubah. Pergantian giliran saja tidak mengurangi nilai.
