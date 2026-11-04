# WinDock

Dock melayang untuk Windows: bilah minimalis dengan latar kaca bergradasi, sudut membulat, dan ikon aplikasi yang seragam. Menampilkan aplikasi yang sedang berjalan dan aplikasi yang dipin, dengan tombol Start menu Windows, tema gelap/terang, ukuran ikon dan opasitas latar yang bisa diatur, serta ikon kustom per aplikasi maupun per tombol dock.

- Versi: **1.4.2**
- Platform: **Windows 10 / Windows 11 (64-bit)**
- Tidak perlu memasang .NET Runtime: aplikasi sudah dibungkus di dalam installer.

## Cara instal

1. Unduh `WinDock-Setup-1.4.2.exe`.
2. Klik dua kali file tersebut.
3. Di jendela installer, klik **Instal**.
4. Tunggu progress bar sampai selesai, lalu klik **Selesai**.

Instalasi berjalan per pengguna, jadi **tidak meminta hak administrator**. WinDock terpasang di:

```
%LOCALAPPDATA%\Programs\WinDock
```

Shortcut dibuat di Desktop (bisa dilewati lewat checkbox) dan menu Mulai.

> Jika Windows SmartScreen menampilkan peringatan karena file belum ditandatangani, pilih **More info > Run anyway**.

## WinDock Free dan Pro

WinDock memakai dua tingkat lisensi:

| Fitur | Free | Pro |
| --- | --- | --- |
| Jam dan tanggal di dock | - | Ya |
| Jam di notch | - | Ya |
| Persentase baterai di notch | - | Ya |
| Jalankan saat Windows menyala | - | Ya |
| Animasi bounce dan shake ikon | - | Ya |
| Pilih monitor untuk dock | - | Ya |
| Jumlah aplikasi pin | 8 | Tanpa batas |
| Ganti ikon aplikasi/tombol | - | Ya |
| Ukuran ikon quick action, jarak, dan teks jam/tanggal | - | Ya |

Lisensi Pro bersifat permanen, berlaku untuk update berikutnya, dan terikat ke
satu perangkat. Aktivasi offline:

1. Buka **Pengaturan > Lisensi**.
2. Salin **ID Perangkat**, kirim ke penjual saat membeli.
3. Tempel kunci lisensi, lalu klik **Aktifkan**.

Kunci lisensi disimpan di `%APPDATA%\WinDock\license.key` dan tidak dihapus
saat update atau uninstall. Alat pembuat kunci untuk penjual
(`tools\WinDockKeygen.cmd`) adalah aplikasi terpisah dan tidak ikut di dalam
installer WinDock.

## Cara membeli WinDock Pro

Pembelian dilakukan langsung ke penjual. Hubungi penjual melalui tautan
Saweria (`https://saweria.co/sansandev`) atau GitHub
(`https://github.com/ihsanmaulanahamdani/win-dock`), lalu sampaikan bahwa Anda
ingin membeli lisensi WinDock Pro. Harga dan metode pembayaran diinformasikan
langsung oleh penjual.

Data yang perlu dikirim:

| Data | Keterangan |
| --- | --- |
| ID Perangkat | Wajib. Salin dari **Pengaturan > Lisensi**. Format `WD-XXXX-XXXX-XXXX-XXXX-XXXX` dan unik per PC. |
| Nama pemilik lisensi | Wajib. Nama yang tampil di detail lisensi. |
| Email | Wajib. Dipakai untuk mengirim kunci lisensi dan invoice. |
| Nomor invoice/order | Wajib. Nomor transaksi pembayaran yang dipakai penjual untuk mencatat lisensi. |

Setelah pembayaran diterima, penjual mengirim kunci lisensi dan invoice.
Tempel kunci di **Pengaturan > Lisensi**, lalu klik **Aktifkan**.

Lisensi terikat ke satu perangkat. Install ulang Windows biasanya memakai ID
Perangkat yang sama, tetapi mengganti motherboard/BIOS atau pindah PC
memerlukan kunci baru. Kunci offline tidak bisa dicabut, jadi pembelian tidak
dapat dibatalkan setelah kunci dikirim.

## Yang baru di 1.4.2

- **Efek shake saat aplikasi ditutup (Pro)**: ikon aplikasi bergetar singkat ketika aplikasi ditutup, baik dari menu dock maupun lewat tombol X, Alt+F4, atau taskbar. Animasi memberi tanda bahwa aplikasi sedang ditutup. Animasi bounce saat membuka aplikasi juga khusus Pro.
- **Toggle animasi terpisah (Pro)**: buka **Pengaturan > Umum > Animasi** untuk menyalakan atau mematikan sendiri animasi bounce saat membuka aplikasi dan animasi shake saat menutup aplikasi.
- **Pilih monitor dock (Pro)**: dock bisa dipindahkan ke monitor lain lewat **Pengaturan > Umum > Dock > Monitor dock**. Versi Free selalu memakai monitor utama.
- Versi **1.4.2**.

## Fitur

- Ikon aplikasi yang sedang berjalan, dikelompokkan per proses.
- Aplikasi yang dipin selalu tampil di dock walaupun belum berjalan; klik untuk membuka.
- Saat aplikasi pin dibuka dari dock, ikonnya memantul halus sampai jendela aplikasi muncul (Pro).
- Toggle terpisah untuk animasi bounce dan shake di **Pengaturan > Umum > Animasi** (Pro).
- Monitor dock bisa dipilih di **Pengaturan > Umum > Dock > Monitor dock** (Pro); Free selalu memakai monitor utama.
- Aplikasi pin yang sedang berjalan tetap memakai satu ikon, dengan titik biru sebagai penanda aktif.
- Tombol Start menu Windows di ujung kiri dock, dengan opsi tampil/sembunyi.
- Tombol pengaturan roda gigi di ujung kanan dock.
- Ikon aplikasi, tombol Start, dan tombol pengaturan bisa diganti sendiri.
- Tutup aplikasi atau semua jendelanya langsung dari menu klik kanan dock; ikon bergetar singkat saat aplikasi ditutup (Pro).
- Hover memperbesar ikon sedikit dan memberi highlight halus sesuai tema.
- Ikon diekstrak hingga 256 px supaya tetap tajam di layar ber-DPI tinggi.
- Jarak ikon, padding, sudut membulat, dan inset ikon diskalakan proporsional terhadap ukuran ikon.
- Semua ikon dibungkus tile kaca tanpa border dengan sudut membulat yang konsisten.
- Ikon tiap aplikasi bisa diganti sendiri tanpa mengubah aplikasi aslinya. Format yang didukung: `.ico`, `.png`, `.jpg`, `.jpeg`, `.bmp`, `.gif` (termasuk GIF beranimasi), atau ambil ikon dari `.exe`/`.dll`.
- Ikon kustom disalin ke `%APPDATA%\WinDock\icons\`, jadi tetap tampil walau file aslinya dipindah atau dihapus.
- Pengaturan: ukuran ikon, ukuran dan jarak quick action, ukuran teks jam/tanggal, mode gelap/terang, opasitas latar dock, bahasa, posisi dock, tombol Start menu, dan toggle **Jalankan saat Windows menyala**.
- Kelola aplikasi pin dan pindai aplikasi terinstall.
- Daftar aplikasi memakai grid kartu dengan pencarian dan indikator aplikasi yang sudah dipin.
- Sidebar pengaturan menampilkan nama, versi, dan pemakaian RAM WinDock secara langsung.
- Tombol **Tutup WinDock** di sidebar pengaturan untuk keluar dan mengembalikan taskbar Windows.
- Tautan GitHub dan Buy me a Coffee (Saweria) di halaman Tentang.
- Dock tampil di semua virtual desktop Windows.
- Ikon WinDock tersedia untuk exe, shortcut, dan jendela pengaturan.
- Jam dock, tanggal, dan jam notch punya toggle terpisah; format hari/tanggal bisa dipilih dari dropdown.
- WinDock Pro: lisensi permanen satu perangkat, aktivasi offline, dan pin tanpa batas.
- Menu klik kanan aplikasi yang sedang berjalan menyediakan **Buka aplikasi lagi** untuk membuka instance/jendela baru.
- Setelan dan daftar ikon kustom disimpan di `%APPDATA%\WinDock\settings.json`.

## Kontrol

| Aksi | Hasil |
| --- | --- |
| Klik kiri ikon berjalan | Fokus ke jendela aplikasi (restore bila minimize) |
| Klik kiri ikon pin yang belum berjalan | Jalankan aplikasi; ikon memantul sampai jendela muncul (Pro) |
| Klik tombol Start menu | Buka menu Mulai Windows |
| Klik tombol Start saat menu terbuka | Tutup menu Mulai |
| Arahkan kursor ke notch | Tampilkan dock kembali dan tutup menu Mulai |
| Klik kanan ikon aplikasi | Pin/lepas pin, tutup aplikasi, ganti ikon, atau kembalikan ikon asli |
| Klik kanan ikon lalu pilih **Tutup aplikasi** | Tutup jendela aplikasi; ikon bergetar singkat (Pro) |
| Tutup aplikasi lewat tombol X, Alt+F4, atau taskbar | Ikon di dock bergetar singkat (Pro), lalu hilang bila aplikasi tidak dipin |
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

WinDock mengirim permintaan tutup yang sama seperti tombol X di jendela aplikasi, jadi dialog simpan perubahan tetap muncul bila aplikasi memilikinya. Untuk lisensi Pro, ikon di dock bergetar singkat saat aplikasi ditutup, termasuk ketika ditutup lewat tombol X atau taskbar.

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

- Dock hanya tampil di satu monitor: monitor utama untuk Free, atau monitor pilihan untuk Pro. Dock selalu di atas jendela lain.
- Taskbar asli Windows tidak diubah secara permanen; WinDock hanya menyembunyikannya selama aplikasi berjalan.
- Menutup WinDock mengembalikan taskbar dan menu Mulai Windows ke perilaku normal.
- Aplikasi yang hanya punya ikon tray (tanpa jendela) tidak ditampilkan.
- Pemindai aplikasi membaca shortcut Start Menu; aplikasi tanpa shortcut tidak muncul di daftar scan.
- Ikon indikator baterai, jaringan, dan volume belum bisa diganti; ukurannya bisa diatur lewat slider quick action.
- Ikon kustom terikat ke path aplikasi. Jika aplikasi dipindah atau di-install ulang ke path berbeda, atur ulang ikonnya.

## Lisensi

WinDock Free bebas dipakai untuk keperluan pribadi maupun komunitas. Jangan mengklaim WinDock sebagai karya sendiri atau menghapus kredit pembuat aslinya. Perangkat lunak disediakan apa adanya, tanpa garansi.

WinDock Pro adalah lisensi berbayar permanen untuk satu perangkat. Kunci lisensi bersifat pribadi dan tidak boleh dibagikan atau dijual ulang. Alat pembuat kunci (keygen) hanya untuk penjual dan tidak disertakan dalam installer.
