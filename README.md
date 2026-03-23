# 🎵 Spotify Clone React

Project ini clone platform musik Spotify yang dibangun menggunakan ekosistem modern web development. Fokus utama project ini adalah performa pemutaran musik yang lancar dan sinkronisasi database. 

> **Catatan:** Cari tahu terlebih dahulu di AI karena files ini belum 100% mempunyai database/fitur yang lengkap bisa ke email saya : skyzoc1a@gmail.com atau wa : 088225879928

​🚀 STEP 1: PERSIAPAN LINGKUNGAN (PILIH SALAH SATU)
​A. Untuk Pengguna Laptop/PC (VS Code/Terminal)
​Jalankan perintah ini secara berurutan:
```text
git clone https://github.com/Skyzo-himonoto/SpotifyClone-data
cd SpotifyClone-data
npm install
npm run dev
```
B. Untuk Pengguna HP (Termux)
​Wajib install Node.js terlebih dahulu:
```text
pkg update && pkg upgrade -y
pkg install nodejs-lts git -y
git clone https://github.com/Skyzo-himonoto/SpotifyClone-data
cd SpotifyClone-data
npm install
npm run dev -- --host
```
Note Termux: Jika terjadi error saat instalasi library, jalankan perintah termux-chroot sebelum running

 STEP 2: GENERATE CODE VIA AI (Gemini, GPT, DeepSeek, Claude, Grok)
​Gunakan prompt di bawah ini secara bertahap (satu-satu) agar AI tidak memberikan kode yang terpotong/hallucinate:

​1. Setup Database, Schema & Hooks (Logic & Data)
```text

​"Gue mau bangun Spotify Clone Full Stack. Pertama, buatkan shared/schema.ts menggunakan Drizzle ORM atau standar TypeScript untuk tabel songs (id, title, artist, coverUrl, audioUrl, duration) dan playlists.
​Lalu, buatkan client/src/lib/supabase.ts untuk koneksi API. Terakhir, buatkan client/src/hooks/use-store.ts menggunakan Howler.js dan Zustand (atau React Context) untuk state global musik. Harus ada fungsi: playSong(song), pause(), resume(), next(), previous(), dan volume(val). Pastiin logic durasi lagunya akurat."
```
untuk koneksi database dan client/src/hooks/use-store.ts menggunakan Howler.js untuk handle state global pemutar musik."

​2. Setup Backend & API (Server Side)
```text
"Lanjut ke backend. Buat file server/routes.ts pake Express. Gue butuh API endpoint:
​GET /api/songs (Ambil semua lagu dari Supabase).
​GET /api/songs/:id (Ambil detail satu lagu).
​POST /api/playlists (Buat playlist baru).
​Buatkan juga server/storage.ts untuk interface penyimpanan datanya. Pastiin ada handling error kalau koneksi database gagal." 
```
untuk logika penyimpanan data ke database."


​3. Setup UI & Components (Frontend)
```text
​"Sekarang buatkan UI Components di client/src/components/.
​Player.tsx: Harus ada progress bar yang bisa di-klik/drag (Draggable), display waktu (0:00 / 3:45), tombol shuffle, dan repeat.
​SongCard.tsx: Tampilan cover album yang punya efek hover 'Play Button' muncul di tengah.
​Sidebar.tsx: Navigasi yang responsif, ada menu Home, Search, dan Your Library.
​Gunakan Tailwind CSS dan Lucide Icons. Pastikan kodenya mendukung Dark Mode Spotify."
```
​4. Setup Halaman (Pages)
```text
​"Buatkan 3 halaman utama di client/src/pages/:
​Home.tsx: Tampilkan grid lagu dengan section 'Recently Played'.
​Search.tsx: Input search yang langsung filter daftar lagu secara real-time.
​Library.tsx: Tampilkan lagu yang udah di-like.
​Hubungkan semua halaman di client/src/App.tsx pake library wouter. Tambahkan juga Toaster di root biar kalau ada error/sukses Like lagu muncul notifikasi kecil di pojok."
```

​5. Tambahan: Optimasi Mobile & UU
```text
"Buatkan hook client/src/hooks/use-mobile.ts untuk mendeteksi ukuran layar. Jika user buka dari HP, buat Player.tsx otomatis berubah jadi mode 'Mini Player' yang bisa di-expand jadi 'Full Screen Player' dengan padding bawah pb-24 agar tidak tertutup navigasi."
```


​📂 STEP 3: STRUKTUR FILES (WAJIB SESUAI!)

​Pindahkan hasil kodingan ke folder masing-masing sesuai struktur Replit Pro:

​📁 client/src/components/ -> Player.tsx, SongCard.tsx, Sidebar.tsx.


📁 client/src/components/ui/ -> slider.tsx, toast.tsx, button.tsx, progress.tsx, dialog.tsx.
​

📁 client/src/hooks/ -> use-store.ts (Otak Musik), use-mobile.ts (Auto-Responsive).

​
📁 client/src/lib/ -> supabase.ts, uuid-utils.ts.
​

📁 client/src/pages/ -> Home.tsx, Search.tsx, Library.tsx.
​

📁 server/ -> routes.ts, storage.ts, index.ts.
​

📁 shared/ -> schema.ts.


​⚙️ STEP 4: KONFIGURASI DATABASE (.env)
​Buat file .env di folder paling luar (root) dan isi dengan kredensial lu:
```text
VITE_SUPABASE_URL=URL_SUPABASE_LU
VITE_SUPABASE_ANON_KEY=ANON_KEY_LU
DATABASE_URL=URL_POSTGRES_LU (Opsional)
```
🛠️ STEP 5: OPTIMASI & FIX (Gak baca bisulan)
​Fix Mobile Layout: Jika slider progress di HP tertutup navigasi bawah, buka Player.tsx dan tambahkan pb-24 pada container Full-Screen Player.
​Font Premium: Pastikan font Figtree atau Circular Std sudah terdaftar di index.html agar UI terlihat elegan.
​TypeScript Safety: Gunakan format .tsx agar kode divalidasi otomatis dan aman dari suspend GitHub.

​📝 CARA LAPOR BUG (ISSUES)
​Jika ada file yang hilang atau kodingan dari AI error, lapor ke GitHub:
​Buka tab Issues.
​Masukkan judul: [BUG] Nama Error.
​Screenshot: Cukup Copy-Paste atau Drag & Drop foto error lu langsung ke kotak pesan GitHub. Gue (AI) bakal bantu analisa lewat gambar tersebut!
bisa lewat email dan wa
