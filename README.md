# Transfer Learning & Object Counting - Faster R-CNN

Proyek ini merupakan implementasi Object Detection menggunakan arsitektur **Faster R-CNN ResNet-50 FPN V2**. Fokus utama proyek adalah melakukan transfer learning pada dataset kustom, mengekspor model ke format universal (ONNX), dan melakukan perhitungan objek (*object counting*) dalam zona tertentu.

---

## 📑 Struktur Materi

### 1. 8.1 Transfer Learning (Google Colab)
* **Dataset:** Scissors Dataset dari Roboflow (Format COCO).
* **Model:** Faster R-CNN Pre-trained on COCO.
* **Output:** Model yang telah dilatih diekspor ke file `.onnx`.
* **Environment:** Membutuhkan GPU (T4 recommended).

### 2. 8.2 Inferencing (Local VS Code)
* Menggunakan **ONNX Runtime** untuk eksekusi model yang lebih ringan dan efisien.
* Penyelesaian masalah kompatibilitas pada OpenCV DNN (v4.7+).

### 3. 8.3 Object Counting (Local VS Code)
* **Library:** [Supervision](https://github.com/roboflow/supervision).
* **Fitur:** Menentukan zona deteksi menggunakan ROI Polygon secara interaktif dan menghitung jumlah objek yang masuk ke dalam area tersebut.

## Video Presentasi 



## ⚙️ Persiapan Environment

Gunakan Anaconda/Conda untuk manajemen environment:

### Environment 1: BelajarOpenCV (Untuk Deteksi Umum)
```bash
conda create --name BelajarOpenCV python=3.9
conda activate BelajarOpenCV
pip install opencv-python==4.7.0.72 numpy onnx onnxruntime

Environment 2: BelajarSuperVision (Untuk Object Counting)
Bash

conda create --name BelajarSuperVision python=3.8
conda activate BelajarSuperVision
pip install supervision ultralytics onnxruntime opencv-python

🚀 Cara Penggunaan

    Training: Jalankan notebook 8.1_Transfer_Learning_Faster_RCNN.ipynb di Google Colab. Pastikan memasukkan API Key Roboflow Anda.

    Download Model: Simpan file fasterrcnn_resnet50_fpn_v2_scissors.onnx ke folder model/ di direktori lokal Anda.

    Inference: Jalankan 8.2_Inference_ONNX.ipynb untuk melihat hasil deteksi pada gambar tunggal.

    Counting: Jalankan 8.3_Object_Counting.ipynb, pilih area ROI dengan mouse (drag), lalu tekan Enter untuk mulai menghitung.


👤 Anggota Kelompok

- Alfadrian Januarsyah (231001067)
- Tasri Zulfitriyati (231001074)

---


