# AGENTS.md — Aturan Utama Pengembangan

Dokumen ini menjadi pedoman utama bagi siapa pun yang membantu mengembangkan repository CV_Suryo_Wedo_Susilo.

## 1. Bahasa dan komunikasi
- Gunakan bahasa Indonesia untuk komunikasi, dokumentasi, penjelasan perubahan, dan laporan pekerjaan.
- Jelaskan rencana dengan bahasa yang sederhana, jelas, dan tidak bertele-tele.
- Jangan mengaku telah melakukan pemeriksaan, perubahan, atau pengujian jika hal tersebut belum benar-benar dilakukan.

## 2. Tujuan proyek
- Repository ini merupakan website CV dan portofolio pribadi.
- Pertahankan identitas, isi, tujuan, dan karakter personal pemilik website.
- Tingkatkan kualitas tampilan dan pengalaman pengguna tanpa mengubah arah proyek menjadi template generik.

## 3. Batas ruang lingkup
- Fokus pekerjaan adalah frontend: HTML, CSS, JavaScript sisi klien, serta aset visual.
- Jangan menambahkan backend, API, database, autentikasi, atau layanan server baru.
- Jangan mengubah konfigurasi hosting, domain, deployment, atau workflow otomatis tanpa persetujuan terpisah.
- Jangan mengubah isi pengalaman, pendidikan, proyek, kontak, maupun informasi pribadi tanpa konfirmasi pemilik.
- Jangan menghapus bagian, tautan, interaksi, atau fitur yang sudah ada hanya demi menyederhanakan desain.

## 4. Audit sebelum perubahan
- Periksa struktur repository dan file yang terkait sebelum mengedit.
- Identifikasi hubungan antara HTML, stylesheet, JavaScript, dan aset.
- Catat fitur serta perilaku yang harus tetap berfungsi.
- Sebelum mengedit, sampaikan file yang akan diubah, tujuan, dan rencana singkat.
- Jika perubahan berpotensi memengaruhi fungsi yang sudah ada, jelaskan risikonya dan minta persetujuan terlebih dahulu.

## 5. Aturan implementasi frontend
- Pertahankan struktur proyek yang sudah digunakan kecuali ada alasan teknis yang kuat dan telah disetujui.
- Utamakan perubahan bertahap, terukur, dan mudah ditinjau.
- Hindari duplikasi CSS, JavaScript, komponen, dan aturan responsif.
- Gunakan HTML semantik, CSS yang terorganisasi, serta JavaScript yang mudah dipahami.
- Jangan menambahkan dependensi atau library baru jika solusi sederhana yang sudah tersedia mencukupi.
- Pastikan navigasi, tautan, tombol, animasi, dan interaksi tetap berfungsi.
- Pastikan tampilan responsif pada ponsel, tablet, dan desktop.
- Perhatikan aksesibilitas dasar: kontras, ukuran teks, fokus keyboard, label, dan teks alternatif gambar.

## 6. Keamanan dan privasi
- Jangan pernah memasukkan API key, token, password, kredensial, atau informasi rahasia ke repository.
- Jangan mengunggah file konfigurasi lokal atau data pribadi yang tidak diperlukan.
- Jangan mengirimkan data formulir atau informasi pengunjung ke layanan eksternal tanpa persetujuan pemilik.
- Jangan menambahkan pelacak, analitik, atau skrip pihak ketiga baru tanpa izin.

## 7. Aturan GitHub dan persetujuan
- Gunakan branch utama `main` sebagai alur kerja standar.
- Jangan membuat branch, pull request, menghapus file, mengganti nama file, mengubah konfigurasi penting, atau mengubah pengaturan repository tanpa persetujuan.
- Jangan melakukan force push atau menulis ulang riwayat Git.
- Jangan melakukan commit perubahan fitur sebelum pemilik menyetujui rencana perubahan.
- Pembuatan atau pembaruan dokumentasi yang secara eksplisit diminta pemilik boleh dilakukan sesuai instruksi tersebut.
- Jangan melakukan tindakan berbayar atau mengaktifkan layanan berbayar.

## 8. Pengujian
- Periksa hasil perubahan pada ukuran layar berbeda jika memungkinkan.
- Periksa konsol browser, tautan, navigasi, aset, dan interaksi yang terdampak.
- Jangan menyatakan pengujian berhasil jika belum dijalankan.
- Jika pengujian tidak dapat dilakukan, jelaskan keterbatasannya.

## 9. Laporan setiap pekerjaan
Setelah pekerjaan selesai, laporkan:
1. File yang dibuat, diubah, atau dihapus.
2. Ringkasan perubahan dan alasan teknisnya.
3. Fitur yang dipertahankan.
4. Pengujian yang benar-benar dilakukan dan hasilnya.
5. Commit SHA atau tautan commit jika memang dibuat.
6. Hal yang belum selesai atau perlu diperiksa pemilik.

## 10. Prinsip utama
Pemilik repository adalah pengambil keputusan akhir. Jangan mengambil inisiatif yang mengubah ruang lingkup, isi personal, fungsi, biaya, atau konfigurasi penting tanpa persetujuan yang jelas.
