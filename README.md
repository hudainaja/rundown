# Date Itinerary & Auto-Rundown Planner

Aplikasi web satu halaman (Single-Page Application) interaktif bertema **Date Itinerary & Auto-Rundown Planner** yang dibangun menggunakan HTML, Tailwind CSS, dan Vanilla JavaScript.

## ✨ Fitur Utama
- **Auto-Rundown Beruntun**: Tentukan jam mulai (*Anchor Time*), jadwal kegiatan akan terhitung berantai secara instan & real-time.
- **Dukungan Durasi Jam & Menit**: Input kombinasi jam & menit yang fleksibel beserta tombol cepat durasi (15m, 30m, 45m, 1 Jam, 1.5 Jam, 2 Jam, 2.5 Jam, 3 Jam).
- **Undo & Redo Lengkap**:
  - Tombol Undo (↩️) dan Redo (↪️) di header untuk membatalkan atau mengulang aksi kapan saja.
  - Shortcut keyboard cepat: `Ctrl+Z` (Undo) dan `Ctrl+Y` / `Ctrl+Shift+Z` (Redo).
  - Tombol **Undo langsung di Toast** notifikasi setiap kali ada kegiatan yang terhapus atau dibersihkan.
- **Penyimpanan Aman (Anti-Kereset)**:
  - Data tersimpan otomatis dan persisten di browser (`localStorage`).
  - Reload browser tidak akan menghapus atau menimpa jadwal kamu dengan contoh bawaan.
  - Konfirmasi aman sebelum memuat contoh itinerary atau mengosongkan jadwal.
- **Multi-Day Support (Bisa Tambah Hari)**:
  - Tab navigasi hari (`Hari 1`, `Hari 2`, dst.) dengan tombol `+ Tambah Hari`.
  - Tiap hari memiliki *Anchor Time* mandiri dan daftar kegiatan terpisah tanpa bentrok antar hari.
- **Kolaborasi Real-Time (Multi-User Sync)**:
  - Fitur Room / Session link (`?room=date-kita-123`).
  - Tombol **"Bagikan ke Doi"** untuk menyalin link sesi kencan unik.
  - Setiap perubahan otomatis tersinkronisasi di layar pacar secara real-time via Firebase Realtime Database & BroadcastChannel tanpa perlu refresh halaman.
  - Indikator status koneksi: `🟢 Room: [id-room]`.
- **Ekspor Fleksibel ke WhatsApp**:
  - Salin hari yang sedang aktif saja, **atau**
  - Salin seluruh hari (Hari 1 s/d Hari N) sekaligus dalam satu format chat rapi.

## 🚀 Deployment
Aplikasi ini adalah static SPA tanpa dependensi build, siap langsung di-deploy di Vercel, Netlify, atau GitHub Pages.
