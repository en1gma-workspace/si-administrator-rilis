<div align="center">

<img src="merek-persegi.svg" alt="Logo si administrator" width="96">

# si administrator

**Aplikasi administrasi pondok pesantren untuk Windows yang bekerja tanpa internet.**

[Unduh versi terbaru](https://github.com/en1gma-workspace/si-administrator-rilis/releases/latest) ·
[Laporkan masalah](https://github.com/en1gma-workspace/si-administrator-rilis/issues/new/choose) ·
[English](#english)

</div>

## Apa ini

si administrator menyatukan administrasi pondok pesantren dalam satu program: santri dan pengasuh, jadwal dan halaqah,
tahfidz, nilai, perizinan, keuangan dan kuitansi, rapor Madrasah Diniyyah berbahasa Arab, kelulusan dan ijazah, hingga
Pondok Ramadhan. Semua data tersimpan di komputer lembaga sendiri: tanpa internet, tanpa server awan, tanpa langganan.

## Unduh

Buka halaman [Rilis](https://github.com/en1gma-workspace/si-administrator-rilis/releases/latest), lalu pilih installer
yang sesuai komputer Anda:

| Installer | Untuk |
|---|---|
| `Pasang-SiAdministrator-<versi>-x64.exe` | Sebagian besar komputer dan laptop Windows 10/11 (64-bit) |
| `Pasang-SiAdministrator-<versi>-x86.exe` | Komputer lama dengan Windows 10 32-bit |

**Cara mengetahui jenis komputer:** buka *Pengaturan Windows → Sistem → Tentang*, lihat baris *Jenis sistem*.
"Sistem operasi 64-bit, prosesor berbasis x64" berarti x64; "32-bit" berarti x86.

Setiap rilis menyertakan berkas `SHA256SUMS.txt` untuk memastikan installer tidak rusak atau diubah.

## Memasang

1. Jalankan installer. Tidak perlu hak administrator.
2. Bila muncul peringatan *Windows melindungi PC Anda*, klik **Info selengkapnya → Tetap jalankan**. Peringatan ini
   muncul untuk aplikasi baru yang belum banyak diunduh.
3. Ikuti langkah pemasangan, lalu buka si administrator dari ikon di desktop.
4. Aktifkan dengan kunci lisensi. Tanpa internet: pilih *Aktivasi manual* dan kirim kode
   permintaannya ke en1gma-workspace.
5. Masuk dengan akun awal yang tertera di layar masuk, lalu **segera ganti kata sandinya** di *Sistem → Pengaturan → Akun saya*.

## Data dan cadangan

- Program dan seluruh data berada dalam satu folder (bawaan `D:\si-administrator` bila ada drive D:). Data ada di
  subfolder `data`.
- Buat cadangan secara berkala di *Sistem → Pengaturan → Data & cadangan*, dan simpan salinannya di flashdisk
  atau penyimpanan lain.

## Pindah komputer

Lisensi terikat ke komputer; folder yang disalin ke komputer lain tidak bisa dipakai sampai diaktifkan di sana.

1. Di komputer lama: buat cadangan, lalu **Sistem → Pengaturan → Tentang → Lepas lisensi dari komputer ini** (butuh internet sebentar).
2. Salin seluruh folder aplikasi ke komputer baru.
3. Jalankan `si-administrator.exe` di komputer baru dan aktifkan dengan kunci yang sama.

Komputer lama rusak atau hilang? Buka [issue](https://github.com/en1gma-workspace/si-administrator-rilis/issues/new/choose)
atau hubungi en1gma-workspace agar lisensinya dilepas dari server.

## Persyaratan sistem

- Windows 10 atau 11 (x64 atau x86)
- Ruang disk sekitar 800 MB
- Aplikasi bekerja tanpa internet. Internet dipakai sebentar untuk aktivasi dan melepas lisensi; lisensi berjangka juga
  memperpanjang diri otomatis saat online (atau lewat aktivasi manual)

## Bantuan

- Masalah atau pertanyaan: buka [issue baru](https://github.com/en1gma-workspace/si-administrator-rilis/issues/new/choose).
  Jangan sertakan data pribadi santri.
- Celah keamanan: gunakan laporan privat (lihat `SECURITY.md`).

## Lisensi

si administrator adalah perangkat lunak proprietary. Hak cipta (c) 2026 en1gma-workspace, seluruh hak dilindungi.
Lihat `LICENSE`. Komponen pihak ketiga tercantum di `THIRD-PARTY-NOTICES.md`.

---

## English

**si administrator** is an offline administration app for Islamic boarding schools (pondok pesantren) on Windows 10/11.
Download the installer that matches your PC from the
[latest release](https://github.com/en1gma-workspace/si-administrator-rilis/releases/latest): `x64` for most 64-bit PCs,
`x86` for 32-bit Windows 10. No administrator rights needed; internet is needed once for licence activation.
Verify downloads with `SHA256SUMS.txt`. Report problems through
[issues](https://github.com/en1gma-workspace/si-administrator-rilis/issues/new/choose) and security issues through
private vulnerability reporting. Proprietary software, all rights reserved; see `LICENSE`.
