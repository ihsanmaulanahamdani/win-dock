# WinDock

Dock melayang untuk Windows: bilah minimalis dengan latar kaca bergradasi, sudut membulat, dan ikon aplikasi yang seragam. Menampilkan aplikasi yang sedang berjalan dan aplikasi yang dipin, dengan tombol Start menu Windows, tema gelap/terang, ukuran ikon dan opasitas latar yang bisa diatur, serta ikon kustom per aplikasi maupun per tombol dock.

- Versi: **1.3.8**
- Platform: **Windows 10 / Windows 11 (64-bit)**
- Tidak perlu memasang .NET Runtime: aplikasi sudah dibungkus di dalam installer.

## Cara instal

1. Unduh `WinDock-Setup-1.3.8.exe`.
2. Klik dua kali file tersebut.
3. Di jendela installer, klik **Instal**.
4. Tunggu progress bar sampai selesai, lalu klik **Selesai**.

Instalasi berjalan per pengguna, jadi **tidak meminta hak administrator**. WinDock terpasang di:

```
%LOCALAPPDATA%\Programs\WinDock
```

Shortcut dibuat di Desktop (bisa dilewati lewat checkbox) dan menu Mulai.

> Jika Windows SmartScreen menampilkan peringatan karena file belum ditandatangani, pilih **More info > Run anyway**.

## Yang baru di 1.3.8

- **Taskbar tidak muncul lagi**: taskbar Windows dipantau terus selama WinDock berjalan. Kalau explorer menampilkan ulang taskbar saat Start menu dibuka atau focus berubah, WinDock langsung menyembunyikannya kembali. Handle taskbar juga dicari ulang otomatis kalau explorer restart.
- **Tombol Tutup WinDock**: tombol kaca merah di paling bawah sidebar pengaturan untuk menutup WinDock sepenuhnya. Setelah ditutup, taskbar dan menu Mulai Windows kembali normal.
- **Menu tray dirapikan**: item **Keluar** dihapus dari menu system tray. Penutupan aplikasi dilakukan lewat tombol merah di pengaturan.
- **Tutup aplikasi dari dock**: klik kanan ikon aplikasi yang sedang berjalan, pilih **Tutup aplikasi**. Kalau aplikasi punya beberapa jendela, menu berubah menjadi **Tutup semua jendela (N)** dan menutup semuanya sekaligus.
- **Watchdog taskbar**: taskbar yang dipaksa tampil oleh shell akan disembunyikan lagi dalam hitungan milidetik, jadi tidak ada kedipan taskbar saat Start menu dibuka.
- **Tautan di halaman Tentang**: kartu GitHub dan Buy me a Coffee (Saweria) untuk melihat proyek atau mendukung pengembangan WinDock.
- Versi dinaikkan ke **1.3.8**.

## Fitur

- Ikon aplikasi yang sedang berjalan, dikelompokkan per proses.
- Aplikasi yang dipin selalu tampil di dock walaupun belum berjalan; klik untuk membuka.
- Aplikasi pin yang sedang berjalan tetap memakai satu ikon, dengan titik biru sebagai penanda aktif.
- Tombol Start menu Windows di ujung kiri dock, dengan opsi tampil/sembunyi.
- Tombol pengaturan roda gigi di ujung kanan dock.
- Ikon aplikasi, tombol Start, dan tombol pengaturan bisa diganti sendiri.
- Tutup aplikasi atau semua jendelanya langsung dari menu klik kanan dock.
- Hover memperbesar ikon sedikit dan memberi highlight halus sesuai tema.
- Ikon diekstrak hingga 256 px supaya tetap tajam di layar ber-DPI tinggi.
- Jarak ikon, padding, sudut membulat, dan inset ikon diskalakan proporsional terhadap ukuran ikon.
- Semua ikon dibungkus tile kaca tanpa border dengan sudut membulat yang konsisten.
- Ikon tiap aplikasi bisa diganti sendiri tanpa mengubah aplikasi aslinya. Format yang didukung: `.ico`, `.png`, `.jpg`, `.jpeg`, `.bmp`, `.gif` (termasuk GIF beranimasi), atau ambil ikon dari `.exe`/`.dll`.
- Ikon kustom disalin ke `%APPDATA%\WinDock\icons\`, jadi tetap tampil walau file aslinya dipindah atau dihapus.
- Pengaturan: ukuran ikon, mode gelap/terang, opasitas latar dock, bahasa, posisi dock, tombol Start menu, dan toggle **Jalankan saat Windows menyala**.
- Kelola aplikasi pin dan pindai aplikasi terinstall.
- Daftar aplikasi memakai grid kartu dengan pencarian dan indikator aplikasi yang sudah dipin.
- Sidebar pengaturan menampilkan nama, versi, dan pemakaian RAM WinDock secara langsung.
- Tombol **Tutup WinDock** di sidebar pengaturan untuk keluar dan mengembalikan taskbar Windows.
- Tautan GitHub dan Buy me a Coffee (Saweria) di halaman Tentang.
- Dock tampil di semua virtual desktop Windows.
- Ikon WinDock tersedia untuk exe, shortcut, dan jendela pengaturan.
- Setelan dan daftar ikon kustom disimpan di `%APPDATA%\WinDock\settings.json`.

## Kontrol

| Aksi | Hasil |
| --- | --- |
| Klik kiri ikon berjalan | Fokus ke jendela aplikasi (restore bila minimize) |
| Klik kiri ikon pin yang belum berjalan | Jalankan aplikasi |
| Klik tombol Start menu | Buka menu Mulai Windows |
| Klik tombol Start saat menu terbuka | Tutup menu Mulai |
| Arahkan kursor ke notch | Tampilkan dock kembali dan tutup menu Mulai |
| Klik kanan ikon aplikasi | Pin/lepas pin, tutup aplikasi, ganti ikon, atau kembalikan ikon asli |
| Klik kanan tombol Start / roda gigi | Ganti atau kembalikan ikon tombol |
| Klik indikator baterai/jaringan/volume | Buka panel pengaturan cepat Windows |
| Scroll di indikator volume | Naikkan / turunkan volume |
| Klik ikon roda gigi | Buka jendela pengaturan |
| Klik **Tutup WinDock** | Tutup aplikasi dan kembalikan taskbar Windows |
| `Ctrl` + scroll | Perbesar / perkecil ikon (24–72 px) |
| Klik kanan area kosong dock | Menu pengaturan, tema, posisi, ukuran ikon, keluar |

## Tutup aplikasi dari dock

1. Klik kanan ikon aplikasi yang sedang berjalan.
2. Pilih **Tutup aplikasi**.
3. Kalau aplikasi punya lebih dari satu jendela, menu menampilkan **Tutup semua jendela (N)**. Semua jendela aplikasi tersebut ditutup sekaligus.

WinDock mengirim permintaan tutup yang sama seperti tombol X di jendela aplikasi, jadi dialog simpan perubahan tetap muncul bila aplikasi memilikinya.

## Tautan proyek dan dukungan

Buka **Pengaturan > Tentang** untuk menemukan dua tombol kaca:

- **GitHub** — `https://github.com/ihsanmaulanahamdani/win-dock`
- **Buy me a Coffee** — `https://saweria.co/sansandev`

Keduanya membuka browser default.

## Tutup WinDock dan kembalikan taskbar

Buka jendela pengaturan, lalu klik tombol merah **Tutup WinDock** di paling bawah sidebar.

WinDock akan berhenti sepenuhnya. Taskbar Windows dan menu Mulai kembali ke perilaku normal, termasuk saat tombol Win ditekan. Pengaturan dan ikon kustom tetap tersimpan di `%APPDATA%\WinDock`.

## Start menu dan taskbar

Saat tombol Start di dock diklik, menu Mulai Windows terbuka dan dock melipat menjadi notch kecil. Taskbar Windows disembunyikan agar layar hanya menampilkan menu Mulai dan dock.

Arahkan kursor ke notch untuk membuka dock kembali; menu Mulai otomatis tertutup. Taskbar tetap tersembunyi selama WinDock berjalan dan hanya muncul kembali ketika WinDock ditutup atau dock disembunyikan lewat menu tray.

Tombol Start bisa disembunyikan lewat **Pengaturan > Umum > Tombol dock > Menu Mulai Windows**.

## Atur opasitas latar dock

1. Buka jendela pengaturan, lalu pilih **Umum**.
2. Di kartu **Tema**, geser slider **Opasitas latar dock**.
3. Nilai 100% membuat latar pekat; nilai lebih rendah membuat wallpaper terlihat melalui kaca.
4. Perubahan langsung terlihat dan tersimpan otomatis.

Opasitas hanya memengaruhi latar kaca. Ikon, teks, badge, dan bayangan dock tidak ikut memudar.

## Ganti ikon aplikasi dan tombol

Untuk ikon aplikasi:

1. Klik kanan ikon aplikasi di dock.
2. Pilih **Ganti ikon...**.
3. Pilih file ikon atau aplikasi yang ikonnya ingin dipakai.
4. Ikon langsung berubah tanpa restart.

Untuk tombol Start dan tombol pengaturan, langkahnya sama: klik kanan tombolnya, pilih **Ganti ikon...**. Pilih **Kembalikan ikon asli** untuk kembali ke logo Windows atau roda gigi bawaan.

Gunakan GIF dengan latar transparan. GIF yang latarnya putih akan menampilkan kotak putih di sekitar ikon. Kecepatan animasi GIF otomatis dipelankan 2x.

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
- Taskbar asli Windows tidak diubah secara permanen; WinDock hanya menyembunyikannya selama aplikasi berjalan.
- Menutup WinDock mengembalikan taskbar dan menu Mulai Windows ke perilaku normal.
- Aplikasi yang hanya punya ikon tray (tanpa jendela) tidak ditampilkan.
- Pemindai aplikasi membaca shortcut Start Menu; aplikasi tanpa shortcut tidak muncul di daftar scan.
- Ikon indikator baterai, jaringan, dan volume belum bisa diganti.
- Ikon kustom terikat ke path aplikasi. Jika aplikasi dipindah atau di-install ulang ke path berbeda, atur ulang ikonnya.

## Lisensi

Bebas dipakai, dimodifikasi, dan dibagikan ulang, termasuk untuk keperluan pribadi maupun komunitas. Syaratnya sederhana: jangan mengklaim WinDock sebagai karya sendiri dan jangan menghapus kredit pembuat aslinya. Perangkat lunak disediakan apa adanya, tanpa garansi.
