# 
<h1 align="center"> Brain-Tumor_Image-Classificationy</h1>
<p align="center"> Convolutional Neural Network</p>

# 🧠 Brain Tumor Classification with CNN

Proyek ini bertujuan untuk membangun sistem klasifikasi dengan dataset gambar MRI otak untuk deteksi keberadaan tumor menggunakan model Convolutional Neural Network (CNN). Dataset yang digunakan diambil dari Kaggle dengan dua kelas: **"Yes" (tumor)** dan **"No" (no tumor)**.

---

## 🔧 Teknologi yang Digunakan

- **Python + Google Colab** — Platform utama pemrograman dan eksperimen.
- **TensorFlow & Keras** — Untuk membangun dan melatih model deep learning CNN.
- **OpenCV (cv2)** — Untuk preprocessing gambar (meski penggunaannya minimal).
- **Pillow (PIL)** — Untuk manipulasi gambar seperti resize dan konversi warna.
- **Matplotlib** — Untuk visualisasi hasil pelatihan dan evaluasi model.
- **KaggleHub** — Untuk mengunduh dataset dari Kaggle langsung di Colab.

---

## 🧠 Arsitektur Model CNN

Model CNN yang digunakan memiliki arsitektur sederhana namun cukup efektif untuk klasifikasi biner:

```text
Input: (224, 224, 3)

→ Conv2D(32 filter, kernel=3x3, relu)
→ MaxPooling2D(pool=2x2)
→ Flatten
→ Dense(256, relu)
→ Dropout(0.5)
→ Dense(1, sigmoid)  → Output (1 = Tumor, 0 = Tidak Tumor)
