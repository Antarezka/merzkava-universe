# Merzkava Universe — Character Profile Field Definitions

**File ini mendefinisikan arti field dan konsistensi state. Bentuk visual lengkap, urutan field, ornamen, dan penutup setiap balasan gameplay hanya ditentukan oleh `templates/GAMEPLAY_RESPONSE_TEMPLATE.md`.**

## Field Profil Resmi

Pertahankan nama dan urutan field sesuai `templates/GAMEPLAY_RESPONSE_TEMPLATE.md`:

1. `Nama`: nama karakter yang tercatat.
2. `Usia`: usia karakter yang tercatat.
3. `Spirit Realm`: selalu tulis nama field dan tingkat kultivasi sebagai `Spirit Realm` (bukan `Realm` atau `Cultivation Realm`), beserta Stage dan progres sesuai sistem resmi. Mortal ditulis `Mortal/0`, bukan `Spirit Realm 0`.
4. `Sync progress`: progres saat ini dibandingkan dengan cap kompatibilitas ring saat ini. Cap tidak selalu 100%; misalnya `45%/45%` berarti cap telah tercapai. Ini bukan penguasaan penuh atas kekuatan ring. Jika karakter belum memiliki Spirit Ring yang sedang diproses, tampilkan `0%/0%` dan jelaskan bahwa belum ada cap kompatibilitas aktif; jangan gunakan `???`.
5. `Spirit Ring Absorption`: status apakah karakter memenuhi syarat untuk menjalani proses penyerapan Spirit Ring berikutnya jika Spirit Ring tersedia. Periksa Awakening untuk ring pertama; untuk ring berikutnya, periksa Sync progress/bottleneck, jeda minimum, item wajib, toleransi tubuh, dan seluruh syarat resmi yang berlaku. Field ini menilai kelayakan karakter, bukan ketersediaan fisik Spirit Ring. Gunakan `Eligible` hanya jika semua syarat karakter/proses yang berlaku terpenuhi; selain itu gunakan `Not Eligible — [alasan singkat]`. Mortal yang belum Awakening tidak eligible untuk ring pertama; Mortal yang sudah Awakening tidak memerlukan bottleneck atau jeda antar-ring untuk ring pertama.
6. `Day left`: hitung mundur khusus sisa jeda minimum antarpenyerapan Spirit Ring yang berhasil. Untuk ring kedua dan seterusnya, nilai ini wajib mencapai `0` sebelum status penyerapan dapat menjadi `Eligible`. Hitung interval resmi berdasarkan nomor ring berikutnya, tetapi kurangi hanya waktu dunia yang dijalani secara normal di luar Kultivasi. **Waktu yang dipakai untuk Kultivasi tidak mengurangi `Day left`, termasuk time skip Kultivasi satu bulan; timestamp dan kalender dunia tetap maju.** Lacak durasi normal yang memenuhi syarat sejak penyerapan berhasil terakhir dan kecualikan semua durasi Kultivasi. Jika riwayat tidak memisahkan durasi Kultivasi dari waktu normal, atau data penyerapan tidak tersedia/bertentangan, tulis `Belum ditetapkan Day left`; jangan menebak nol.
7. `Martial Soul`: Martial Soul karakter sesuai sumber resmi dan riwayat.
8. `Thinker Grade`: grade yang sudah ditetapkan oleh mekanik/riwayat.
9. `HP`: current HP dan maksimum HP mengikuti `core/HP_SYSTEM.md`.
10. `Satiety`: nilai kenyang 0–100 mengikuti `core/HUNGER_AND_METABOLISM.md`; bukan HP atau Qi. Format tampilan wajib `Satiety: nilai/100`. Jika snapshot awal dibuat sebelum field ini ditambahkan, tetapkan estimasi awal GM yang wajar saat bootstrap sesi baru berdasarkan modul tersebut; jangan otomatis memakai 0 atau 100, jangan menyimpulkan kekebalan/metabolisme khusus tanpa sumber, dan jangan mengubah snapshot hanya untuk mengisi state sesi.
11. `Qi`: nilai/state Qi yang benar-benar ditetapkan oleh sumber resmi dan riwayat; jangan mengarang batas atau pemulihan.
12. `Kondisi Tubuh`: kondisi fisik yang didukung kejadian dan mekanik, termasuk cedera yang relevan.
13. `Equipment`: perlengkapan yang sedang dimiliki/digunakan sesuai state.
14. `Inventory`: barang bawaan yang tercatat.
15. `Assets Bangunan`: hanya bangunan atau properti yang benar-benar dimiliki karakter dan tercatat sebagai aset. Penghasilan, tabungan, uang tunai, dan barang bawaan bukan Assets Bangunan; uang hanya dicatat pada `Wallet (wealth)`, sedangkan barang bawaan dicatat pada `Inventory`.
16. `Wallet (wealth)`: saldo mata uang sesuai sistem ekonomi dan transaksi tercatat. Pertahankan format canonical: `... xc | ... xs | ... xg | ... zj | ... az`; jangan mengarang kurs atau saldo.
17. `Teknik / Kemampuan`: kemampuan serta rincian Spirit Ring yang dimiliki, dengan fungsi jelas dan sumber yang sah.
18. `Tujuan Saat Ini`: tujuan karakter yang dinyatakan pemain atau sudah tercatat; jangan mengambil alih keputusan pemain.

## Sumber Currency dan Konsistensi Saldo

- Untuk sesi baru, cocokkan nama karakter melalui `players.md`, lalu ambil saldo Wallet dari file individual yang tepat `players/<Nama>.md`. Jangan menggunakan file karakter lain. Jika Authority secara eksplisit menyediakan saldo yang sah untuk karakter/sesi tersebut, gunakan saldo Authority dan abaikan pencarian saldo awal di snapshot. Untuk sesi berjalan/recall, gunakan Wallet pada profil gameplay terakhir lalu terapkan transaksi sah yang terjadi setelahnya.
- `core/10_ECONOMY_SYSTEM.md` adalah sumber aturan kurs, harga, valuasi, dan transaksi; file itu bukan sumber saldo individual.
- Salin saldo secara persis ke field `Wallet (wealth)` dengan format `... xc | ... xs | ... xg | ... zj | ... az`. Jangan memakai deskripsi penghasilan atau Assets untuk menebak saldo bila saldo sudah tercatat.
- Jika saldo awal tidak tercatat di snapshot atau riwayat, lakukan **undian bootstrap satu kali** untuk menentukan saldo awal konkret, lalu tampilkan angka yang dipilih sebagai saldo awal tetap. Jangan menghitung saldo dari latar, pekerjaan, Assets, atau penghasilan masa lalu, dan jangan mengarang transaksi lampau. Jika snapshot sudah mencatat saldo, snapshot menjadi sumber utama dan tidak boleh diundi ulang.
- Setelah saldo awal ditetapkan, jangan mengundi ulang atau mengubahnya hanya karena giliran baru. Setiap perubahan harus memiliki sebab dan waktu yang jelas, jumlah masuk/keluar yang sesuai dengan aturan ekonomi, serta saldo akhir yang konsisten dengan riwayat gameplay. Profil akhir giliran menampilkan saldo setelah transaksi sah; tidak ada file ledger terpisah yang wajib dibuat.

## Aturan Pengisian

- Jangan menambah field terpisah untuk **Spirit Rings** atau **Law** tanpa persetujuan pemilik. Jumlah slot mengikuti Spirit Realm; rincian ring masuk ke **Teknik / Kemampuan** atau deskripsi Martial Soul.
- Gunakan profil gameplay terakhir ditambah kejadian yang benar-benar terjadi. Jangan menganggap HP penuh, mengisi ulang sumber daya, mengubah saldo, atau menghapus konsekuensi tanpa sebab yang sah.
- Estimasi praktis untuk karakter baru hanya boleh digunakan bila wajar dan harus diberi label estimasi GM. Jangan mengarang rahasia besar, garis keturunan, artefak langka, atau teknik formal.
- `???` hanya boleh digunakan untuk **identitas karakter yang benar-benar tidak dikenal** atau **nama Martial Soul yang belum diketahui**. Jangan gunakan `???` pada field lain.
- Field numerik yang belum tercatat diisi `0`, bukan `???`. Pengecualian hanya bila angka tersebut punya makna mekanik khusus yang akan menjadi klaim palsu jika dipaksa menjadi nol; gunakan `Belum ditetapkan` untuk field seperti `Day left` jika timestamp/riwayat yang dibutuhkan tidak tersedia.
- Field nonnumerik lain yang belum ditetapkan ditulis `Belum ditetapkan`; gunakan `Tidak ada` hanya jika memang diketahui tidak ada. Jangan menebak atau menciptakan fakta.
- HP dan injury adalah state terpisah: `core/HP_SYSTEM.md` mengatur HP, sedangkan `core/INJURY_SYSTEM.md` mengatur klasifikasi dan progres pemulihan cedera.
- Satiety dan metabolisme hanya mengikuti `core/HUNGER_AND_METABOLISM.md`. Tidur malam yang dilindungi mengunci Satiety, tetapi tidak otomatis memulihkan HP, Qi, atau injury.
- Profil adalah snapshot state setelah giliran, bukan pengganti narasi kejadian atau riwayat transaksi.
- Jangan mengubah, menghilangkan, atau memindahkan field maupun mengubah ornamen visual yang ditetapkan oleh `templates/GAMEPLAY_RESPONSE_TEMPLATE.md` tanpa persetujuan pemilik repository.

## Perhitungan Day left — Pengecualian Penyerapan Spirit Ring

`Day left` hanya menghitung jeda minimum antara penyerapan Spirit Ring yang berhasil; ini bukan penghitung waktu breakthrough Kultivasi atau aktivitas lain.

**Formulasi kanonis `Day left` (wajib):**

Definisikan:
- `T_min` = interval minimum resmi untuk penyerapan berikutnya, sesuai jumlah ring yang telah berhasil diserap dan tabel interval di `bestiary/SPIRIT_BEAST_RULES.md`.
- `T_eligible` = total durasi waktu dunia yang benar-benar dijalani secara normal di luar Kultivasi sejak penyerapan Spirit Ring terakhir yang berhasil.
- `T_remaining` = sisa interval yang harus dipenuhi.

Rumus:
```text
T_remaining = max(0, T_min - T_eligible)

Jika T_remaining = 0:
    Day left = 0
Jika T_remaining > 0:
    Day left = ceil(T_remaining / 24 jam)
```

`T_eligible` adalah akumulasi durasi yang memenuhi syarat, bukan selisih timestamp mentah. Waktu dari aksi normal, aktivitas harian, perjalanan, istirahat, atau tidur hanya dihitung selama waktu dunia benar-benar berlalu dan tidak tumpang tindih dengan durasi lain. **Semua durasi yang diklasifikasikan sebagai Kultivasi dikecualikan sepenuhnya dari `T_eligible`**, termasuk time skip Kultivasi hingga satu bulan. Timestamp dan kalender dunia tetap maju selama Kultivasi, tetapi `T_eligible` dan `Day left` tidak berubah akibat durasi tersebut.

Pembulatan dilakukan pada sisa interval: sisa 1 jam hingga 24 jam = `1 Day left`; sisa lebih dari 24 jam hingga 48 jam = `2 Day left`. Angka hanya menjadi `0 Day left` saat `T_eligible >= T_min`. Jangan mengurangi satu hari penuh hanya karena giliran berganti atau tanggal kalender berubah.

Jika riwayat penyerapan atau catatan durasi normal/Kultivasi tidak cukup untuk menghitung `T_eligible` secara andal, gunakan `Belum ditetapkan Day left`; jangan memperkirakan dan jangan menganggap cooldown selesai. Untuk ring kedua hingga kesembilan, `Day left = 0` adalah gerbang wajib yang terpisah dari Sync/bottleneck, ketersediaan ring, item, toleransi tubuh, dan syarat resmi lainnya.

Gunakan formulasi di atas sebagai satu-satunya metode hitung. Nilai yang ditampilkan pada profil harus berasal dari `T_min` dan akumulasi `T_eligible` yang dapat ditelusuri dalam riwayat sesi.
