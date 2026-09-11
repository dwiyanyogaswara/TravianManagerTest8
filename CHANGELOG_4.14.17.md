# Changelog v4.14.17

## Resource Builder — Hero Resource Transfer DOM Click
- Memperbaiki alur saat resource village kurang untuk upgrade.
- Aplikasi sekarang mencari elemen DOM dengan class tepat `.inlineIcon.resource.transfer`.
- Aplikasi melakukan klik langsung pada elemen DOM (`el.click()`), sehingga `onclick="window.Travian.React.Hero.openResourceTransfer(...)"` milik Travian dijalankan secara natural.
- Tidak lagi memanggil `window.Travian.React.Hero.openResourceTransfer(...)` secara langsung dari aplikasi.
- Menghindari fallback ke selector umum `[onclick*="openResourceTransfer"]` yang berpotensi memilih elemen yang salah.
- Setelah DOM transfer diklik, aplikasi menunggu 900 ms lalu mencari dan mengklik tombol **Transfer Selected**.
- Jika elemen transfer tidak tersedia setelah retry, village dilewati dengan aman.
