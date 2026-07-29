# UAS Data Mining - Implementasi Supervised dan Unsupervised Learning

## 📋 Identitas Mahasiswa
- **Nama:** Harnanda
- **NIM:** 23146013
- **Mata Kuliah:** Data Mining (SIF304)
- **Dosen Pengampu:** Teuku Rizky Noviandy, S.Kom., M.Kom.

---

## 🎯 Penjelasan Proyek

Jadi proyek UAS ini saya buat aplikasi web interaktif pakai **Streamlit** untuk implementasi dua jenis teknik data mining yang udah dipelajarin di kelas. Basically, proyek ini ada 2 bagian utama yang bisa dicoba:

### A. Klasifikasi Diabetes (Supervised Learning) 🏥
Bagian ini tentang bikin model untuk prediksi risiko diabetes pasien berdasarkan data kesehatan mereka. Saya coba tiga algoritma yang udah dipelajarin di kelas:
- **K-Nearest Neighbors (KNN)** - yang ini berdasarkan tetangga terdekat, simple tapi ampuh
- **Naïve Bayes** - pakai probabilitas, straightforward dan cepat
- **Decision Tree** - yang ini kayak buat keputusan bertingkat-tingkat

Hasil evaluasinya bisa dilihat dari:
- **Accuracy** - berapa persen yang benar diprediksi
- **Precision** - dari yang diprediksi positif, berapa yang bener
- **Recall** - dari yang seharusnya positif, berapa yang ketangkap
- **F1-Score** - kombinasi precision dan recall
- **Confusion Matrix** - visualisasi akurat/salah prediksi

### B. Clustering Gerai Kopi (Unsupervised Learning) ☕
Bagian ini saya coba analisis klaster untuk liat pola sebaran gerai kopi dan cari tahu zona mana yang sepi/berisiko. Pakai algoritma **K-Means Clustering** buat ngomong-ngomong lokasi kopi berdasarkan:
- **Koordinat geografis** (latitude & longitude)
- **Kepadatan pelanggan** - berapa banyak orang di area
- **Tingkat kompetisi** - berapa banyak kompetitor di sekitar
- **Jarak ke pusat kota** - lokasi strategis atau enggak

---

## 🚀 Cara Jalanin Aplikasi (Lokal)

### 1️⃣ Clone Repository
Buka terminal/CMD dan jalankan:
```bash
git clone https://github.com/harnandamulia-max/harnanda-main.git
cd harnanda-main
```

### 2️⃣ Install Requirements
```bash
pip install -r requirements.txt
```

Atau kalo requirements.txt belum ada, install manual:
```bash
pip install streamlit pandas numpy scikit-learn matplotlib seaborn plotly
```

### 3️⃣ Jalanin Aplikasi
```bash
streamlit run app.py
```

Habis itu aplikasi otomatis buka di browser default kamu, biasanya di `http://localhost:8501`

---

## 📁 Struktur Folder Proyek

```
harnanda-main/
├── app.py                          # Main aplikasi Streamlit
├── requirements.txt                # Dependencies yang diperlukan
├── README.md                       # File ini
├── data/
│   ├── diabetes.csv               # Dataset diabetes untuk klasifikasi
│   └── coffee_shops.csv           # Dataset gerai kopi untuk clustering
├── models/                         # Folder model terlatih (optional)
└── utils/
    ├── preprocessing.py           # Fungsi preprocessing data
    ├── modeling.py                # Fungsi training model
    └── visualization.py           # Fungsi visualisasi hasil
```

---

## 📊 Dataset yang Digunakan

### Dataset Diabetes
- **Jumlah sample:** ~768 records
- **Feature:** Pregnancies, Glucose, BloodPressure, SkinThickness, Insulin, BMI, DiabetesPedigreeFunction, Age
- **Target:** Outcome (0 = No Diabetes, 1 = Diabetes)

### Dataset Coffee Shops
- **Jumlah sample:** Sesuai data yang diinput
- **Feature:** Latitude, Longitude, Customer Density, Competition Level, Distance to City Center
- **Output:** Cluster assignment untuk setiap gerai

---

## 🛠️ Tools & Library yang Dipakai

```
Streamlit      - Buat web app interaktif dengan Python
Pandas         - Data manipulation & analysis
NumPy          - Numerical computing
Scikit-learn   - Machine learning algorithms
Matplotlib     - Visualisasi grafik
Seaborn        - Visualisasi statistik
Plotly         - Interactive charts
```

---

## 📈 Hasil yang Bisa Dilihat

### Di Menu Klasifikasi Diabetes:
✅ Perbandingan akurasi ketiga model (KNN, Naïve Bayes, Decision Tree)  
✅ Confusion Matrix untuk masing-masing model  
✅ Precision, Recall, F1-Score detailed  
✅ Feature importance (terutama untuk Decision Tree)  
✅ Prediksi real-time dengan input data pasien baru  

### Di Menu Clustering Kopi:
✅ Visualisasi sebaran gerai kopi di peta (scatter plot)  
✅ Cluster assignment untuk setiap gerai  
✅ Centroid lokasi cluster  
✅ Karakteristik tiap cluster (rata-rata feature)  
✅ Silhouette score untuk validasi clustering  

---

## 🎓 Konsep yang Diimplementasikan

### Supervised Learning (Klasifikasi)
- **Data Splitting** - Train 70% : Test 30%
- **Feature Scaling** - Normalisasi data biar comparable
- **Cross Validation** - Validasi model multiple times
- **Hyperparameter Tuning** - Cari parameter terbaik

### Unsupervised Learning (Clustering)
- **Elbow Method** - Cari jumlah cluster optimal
- **K-Means Algorithm** - Iterative clustering
- **Silhouette Analysis** - Evaluasi kualitas clustering
- **Cluster Profiling** - Karakterisasi setiap cluster

---

## 💡 Tips Pemakaian Aplikasi

1. **Bagian Klasifikasi**: Upload atau pilih dataset, aplikasi otomatis train ketiga model dan comparison hasilnya
2. **Bagian Clustering**: Input parameter k (jumlah cluster), aplikasi akan visualisasi dan analisis sebaran gerai
3. **Export Hasil**: Bisa download hasil prediksi/clustering as CSV
4. **Parameter Tuning**: Coba-coba parameter berbeda di sidebar buat liat impact ke hasil

---

## ⚠️ Catatan Penting

- Pastikan Python version 3.7+ 
- Internet connection buat download package pertama kali
- RAM cukup (minimal 2GB) kalo dataset besar
- Kalo ada error, check lagi requirements.txt udah install semua

---

## 🤝 Kontribusi & Issues

Kalo ada bug atau saran, bisa buka issue di GitHub atau contact saya langsung. Thanks!

---

## 📝 License

Proyek ini dibuat untuk keperluan UAS mata kuliah Data Mining. 

**Created with ❤️ by Harnanda | 23146013**
