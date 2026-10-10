# Praktikum 1: Scene Perkenalan Diri (AR/VR)

- **Nama:** Dinda Aulia Putri
- **NIM:** 2309020297
- **Kelas:** Teknologi Informasi
- **Link Demo GitHub Pages:** https://aulnyenye-debug.github.io/arvr-prak-2309020297/

---

## Jawaban Pertanyaan Refleksi

### 1. Mengapa posisi objek yang terlihat pertama kali oleh pengguna memakai nilai z negatif?
Dalam sistem koordinat 3D A-Frame, kamera pengguna awal mulanya berada di titik asal `(0, 0, 0)` dan menghadap ke arah sumbu **Z negatif**. Oleh karena itu, agar suatu objek dapat berada tepat di depan pandangan mata pengguna saat pertama kali memuat halaman, posisi koordinat Z objek tersebut harus diberi nilai negatif (seperti `-3` atau `-5`). Jika nilai Z bernilai positif, objek akan berada di belakang pandangan pengguna.

### 2. Mengapa WebXR hanya aktif pada HTTPS atau localhost?
Sebab WebXR API memerlukan akses langsung ke perangkat keras sensor sensitif (seperti sensor pelacakan gerak, kamera, dan kacamata VR). Demi alasan keamanan dan privasi data pengguna, browser membatasi WebXR API agar **hanya boleh berjalan di lingkungan aman (Secure Context)** yaitu protokol **HTTPS** saat online, atau pada **`localhost` / `127.0.0.1`** untuk pengembangan lokal.

### 3. Jelaskan perbedaan peran WebXR Device API, three.js, dan A-Frame dengan bahasa Anda sendiri.
* **WebXR Device API:** Standar/API bawaan browser untuk menjembatani komunikasi langsung antara web dengan perangkat keras VR/AR (kacamata VR dan *controller*).
* **three.js:** Pustaka (*library*) JavaScript tingkat menengah untuk mengolah grafis 3D (pembuatan objek, material, pencahayaan) dengan lebih mudah tanpa menulis kode WebGL murni dari awal.
* **A-Frame:** Kerangka kerja (*framework*) tingkat tinggi berbasis HTML buatan Mozilla yang membungkus three.js dan WebXR Device API, sehingga kita bisa membangun scene 3D/VR secara deklaratif menggunakan tag HTML seperti `<a-scene>` dan `<a-box>`.