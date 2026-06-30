<img width="655" height="172" alt="image" src="https://github.com/user-attachments/assets/270a185e-0f4c-42bc-afa8-4c0cd200e61e" /># 🌊 HabitRiver - Flow Your Progress, Level Up Your Life

**HabitRiver** adalah aplikasi pelacak kebiasaan (*habit-tracking*) berbasis web yang mengombinasikan visualisasi data modern dengan sistem **gamifikasi (RPG)** untuk membantu pengguna membangun kebiasaan produktif secara konsisten dan menyenangkan. 

Proyek ini dibangun menggunakan teknologi **Vanilla HTML, CSS, dan JavaScript murni** sebagai bagian dari eksperimen proyek pribadi untuk mengeksplorasi manipulasi DOM, manajemen state lokal, logika algoritma berbasis waktu, serta integrasi library visualisasi data.

---

## ✨ Fitur Utama

- **🔥 Dynamic Streak Counter**: Algoritma cerdas yang menghitung runtunan hari berturut-turut keberhasilan habit. *Streak* akan otomatis pecah (*reset* ke 0) jika ada satu hari yang terlewat.
- **🎮 RPG Leveling & XP System**: Setiap menyelesaikan habit harian, pengguna mendapatkan **+15 XP**. Akumulasi XP yang mencukupi akan menaikkan level profil pemain secara otomatis.
- **🏆 Top Chart (Leaderboard Simulator)**: Sistem papan peringkat *real-time* yang mensimulasikan persaingan sehat antara skor total XP pengguna dengan bot kompetitor cerdas.
- **📊 Weekly Progress Analytics**: Integrasi **Chart.js** untuk menyajikan grafik garis tren penyelesaian seluruh habit selama 7 hari terakhir.
- **🟩 GitHub-style Contribution Grid**: Visualisasi mini 7 hari ke belakang menggunakan kotak indikator warna (hijau untuk selesai, abu-abu untuk kosong).
- **🏷️ Category Management & Filtering**: Pengelompokan habit berdasarkan kategori khusus (💻 Coding, 🏃 Health, 📚 Study, 💰 Finance) lengkap dengan menu filter interaktif.
- **🌙 Adaptive Light/Dark Mode Toggle**: Fitur perpindahan tema yang halus dengan perbaikan kontras penuh pada seluruh komponen antarmuka, termasuk area profil level.
- **💾 Persistent LocalStorage**: Seluruh data profil, riwayat habit, dan tema disimpan secara lokal di dalam *browser*, sehingga data tidak hilang saat halaman di-*refresh*.

---

## 🛠️ Stack Teknologi

- **Frontend**: HTML5, CSS3 (Custom Variables & Flexbox/Grid Layout)
- **Scripting**: Vanilla JavaScript (ES6+)
- **Library & API**: [Chart.js](https://www.chartjs.org/) (via CDN)
- **Storage**: Browser LocalStorage API

---

## 📂 Struktur File

```text
habit-river/
│
├── index.html        # Struktur markup dashboard & layout dua kolom
├── style.css         # Desain responsif, CSS variables, & styling tema adaptif
├── script.js         # Logika algoritma (Streak, XP, Filter, Chart, & CRUD)
└── README.md         # Dokumentasi proyek
```

🚀 Cara Menjalankan Secara Lokal

Proyek ini sepenuhnya berjalan di sisi klien (client-side), sehingga tidak memerlukan instalasi backend server atau database rumit.

1. Clone atau Unduh Repository Ini
   git clone [https://github.com/username-kamu/habit-river.git](https://github.com/username-kamu/habit-river.git)

2. Buka Folder Proyek
   Masuk ke dalam direktori tempat kamu menyimpan file proyek.

3. Jalankan di Browser
   Klik dua kali pada file index.html atau gunakan ekstensi Live Server di VS Code untuk membukanya secara langsung di browser pilihanmu.


🧠 Logika Algoritma Penting
1. Kalkulasi Streak Beruntun
Aplikasi ini tidak sekadar menghitung total centang, melainkan melakukan looping mundur berbasis objek tanggal dari hari ini untuk memeriksa apakah rantai harian terputus:

