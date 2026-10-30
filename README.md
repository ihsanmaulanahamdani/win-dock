# WinDock

Dock melayang untuk Windows: bilah minimalis dengan latar kaca bergradasi, sudut membulat, dan ikon aplikasi yang seragam. Menampilkan aplikasi yang sedang berjalan dan aplikasi yang dipin, dengan tema gelap/terang, ukuran ikon yang bisa diatur, dan ikon kustom per aplikasi.

- Versi: **1.3.0**
- Platform: **Windows 10 / Windows 11 (64-bit)**
- Tidak perlu memasang .NET Runtime: aplikasi sudah dibungkus di dalam installer.

## Cara instal

1. Unduh `WinDock-Setup-1.3.0.exe`.
2. Klik dua kali file tersebut.
3. Di jendela installer, klik **Instal**.
4. Tunggu progress bar sampai selesai, lalu klik **Selesai**.

Instalasi berjalan per pengguna, jadi **tidak meminta hak administrator**. WinDock terpasang di:

```
%LOCALAPPDATA%\Programs\WinDock
```

Shortcut dibuat di Desktop (bisa dilewati lewat checkbox) dan menu Mulai.

> Jika Windows SmartScreen menampilkan peringatan karena file belum ditandatangani, pilih **More info > Run anyway**.

## Yang baru di 1.3.0

- **Ikon kustom per aplikasi**: klik kanan ikon di dock, pilih **Ganti ikon...**. Berlaku untuk aplikasi yang dipin maupun yang sedang berjalan. Aplikasi aslinya tidak diubah.
- **Kembalikan ikon asli**: klik kanan ikon yang sudah dikustom, pilih **Kembalikan ikon asli**.
- **Tampilan light mode baru**: dock dan tile ikon memakai kaca gelap transparan, tile tanpa border, dan glyph pengaturan, baterai, jaringan, serta volume berwarna putih.
- **Teks pengaturan lebih terbaca**: warna teks sekunder di light mode dibuat lebih gelap.
- **RAM WinDock di sidebar pengaturan**: bagian paling bawah sidebar menampilkan pemakaian RAM proses WinDock, diperbarui tiap 2 detik.
- **Padding konten pengaturan**: jarak atas dan bawah halaman sekarang memakai padding di dalam area scroll, jadi konten tidak terpotong di tepi jendela.
- **Logo WinDock tajam**: logo di sidebar dan halaman Tentang memakai frame ICO 256 px, tidak lagi pecah.
- **Menu klik kanan diperbaiki**: membuka menu ikon aplikasi tidak lagi menutup paksa WinDock. Menu dock dan menu ikon kini memakai style item yang aman untuk separator.

## Fitur

- Ikon aplikasi yang sedang berjalan, dikelompokkan per proses.
- Aplikasi yang dipin selalu tampil di dock walaupun belum berjalan; klik untuk membuka.
- Aplikasi pin yang sedang berjalan tetap memakai satu ikon, dengan titik biru sebagai penanda aktif.
- Hover memperbesar ikon sedikit dan memberi highlight halus sesuai tema.
- Ikon diekstrak hingga 256 px supaya tetap tajam di layar ber-DPI tinggi.
- Jarak ikon, padding, sudut membulat, dan inset ikon diskalakan proporsional terhadap ukuran ikon.
- Semua ikon dibungkus tile kaca tanpa border dengan sudut membulat yang konsisten.
- Ikon tiap aplikasi bisa diganti sendiri tanpa mengubah aplikasi aslinya. Format yang didukung: `.ico`, `.png`, `.jpg`, `.jpeg`, `.bmp`, `.gif`, atau ambil ikon dari `.exe`/`.dll`.
- Ikon kustom disalin ke `%APPDATA%\WinDock\icons\`, jadi tetap tampil walau file aslinya dipindah atau dihapus.
- Tombol roda gigi untuk membuka jendela pengaturan.
- Pengaturan: ukuran ikon, mode gelap/terang, bahasa, posisi dock, dan toggle **Jalankan saat Windows menyala**.
- Kelola aplikasi pin dan pindai aplikasi terinstall.
- Daftar aplikasi memakai grid kartu dengan pencarian dan indikator aplikasi yang sudah dipin.
- Sidebar pengaturan menampilkan versi dan pemakaian RAM WinDock secara langsung.
- Dock tampil di semua virtual desktop Windows.
- Ikon WinDock tersedia untuk exe, shortcut, dan jendela pengaturan.
- Setelan dan daftar ikon kustom disimpan di `%APPDATA%\WinDock\settings.json`.

## Kontrol

| Aksi | Hasil |
| --- | --- |
| Klik kiri ikon berjalan | Fokus ke jendela aplikasi (restore bila minimize) |
| Klik kiri ikon pin yang belum berjalan | Jalankan aplikasi |
| Klik kanan ikon aplikasi | Pin/lepas pin, ganti ikon, atau kembalikan ikon asli |
| Klik indikator baterai/jaringan/volume | Buka panel pengaturan cepat Windows |
| Scroll di indikator volume | Naikkan / turunkan volume |
| Klik ikon roda gigi | Buka jendela pengaturan |
| `Ctrl` + scroll | Perbesar / perkecil ikon (24–72 px) |
| Klik kanan area kosong dock | Menu pengaturan, tema, posisi, ukuran ikon, keluar |

## Ganti ikon aplikasi

1. Klik kanan ikon aplikasi di dock.
2. Pilih **Ganti ikon...**.
3. Pilih file ikon atau aplikasi yang ikonnya ingin dipakai.
4. Ikon langsung berubah tanpa restart.

Untuk kembali ke ikon asli, klik kanan ikon yang sama lalu pilih **Kembalikan ikon asli**.

Ikon hanya diubah di dalam WinDock. File aplikasi asli tidak disentuh. Salinan ikon disimpan di:

```
%APPDATA%\WinDock\icons\
```

## Jalankan saat Windows menyala

Buka **Pengaturan > Umum**, lalu aktifkan toggle **Jalankan saat Windows menyala**. WinDock akan terbuka otomatis setiap login. Matikan toggle untuk membatalkannya. Tidak perlu hak administrator.

## Hapus instalasi

Buka **Settings > Apps > Installed apps > WinDock > Uninstall**, atau jalankan:

```
%LOCALAPPDATA%\Programs\WinDock\WinDock.exe --uninstall
```

Setelan dan ikon kustom di `%APPDATA%\WinDock` tidak dihapus otomatis.

## Catatan

- Dock hanya muncul di monitor utama dan selalu di atas jendela lain.
- Taskbar asli Windows tidak diubah.
- Aplikasi yang hanya punya ikon tray (tanpa jendela) tidak ditampilkan.
- Pemindai aplikasi membaca shortcut Start Menu; aplikasi tanpa shortcut tidak muncul di daftar scan.
- Ikon indikator baterai, jaringan, dan volume belum bisa diganti.
- Ikon kustom terikat ke path aplikasi. Jika aplikasi dipindah atau di-install ulang ke path berbeda, atur ulang ikonnya.

## Lisensi

Bebas dipakai, dimodifikasi, dan dibagikan ulang, termasuk untuk keperluan pribadi maupun komunitas. Syaratnya sederhana: jangan mengklaim WinDock sebagai karya sendiri dan jangan menghapus kredit pembuat aslinya. Perangkat lunak disediakan apa adanya, tanpa garansi.
