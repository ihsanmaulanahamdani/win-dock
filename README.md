# WinDock

Dock melayang untuk Windows: bilah minimalis dengan latar kaca bergradasi, sudut membulat, dan ikon aplikasi yang seragam. Menampilkan aplikasi yang sedang berjalan dan aplikasi yang dipin, dengan tema gelap/terang serta ukuran ikon yang bisa diatur.

- Versi: **1.2.0**
- Platform: **Windows 10 / Windows 11 (64-bit)**
- Tidak perlu memasang .NET Runtime: aplikasi sudah dibungkus di dalam installer.

## Cara instal

1. Unduh `WinDock-Setup-1.2.0.exe`.
2. Klik dua kali file tersebut.
3. Di jendela installer, klik **Instal**.
4. Tunggu progress bar sampai selesai, lalu klik **Selesai**.

Instalasi berjalan per pengguna, jadi **tidak meminta hak administrator**. WinDock terpasang di:

```
%LOCALAPPDATA%\Programs\WinDock
```

Shortcut dibuat di Desktop (bisa dilewati lewat checkbox) dan menu Mulai.

> Jika Windows SmartScreen menampilkan peringatan karena file belum ditandatangani, pilih **More info > Run anyway**.

## Fitur

- Ikon aplikasi yang sedang berjalan, dikelompokkan per proses.
- Aplikasi yang dipin selalu tampil di dock walaupun belum berjalan; klik untuk membuka.
- Aplikasi pin yang sedang berjalan tetap memakai satu ikon, dengan titik biru sebagai penanda aktif.
- Hover memperbesar ikon sedikit dan memberi highlight halus sesuai tema.
- Ikon diekstrak hingga 256 px supaya tetap tajam di layar ber-DPI tinggi.
- Jarak ikon, padding, sudut membulat, dan inset ikon diskalakan proporsional terhadap ukuran ikon.
- Semua ikon dibungkus tile kaca dengan sudut membulat yang konsisten.
- Tombol roda gigi untuk membuka jendela pengaturan.
- Pengaturan: ukuran ikon, mode gelap/terang, bahasa, posisi dock, dan toggle **Jalankan saat Windows menyala**.
- Kelola aplikasi pin dan pindai aplikasi terinstall.
- Daftar aplikasi memakai grid kartu dengan pencarian dan indikator aplikasi yang sudah dipin.
- Dock tampil di semua virtual desktop Windows.
- Ikon WinDock tersedia untuk exe, shortcut, dan jendela pengaturan.
- Setelan disimpan di `%APPDATA%\WinDock\settings.json`.

## Kontrol

| Aksi | Hasil |
| --- | --- |
| Klik kiri ikon berjalan | Fokus ke jendela aplikasi (restore bila minimize) |
| Klik kiri ikon pin yang belum berjalan | Jalankan aplikasi |
| Klik ikon roda gigi | Buka jendela pengaturan |
| `Ctrl` + scroll | Perbesar / perkecil ikon (24–72 px) |
| Klik kanan | Menu pengaturan, tema, ukuran ikon, keluar |

## Jalankan saat Windows menyala

Buka **Pengaturan > Umum**, lalu aktifkan toggle **Jalankan saat Windows menyala**. WinDock akan terbuka otomatis setiap login. Matikan toggle untuk membatalkannya. Tidak perlu hak administrator.

## Hapus instalasi

Buka **Settings > Apps > Installed apps > WinDock > Uninstall**, atau jalankan:

```
%LOCALAPPDATA%\Programs\WinDock\WinDock.exe --uninstall
```

Setelan di `%APPDATA%\WinDock` tidak dihapus otomatis.

## Catatan

- Dock hanya muncul di monitor utama dan selalu di atas jendela lain.
- Taskbar asli Windows tidak diubah.
- Aplikasi yang hanya punya ikon tray (tanpa jendela) tidak ditampilkan.
- Pemindai aplikasi membaca shortcut Start Menu; aplikasi tanpa shortcut tidak muncul di daftar scan.

## Lisensi

Bebas dipakai, dimodifikasi, dan dibagikan ulang, termasuk untuk keperluan pribadi maupun komunitas. Syaratnya sederhana: jangan mengklaim WinDock sebagai karya sendiri dan jangan menghapus kredit pembuat aslinya. Perangkat lunak disediakan apa adanya, tanpa garansi.
