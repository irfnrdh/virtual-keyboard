# Papan Ketik Cadangan (Virtual Keyboard)

Halaman web sederhana berisi **keyboard virtual** yang bisa diklik dengan
mouse/jari, untuk membantu mengetik saat sebagian tombol di keyboard fisik
**rusak atau tidak berfungsi**. Hasil ketikan ditampung di kotak teks dan
tinggal disalin (copy) untuk ditempel (paste) ke aplikasi lain — chat, Word,
form, kode, dan sebagainya.

100% berjalan di browser (HTML, CSS, JS biasa), tanpa server, tanpa instalasi,
tanpa koneksi internet (kecuali untuk memuat font dari Google Fonts).

## ✨ Fitur

- **Keyboard QWERTY lengkap**: huruf, angka, dan simbol (`! @ # $ % ^ & * ( ) - = [ ] { } \ | ; : ' " , . / < > ?`).
- **Tombol Shift & Caps Lock** yang berfungsi seperti keyboard asli (klik untuk mengaktifkan, indikator menyala saat aktif).
- **Tombol fungsi penting**: `Backspace`, `Tab`, `Enter`, `Spasi`, `Delete`.
- **Navigasi kursor**: `←` `→` `Home` `End` untuk memindahkan posisi ketik tanpa mouse di dalam teks.
- **Simbol tambahan** yang sering tidak ada di keyboard biasa: `€ £ ¥ © ® ™ ° × ÷ — – … " " ' ' • § ¶ ± ≈ ≠ → ←` dll.
- **Tombol "Salin Semua"** — menyalin seluruh isi kotak teks ke clipboard dengan satu klik, lengkap dengan notifikasi.
- **Tombol "Bersihkan"** — mengosongkan kotak teks untuk mulai dari awal.
- **Penghitung karakter** otomatis.
- Kotak teks tetap bisa diketik langsung pakai tombol fisik yang masih berfungsi — jadi keyboard virtual hanya melengkapi tombol yang rusak, bukan menggantikan semuanya.
- Desain gelap, ringan, dan **responsif** — bisa dipakai di laptop maupun HP.

## 🚀 Cara Pakai

1. Unduh/clone repo ini.
2. Buka file `index.html` langsung di browser (Chrome, Edge, Firefox, Safari) — bisa dengan klik dua kali pada filenya.
3. Ketik dengan kombinasi:
   - Tombol fisik yang masih berfungsi (klik dulu di kotak teks).
   - Klik tombol-tombol virtual untuk huruf/simbol yang tombol fisiknya rusak.
4. Setelah teks selesai, klik **📋 Salin Semua**.
5. Tempel (`Ctrl+V` atau klik kanan → Paste, atau tahan lalu pilih *Tempel* di HP) ke aplikasi tujuan.

> 💡 Tips: Untuk huruf besar, klik **Shift** (berlaku 1 huruf saja) atau **Caps Lock** (tetap aktif sampai dimatikan lagi).

## 📂 Struktur File

```
.
├── index.html   # Aplikasi utama (HTML + CSS + JS dalam satu file)
└── README.md    # Dokumen ini
```

Karena semuanya ada dalam satu file `index.html`, kamu bisa:
- Membukanya langsung secara lokal (offline, kecuali font).
- Meng-host-nya di GitHub Pages, Netlify, Vercel, atau hosting statis lainnya tanpa konfigurasi tambahan.

## 🛠️ Kustomisasi

Beberapa bagian yang mudah diubah di dalam `index.html`:

- **Tata letak tombol**: ubah array `ROW1`–`ROW6` dan `ROW5_SYMBOLS` di bagian `<script>`.
- **Tampilan/warna**: ubah variabel CSS di bagian `:root` (mis. `--accent`, `--bg`, `--key`).
- **Font**: diambil dari Google Fonts (`Sora` untuk judul/UI, `JetBrains Mono` untuk kotak teks dan tombol).

## ⚠️ Catatan

- Tombol seperti `Ctrl`, `Alt`, `Win/Cmd`, dan `F1–F12` **tidak disertakan**, karena tombol-tombol ini umumnya digunakan untuk *shortcut sistem operasi* (misalnya `Ctrl+C`), bukan untuk menghasilkan karakter teks — sehingga tidak relevan untuk kebutuhan "mengetik teks lalu copy-paste".
- Fitur salin otomatis (`navigator.clipboard`) memerlukan halaman dibuka melalui `http://`, `https://`, atau langsung dari file lokal di sebagian besar browser modern. Jika gagal, halaman akan otomatis memakai cara salin cadangan.

## 📄 Lisensi

Bebas digunakan, dimodifikasi, dan dibagikan untuk keperluan apa pun.
