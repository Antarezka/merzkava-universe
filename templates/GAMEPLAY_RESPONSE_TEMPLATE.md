# Merzkava Universe — Canonical Gameplay Response Template

Status: **Template visual resmi dan wajib untuk setiap balasan gameplay. Gunakan susunan, urutan, ornamen, pembatas, nama field, dan footer di bawah ini persis; ganti placeholder dengan data gameplay yang terverifikasi.**

## Aturan Kepatuhan Wajib

- **GERBANG IDENTITAS HASH/VER — WAJIB, TANPA FALLBACK:** mulai dari `INDEX.md` pada SHA/commit yang tercantum di URL pemanggilan gameplay; jika URL menunjuk `main`, kunci commit yang benar-benar dipakai untuk membaca INDEX. Setelah itu baca `templates/AUTHORITY_ORDER.md`, lalu template, state, dan modul relevan dari `ACTIVE_SHA` yang sama. Jangan membaca `README.md` sebagai pintu masuk gameplay atau sumber Hash. `Hash` = tujuh karakter pertama `ACTIVE_SHA`. `Ver` hanya boleh diambil dari nilai `Current Nightly version` di `NIGHTLY_VERSION.md` pada snapshot yang sama. Jika `NIGHTLY_VERSION.md` tidak tersedia atau snapshot tidak konsisten, hentikan bootstrap dan laporkan sumber yang gagal; jangan menebak atau memakai fallback. README hanya digunakan untuk tugas pemeliharaan/update pin.
- **Pembagian kerja dua file pengendali:** `INDEX.md` menentukan urutan bootstrap, state awal/lanjutan, pemetaan kebutuhan ke modul, dan jalur masuk canon; `templates/AUTHORITY_ORDER.md` menentukan bagaimana GM memilih otoritas, menyelesaikan aksi, menjaga state, dan mencatat perubahan. Gunakan keduanya bersama-sama: INDEX memberi tahu *apa yang harus dibuka*, Authority Order memberi tahu *bagaimana keputusan dibuat*. Jangan mengganti isi file dengan ingatan, ringkasan chat, atau asumsi. Jika keduanya tampak bertentangan, periksa `world/CANON_DECISIONS_AND_PRECEDENCE.md` pada snapshot yang sama untuk konflik canon; jangan diam-diam mengabaikan salah satu file pengendali.
- Setelah alur bootstrap, periksa `world/DYNAMIC_EVENTS.md` pada snapshot yang sama setiap giliran. Gunakan tabel kebutuhan di `INDEX.md` untuk memilih modul berdasarkan aksi, lokasi, waktu, dan kondisi; ikuti prosedur resolusi pada `templates/AUTHORITY_ORDER.md`. Baca semua sumber terkait yang dapat mengubah hasil, tetapi jangan memuat arsip yang tidak relevan.
- **Telusuri dependensi sampai keputusan dapat dipertanggungjawabkan:** ketika sebuah sumber `world/` merujuk sumber canon lain, ikuti rujukan itu sejauh dapat memengaruhi lokasi, identitas, hubungan, ekonomi, sejarah, rute, NPC, faksi, atau konsekuensi. Gunakan `world/CANON_LOAD_ROUTER.md` untuk memilih jalur regional/NPC dan `world/CANON_DECISIONS_AND_PRECEDENCE.md` untuk menyelesaikan konflik. Misalnya, perjalanan dapat membutuhkan jaringan rute, geografi, serta sumber wilayah asal/tujuan; NPC dapat membutuhkan registry/profil, faksi, dan canon wilayah; dampak lintas sesi membutuhkan `world/DYNAMIC_EVENTS.md`. Jangan berhenti pada satu cuplikan bila dependensi yang dirujuk bisa mengubah hasil, tetapi jangan membaca semua file tanpa alasan.
- Jika sumber wajib tidak dapat diakses, sebutkan path yang gagal dan batasi resolusi pada fakta yang masih terverifikasi. Jangan mengarang isi sumber atau menyatakan pemeriksaan selesai.
- Template ini adalah **kerangka output**, bukan contoh opsional. Setiap giliran gameplay—termasuk respons pertama, recall, adegan dialog singkat, dan giliran tanpa perubahan state—wajib memuat header waktu, pembatas pembuka, narasi, seluruh bagan profil, seluruh bagan inventaris/keuangan, seluruh bagan teknik/tujuan, catatan konsistensi, dan footer pemain.
- **Dilarang mengirim narasi bebas saja.** Jangan menghilangkan bagan karena nilainya tidak berubah, informasinya sederhana, atau tidak ada aksi pemain yang eksplisit.
- Ganti setiap placeholder dengan state terverifikasi. Jangan menampilkan instruksi dalam tanda kurung siku sebagai isi respons final. Jika nilai belum diketahui, gunakan default resmi dari `templates/CHARACTER_PROFILE_TEMPLATE.md`; jangan menghapus field atau mengarang nilai.
- Field `Spirit Ring Absorption` wajib memakai status tahap kanonis dari `templates/CHARACTER_PROFILE_TEMPLATE.md` dengan format `status | Day left`. Mortal yang belum menjalani Awakening wajib ditampilkan sebagai `not eligible yet | ??? Day left`, bukan `Tidak ada | 0 Day left`.
- `Wallet (wealth)` wajib selalu memakai urutan persis `xc | xs | xg | zj | az`. Salin nominal tiap denominasi dari state aktif tanpa menukar posisi atau mengubah saldo.
- Untuk item yang identitas, jenis pasti, atau detail relevannya belum ditetapkan oleh kanon/GM, gunakan label persis `*Unknown* *membutuhkan appraisal untuk lebih pastinya*` pada Inventory, Equipment, loot, transaksi, dan deskripsi item yang ditampilkan ke pemain. Jangan gunakan `???` untuk label item atau mengarang nilai, tier, fungsi, kelangkaan, maupun bahaya. Appraisal hanya memperbarui fakta yang benar-benar ditetapkan oleh hasilnya.
- `LEDGER LOG` adalah satu-satunya blok visual kondisional. Tampilkan hanya jika ada perubahan state yang memenuhi aturan ledger. Jika tidak ada perubahan relevan, hilangkan blok ledger dan pembatas ledger saja—**jangan pernah menghilangkan bagan profil atau bagian visual lain**.
- **Validasi header sebelum kirim:** cocokkan `Hash` dengan 7 karakter awal SHA aktif dan `Ver` dengan `Nightly-` + nilai `Current Nightly version` persis dari `NIGHTLY_VERSION.md`, termasuk awalan `v`. Bungkus nilai Hash dan Ver dengan dua backtick. Jika salah satu tidak cocok atau belum terverifikasi, jangan kirim gameplay; laporkan sumber yang gagal.
- Sebelum mengirim, jalankan dua pemeriksaan berbeda: **(a) validasi keputusan** menurut `templates/AUTHORITY_ORDER.md`—aksi, waktu, syarat, sumber daya, pengetahuan karakter, dan perubahan state didukung sumber; **(b) validasi tampilan** menurut template ini—identitas Hash/Ver, header sampai footer lengkap, urutan/field/ornamen tetap, dan hanya `LEDGER LOG` yang boleh kondisional. Jika salah satu gagal, perbaiki sebelum mengirim. Jangan menampilkan laporan bootstrap atau daftar file yang dibaca sebagai pengganti adegan gameplay.
- Pisahkan pengetahuan GM dan karakter. Jangan membocorkan catatan GM, potensi tersembunyi, asal-usul misterius, atau kemampuan yang belum disadari sebagai fakta terbuka. Narasikan gejala yang benar-benar dapat diamati sampai karakter memiliki dasar sah untuk memahaminya.

```text
༺━━━━━━━━━━━━━━━━༻
Hash: ``<short SHA snapshot>`` | Ver: ``Nightly–<versi Nightly terverifikasi>``
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

[Jika Satiety, uang, item, equipment, loot, atau aset benar-benar berubah, laporkan perubahan terverifikasi dan akhiri kalimat laporan perubahan dengan `Log tercatat!`. Gunakan satu ledger gabungan untuk satu rangkaian aksi. Jangan membuat laporan atau ledger untuk perubahan yang tidak terjadi.]

╭─ LEDGER LOG · #[ID]
│ Peristiwa/Aksi: [Aksi atau peristiwa yang menghasilkan perubahan]
│ Pihak: [Karakter/NPC/pihak yang terlibat, jika relevan]
│ Penyebab: [Alasan sah perubahan]
│ [Waktu] · [Berhasil/Gagal/Dibatalkan]
│ Item/Equipment/Loot/Aset: [Perubahan yang terjadi → keadaan akhir, jika relevan]
│ Uang: [Saldo awal] → [Perubahan bersih] → [Saldo akhir, jika berubah]
│ Satiety: [Awal] → [Perubahan] → [Akhir, jika berubah]
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
