# ⚽ Simulasi Optimasi Formasi Sepak Bola — Hill Climbing Algorithm

> Tugas Project Mata Kuliah Kecerdasan Buatan  
> Topik: Pencarian Lokal dan Optimasi

## 📌 Deskripsi Proyek

Aplikasi web simulasi yang mengimplementasikan algoritma **Hill Climbing** untuk mengoptimalkan penempatan posisi pemain dalam formasi tim sepak bola. Sistem mengevaluasi setiap kombinasi penempatan berdasarkan atribut pemain (serangan, pertahanan, kecepatan, teknik) dan kecocokan dengan posisi formasi.

### Problem Statement
Diberikan 11 pemain dengan atribut masing-masing, temukan susunan formasi yang **memaksimalkan skor kekuatan tim** dengan mempertimbangkan kecocokan posisi setiap pemain.

### Fungsi Fitness
```
f(formasi) = Σ [ (atribut_pemain · bobot_posisi) × bonus_kecocokan_posisi ]
```

## 🧠 Algoritma yang Diimplementasikan

| Varian | Deskripsi | Kompleksitas |
|--------|-----------|--------------|
| **Simple HC** | Pilih 2 pemain acak, tukar jika skor naik. Berhenti di local optima. | O(n) per iterasi |
| **Steepest-Ascent HC** | Evaluasi semua 55 kemungkinan swap, pilih yang terbaik. | O(n²) per iterasi |
| **Stochastic HC** | Terima swap dengan probabilitas e^(Δ/T), bisa lolos local optima. | O(n) per iterasi |

## ✨ Fitur Aplikasi

- 🏟️ **Visualisasi lapangan** interaktif dengan 5 pilihan formasi (4-4-2, 4-3-3, 3-5-2, 4-5-1, 5-3-2)
- 👤 **Data 11 pemain** dengan atribut yang bisa dikustomisasi
- ⚙️ **Kontrol parameter** algoritma secara real-time
- 📈 **Grafik konvergensi** skor per iterasi
- 📋 **Log iterasi** step-by-step dengan deteksi local optima
- 📊 **Tab perbandingan** ketiga algoritma sekaligus

## 🚀 Demo

🌐 **Live App:** [namaproject.my.id](https://namaproject.my.id)  
🎥 **Video Demo:** [YouTube Link]

## 🛠️ Teknologi

- **Frontend:** HTML5, CSS3, Vanilla JavaScript
- **Visualisasi:** Chart.js 4.4.1, Canvas API
- **Deployment:** Railway + Domain .my.id (IDwebhost)
- **Version Control:** Git + GitHub

## 📁 Struktur Folder

```
football-hc-optimizer/
├── index.html          # Aplikasi utama (single file)
├── README.md           # Dokumentasi ini
└── railway.json        # Konfigurasi Railway (opsional)
```

## ⚙️ Cara Menjalankan Lokal

1. Clone repository ini:
   ```bash
   git clone https://github.com/USERNAME/football-hc-optimizer.git
   ```
2. Masuk ke folder:
   ```bash
   cd football-hc-optimizer
   ```
3. Buka `index.html` di browser (double-click atau gunakan Live Server di VS Code)

Tidak memerlukan instalasi dependencies — aplikasi berjalan langsung di browser.

## 📖 Cara Penggunaan

1. **Tab "Data Pemain"** — Lihat/acak atribut pemain, pilih formasi dan bobot strategi tim
2. **Tab "Simple HC"** — Jalankan atau step-by-step simulasi Simple Hill Climbing
3. **Tab "Steepest-Ascent HC"** — Jalankan Steepest-Ascent yang mengevaluasi semua tetangga
4. **Tab "Stochastic HC"** — Jalankan Stochastic HC dengan parameter suhu
5. **Tab "Perbandingan"** — Bandingkan ketiga algoritma sekaligus, lihat tabel dan grafik

## 📊 Hasil Simulasi

| Algoritma | Keunggulan | Kelemahan |
|-----------|-----------|-----------|
| Simple HC | Cepat, mudah dipahami | Mudah terjebak local optima |
| Steepest-Ascent | Konsisten, selalu pilih terbaik | Lambat (55 evaluasi/iterasi) |
| Stochastic HC | Bisa lolos local optima | Tidak selalu konvergen ke global optimum |

## 👤 Author

**[Nama Lengkap]**  
NIM: [NIM]  
Program Studi: Teknik Informatika  
Mata Kuliah: Kecerdasan Buatan

## 📄 Lisensi

MIT License — bebas digunakan untuk keperluan akademik.