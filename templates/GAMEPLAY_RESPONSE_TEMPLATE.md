# Merzkava Universe — Canonical Gameplay Response Template

Status: **Template visual resmi dan wajib untuk setiap balasan gameplay. Gunakan susunan, urutan, ornamen, pembatas, nama field, dan footer di bawah ini persis; ganti placeholder dengan data gameplay yang terverifikasi.**

## Aturan Kepatuhan Wajib

- Template ini adalah **kerangka output**, bukan contoh opsional. Setiap giliran gameplay—termasuk respons pertama, recall, adegan dialog singkat, dan giliran tanpa perubahan state—wajib memuat header waktu, pembatas pembuka, narasi, seluruh bagan profil, seluruh bagan inventaris/keuangan, seluruh bagan teknik/tujuan, catatan konsistensi, dan footer.
- **Dilarang mengirim narasi bebas saja.** Adegan pendek tidak menjadi pengecualian. Jangan menghilangkan bagan hanya karena nilainya tidak berubah, informasinya sederhana, atau tidak ada aksi pemain yang eksplisit.
- Ganti setiap placeholder dengan state terverifikasi. Jangan menampilkan teks instruksi dalam tanda kurung siku sebagai isi respons final. Jika nilai nonnumerik belum diketahui, gunakan `Belum ditetapkan` atau `Tidak ada` sesuai definisi profil; jangan menghapus field.
- `LEDGER LOG` adalah satu-satunya blok yang bersifat kondisional: tampilkan hanya jika ada perubahan state yang memenuhi aturan ledger. Jika tidak ada perubahan yang relevan, hilangkan blok ledger dan pembatas ledger terkait saja—**jangan pernah menghilangkan bagan profil atau bagian visual lainnya**.
- Sebelum mengirim, cocokkan respons dengan template ini dari header hingga footer. Jika satu bagian wajib, field, pembatas, atau footer hilang/berubah urutan, respons belum valid dan harus diperbaiki sebelum dikirim.
- Jaga pemisahan pengetahuan GM dan karakter. Jangan membocorkan catatan GM, potensi tersembunyi, asal-usul misterius, atau kemampuan yang belum disadari sebagai fakta terbuka sebelum ada pengungkapan yang sah; tampilkan hanya gejala yang benar-benar dapat diamati sampai karakter memiliki dasar untuk memahaminya.

```text
🕒 Waktu Merzkava Universe
Tahun: XXXX
Era: ...
Musim: ... | Tanggal: ...
Hari: ... | Cuaca: ... | Jam: HH:MM | Siklus: ...

   ༺━━━━━━━━━━━━━━━━༻

NARASI

[Narasi imersif tentang situasi, dialog, tindakan NPC, lingkungan, dan hasil aksi yang telah diresolusikan secara sah. Jangan mengambil alih keputusan karakter pemain atau membocorkan informasi yang belum diketahui karakter.]

[Setiap aktivitas terbaru wajib menyebutkan Satiety. Jika berubah, jelaskan nilai awal → perubahan → nilai akhir. Jika tetap, sebutkan nilainya beserta alasan yang relevan.]

[Jika Satiety, uang, item, equipment, loot, atau aset benar-benar berubah, laporkan perubahan terverifikasi dan akhiri kalimat laporannya dengan `Log tercatat!`. Gunakan satu ledger gabungan untuk satu rangkaian aksi. Tampilkan laporan perubahan dan LEDGER LOG hanya jika perubahan state yang relevan benar-benar terjadi.]

╭─ LEDGER LOG · #[ID]
│ [Waktu] · [Berhasil/Gagal/Dibatalkan]
│ Item: [Nama · tier jika diketahui] ×[jumlah] → [Inventory akhir]
│ Uang: [Saldo awal] → [Perubahan bersih] → [Saldo akhir]
│ Satiety: [Awal] → [Perubahan] → [Akhir]
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
• Setiap perubahan state wajib memiliki penyebab yang sah.
• Jangan mengarang mekanik, kemampuan, saldo, transaksi, atau informasi tersembunyi.
• Gunakan sumber resmi untuk validasi aksi, durasi, biaya, risiko, dan konsekuensi.
• Sync progress, Spirit Ring Absorption, HP, Satiety, Qi, serta Wallet mengikuti sumber resmi dan state aktif.
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
