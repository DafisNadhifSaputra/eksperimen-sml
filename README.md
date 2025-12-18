# Eksperimen SML - Breast Cancer Classification
## Proyek Akhir: Membangun Sistem Machine Learning
### Dicoding Indonesia

---

**Nama**: Dafis Nadhif Saputra

---

## 📋 Deskripsi Proyek

Proyek ini melakukan eksperimen machine learning untuk klasifikasi **Breast Cancer Wisconsin (Diagnostic)** dataset. Tujuan adalah memprediksi apakah tumor bersifat **malignant** (ganas) atau **benign** (jinak) berdasarkan fitur-fitur hasil pemeriksaan.

## 📊 Dataset

- **Nama**: Breast Cancer Wisconsin (Diagnostic)
- **Sumber**: UCI Machine Learning Repository / sklearn.datasets
- **Samples**: 569
- **Features**: 30 fitur numerik
- **Target**: Binary (0 = Malignant, 1 = Benign)

### Fitur Dataset:
- Mean, standard error, dan "worst" dari:
  - Radius, Texture, Perimeter, Area
  - Smoothness, Compactness, Concavity
  - Concave points, Symmetry, Fractal dimension

## 📁 Struktur Repository

```
eksperimen-sml/
├── README.md
├── requirements.txt
├── data/
│   └── breast_cancer_data.csv
├── notebooks/
│   └── eksperimen_notebook.ipynb
├── src/
│   └── Dafis-Nadhif-Saputra.py    # Script preprocessing otomatis
└── .github/
    └── workflows/
        └── preprocessing.yml       # GitHub Actions untuk preprocessing
```

## 🚀 Cara Menjalankan

### 1. Clone Repository
```bash
git clone https://github.com/YOUR_USERNAME/eksperimen-sml.git
cd eksperimen-sml
```

### 2. Install Dependencies
```bash
pip install -r requirements.txt
```

### 3. Jalankan Eksperimen (Notebook)
```bash
jupyter notebook notebooks/eksperimen_notebook.ipynb
```

### 4. Jalankan Preprocessing Otomatis
```bash
python src/Dafis-Nadhif-Saputra.py \
  --input data/breast_cancer_data.csv \
  --output data/preprocessed_data.csv \
  --target target \
  --scaling standard
```

## 📈 Hasil Eksperimen

### Baseline Model: Random Forest Classifier
- **Accuracy**: ~96%
- **Precision**: ~95%
- **Recall**: ~96%
- **F1-Score**: ~95%

## 🔧 GitHub Actions

Repository ini dilengkapi dengan GitHub Actions workflow yang dapat melakukan preprocessing secara otomatis setiap kali ada perubahan pada folder `data/`.

Workflow akan:
1. Checkout repository
2. Setup Python environment
3. Install dependencies
4. Menjalankan script preprocessing
5. Menyimpan hasil sebagai artifact

## 📝 Kriteria Dicoding

✅ Melakukan tahapan eksperimentasi (data loading, EDA, preprocessing)  
✅ Membuat file automate preprocessing (`Dafis-Nadhif-Saputra.py`)  
✅ Struktur folder preprocessing berbeda dari notebook eksperimen  
✅ Membuat workflow GitHub Actions untuk preprocessing  

---

**© 2024 Dafis Nadhif Saputra - Dicoding Indonesia**
