# Ruang — Planner Pelajar

Aplikasi planner sekolah pribadi, responsif, dan dapat dipasang sebagai PWA. Antarmuka berbahasa Indonesia. Tidak ada akun demo, tugas contoh, atau data dummy.

## Fitur
- Ringkasan tugas, tenggat, progres, dan jadwal hari ini
- CRUD jadwal pelajaran per hari dengan jam, guru, dan ruang
- Tugas/PR, ujian, agenda, kumpul buku, dan tugas kelompok; prioritas, tenggat, pencarian, filter, status selesai, edit, dan hapus
- Kalender bulanan dengan penanda agenda
- Rutinitas: piket, seragam, perlengkapan/buku, tugas kelompok
- Catatan pribadi per mata pelajaran/kategori
- Profil pelajar, tema terang/gelap
- Ekspor dan impor cadangan JSON
- Penyimpanan lokal browser dan cache dasar untuk akses offline
- Layout desktop dan mobile, navigasi bawah untuk HP, animasi ringan dan dukungan `prefers-reduced-motion`

## Menjalankan di komputer
1. Ekstrak ZIP.
2. Buka folder di VS Code.
3. Jalankan server lokal sederhana. Jika Python tersedia, dari terminal folder ini:
   ```bash
   python -m http.server 8080
   ```
4. Buka `http://localhost:8080`.

File dapat dibuka langsung untuk mencoba UI, tetapi service worker/PWA memerlukan `localhost` atau HTTPS.

## Memasang di HP Android
Untuk opsi **Instal aplikasi / Tambahkan ke layar utama**:
1. Host folder ini di layanan HTTPS statis seperti GitHub Pages atau Vercel (paket gratis cukup untuk aplikasi statis).
2. Buka URL HTTPS itu di Chrome Android.
3. Pilih menu ⋮ → **Instal aplikasi** atau **Tambahkan ke layar utama**.

PWA dipilih agar pemasangan tidak perlu Play Store, biaya, atau build APK. Jika harus menjadi APK native, proyek ini dapat dibungkus dengan Capacitor pada tahap berikutnya.

## Data dan privasi
- Data disimpan di `localStorage` pada browser/perangkat ini; tidak dikirim ke server.
- Data tidak otomatis tersinkron ke perangkat lain.
- Menghapus data browser dapat menghapus data aplikasi. Gunakan Pengaturan → Ekspor data JSON secara berkala.
- Impor cadangan mengganti data lokal yang sedang aktif setelah konfirmasi.

## Batasan yang perlu diketahui
- Notifikasi pengingat terjadwal belum diaktifkan; browser/PWA memiliki batasan background notification yang berbeda-beda.
- Belum ada akun, sinkronisasi cloud, atau multi-perangkat karena versi ini sengaja berjalan tanpa backend dan tanpa biaya.
- Tidak ada data demo. Tampilan kosong saat pertama kali dipakai adalah kondisi yang disengaja.

## Struktur
```
ruang/
├── index.html
├── styles.css
├── app.js
├── manifest.webmanifest
├── sw.js
├── icon.svg
└── README.md
```
