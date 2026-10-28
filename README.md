# Date Itinerary & Auto-Rundown Planner

Aplikasi web satu halaman (Single-Page Application) interaktif bertema **Date Itinerary & Auto-Rundown Planner** yang dibangun menggunakan HTML, Tailwind CSS, dan Vanilla JavaScript.

## ✨ Fitur Utama
- **Auto-Rundown Beruntun**: Tentukan jam mulai (*Anchor Time*), jadwal kegiatan akan terhitung berantai secara instan & real-time.
- **Multi-Day Support (Bisa Tambah Hari)**:
  - Tab navigasi hari (`Hari 1`, `Hari 2`, dst.) dengan tombol `+ Tambah Hari`.
  - Tiap hari memiliki *Anchor Time* mandiri dan daftar kegiatan terpisah tanpa bentrok antar hari.
  - Opsi hapus hari dengan konfirmasi aman.
- **Kolaborasi Real-Time (Multi-User Sync)**:
  - Fitur Room / Session link (`?room=date-kita-123`).
  - Tombol **"Bagikan Link ke Doi"** untuk menyalin link sesi kencan unik.
  - Setiap perubahan (tambah kegiatan, geser urutan, ganti jam/durasi) otomatis tersinkronisasi di layar pacar secara real-time via Firebase Realtime Database & BroadcastChannel tanpa perlu me-refresh halaman.
  - Indikator status koneksi: `🟢 Terhubung ke Room • Online`.
- **Ekspor Fleksibel ke WhatsApp**:
  - Salin hari yang sedang aktif saja, **atau**
  - Salin seluruh hari (Hari 1 s/d Hari N) sekaligus dalam satu format chat rapi.
- **Interaktif & Responsif**:
  - Reorder kegiatan (naik/turun), edit, dan hapus secara dinamis.
  - Tombol cepat durasi (15m, 30m, 45m, 60m, 90m, 120m) & preset kategori emoji.
  - Tampilan split 2-kolom pada laptop/desktop, dan 1-kolom reflow pada smartphone.
  - Penyimpanan otomatis di peramban (`localStorage`).

## 🚀 Deployment
Aplikasi ini adalah static SPA tanpa dependensi build, siap langsung di-deploy di Vercel, Netlify, atau GitHub Pages.
