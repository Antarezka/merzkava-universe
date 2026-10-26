# Merzkava Universe — Spirit Beast Rules

Status: Modul mekanik resmi.
Cakupan: kategori Beast, Spirit Beast, Demonic Beast, Heavenly Beast, perilaku, persyaratan penyerapan Spirit Ring, dan item khusus.

## 1. Kategori dan Sumber

Gunakan kategori Beast yang ditetapkan lore resmi. Jangan menciptakan tier atau kemampuan khusus sebagai canon tanpa dasar yang disahkan.

Setelah Spirit Beast dikalahkan, Spirit Ring dapat muncul mengambang di atas tubuhnya. Kekalahan Beast tidak membuat ring otomatis berhasil diserap. Penyerapan harus diselesaikan sesuai `core/SPIRIT_RING_RULES.md`.

## 1.1 Estimating Hunt Danger Without Invented Odds

When preparing a Spirit Beast hunt, the GM should estimate danger from the evidence available rather than assign an invented universal encounter percentage or difficulty score.

- **Habitat and access:** use the known regional module and `world/GEOGRAPHY_AND_TRAVEL.md`. Deep or hard-to-reach wilderness tends to contain higher-tier Spirit Beasts, but this is not a guarantee. Do not assume every forest has the same population or threat.
- **Target evidence:** distinguish confirmed species/age/tier from a report, rumor, track, or unverified sighting. A clue may be incomplete or misleading; do not turn uncertain information into a confirmed stat.
- **Party readiness:** compare the actual abilities, PowerScale, Qi, equipment, readiness, injuries, terrain, and coordination of the hunters with the target's established capabilities. Apply `gameplay/COMBAT_SYSTEM.md` for combat outcomes. The existence of a team is not itself a numeric bonus.
- **Route context:** an academy Safe Route should be selected to reduce avoidable danger for the group's demonstrated readiness, but it may still contain hazards or unexpected encounters. A Guild party can have uneven experience or hidden motives. A solo hunter has no team support or guaranteed rescue, but the actual risk still depends on their capability and preparation.
- **No automatic success:** hunting, defeating the Beast, securing the ring, and absorbing it are separate stages. Do not grant a guaranteed encounter, victory, ring ownership, or absorption.
- **No made-up odds:** if the available facts do not support a numeric chance, resolve the situation qualitatively or use the existing combat formula when a combat comparison is possible. Do not invent a new encounter chance, success percentage, age cap, or danger multiplier.

## 2. Persyaratan Item untuk Breakthrough

Persyaratan item pada bagian ini berlaku sebagai syarat breakthrough untuk menyerap Spirit Ring berikutnya, bukan syarat tambahan untuk kelayakan Mortal menyerap Spirit Ring pertama. Mortal dapat mencoba menyerap ring pertama setelah Awakening Martial Soul; ring harus tersedia melalui proses yang sah.

- Persyaratan item breakthrough bergantung pada Beast target dan sebaiknya dicatat pada entri Beast yang relevan ketika telah ditetapkan.
- Jika item wajib spesifik untuk Beast target belum tercatat, GM **wajib menetapkan requirement sementara untuk breakthrough agar dapat menyerap Spirit Ring target tersebut** berdasarkan dua hal: (1) tier/usia Spirit Ring yang hendak diperoleh, dan (2) jenis serta karakteristik Spirit Beast target. Jangan membiarkan requirement breakthrough kosong, jangan menganggap tidak ada syarat, dan jangan meminta keputusan pemilik hanya karena entri Beast belum lengkap.
- Pilih bahan atau item yang masuk akal dan relevan dengan jenis Beast serta tingkat ringnya; gunakan bahan/lore yang sudah ada bila tersedia. Semakin tinggi tier/usia ring dan semakin langka atau berbahaya karakteristik Beast, requirement harus mencerminkan kesulitan dan kelangkaan yang sepadan. Jangan menetapkan item yang tidak berkaitan hanya untuk menghalangi pemain.
- Nyatakan item yang dibutuhkan secara konkret, lalu perlakukan sebagai syarat wajib breakthrough untuk menyerap ring target itu. Requirement yang dibuat untuk menutup data yang kosong berlaku sebagai keputusan GM pada proses tersebut, bukan otomatis menjadi fakta permanen untuk semua Beast sejenis. Catat pada hasil/profil sesi; jadikan data kanon permanen hanya jika pemilik kemudian menyetujuinya.
- Item wajib breakthrough harus benar-benar dimiliki atau diperoleh melalui proses sah sebelum breakthrough yang mensyaratkannya dapat dilakukan. Untuk ring pertama, Mortal hanya perlu telah Awakening dan ring harus tersedia melalui proses yang sah; jangan menerapkan syarat breakthrough atau jeda antar-ring.
- Item yang dikonsumsi atau rusak selama proses harus dicatat sebagai konsekuensi hanya jika aturan atau kejadian yang sah menetapkannya.
- Mengalahkan Beast, memiliki ring yang muncul, atau mencapai bottleneck tidak menggantikan persyaratan item.

## Status Kanonis Spirit Ring Absorption

Status ditentukan oleh tahap karakter terlebih dahulu, lalu kelayakan proses penyerapan berikutnya. Tampilkan **tepat satu status**, jangan menampilkan alternatif sekaligus, dan jangan menambahkan alasan/label lain di dalam field profil.

- **Mortal, tidak sedang menjalani Awakening:** `Spirit Ring Absorption: not eligible yet`
- **Proses Martial Soul Awakening sedang berlangsung:** `Spirit Ring Absorption: pending`
- **Awakening selesai, belum pernah menyerap ring pertama, syarat ring pertama terpenuhi:** `Spirit Ring Absorption: eligible | ??? Day left`
- **Awakening selesai, belum pernah menyerap ring pertama, syarat ring pertama belum terpenuhi:** `Spirit Ring Absorption: not eligible yet | ??? Day left`
- **Spirit Realm 1–8, syarat penyerapan berikutnya belum lengkap:** `Spirit Ring Absorption: not eligible yet | N Day left`
- **Spirit Realm 1–8, seluruh syarat karakter/proses penyerapan berikutnya terpenuhi:** `Spirit Ring Absorption: eligible | 0 Day left`
- **Spirit Realm 9 (Spirit Primordial), batas puncak sistem:** `Spirit Ring Absorption: max | ∞ Day left`

Aturan:
- `pending` hanya digunakan selama proses Awakening benar-benar berlangsung, bukan sekadar karena karakter belum Awakening.
- Untuk Mortal yang tidak sedang menjalani Awakening, tampilkan hanya `Spirit Ring Absorption: not eligible yet`; jangan tambahkan Day left.
- Setelah Awakening selesai tetapi sebelum penyerapan pertama berhasil, `Day left` adalah `???` karena jeda belum dimulai. Awakening sendiri tidak otomatis memberikan ring atau membuat status `eligible`.
- Pada Spirit Realm 1–8, cooldown positif berarti `not eligible yet`. Cooldown nol hanyalah satu gerbang; status `eligible` hanya jika seluruh syarat resmi lain terpenuhi. Ketersediaan ring fisik tetap terpisah dari kelayakan karakter/proses.
- Spirit Realm 9 selalu `max | ∞ Day left`. Sembilan slot adalah batas sistem; jangan hitung cooldown ke ring kesepuluh, jangan tampilkan `eligible`, dan jangan menambahkan Spirit Realm atau slot kesepuluh tanpa revisi canon eksplisit pemilik.
- `Belum ditetapkan Day left` hanya untuk save lama yang diketahui pernah menyerap ring tetapi riwayat waktunya tidak cukup untuk merekonstruksi cooldown. Jangan gunakan untuk Mortal, Awakening, karakter yang belum pernah menyerap ring, atau Spirit Realm 9.

## 3. Jeda Minimum Antar-Penyerapan Spirit Ring

Jeda dihitung dari waktu penyerapan Spirit Ring sebelumnya yang berhasil sampai waktu paling awal penyerapan ring berikutnya. Jeda minimum awal yang berlaku bertingkat:

| Penyerapan berikutnya | Jeda minimum |
|---|---:|
| Ring 1 → Ring 2 | 2 minggu |
| Ring 2 → Ring 3 | 1 bulan |
| Ring 3 → Ring 4 | 3 bulan |
| Ring 4 → Ring 5 | 6 bulan |
| Ring 5 → Ring 6 | 1 tahun |
| Ring 6 → Ring 7 | 2 tahun |
| Ring 7 → Ring 8 | 3 tahun |
| Ring 8 → Ring 9 | 4 tahun |

Jeda ini adalah waktu minimum, bukan jaminan bahwa penyerapan akan berhasil. Pemetaan status mengikuti `templates/CHARACTER_PROFILE_TEMPLATE.md`: Mortal tanpa Awakening aktif = `not eligible yet` tanpa timer; Awakening aktif = `pending`; setelah Awakening, evaluasi kelayakan ring pertama dan gunakan `??? Day left`; Spirit Realm 1–8 memakai status kelayakan dan cooldown; Spirit Realm 9 selalu `max | ∞ Day left` karena tidak ada ring berikutnya. Jika karakter belum pernah menyerap Spirit Ring, jeda antarpenyerapan belum berlaku dan profil harus menampilkan `??? Day left`. **Setiap penyerapan yang berhasil langsung menjadi titik awal cooldown berikutnya:** tetapkan `T_eligible = 0` dan isi `Day left` berdasarkan interval resmi menuju ring berikutnya saat itu juga. Gunakan hanya formulasi kanonis `Day left` di `gameplay/TIME_AND_ACTION_RULES.md` §7: `T_remaining = max(0, T_min - T_eligible)`; jika sisa nol, `Day left = 0`, selain itu `Day left = ceil(T_remaining / 24 jam)`. `T_eligible` hanya mengakumulasi waktu dunia normal di luar Kultivasi; semua durasi Kultivasi dikecualikan meskipun timestamp dunia maju. Catat durasi time skip Kultivasi dalam riwayat sesi agar bisa dikecualikan. `Belum ditetapkan Day left` hanya berlaku untuk state lama yang diketahui pernah menyerap ring tetapi tidak memiliki data cukup untuk merekonstruksi cooldown, bukan untuk karakter yang belum pernah menyerap ring atau penyerapan yang baru berhasil. Untuk ring kedua dan seterusnya sebelum Spirit Realm 9, `Day left = 0` wajib dipenuhi terpisah dari syarat Sync, ring, item, toleransi tubuh, dan aturan resmi lain.

Jika penyerapan dipaksakan sebelum jeda minimum, GM wajib menetapkan deviasi minimal dan menentukan tingkatnya berdasarkan seberapa besar jeda yang dilanggar, kondisi tubuh, serta bukti yang tersedia. Deviasi dapat ringan hingga berat. Jangan mengarang angka peluang atau jumlah damage yang tidak memiliki rumus resmi.

## 4. Deviasi Saat Menerobos

Untuk percobaan menerobos, hitung jarak dari Sync progress saat ini ke cap kompatibilitas ring aktif:

`Gap = Cap kompatibilitas - Sync progress saat ini`

Syarat bottleneck hanya terpenuhi jika Gap kurang dari 10 poin persentase. Gap yang lebih besar atau sama dengan 10 poin persentase berarti syarat bottleneck belum terpenuhi dan percobaan menerobos tidak sah.

Semakin besar Gap di dalam rentang yang diizinkan, semakin tinggi tingkat deviasi. Jika Gap nol atau sangat kecil, jangan menyimpulkan deviasi pasti nol; periksa juga jeda minimum, item, toleransi tubuh, dan syarat resmi lainnya.

Setiap deviasi wajib dicatat sesuai `core/SPIRIT_RING_RULES.md` §5, yang merupakan satu-satunya sumber formula numerik untuk deviasi. Catat tingkat deviasi, dampak pada cap ring berikutnya, kehilangan HP aktual, kategori risiko, cedera, dan kondisi tubuh. Jangan menyalin atau menghitung ulang formula di modul bestiary. Pengurangan cap kompatibilitas dan durasi pemulihan masih belum memiliki formula numerik. Cedera yang timbul harus diklasifikasikan dan dipulihkan menurut `core/INJURY_SYSTEM.md`; kategori risiko HP bukan diagnosis cedera.

## 5. Catatan Setelah Proses

Catat tanggal/waktu penyerapan berhasil, nomor ring, jeda sejak penyerapan sebelumnya, item wajib yang digunakan jika ada, cap kompatibilitas ring, Sync progress, serta semua deviasi, damage HP, dan cedera yang terjadi. Gunakan profil karakter yang tersedia; jangan menambahkan field profil baru tanpa persetujuan pemilik.

## 6. Konsistensi Sumber

Gunakan istilah **Spirit Realm** secara konsisten untuk tingkat kultivasi; `Mortal` adalah status dasar sebelum sembilan Spirit Realm, bukan Spirit Realm 0.

- Gunakan `core/SPIRIT_RING_RULES.md` untuk formula kompatibilitas dan aturan ring.
- Gunakan `core/CULTIVATION_SYSTEM.md` untuk Spirit Realm, bottleneck, dan syarat menerobos.
- Gunakan `core/HP_SYSTEM.md` dan aturan pertarungan resmi untuk damage HP jika mekanik tersebut tersedia.
- Gunakan entri Beast yang sah untuk persyaratan item spesifik.
- Jika aturan penting belum tersedia, nyatakan keterbatasannya dan jangan mengarang fakta canon.
