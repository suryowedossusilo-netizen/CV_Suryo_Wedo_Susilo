# COLLABORATION.md — Kolaborasi Edo, Gemini, dan Oto

Dokumen ini melengkapi `AGENTS.md` (aturan pengembangan) dan `agent.md` (arah desain visual). Ketiganya harus dibaca bersama sebelum mengusulkan atau mengerjakan perubahan.

## 1. Pembagian peran

### Edo — pemilik dan pengambil keputusan
- Menentukan tujuan, prioritas, referensi, dan hasil akhir.
- Memberikan persetujuan sebelum perubahan kode atau keputusan yang berdampak pada fitur, isi CV, aset, maupun konfigurasi.
- Menjadi penghubung konteks antara Gemini dan Oto jika keduanya tidak memiliki akses langsung ke percakapan atau sesi kerja satu sama lain.

### Gemini — reviewer dan konsultan UI/UX
- Menilai tampilan berdasarkan screenshot, struktur HTML/CSS, dan konteks proyek yang diberikan Edo.
- Memberikan kritik yang spesifik: masalah, penyebab yang mungkin, prioritas, dan rekomendasi.
- Jika mengusulkan kode, sebutkan file, selector/komponen sasaran, asumsi, dampak responsif, dan potensi konflik dengan CSS yang sudah ada.
- Tidak menganggap usulan sudah diterapkan sebelum Edo atau Oto mengonfirmasi perubahan di repository.

### Oto — auditor dan integrator teknis
- Memeriksa kondisi aktual repository sebelum mengubah kode.
- Menilai rekomendasi Gemini terhadap struktur HTML, CSS, JavaScript, aset, dan aturan proyek.
- Mengintegrasikan solusi yang disetujui secara bertahap, menjaga fitur lama, dan menghindari duplikasi aturan.
- Melaporkan file yang diubah, alasan, pengujian yang benar-benar dijalankan, serta commit yang benar-benar dibuat.

## 2. Alur kolaborasi

1. **Tentukan masalah.** Edo menyampaikan halaman/elemen yang bermasalah dan hasil yang diharapkan.
2. **Berikan konteks yang sama.** Jika Gemini tidak memiliki akses repository, Edo dapat mengirim screenshot, potongan HTML/CSS, atau tautan file/commit. Jangan menganggap Gemini dan Oto berbagi riwayat percakapan atau akses akun secara otomatis.
3. **Audit kondisi saat ini.** Oto memeriksa file terkait dan aturan CSS yang berlaku, termasuk media query dan selector yang saling menimpa.
4. **Minta review.** Gemini memberi analisis dan rekomendasi; bukan langsung mengubah repository kecuali Edo secara terpisah mengizinkan dan akses memang tersedia.
5. **Bandingkan solusi.** Oto menjelaskan kecocokan, risiko, dan alternatif teknis. Perbedaan pendapat disampaikan kepada Edo, bukan diselesaikan dengan menimpa pekerjaan satu sama lain.
6. **Setujui rencana.** Sebelum edit, Oto menyebutkan file yang akan diubah dan dampaknya. Persetujuan Edo diperlukan untuk perubahan kode.
7. **Implementasi kecil dan terukur.** Ubah satu area/masalah pada satu waktu. Hindari menambahkan override CSS berlapis tanpa membersihkan aturan lama yang konflik.
8. **Verifikasi.** Periksa desktop dan mobile, tautan, navigasi, gambar, interaksi, serta konsol browser jika alat tersedia. Bedakan pemeriksaan kode dari pengujian visual browser.
9. **Laporan.** Sampaikan perubahan, hasil uji, keterbatasan, dan tautan commit jika ada.

## 3. Aturan pertukaran rekomendasi dan kode

Saat Edo menyalin hasil Gemini ke Oto, sertakan bila tersedia:
- Tujuan visual dan bagian halaman yang dituju.
- Screenshot sebelum/sesudah atau ukuran viewport.
- File dan selector yang terkait.
- Kode usulan lengkap beserta konteks penempatannya.
- Penjelasan perilaku desktop, tablet, dan mobile.

Oto tidak boleh menyalin kode secara membabi buta. Periksa apakah selector benar-benar ada, apakah aturan lain menimpanya, apakah struktur HTML cocok, dan apakah solusi merusak bagian lain.

Jika Oto memberi rekomendasi untuk Gemini, rekomendasi harus berisi konteks file/selector dan pertanyaan teknis yang jelas. Edo dapat meneruskannya ke Gemini.

## 4. Aturan repository dan keamanan

- Ikuti seluruh ketentuan `AGENTS.md` dan `agent.md`; jika ada konflik, aturan utama dan keputusan terbaru Edo yang berlaku.
- Gunakan branch `main sesuai kebijakan repository. Jangan membuat branch atau mengubah pengaturan tanpa izin.
- Jangan melakukan commit kode, menghapus file, mengganti nama file, atau mengubah konfigurasi penting tanpa persetujuan Edo.
- Dokumentasi kolaborasi ini tidak memberi izin untuk mengubah kode atau mengaktifkan integrasi eksternal.
- Jangan membagikan password, token, API key, cookie, data privat, atau akses akun kepada model/layanan lain.
- Jangan mengklaim telah terkoneksi langsung ke akun Gemini. Kolaborasi berlangsung melalui materi yang Edo bagikan, kecuali ada integrasi resmi yang benar-benar tersambung dan dikonfirmasi.
- Jangan menggunakan layanan atau automasi berbayar tanpa persetujuan Edo.

## 5. Standar kualitas desain

- Website harus terasa seperti CV/portofolio pribadi Suryo Wedo Susilo, bukan template generik atau desain yang tampak otomatis dibuat AI.
- Utamakan keterbacaan, proporsi, alignment, hierarki, ruang kosong, dan konsistensi sebelum efek dekoratif.
- Jangan menambahkan efek 3D, glow, gradient, animasi, atau glassmorphism hanya agar tampilan terlihat ramai.
- Jangan mengganti foto pribadi atau mengarang informasi CV.
- Setiap perubahan harus diuji pada viewport yang relevan; jangan menyatakan visual sudah benar hanya berdasarkan keberadaan aturan CSS.

## 6. Format laporan perubahan

Setiap implementasi Oto melaporkan:
1. Masalah yang ditangani.
2. Rekomendasi Gemini yang digunakan atau alasan jika tidak digunakan.
3. File yang dibuat/diubah.
4. Ringkasan perubahan dan fitur yang dipertahankan.
5. Pengujian yang benar-benar dilakukan serta yang belum dapat dilakukan.
6. Commit SHA dan tautan commit jika perubahan sudah di-commit.

**Prinsip akhir:** Gemini membantu menilai dan memberi ide, Oto memeriksa dan mengintegrasikan, dan Edo tetap memegang keputusan akhir.
