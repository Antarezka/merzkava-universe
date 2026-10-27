# Merzkava Universe — Canonical Gameplay Response Template

Status: **Template visual resmi dan wajib untuk setiap balasan gameplay. Gunakan susunan, urutan, ornamen, pembatas, nama field, dan footer di bawah ini persis; ganti placeholder dengan data gameplay yang terverifikasi.**

## Aturan Kepatuhan Wajib

- **Alur otoritas wajib sebelum setiap giliran:** baca `INDEX.md` → `templates/AUTHORITY_ORDER.md` → template, profil aktif, dan sumber canon yang relevan. Jangan melewati INDEX atau Authority Order, termasuk saat recall, dialog singkat, atau aksi sederhana.
- Gunakan snapshot canon yang ditetapkan oleh prosedur bootstrap di `INDEX.md` dan `templates/AUTHORITY_ORDER.md`. Jangan mencampur snapshot pin dengan `main`, jangan mengganti sumber dengan ingatan/ringkasan, dan jangan mengaku membaca file yang gagal diakses.
- Periksa `world/DYNAMIC_EVENTS.md` setiap giliran. Baca modul tambahan berdasarkan aksi, lokasi, dan konteks yang benar-benar relevan.
- **Keterhubungan sumber world wajib:** saat memanggil atau memakai satu sumber `world/`, telusuri rujukan silang dan dependensi canon yang dapat mengubah jawaban. Gunakan `world/CANON_LOAD_ROUTER.md` untuk jalur regional/NPC dan `world/CANON_DECISIONS_AND_PRECEDENCE.md` untuk konflik canon. Contoh: perjalanan memerlukan peta jaringan rute, geografi, dan modul wilayah asal/tujuan; NPC dapat memerlukan registry, profil, faksi, dan sumber wilayah; dampak persisten memerlukan pemeriksaan dynamic events. Jangan menganggap satu file cukup bila sumber terkait berpengaruh.
- Jika sumber wajib tidak dapat diakses, sebutkan path yang gagal dan batasi resolusi pada fakta yang masih terverifikasi. Jangan mengarang isi sumber atau menyatakan pemeriksaan selesai.
- Template ini adalah **kerangka output**, bukan contoh opsional. Setiap giliran gameplay—termasuk respons pertama, recall, adegan dialog singkat, dan giliran tanpa perubahan state—wajib memuat header waktu, pembatas pembuka, narasi, seluruh bagan profil, seluruh bagan inventaris/keuangan, seluruh bagan teknik/tujuan, catatan konsistensi, dan footer pemain.
- **Dilarang mengirim narasi bebas saja.** Jangan menghilangkan bagan karena nilainya tidak berubah, informasinya sederhana, atau tidak ada aksi pemain yang eksplisit.
- Ganti setiap placeholder dengan state terverifikasi. Jangan menampilkan instruksi dalam tanda kurung siku sebagai isi respons final. Jika nilai belum diketahui, gunakan default resmi dari `templates/CHARACTER_PROFILE_TEMPLATE.md`; jangan menghapus field atau mengarang nilai.
- Field `Spirit Ring Absorption` wajib memakai status tahap kanonis dari `templates/CHARACTER_PROFILE_TEMPLATE.md` dengan format `status | Day left`. Mortal yang belum menjalani Awakening wajib ditampilkan sebagai `not eligible yet | ??? Day left`, bukan `Tidak ada | 0 Day left`.
- `Wallet (wealth)` wajib selalu memakai urutan persis `xc | xs | xg | zj | az`. Salin nominal tiap denominasi dari state aktif tanpa menukar posisi atau mengubah saldo.
- `LEDGER LOG` adalah satu-satunya blok visual kondisional. Tampilkan hanya jika ada perubahan state yang memenuhi aturan ledger. Jika tidak ada perubahan relevan, hilangkan blok ledger dan pembatas ledger saja—**jangan pernah menghilangkan bagan profil atau bagian visual lain**.
- Sebelum mengirim, cocokkan respons dari header sampai footer. Jika bagian wajib, field, pembatas, atau urutan hilang/berubah, perbaiki dahulu sebelum mengirim.
- Pisahkan pengetahuan GM dan karakter. Jangan membocorkan catatan GM, potensi tersembunyi, asal-usul misterius, atau kemampuan yang belum disadari sebagai fakta terbuka. Narasikan gejala yang benar-benar dapat diamati sampai karakter memiliki dasar sah untuk memahaminya.

```text
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
