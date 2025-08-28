# 🧑‍⚕️ Klasifikasi Objek dengan Transfer Learning (Face Mask Detection)

Proyek ini mendemonstrasikan cara melakukan **klasifikasi objek** menggunakan **ResNet18 pre-trained** dengan teknik **transfer learning** di PyTorch.  
Tujuannya adalah untuk membangun pengklasifikasi yang dapat membedakan antara gambar orang yang **memakai masker wajah** dan yang **tidak memakai masker**.

---

## 🎯 Tujuan Proyek
Mengembangkan dan melatih model CNN agar dapat mengklasifikasikan gambar secara akurat ke dalam dua kategori:
- `with_mask`
- `without_mask`

---

## 🛠️ Tumpukan Teknologi
- **Python 3**
- **PyTorch** – framework deep learning
- **Torchvision** – model pre-trained + transformasi gambar
- **Scikit-learn** – split data train/test
- **Matplotlib** – visualisasi grafik training
- **tqdm** – progress bar

---

## 📁 Dataset
Struktur dataset:  
.
└── data/
    ├── with_mask/
    └── without_mask/

- `with_mask/` : gambar orang memakai masker  
- `without_mask/` : gambar orang tanpa masker  

---

## 🧠 Arsitektur Model
- **Base model**: `ResNet18` pretrained di **ImageNet**  
- **Modifikasi**: lapisan fully-connected terakhir (`fc`) diganti dari 1000 kelas → 2 kelas  

---

## 🚀 Pelatihan & Evaluasi
- **Epochs**: 25  
- **Batch size**: 32  
- **Optimizer**: Adam (`lr=1e-4`)  
- **Loss function**: CrossEntropyLoss  

Training loop meliputi:
- `model.train()` → update bobot  
- `model.eval()` → hitung loss & akurasi pada data uji  

---

## 📊 Hasil
- Model mencapai akurasi tinggi pada data uji  
- Training dan test loss stabil → **tidak overfitting**  

---

## 🔧 Cara Menjalankan

1. **Kloning repositori**  
   ```bash
   git clone https://github.com/username/face-mask-dataset.git
   cd face-mask-dataset
