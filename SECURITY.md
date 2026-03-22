# Security Policy

Gue sangat menghargai keamanan kode di project Spotify Clone ini. Karena project ini terhubung ke database (Supabase), ada beberapa hal yang wajib diperhatikan.

## Versi yang Didukung 

Gue cuma kasih update keamanan buat versi terbaru yang ada di branch `main`.

| Versi | Status Keamanan |
| :--- | :--- |
| 1.0.x | ✅ Supported |
| < 1.0 | ❌ Not Supported |

🚨 Cara Melaporkan Celah Keamanan (Vulnerability)

**JANGAN** laporin celah keamanan lewat **Public Issues**. Kalau lu nemu bug yang bisa ngerusak database atau ngebocorin data:

1. Langsung laporin secara privat lewat **GitHub Security Advisory**.
2. Atau bisa hubungi gue lewat kontak yang ada di profil GitHub ini.
3. Jelasin langkah-langkah gimana celah itu bisa ditemuin.

🔒 Hal yang Harus Lu Jaga (PENTING!)

Gue udah nyiapin `.gitignore`, tapi tetep inget:
- **Jangan pernah hapus `.env` dari `.gitignore`.**
- Kalau lu nggak sengaja nge-push file `.env` ke GitHub, langsung **Ganti/Rollback** API Key lu di dashboard Supabase secepatnya!
- Semua file di folder `client/src/lib` adalah konfigurasi sensitif, jangan diubah sembarangan kalau nggak paham alurnya.

*Keamanan project ini adalah tanggung jawab kita bersama sebagai developer.*
