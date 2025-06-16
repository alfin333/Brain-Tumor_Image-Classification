<h1 align="center"> Brain-Tumor_Image-Classificationy</h1>
<p align="center"> Convolutional Neural Network</p>

### Name : Muhammad Alfin

# 🧠 Brain Tumor Classification with CNN

Proyek ini bertujuan untuk membangun sistem klasifikasi dengan dataset gambar MRI otak untuk deteksi keberadaan tumor menggunakan model Convolutional Neural Network (CNN). Dataset yang digunakan diambil dari Kaggle dengan dua kelas: **"Yes" (tumor)** dan **"No" (no tumor)**.
---
## ❗Saran Penting

- Jalankan file "Tumor_Otak_by_Alfin.ipynb" pada Google collab agar tidak ada kendala
---

## 🔧 Teknologi yang Digunakan

- **Python + Google Colab** — Platform utama pemrograman dan eksperimen.
- **TensorFlow & Keras** — Untuk membangun dan melatih model deep learning CNN.
- **OpenCV (cv2)** — Untuk preprocessing gambar (meski penggunaannya minimal).
- **Pillow (PIL)** — Untuk manipulasi gambar seperti resize dan konversi warna.
- **Matplotlib** — Untuk visualisasi hasil pelatihan dan evaluasi model.
- **KaggleHub** — Untuk mengunduh dataset dari Kaggle langsung di Colab.

---

## 🏢 Arsitektur Model CNN

Model CNN yang digunakan memiliki arsitektur sederhana namun cukup efektif untuk klasifikasi biner:

```text
Input: (224, 224, 3)

→ Conv2D(32 filter, kernel=3x3, relu)
→ MaxPooling2D(pool=2x2)
→ Flatten
→ Dense(256, relu)
→ Dropout(0.5)
→ Dense(1, sigmoid)  → Output (1 = Tumor, 0 = Tidak Tumor)

```
---
## 🔄 Cara Kerja Sistem Deteksi

📥 Dataset Import
- Gambar MRI otak dikumpulkan dari dua folder: yes/ (mengandung tumor) dan no/ (tidak ada tumor).

🧽 Preprocessing

- Semua gambar diubah ke ukuran 224x224 piksel.

- Konversi ke format RGB (jika grayscale).

- Normalisasi ke rentang [0,1].

🏷️ Labeling

- Kelas "tumor" dilabeli 1

- Kelas "no tumor" dilabeli 0

📊 Split Data
- Dataset dibagi menjadi:

- 80% data latih

- 20% data uji

🧠 Training CNN

- Model dilatih selama 10 epoch dengan batch size 32.

🧪 Evaluasi & Visualisasi

- Akurasi dan loss ditampilkan dalam bentuk grafik.

- Evaluasi dilakukan pada data uji.

📷 Prediksi Gambar Baru

- Pengguna dapat upload gambar MRI otak dan sistem akan memprediksi apakah gambar tersebut mengandung tumor atau tidak.
