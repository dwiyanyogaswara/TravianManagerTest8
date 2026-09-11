# 4.14.15

- Memperbaiki scan resource field pada REFRESH VILLAGE agar ID field, GID, dan level selalu diambil dari elemen field yang sama.
- Tidak lagi menggunakan `gid=1` sebagai fallback; target dianggap valid hanya jika ID, GID, dan level terbaca.
- Pemilihan level terendah dilakukan dari pasangan `{fieldId, gid, level}` yang sudah tervalidasi, sehingga tidak tertukar antar-field.
- Link resource target dibentuk kembali dengan `gid` hasil scan dan `newdid` village yang sedang diverifikasi.
- DATABASE VILLAGE dan log scan menampilkan Resource ID dan GID untuk memudahkan verifikasi.
