# Xuanling Realm — Character Profile Template

Gunakan template ini untuk profil karakter gameplay. Pertahankan nama field dan urutannya. Jangan menambah field baru tanpa persetujuan pemilik repository.

## Profil Karakter

- **Nama:** ???
- **Usia:** ???
- **Spirit Realm:** ???/???
- **Sync progress:** ???%/???%
- **Martial Soul:** ???
- **Thinker Grade:** ???
- **HP:** ???/???
- **Qi:** ...
- **Kondisi Tubuh:** ???
- **Equipment:** ???
- **Inventory:** ???
- **Assets:** ???
- **Currency (xuan/zun):** ...xc | ...xs | ...xg | ...zj | ...az
- **Teknik / Kemampuan:** ???
- **Tujuan Saat Ini:** ???

## Format Field Wajib

1. **Spirit Realm:** gunakan `Nama Realm/angka Stage`, dengan Stage numerik: `1` = Early, `2` = Middle, `3` = Late, `4` = Peak. Contoh: `Spirit Ancestor/2`. Mortal tidak memiliki Stage kultivasi dan ditulis `Mortal/0`. Jika Realm atau Stage belum diketahui, gunakan `???/???`.
2. **HP:** gunakan `HP saat ini/HP maksimum`. Contoh Mortal penuh: `100/100`; Spirit Primordial/4 penuh: `8950/8950`. Gunakan `???/maksimum` jika HP saat ini tidak diketahui tetapi Realm/Stage diketahui. Gunakan `???/???` jika Realm/Stage juga tidak diketahui. HP maksimum wajib mengikuti `core/HP_SYSTEM.md`; jangan otomatis mengisi HP saat ini dengan nilai maksimum.
3. **Qi:** jika karakter belum menyerap Spirit Ring pertama, tulis tepat `...`. Setelah ring pertama berhasil diserap, gunakan `Qi saat ini/Qi maksimum`; Qi maksimum dasar mengikuti jumlah ring pada `core/SPIRIT_RING_RULES.md`. Jika jumlah ring diketahui tetapi Qi saat ini tidak diketahui, gunakan `???/Qi maksimum`. Jangan mengarang nilai saat ini.
4. **Sync progress:** gunakan format `progres saat ini%/batas kompatibilitas maksimum%`, misalnya `Sync progress: 0%/78%` hanya jika 78% adalah batas resmi ring karakter tersebut. Batas tiap ring dapat berbeda dan tidak otomatis 100%. Jika nilai belum diketahui, gunakan `???%/???%` tanpa mengarang.
6. **Thinker Grade:** gunakan angka Grade 1–10 sesuai modul Thinker; jika belum diketahui, `???`.

## Aturan Pengisian

1. Jangan membiarkan field kosong. Gunakan penanda `???`, `???/???`, atau `...` sesuai aturan format di atas.
2. Gunakan `???` untuk informasi yang belum diketahui atau belum tercatat. Untuk Qi sebelum Spirit Ring pertama, gunakan `...` sesuai format khusus Qi.
3. Jangan menganggap Martial Soul belum awakening hanya karena karakter berstatus Mortal, kecuali hal itu dinyatakan pemain atau ditetapkan riwayat.
4. Jangan menambahkan field terpisah bernama Law atau Spirit Rings. Catat rincian ring dalam **Teknik / Kemampuan** atau deskripsi **Martial Soul**.
5. Jangan menciptakan nilai HP, Qi saat ini, uang, item, statistik, atau sumber daya. Terapkan hanya rumus dan sumber resmi yang tersedia. Saldo uang wajib dicatat pada field **Currency (xuan/zun)** dalam format persis seperti pada template. Kepanjangan singkatan mata uang hanya didefinisikan di `core/10_ECONOMY_SYSTEM.md`, bukan di template.
6. HP maksimum wajib dihitung dari `core/HP_SYSTEM.md`; perubahan Realm/Stage tidak memulihkan HP saat ini secara otomatis.
7. Pertahankan semua perubahan profil yang didukung kejadian dalam gameplay. Jangan menghapus luka, pengeluaran, barang, atau konsekuensi tanpa alasan sah.
