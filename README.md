# Halaman Harga Produk Indonesia Calon Gloria

Direktori statis ini dapat dipublikasikan ke GitHub Pages.

- `index.html`: halaman harga pasar; akses memakai akun yang aktif di manajemen akun admin; PPN dikelola dari admin.
- `admin.html`: halaman admin jarak jauh; izin edit dikontrol oleh Supabase RLS.
- `reset-password.html`: halaman reset kata sandi admin.
- `supabase-config.js`: konfigurasi Project URL dan anon key Supabase.
- `CNAME`: domain kustom default `pricing.calongloria.id`.

## Admin Jarak Jauh

1. Buat proyek Supabase dan aktifkan Email/Password Auth.
2. Jalankan file lokal `../docs/supabase-remote-backend.sql` di Supabase SQL Editor.
3. Setelah pengguna Auth pertama dibuat, jadikan pengguna tersebut sebagai `owner` memakai perintah bootstrap di bagian bawah file SQL.
4. Jalankan file lokal `../docs/supabase-seed-pricing.sql` untuk mengimpor model admin dan harga publikasi awal.
5. Isi `url` dan `anonKey` di `supabase-config.js` dengan Project URL dan publishable/anon key dari Supabase.
6. Setelah GitHub Pages dipublikasikan, buka `/admin.html`.

## Pengaturan DNS

Tambahkan CNAME berikut di DNS `calongloria.id`:

- Host/Name: `pricing`
- Type: `CNAME`
- Value/Target: `fangwj0105.github.io`

Di repositori GitHub Pages, atur Pages Source ke root cabang `main`, lalu isi Custom domain dengan `pricing.calongloria.id`.
