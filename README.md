# 🎵 Spotify Clone React

Project ini clone platform musik Spotify yang dibangun menggunakan ekosistem modern web development. Fokus utama project ini adalah performa pemutaran musik yang lancar dan sinkronisasi database. 

> **Catatan:** Cari tahu terlebih dahulu di AI karena files ini belum 100% mempunyai database/fitur yang lengkap bisa ke email saya : skyzoc1a@gmail.com atau wa : 088225879928

​🚀 STEP 1: PERSIAPAN LINGKUNGAN (PILIH SALAH SATU)
​A. Untuk Pengguna Laptop/PC (VS Code/Terminal)
​Jalankan perintah ini secara berurutan:
```text
npm create vite@latest spotify-clone -- --template react-ts
cd spotify-clone
npm install
npm install lucide-react howler wouter @tanstack/react-query @supabase/supabase-js drizzle-orm express
npm run dev
```
B. Untuk Pengguna HP (Termux)
​Wajib install Node.js terlebih dahulu:
```text
pkg update && pkg upgrade
pkg install nodejs-lts
npx create-vite spotify-clone --template react-ts
cd spotify-clone
npm install
npm install lucide-react howler wouter @tanstack/react-query @supabase/supabase-js
npm run dev -- --host
```
Note Termux: Jika terjadi error saat instalasi library, jalankan perintah termux-chroot sebelum running

 STEP 2: GENERATE CODE VIA AI (Gemini, GPT, DeepSeek, Claude, Grok)
​Gunakan prompt di bawah ini secara bertahap (satu-satu) agar AI tidak memberikan kode yang terpotong/hallucinate:

​1. Setup Database, Schema & Hooks (Logic & Data)
```text
​"Gue lagi bangun Spotify Clone. Buatkan struktur file shared/schema.ts untuk tabel lagu (id, title, artist, coverUrl, audioUrl). Lalu buatkan client/src/lib/supabase.ts untuk koneksi API dan client/src/hooks/use-store.ts menggunakan Howler.js untuk handle Play, Pause, dan Next lagu secara global."
```
untuk koneksi database dan client/src/hooks/use-store.ts menggunakan Howler.js untuk handle state global pemutar musik."

​2. Setup Backend & API (Server Side)
```text
"Buatkan file server/routes.ts menggunakan Express untuk menyediakan API endpoint daftar lagu, dan server/storage.ts 
```
untuk logika penyimpanan data ke database."


​3. Setup UI & Components (Frontend)
```text
​"Buatkan komponen React Player.tsx yang punya progress bar musik, SongCard.tsx untuk display album art, dan Sidebar.tsx. Gunakan Tailwind CSS. Pastikan slider progress musik bisa digeser (draggable)."
```
​4. Setup Halaman (Pages)
```text
​"Buatkan halaman Home.tsx untuk daftar lagu, Search.tsx untuk filter pencarian, dan Library.tsx. Hubungkan semuanya di App.tsx menggunakan library wouter."
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
