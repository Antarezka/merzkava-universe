# Merzkava Universe — Martial Soul Awakening Protocol

Status: Modul mekanik resmi.
Cakupan: undian rarity Martial Soul, penilaian kualitas inheren yang berdiri sendiri, peluang mutasi, pilihan pemain, prosedur resolusi, dan batas perilaku GM.

Modul ini adalah sumber mekanik utama untuk proses awakening dan mutasi Martial Soul. **Format hasil untuk pemain:** bungkus setiap hasil final undian rarity, chance mutasi, hasil mutasi, dan nilai yang dihasilkan formula dengan empat tanda bintang di kedua sisi (`****<hasil final>****`), baik hasil berhasil maupun gagal. Format setiap label rarity/klasifikasi dengan pola ``**<istilah>**`` di dalam double backtick; penjelasan tetap di luar backtick. `core/MARTIAL_SOUL.md` tetap menjadi sumber karakteristik, lore, serta interpretasi umum Martial Soul. Jika ada pertentangan mengenai peluang atau prosedur awakening, modul ini yang berlaku untuk bagian tersebut.

---

## 1. Prinsip Dasar

1. Awakening mengungkap Martial Soul seseorang; awakening tidak otomatis memberikan Spirit Ring.
2. Awakening berlangsung pada usia empat tahun atau lebih.
3. Hasil rarity dan peluang mutasi wajib ditentukan dengan prosedur acak yang adil; penilaian kualitas inheren adalah proses terpisah berbasis canon/bukti, bukan undian chance. GM tidak boleh memilih hasil hanya karena cocok dengan cerita, karakter, atau keinginan pemain.
4. Rarity Martial Soul bukan pengganti Spirit Realm, Spirit Ring, kemampuan bertarung, pengalaman, atau profesi. Rarity yang lebih tinggi tidak otomatis berarti menang dalam pertarungan.
5. Bentuk, atribut, kemampuan, batas, dan efek suatu Martial Soul harus memiliki dasar yang dapat dijelaskan. GM tidak boleh menciptakan kemampuan luar biasa hanya berdasarkan rarity.
6. Jika mekanisme pengacakan yang benar-benar acak tidak tersedia, GM harus menyatakan keterbatasan itu dan tidak mengaku telah melakukan pengundian acak yang tidak terjadi.

## 1.1 Awakening Routes, Imperial Subsidy, and Proof Token — Golden Dragon Empire

The Golden Dragon Empire has two separate routes, detailed authoritatively in `core/10_ECONOMY_SYSTEM.md`:

- **Independent paid route:** the individual pays 3 xg 25 xs for service, 8% tax on that service fee (26 xs), 15 xs for documentation, and 10 xs for the token: **3 xg 76 xs total**.
- **Biennial Imperial public route:** the Imperial subsidy pays the service fee, service tax, and documentation. The individual pays **only 10 xs for the proof token**.
- If the person cannot pay the token fee on the public route, an external local financial organization may advance the exact unpaid token charge. The individual signs a debt note to that external lender; the Golden Dragon Empire is not the lender and does not set or guarantee the private loan. The available organization and its interest rate are randomized from plausible local options. Typical reputable lenders charge 3%–8% simple annual interest; an unlucky draw can reach 12%–24% simple annual interest. The selected rate is fixed for that note and must not be rerolled. See the economy module for limits, records, and default consequences.
- Each individual who completes awakening and has the result officially recorded receives a proof token linked to the service record. It helps verify completion for basic employment and education applications but guarantees neither employment nor admission.
- Token and record confirm only information actually established during awakening. They do not change rarity, imply unconfirmed powers, or grant special status.
- A missed loan repayment may damage credit reputation and make decent-paying employment or future credit harder to obtain where relevant records are checked. This is a socioeconomic consequence, not an automatic legal ban across the Golden Dragon Empire on employment.
- These rules apply only to the Golden Dragon Empire. Do not impose them on Tianhai Yunzhou, Beiming Gu, Wanluo, or Lawless Territories unless their own canon adopts them.
- Record actual charges, subsidy expenditure, token issuance, loan advances, debt notes, interest, and repayments. Do not assume a character paid, borrowed, received a token, or defaulted without a supported in-game event and ledger entry.

## 2. Tabel Rarity Awakening

Rarity awal ditentukan dengan satu undian yang merata dari rentang 1–100. Setiap angka hanya masuk ke satu kategori.

| Hasil undian | Rarity | Peluang |
|---|---|---:|
| 1–30 | Common | 30% |
| 31–57 | Uncommon | 27% |
| 58–77 | Rare | 20% |
| 78–89 | Epic | 12% |
| 90–97 | Legendary | 8% |
| 98–100 | Myth | 3% |
| **Total** | | **100%** |

- Lakukan satu undian untuk menentukan rarity awal. Jangan mengulang undian hanya karena hasilnya tidak disukai.
- Hasil undian menetapkan rarity awal sebelum pemeriksaan mutasi.
- Jangan mengubah peluang berdasarkan status sosial, garis keturunan, wilayah, kekayaan, usia, atau kepentingan plot kecuali aturan resmi kelak secara eksplisit mengubah tabel ini.
- Kategori rarity mengukur kelas kelangkaan awakening. Rarity bukan jaminan bahwa Martial Soul tertentu memiliki atribut, kemampuan, atau kekuatan spesifik.

## 2A. Independent Martial Soul Classification (Score-Based)

**Martial Soul rarity must use only these established names: Common, Uncommon, Rare, Epic, Legendary, and Myth. Never use numbered tier labels or invent additional rarity names.** This assessment method does not replace the single rarity chance draw in Section 2; the draw determines the awakening rarity, while this score is only a provisional assessment of the Martial Soul's inherent qualities. If the two appear inconsistent, preserve the actual rarity draw and label the score result as a separate provisional assessment—never silently overwrite one with the other.

### Assessment dimensions

Score each applicable dimension from 0–15 using established lore, confirmed traits, demonstrated function, or reliable appraisal evidence. Do not award points merely because the name sounds grand, the form is mythical, the owner has a powerful family, or the result would be dramatic.

| Dimension | Martial Soul evidence to assess |
|---|---|
| 1. Core potential | Demonstrated or canonically established ceiling of its own nature |
| 2. Primary function | Practical effect of the Martial Soul itself, not powers it has not gained |
| 3. Potency | Strength or efficiency of confirmed innate effects |
| 4. Scope | Reach, area, targets, or scale supported by evidence |
| 5. Versatility | Number of distinct uses genuinely supported by its traits |
| 6. Control and stability | Precision, reliability, and control supported by evidence |
| 7. Growth capacity | Supported potential to develop through legitimate cultivation and compatible Spirit Rings |
| 8. Exceptional traits | Verified unusual properties not already scored elsewhere |
| 9. Evidence and provenance | Reliable records, repeatable tests, or authenticated classification evidence |

Each applicable dimension uses the same rubric: 0 = tested/verified negligible; 1–3 = minor; 4–6 = limited; 7–9 = substantial; 10–12 = very high; 13–15 = exceptional within a relevant comparison class. Mark a genuinely irrelevant dimension N/A and exclude it from the average; unknown evidence is not a zero. Avoid counting the same trait twice.

**Formula:** add the scores of applicable dimensions, divide by the number of applicable dimensions to get the mean, multiply the mean by 9, then round to the nearest whole number. Cap the result at 134. At least three dimensions must have reliable evidence; otherwise, do not issue a numerical prediction and mark **Klasifikasi belum ditetapkan — appraisal diperlukan**.

### Named classification bands

| Score | Provisional inherent classification |
|---:|---|
| 0–22 | Common |
| 23–44 | Uncommon |
| 45–66 | Rare |
| 67–88 | Epic |
| 89–110 | Legendary |
| 111–134 | Myth |

These bands are a fallback for an **inherent-quality assessment**, not a second rarity draw and not an automatic rewrite of the awakening result. Keep the wording **Prediksi GM · [score] poin · klasifikasi inheren sementara** until an authorized appraisal or owner-approved canon decision confirms it. Do not present the score band as the result of the rarity chance table.

Rarity Martial Soul hanya boleh memakai enam istilah resmi: **Common, Uncommon, Rare, Epic, Legendary, Myth**. Semua label lama untuk rarity yang memakai angka atau tambahan istilah di luar enam nama resmi harus dihapus dan diselaraskan ke istilah resmi saja. Jangan membuat istilah rarity tambahan. Skor inheren hanya memberi klasifikasi sementara berdasarkan enam istilah ini dan tidak menggantikan hasil undian rarity.

### Awakening resolution order with independent assessment

1. Confirm eligibility and the awakening event.
2. Establish the base Martial Soul form from known, legitimate character/family evidence; do not invent a lineage.
3. Perform the single 1–100 rarity draw from Section 2 and record its named result exactly and display the resolved result as `****<hasil rarity>****`.
4. Assess inherent qualities from established canon first; if no classification is recorded, use this score method only when evidence is sufficient. Record any score as a provisional assessment, never as the rarity draw result.
5. Present the mandatory mutation-anomaly narrative and let the player choose whether to stop or continue.
6. If the player stops, finalize the base Martial Soul with its already determined rarity; keep any inherent-quality score explicitly provisional and separate. Do not roll mutation.
7. If the player continues, perform exactly one mutation draw at 10% and display the resolved mutation outcome as `****<hasil mutasi>****`. Mutation may change traits and therefore may warrant reassessment, but do not automatically change the rarity. Reassess only from the actual resulting traits and available evidence; do not reroll rarity or mutation.
8. If evidence is too limited or mutation effects are not mechanically established, preserve unknown details and request appraisal rather than fabricating a score or effect.

A completed **Merzkava Appraisal Authority (MAA)** ruling is authoritative for the specific examined Martial Soul when its classification was previously unknown or uncertain. The examiner must distinguish the awakening rarity already drawn from any assessed inherent-quality classification. Appraisal does not change the chance draw, grant abilities, establish lineage, guarantee combat victory, or override an already definitive owner-confirmed canon decision.

## 3. Urutan Wajib Awakening

GM harus mengikuti urutan ini setiap kali karakter menjalani awakening yang hasilnya sedang dimainkan:

1. Pastikan karakter memenuhi syarat usia dan proses awakening benar-benar berlangsung.
2. Tentukan bentuk dasar Martial Soul dengan mempertimbangkan informasi karakter yang sah, termasuk kecenderungan keluarga atau leluhur yang benar-benar diketahui. Bentuk Martial Soul tidak memiliki daftar tertutup dan dapat berupa bentuk lazim maupun tidak lazim, termasuk fenomena seperti kabut atau asap. Jangan mengarang silsilah, leluhur, atau kemampuan tersembunyi. Kecenderungan genetik memengaruhi pertimbangan bentuk, bukan mengubah tabel peluang rarity.
3. Undi rarity awal sekali menggunakan tabel di Bagian 2.
4. Catat hasil rarity dengan istilah resmi dari undian. Jika diperlukan dan bukti cukup, nilai kualitas inheren secara terpisah memakai skor Bagian 2A; tandai sebagai prediksi sementara dan jangan menyebutnya hasil rarity.
5. Tampilkan narasi anomali atau gejolak yang menandai adanya kesempatan terakhir untuk menerima risiko mutasi. Narasi ini wajib diberikan setelah rarity diketahui, tetapi sebelum keputusan mutasi dan hasil akhir.
6. Berikan keputusan kepada pemain: menghentikan proses dan mempertahankan hasil awal, atau bertahan untuk mengambil peluang mutasi.
7. Jika pemain memilih berhenti, tetapkan Martial Soul awal dengan rarity hasil undian; penilaian kualitas inheren tetap terpisah dan sementara, serta tidak ada undian mutasi.
8. Jika pemain memilih bertahan, lakukan tepat satu undian mutasi dengan peluang 10% sesuai Bagian 4.
9. Tetapkan hasil akhir berdasarkan undian. Jika mutasi mengubah karakteristik yang relevan, evaluasi ulang klasifikasi kualitas inheren hanya berdasarkan sifat hasil mutasi yang benar-benar ditetapkan; jangan otomatis mengubah rarity atau mengundi ulang rarity/mutasi.
10. Catat hasil final dan fakta yang telah dikonfirmasi dalam profil gameplay. Jangan mencatat kemungkinan yang tidak terjadi sebagai fakta.

GM tidak boleh memilihkan keputusan untuk karakter pemain. Jika pemain belum menjawab, hentikan resolusi pada titik keputusan; jangan menganggap diam sebagai persetujuan untuk bertahan.

## 4. Peluang dan Resolusi Mutasi

- Peluang dasar terjadinya mutasi Martial Soul setelah pemain memilih bertahan adalah **10%**.
- Peluang tidak terjadinya mutasi adalah **90%**.
- Peluang ini hanya berlaku setelah pemain memilih bertahan. Jika pemain memilih berhenti, peluang mutasi tidak dijalankan dan hasil awal tetap berlaku.
- Undi tepat satu kali: hasil 1–10 dari undian merata 1–100 berarti terjadi mutasi; hasil 11–100 berarti tidak terjadi mutasi.
- Hasil undian tidak boleh diulang, diganti, atau dimanipulasi. Jangan menggunakan beberapa undian lalu memilih hasil yang paling menarik.
- Mutasi bukan hasil yang dijamin oleh rarity Myth atau Legendary. Semua rarity mengikuti peluang mutasi yang sama, kecuali canon resmi kelak diubah.
- Undian mutasi menentukan apakah mutasi terjadi, bukan apakah mutasi pasti menguntungkan. Hasil mutasi dapat menguntungkan atau merugikan; arahnya harus ditentukan dari konsekuensi yang masuk akal dan aturan resmi, bukan demi menyenangkan pemain.
- Modul ini belum menetapkan peluang terpisah untuk mutasi menguntungkan versus merugikan, daftar hasil mutasi, besaran bonus, penalti, atau efek samping numerik. GM dilarang mengarang angka atau tabel peluang untuk hal-hal tersebut. Jika hasil mutasi memerlukan mekanik yang belum ditetapkan, jelaskan perubahan secara terbatas dan tandai rincian mekanis yang belum diketahui sebagai `???`; jangan membuat statistik permanen tanpa dasar.
- Jika tidak tersedia metode undian yang adil dan dapat diverifikasi, jangan berpura-pura bahwa angka acak telah dihasilkan. Tunda resolusi mekanis sampai metode yang layak tersedia.

## 5. Narasi Wajib Sebelum Keputusan Pemain

Setelah rarity awal diundi dan sebelum hasil final ditetapkan, GM wajib menyampaikan narasi yang setara maknanya dengan teks berikut. GM boleh menyesuaikan detail suasana, tetapi tidak boleh menghilangkan sifat opsional, peluang rendah, atau risiko yang tidak pasti.

> “Ugh… tunggu. Ada sesuatu yang tidak beres dengan proses awakening ini…”
>
> Energi di sekitar Martial Soul yang baru terbangkitkan mendadak bergejolak. Bentuknya memperlihatkan tanda-tanda perubahan yang tidak biasa. Ini mungkin fenomena langka yang dikenal sebagai mutasi Martial Soul.
>
> Jika proses diteruskan, perubahan itu bisa menghasilkan sesuatu yang menguntungkan—atau justru merugikan. Tidak ada jaminan bahwa hasilnya akan lebih baik daripada Martial Soul yang sudah terbangkitkan.
>
> **“Apa Anda ingin bertahan dan mengambil risiko, atau menghentikan proses sekarang?”**
>
> *Ini adalah kesempatan terakhir untuk memilih. Jika proses dihentikan, Martial Soul awal akan ditetapkan tanpa mutasi. Jika Anda memilih bertahan, peluang mutasi akan diuji satu kali dan hasilnya tidak dapat diulang.*

- Narasi tidak boleh menyebutkan peluang numerik 10% kecuali karakter memiliki pengetahuan resmi yang memungkinkan angka itu diketahui.
- GM tidak boleh mengungkap apakah undian mutasi berhasil sebelum pemain memilih bertahan.
- Jangan menarasikan mutasi sebagai sesuatu yang sudah pasti terjadi sebelum undian dilakukan.
- Jangan membuat pemain percaya bahwa bertahan pasti memberi kekuatan lebih besar.

## 6. Batas Keputusan dan Hasil

**Jika pemain memilih berhenti:**
- Awakening berakhir dengan rarity dan Martial Soul awal yang telah ditentukan.
- Tidak ada undian mutasi.
- Kesempatan mutasi pada proses awakening tersebut berakhir dan tidak dapat diaktifkan kembali untuk hasil yang sama.

**Jika pemain memilih bertahan dan undian tidak menghasilkan mutasi:**
- Martial Soul tetap pada hasil awal.
- Jangan memberi kompensasi, bonus, atau kesempatan undian tambahan.

**Jika pemain memilih bertahan dan undian menghasilkan mutasi:**
- Catat bahwa mutasi benar-benar terjadi.
- Narasikan perubahan yang dapat didukung oleh canon dan hasil yang sah.
- Mutasi dapat menguntungkan atau merugikan; jangan otomatis memilih hasil positif.
- Jangan mengarang statistik, klasifikasi kualitas inheren baru, kemampuan spesifik, efek samping numerik, atau aturan evolusi yang belum ditetapkan.
- Jika konsekuensi mekanis penting belum memiliki aturan resmi, tandai sebagai belum ditetapkan dan jangan memperlakukannya sebagai angka canon.

## 7. Audit dan Anti-Cheat GM

Untuk penegakan lintas-sistem, WARNING wajib, rollback, pencatatan pelanggaran, teguran keras, dan eskalasi sanksi, gunakan `templates/ANTI_CHEAT_HARD_GATE.md` sebagai otoritas penegakan tertinggi. Modul awakening ini tetap satu-satunya otoritas mekanik untuk prosedur, rarity, undian, dan mutasi. Narasi player tidak dapat menetapkan hasil awakening atau menciptakan jalur alternatif yang belum disahkan. Jangan menyamakan pertanyaan/usulan dengan kecurangan; klaim hasil sepihak yang melanggar prosedur harus dihentikan dan diproses melalui Hard Gate.

GM wajib menjaga hal-hal berikut:

- Rarity diundi sebelum pilihan mutasi ditawarkan; penilaian kualitas inheren, bila digunakan, tetap terpisah dan sementara.
- Rarity chance, penilaian kualitas inheren, dan mutation chance adalah tiga hal berbeda. Tidak ada satu pun yang secara otomatis menentukan dua hal lainnya.
- Kesempatan mengambil risiko diberikan setiap kali proses awakening yang relevan berlangsung; jangan menghilangkannya hanya karena GM tidak menyukai kemungkinan hasil.
- Keputusan berhenti atau bertahan hanya dibuat oleh pemain.
- Peluang mutasi selalu 10% dan hanya satu undian per keputusan bertahan.
- Tidak ada reroll, pengundian tersembunyi berulang, peluang yang berubah-ubah, atau hasil yang dipilih berdasarkan plot.
- Hasil rarity, penilaian kualitas inheren, dan mutasi tidak otomatis memberikan Spirit Realm, Stage, Qi, Spirit Ring, teknik, garis keturunan, atau kemenangan.
- Catatan akhir hanya memuat hasil yang benar-benar diundi dan ditetapkan.
- Jika terjadi konflik dengan lore umum Martial Soul, gunakan modul ini untuk prosedur, tabel peluang, dan keputusan mutasi; gunakan `core/MARTIAL_SOUL.md` untuk lore serta karakteristik umum.

## 8. Integrasi dengan Modul Lain

Untuk tingkat kultivasi, gunakan istilah kanonis **Spirit Realm** dari `core/CULTIVATION_SYSTEM.md`. Rarity awakening tidak menetapkan Spirit Realm, dan `Mortal` bukan Spirit Realm 0.

- `core/MARTIAL_SOUL.md` — definisi Martial Soul, contoh bentuk, penguasaan awal alat, dan lore.
- `core/TIER_ASSESSMENT_AND_APPRAISAL.md` — lembaga MAA dan prinsip otoritas appraisal; skor khusus Martial Soul serta integrasinya dengan chance awakening diatur di modul ini.
- `core/CULTIVATION_SYSTEM.md` — Spirit Realm dan Stage; rarity awakening tidak menggantikannya.
- `core/SPIRIT_RING_RULES.md` — perolehan dan penyerapan Spirit Ring; awakening tidak memberikan ring.
- `templates/AUTHORITY_ORDER.md` — prosedur GM dan larangan mengarang atau mengambil keputusan pemain.
- `INDEX.md` — pintu masuk wajib dan pemetaan modul.

Aturan ini berlaku sebagai mekanik resmi sejak tercatat di repository. Jangan menyimpulkan aturan mutasi Martial Soul dari mekanik mutasi Spirit Beast.
