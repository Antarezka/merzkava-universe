# Xuanling Realm — Character Profile Field Definitions

**Format visual lengkap setiap balasan gameplay hanya bersumber dari `templates/GAMEPLAY_RESPONSE_TEMPLATE.md`.** File ini mendefinisikan arti field dan konsistensi state, bukan membuat format output kedua.

## Field Profil Resmi

Pertahankan nama dan urutan field yang ditetapkan di `templates/GAMEPLAY_RESPONSE_TEMPLATE.md`:

- `Nama`, `Usia`: identitas karakter dan usia yang tercatat.
- `Spirit Realm`: Realm/Stage dan progres yang sesuai sistem resmi.
- `Sync progress`: progres saat ini dibandingkan dengan cap kompatibilitas ring saat ini. Cap tidak selalu 100%; misalnya `45%/45%` berarti cap telah tercapai. Ini bukan penguasaan penuh atas kekuatan ring.
- `Breakthrough`: status bottleneck/proses menerobos berdasarkan Realm/Stage, Sync progress terhadap cap, ketersediaan ring berikutnya, item wajib, jeda minimum, dan seluruh syarat resmi lainnya.
- `Day left`: sisa durasi sampai jeda minimum antarpenyerapan Spirit Ring berikutnya terpenuhi. Pilih interval berdasarkan jumlah ring yang telah berhasil diserap (misalnya Ring 1 → Ring 2), lalu hitung dari timestamp dunia penyerapan terakhir yang berhasil menurut `bestiary/SPIRIT_BEAST_RULES.md`.
- `Martial Soul`: Martial Soul karakter sesuai sumber resmi dan riwayat.
- `Thinker Grade`: grade yang sudah ditetapkan oleh mekanik/riwayat.
- `HP`: current HP dan maksimum HP mengikuti `core/HP_SYSTEM.md`.
- `Satiety`: nilai kenyang 0–100 mengikuti `core/HUNGER_AND_METABOLISM.md`; bukan HP atau Qi.
- `Qi`: nilai/state Qi yang benar-benar ditetapkan oleh sumber resmi dan riwayat; jangan mengarang batas atau pemulihan.
- `Kondisi Tubuh`: kondisi fisik yang didukung kejadian dan mekanik, termasuk cedera yang relevan.
- `Equipment`, `Inventory`, `Assets`, `Currency`: state aktual berdasarkan profil terakhir dan kejadian/transaksi tercatat.
- `Teknik / Kemampuan`: kemampuan serta rincian Spirit Ring yang dimiliki, dengan fungsi jelas dan sumber yang sah.
- `Tujuan Saat Ini`: tujuan karakter yang dinyatakan pemain atau sudah tercatat; jangan mengambil alih keputusan pemain.

## Aturan Pengisian

- Jangan menambah field terpisah untuk **Spirit Rings** atau **Law** tanpa persetujuan pemilik. Jumlah slot mengikuti Realm; rincian ring masuk ke **Teknik / Kemampuan** atau deskripsi Martial Soul.
- Gunakan profil gameplay terakhir ditambah kejadian yang benar-benar terjadi. Jangan menganggap HP penuh, mengisi ulang sumber daya, mengubah saldo, atau menghapus konsekuensi tanpa sebab yang sah.
- Estimasi praktis untuk karakter baru hanya boleh digunakan bila wajar dan harus diberi label estimasi GM. Jangan mengarang rahasia besar, garis keturunan, artefak langka, atau teknik formal.
- Gunakan `???` untuk fakta yang belum diketahui atau tidak dapat ditetapkan secara bertanggung jawab. Jangan mengganti ketidakpastian dengan tebakan.
- HP dan injury adalah state terpisah: `core/HP_SYSTEM.md` mengatur HP, sedangkan `core/INJURY_SYSTEM.md` mengatur klasifikasi dan progres pemulihan cedera.
- Satiety dan metabolisme hanya mengikuti `core/HUNGER_AND_METABOLISM.md`. Tidur malam yang dilindungi mengunci Satiety, tetapi tidak otomatis memulihkan HP, Qi, atau injury.
- Profil adalah snapshot state setelah giliran, bukan pengganti narasi kejadian atau riwayat transaksi.

## Perhitungan Day left

- Gunakan selisih waktu dunia yang tercatat, bukan jumlah giliran atau waktu nyata.
- Bulatkan sisa durasi positif ke atas dalam satuan 24 jam: 1 jam tersisa = `1 Day left`, 24 jam = `1 Day left`, 25 jam = `2 Day left`. Ini hitung mundur durasi, bukan hitungan pergantian tanggal kalender.
- Tulis `0 Day left` hanya ketika jeda minimum benar-benar terpenuhi. Nilai nol bukan jaminan breakthrough atau penyerapan ring sah/berhasil.
- Jika timestamp, jumlah ring, atau riwayat penyerapan tidak diketahui atau bertentangan, gunakan `??? Day left`.
- Hitung ulang hanya ketika timestamp dunia atau informasi riwayat yang sah berubah. Pergantian giliran saja tidak mengurangi nilai.
