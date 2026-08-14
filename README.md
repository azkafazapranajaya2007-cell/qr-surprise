Dokumentasi Teknis: Aplikasi Web Interaktif berbasis 3D Transform dan Event-Driven Webhook
 
Ringkasan Proyek
Aplikasi berbasis web ini dikembangkan untuk menyajikan antarmuka interaktif bertahap (multi-stage interface) dengan memanfaatkan teknologi manipulasi 3D CSS3, pemrosesan partikel dinamis via JavaScript, serta integrasi pemantauan real-time berbasis asynchronous Webhook.
 
---
 
Spesifikasi Fitur dan Alur Sistem
 
1. Fase Pertama: Rendering & Transisi Kartu 3D
*3D Card Throw Animation: Implementasi animasi masuk berbasis ruang 3D menggunakan properti `perspective` dan `transform-style: preserve-3d`.
*Audio Interaktivitas Pemicu: Eksekusi aset audio (sound effect) saat terjadi interaksi pemicu pertama pada dokumen HTML.
*Morphing Transition: Transisi bentuk (shape morphing) dari objek kartu awal menuju komponen amplop secara halus melalui manipulasi kelas CSS.
 
2. Fase Kedua: Komponen Amplop & Interaksi Lilin
*Simulasi Pembukaan Amplop: Visualisasi gerak penutup amplop secara sistematis menggunakan kalkulasi rotasi sumbu X pada CSS3.
*Generasi Elemen Latar Belakang: Pembentukan elemen visual bintang secara dinamis menggunakan algoritma acak (random placement) berbasis DOM Manipulation.
*Mekanisme Pemicu Pesan: Penghentian animasi objek lilin oleh pemicu dari pengguna untuk menginisiasi rutinitas efek teks (Typewriter Effect).
 
3. Fase Ketiga: Percabangan Respon & Animasi Partikel
Sistem menyediakan tiga jalur percabangan logika visual berdasarkan masukan pengguna:
 
1. Modus 'Menyayangi':
   * Penyesuaian skema warna antarmuka ke mode ‘Love Red’ (#2b0a1a).
   * Penerapan animasi periodik `heartbeatPulse` serta generasi partikel confetti  khusus.
2. Modus 'Melampiaskan':
   * Penyesuaian skema warna ke mode ‘Rage Dark’ (#1a0000).
   * Animasi frekuensi tinggi `rageShake` yang dipadukan dengan overlay tekstur `damaged-card`.
   * Simulasi Partikel Kompleks: Eksekusi fragmen destruktif (`shatterExplode`) di mana elemen objek dihancurkan, lalu koordinat partikel dihitung ulang untuk membentuk pola objek bulan di area latar.
3. Modus 'Merelakan':
   * Penyesuaian skema warna ke mode ‘Midnight Peace’ (#0b1325).
   * Animasi transisi mengapung (`floatPeace`) dipadukan dengan partikel bernuansa monokrom.
   * Simulasi Partikel Kompleks: Penurunan opasitas dan pemutaran koordinat objek (`disintegrate-ash`) yang mentransformasikan elemen menjadi gugusan partikel bintang baru di latar belakang.
 
4. Integrasi Eksternal & Sistem Audio
*Integrasi Discord Webhook: Pengiriman data payload masukan pengguna (user choice) secara ‘asynchronous’ menggunakan Fetch API menuju endpoint Discord Webhook.
*Sistem Audio Fallback: Implementasi `Web Audio API Synthesizer` sebagai mekanisme ‘fallback’ untuk menghasilkan nada sinusoidal dasar apabila aset audio lokal gagal dimuat.
*Fitur Tersembunyi (Easter Egg): Penanganan rekursif pada jumlah klik ikon untuk memicu modal dialog sekunder.
 
---
 
Teknologi dan Pustaka yang Digunakan
 
*HTML5 & CSS3: Struktur dokumen, Glassmorphism UI, CSS Variables, dan `@keyframes` animation.
*Vanilla JavaScript (ES6+): Manipulasi DOM, penanganan ‘asynchronous’, dan Web Audio API.
*Canvas Confetti API: Pustaka eksternal untuk penanganan komputasi sistem partikel ‘confetti’.
 
---
 
Panduan Pengoperasian Lokal
 
1. Melakukan kloning repositori:
   ```bash
   git clone [https://github.com/USERNAME/qr-surprise.git](https://github.com/USERNAME/qr-surprise.git)