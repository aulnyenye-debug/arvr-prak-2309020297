# Praktikum 1: Scene Perkenalan Diri (AR/VR)

- **Nama:** Dinda Aulia Putri
- **NIM:** 2309020297
- **Kelas:** Teknologi Informasi
- **Link Demo GitHub Pages:** https://aulnyenye-debug.github.io/arvr-prak-2309020297/

---

## Jawaban Pertanyaan Refleksi

### 1. Mengapa posisi objek yang terlihat pertama kali oleh pengguna memakai nilai z negatif?
Karena dari sananya di A-Frame, posisi awal kamera kita itu ada di titik `(0, 0, 0)` dan hadapnya ke depan lewat sumbu **Z negatif**. Makanya, kalau mau objeknya pas kelihatan di depan mata waktu web pertama kali dibuka, koordinat Z-nya harus minus (misal `-3` atau `-5`). Kalau kita isi positif, objeknya malah bakal ada di belakang kita, jadi nggak kelihatan apa-apa.

### 2. Mengapa WebXR hanya aktif pada HTTPS atau localhost?
Karena WebXR ini kan berhubungan langsung sama hardware sensitif kayak sensor gerak HP/laptop, kamera, atau headset VR. Demi keamanan dan privasi data kita biar nggak sembarangan diakses situs web, browser bikin aturan ketat: fitur WebXR cuma diizinkan jalan di tempat yang aman, yaitu pakai protokol HTTPS atau pas lagi dites lokal pakai `localhost`.

### 3. Jelaskan perbedaan peran WebXR Device API, three.js, dan A-Frame dengan bahasa Anda sendiri.
Gampangnya kita bagi jadi tiga tingkatan:
- **WebXR Device API:** Ini yang paling dasar/bawaan dari browser, tugasnya jadi jembatan penghubung antara kodingan kita sama perangkat keras VR/AR yang kita pakai.
- **three.js:** Ini library JavaScript yang ngebantu kita bikin dan ngurusin grafik 3D (kayak bentuk objek, cahaya, warna) biar nggak perlu nulis kode WebGL mentah dari nol yang ribet banget.
- **A-Frame:** Ini yang paling gampang dan paling tinggi tingkatannya. Dibuat pakai dasar HTML, jadi kita tinggal pakai tag-tag simpel kayak `<a-box>` atau `<a-sphere>` buat bikin objek 3D, karena di baliknya udah dibungkus rapi pakai three.js dan WebXR.