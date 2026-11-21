# Kebijakan keamanan / Security policy

## Versi yang didukung

| Versi | Didukung |
|---|---|
| 6.6.x | Ya |
| 1.x (generasi lama) | Tidak; pindahkan data ke versi 6 |

## Melaporkan celah keamanan

Jangan laporkan celah keamanan lewat issue publik. Gunakan **Security → Report a vulnerability** di repositori
[si-administrator-rilis](https://github.com/en1gma-workspace/si-administrator-rilis/security/advisories/new)
(laporan privat GitHub). Sertakan versi aplikasi, langkah untuk mengulang, dan dampaknya.

Perkiraan tanggapan: konfirmasi dalam 3 hari kerja, rencana perbaikan dalam 14 hari untuk celah yang terkonfirmasi.

*English:* please do not open public issues for security problems. Use GitHub's private vulnerability reporting on the
public release repository linked above.

## Model keamanan aplikasi

- **Lokal saja.** Server hanya mendengar di `127.0.0.1`. Permintaan dengan Host selain
  `siadministrator.en1gma.localhost`, `127.0.0.1`, atau `localhost` ditolak (perlindungan DNS rebinding), dan
  permintaan yang mengubah data dari Origin lain ditolak (CSRF). Lihat `internal/server`.
- **Akun.** Kata sandi disimpan dengan scrypt. Sesi memakai cookie HttpOnly dan SameSite=Strict. Hak akses diatur per peran.
- **Data.** Semua data tersimpan di folder data pada komputer pengguna. Aplikasi tidak memanggil layanan internet,
  kecuali aktivasi dan perpanjangan lisensi: hanya kunci lisensi atau sertifikat, sidik komputer (hash, bukan data
  pribadi), dan versi aplikasi yang dikirim ke server aktivasi. Data santri tidak pernah dikirim.
- **Lisensi.** Sertifikat aktivasi ditandatangani Ed25519 dan terikat ke komputer. Server menyimpan hash kunci,
  bukan kunci aslinya.
- **Installer.** Berjalan tanpa hak administrator dan memeriksa SHA-256 muatannya sebelum memasang. Installer belum
  bertanda tangan kode (Authenticode), sehingga SmartScreen memberi peringatan; cocokkan dengan `SHA256SUMS.txt`.
- **Update offline.** Aplikasi hanya memasang paket `.e1w` yang bertanda tangan digital resmi.
- **Akun bawaan.** Instalasi baru membuat akun admin bawaan; segera ganti kata sandinya setelah pemasangan.

## Pengelolaan rahasia (untuk pengelola repo)

- Tidak ada rahasia di repo ini. `.gitignore` menolak `.env`, kunci (`*.key`, `*.pem`, `*.pfx`), dan folder `kunci/`.
- Kunci pribadi penanda tangan paket update dan aktivasi lisensi disimpan **di luar repo**, terenkripsi, dengan minimal
  satu cadangan offline. Hanya kunci publiknya yang ditanam di aplikasi.
- Bila kunci pribadi bocor: terbitkan update yang mengganti kunci publik, lalu umumkan di repo rilis.
