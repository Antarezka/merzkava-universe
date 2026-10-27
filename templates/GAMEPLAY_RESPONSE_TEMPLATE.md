# Merzkava Universe — Canonical Gameplay Response Template

Status: **Template visual resmi dan wajib untuk setiap balasan gameplay. Gunakan susunan, urutan, ornamen, pembatas, nama field, dan footer di bawah ini persis; ganti placeholder dengan data gameplay yang terverifikasi.**

## Aturan Kepatuhan Wajib

- **Sumber dan snapshot:** ikuti bootstrap `INDEX.md` §0 dan prosedur keputusan `templates/AUTHORITY_ORDER.md`. Seluruh file yang digunakan dalam satu giliran harus berasal dari `ACTIVE_SHA` yang sama. Jangan memakai `README.md` sebagai sumber gameplay atau fallback untuk Hash/Ver. Jika sumber wajib tidak tersedia atau versi snapshot tidak dapat diverifikasi, hentikan resolusi dan sebutkan path yang gagal.
- **Pemilihan modul dan dependensi:** gunakan tabel domain di `INDEX.md`; periksa `world/DYNAMIC_EVENTS.md` setiap giliran dan ikuti rujukan canon yang dapat mengubah hasil. Router regional/NPC dimiliki `world/CANON_LOAD_ROUTER.md`; konflik dan kepemilikan canon mengikuti `world/CANON_DECISIONS_AND_PRECEDENCE.md`. Muat hanya dependensi relevan, tetapi jangan berhenti pada cuplikan yang belum cukup untuk memutuskan hasil.
- Jika sumber wajib tidak dapat diakses, sebutkan path yang gagal dan batasi resolusi pada fakta yang masih terverifikasi. Jangan mengarang isi sumber atau menyatakan pemeriksaan selesai.
- Template ini adalah **kerangka output**, bukan contoh opsional. Setiap giliran gameplay—termasuk respons pertama, recall, adegan dialog singkat, dan giliran tanpa perubahan state—wajib memuat header waktu, pembatas pembuka, narasi, seluruh bagan profil, seluruh bagan inventaris/keuangan, seluruh bagan teknik/tujuan, catatan konsistensi, dan footer pemain.
- **Dilarang mengirim narasi bebas saja.** Jangan menghilangkan bagan karena nilainya tidak berubah, informasinya sederhana, atau tidak ada aksi pemain yang eksplisit.
- Ganti setiap placeholder dengan state terverifikasi. Jangan menampilkan instruksi dalam tanda kurung siku sebagai isi respons final. Jika nilai belum diketahui, gunakan default resmi dari `templates/CHARACTER_PROFILE_TEMPLATE.md`; jangan menghapus field atau mengarang nilai.
- Field `Spirit Ring Absorption` wajib memakai status tahap kanonis dari `templates/CHARACTER_PROFILE_TEMPLATE.md` dengan format `status | Day left`. Mortal yang belum menjalani Awakening wajib ditampilkan sebagai `not eligible yet | ??? Day left`, bukan `Tidak ada | 0 Day left`.
- `Wallet (wealth)` wajib selalu memakai urutan persis `xc | xs | xg | zj | az`. Salin nominal tiap denominasi dari state aktif tanpa menukar posisi atau mengubah saldo.
- Untuk item yang identitas, jenis pasti, atau detail relevannya belum ditetapkan oleh kanon/GM, gunakan label persis ```Unknown`` *membutuhkan appraisal untuk lebih pastinya*` pada Inventory, Equipment, loot, transaksi, dan deskripsi item yang ditampilkan ke pemain. Jangan gunakan `???` untuk label item atau mengarang nilai, tier, fungsi, kelangkaan, maupun bahaya. Appraisal hanya memperbarui fakta yang benar-benar ditetapkan oleh hasilnya.
- `LEDGER LOG` adalah satu-satunya blok visual kondisional. Untuk perubahan state terverifikasi, narasikan transaksi secara natural, sertakan penanda inline `🝰 MASUK/KELUAR` dan atribut relevan `⧟`, akhiri laporan dengan inline-code `Log tercatat!` tepat satu kali, lalu tampilkan satu ledger gabungan sebelum profil. Jika tidak ada perubahan relevan, hilangkan penanda dan ledger—**jangan pernah menghilangkan bagan profil atau bagian visual lain**.
- **Validasi header sebelum kirim:** cocokkan `Hash` dengan 7 karakter awal SHA aktif dan `Ver` dengan `Nightly-` + nilai `Current Nightly version` persis dari `NIGHTLY_VERSION.md`, termasuk awalan `v`. Bungkus nilai Hash dan Ver dengan dua backtick. Jika salah satu tidak cocok atau belum terverifikasi, jangan kirim gameplay; laporkan sumber yang gagal.
- Sebelum mengirim, jalankan dua pemeriksaan berbeda: **(a) validasi keputusan** menurut `templates/AUTHORITY_ORDER.md`—aksi, waktu, syarat, sumber daya, pengetahuan karakter, dan perubahan state didukung sumber; **(b) validasi tampilan** menurut template ini—identitas Hash/Ver, header sampai footer lengkap, urutan/field/ornamen tetap, dan hanya `LEDGER LOG` yang boleh kondisional. Jika salah satu gagal, perbaiki sebelum mengirim. Jangan menampilkan laporan bootstrap atau daftar file yang dibaca sebagai pengganti adegan gameplay.
- Pisahkan pengetahuan GM dan karakter. Jangan membocorkan catatan GM, potensi tersembunyi, asal-usul misterius, atau kemampuan yang belum disadari sebagai fakta terbuka. Narasikan gejala yang benar-benar dapat diamati sampai karakter memiliki dasar sah untuk memahaminya.

```text
༺━━━━━━━━━━━━━━━━༻
Hash: ``<short SHA snapshot>`` | Ver: ``Nightly-<versi Nightly terverifikasi>``
༺━━━━━━━━━━━━━━━━༻

🕒 Waktu Merzkava Universe
Tahun: XXXX
Era: ...
Musim: ... | Tanggal: ...
Hari: ... | Cuaca: ... | Jam: HH:MM | Siklus: ...

   ༺━━━━━━━━━━━━━━━━༻

NARASI

[Narasi imersif tentang situasi, dialog, tindakan NPC, lingkungan, dan hasil aksi yang diresolusikan secara sah. Jangan mengambil alih keputusan karakter pemain atau membocorkan informasi yang belum diketahui karakter.]

[Setiap aktivitas terbaru wajib menyebutkan Satiety. Jika berubah, jelaskan nilai awal → perubahan → nilai akhir. Jika tetap, sebutkan nilainya beserta alasan yang relevan.]

[Narasi tetap imersif walau player Converse secara pasif: tampilkan suasana yang relevan, percakapan/tindakan NPC aktif sesuai pengetahuan dan agenda mereka, serta aktivitas sekitar yang didukung canon, wilayah, dan waktu. Jangan memaksa kejadian atau mengambil alih karakter pemain.]

[Jika uang, item, equipment, loot, aset, atau Satiety benar-benar berubah, narasikan kejadian secara natural dengan nilai sebelum → perubahan → sesudah. Untuk item/uang, gunakan penanda inline **🝰 MASUK/KELUAR · [item/uang + jumlah]** ``⧟ [tier/grade/rarity/quality/``Unknown`` jika relevan]`` sesuai arah perubahan; gunakan label ``Unknown`` resmi bila identitas item belum ditetapkan. Akhiri laporan terverifikasi dengan **`Log tercatat!`** tepat satu kali, lalu tampilkan satu ledger gabungan. Jangan membuat penanda atau ledger untuk perubahan yang tidak terjadi.]

╭─ LEDGER LOG · #[ID]
│ Peristiwa/Aksi: [aksi/peristiwa penyebab perubahan]
│ [Waktu] · [Berhasil/Gagal/Dibatalkan]
│ 🝰 Item/Equipment/Loot/Aset: [MASUK/KELUAR · nama · ×jumlah · ⧟ tier/grade/rarity/quality/``Unknown`` jika relevan · awal → perubahan → akhir]
│ 🝰 Uang: [MASUK/KELUAR · sumber/penerima · jumlah · saldo awal → perubahan bersih → saldo akhir · kembalian jika ada]
│ Satiety: [awal → ±perubahan → akhir · penyebab/kategori/durasi jika relevan]
╰─

━━━━━━━━━━━━━━━━━━━━━━━━

╱━━━━━━━━━━━━━━━━━━━━━━╲
◈━━┫ PROFIL KARAKTER ┣━━◈
╲━━━━━━━━━━━━━━━━━━━━━━╱

Nama: ...
Usia: ...
Spirit Realm: ...
Sync progress: ...%/...%
Spirit Ring Absorption: ... | ... Day left
Martial Soul: ...
Thinker Grade: ...
HP: .../...
Satiety: .../100
Qi: ...
Kondisi Tubuh: ...
Equipment: ...

━━━━━━━━━━━━━━━━━━━━━━━━

╱━━━━━━━━━━━━━━━━━━━━━━╲
◈━━┫ INV & KEUANGAN ┣━━◈
╲━━━━━━━━━━━━━━━━━━━━━━╱

Inventory: ...
Assets Bangunan: ...
Wallet (wealth): ... xc | ... xs | ... xg | ... zj | ... az

━━━━━━━━━━━━━━━━━━━━━━━━

╱━━━━━━━━━━━━━━━━━━━━╲
◈━━┫ TEKNIK & TUJUAN ┣━━◈
╲━━━━━━━━━━━━━━━━━━━━╱

Teknik / Kemampuan: ...
Tujuan Saat Ini: ...

━━━━━━━━━━━━━━━━━━━━━━━━

╱━━━━━━━━━━━━━━━━━━━━━━╲
◈━━┫ CATATAN PEMAIN & KONSISTENSI ┣━━◈
╲━━━━━━━━━━━━━━━━━━━━━━╱

• Profil mengikuti state gameplay terakhir dan kejadian sah setelahnya.
• Setiap perubahan state wajib memiliki penyebab yang sah dan dapat ditelusuri.
• Jangan mengarang mekanik, kemampuan, saldo, transaksi, kepemilikan, atau informasi tersembunyi.
• Gunakan sumber resmi untuk validasi aksi, durasi, biaya, risiko, dan konsekuensi.
• Sync progress, Spirit Ring Absorption, HP, Satiety, Qi, Equipment, Inventory, Assets Bangunan, serta Wallet mengikuti sumber resmi dan state aktif.
• Jika tidak ada Spirit Ring yang sedang diproses, gunakan Sync progress 0%/0%.
• `Day left = 0` bukan jaminan penyerapan berhasil.
• Siklus waktu memakai label singkat: Dini hari, Subuh, Pagi, Siang, Sore, atau Malam. Tentukan berdasarkan waktu dunia yang tercatat; jangan mengarang jam batas jika sumber resmi belum menetapkannya.
• Tampilkan `Log tercatat!` dan LEDGER LOG hanya jika perubahan state yang relevan benar-benar terjadi.
• Pada footer, gunakan padanan singkat “Tentukan Aksimu” dalam bahasa yang digunakan pemain; jangan tampilkan instruksi ini sebagai teks footer.
• Jangan mengklaim perubahan tersimpan ke GitHub jika belum dilakukan dan diverifikasi.

✦ Enjoy your convo, player! ✦
━━━━━━━━━━━━━━━━━━━━━━━━
•••_@GM_Authority: Tentukan Aksimu (⁠｡⁠•̀⁠ᴗ⁠-⁠)⁠✧
```
