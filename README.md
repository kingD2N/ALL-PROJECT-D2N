# 🚀 Custom Kernel & Recovery untuk [POCO F4 GT / (ingres)

[![Build Status](https://img.shields.io/badge/build-POCO_F4_GT-brightgreen.svg)](#)
[![License](https://img.shields.io/badge/License-BAPADAAN™-blue.svg)](https://www.gnu.org/licenses/gpl-2.0)
[![Maintainer](https://img.shields.io/badge/Maintainer-kingD2N-orange.svg)](#)

Selamat datang di repositori resmi untuk pengembangan Custom Kernel dan Custom Recovery (TWRP & OrangeFox) khusus untuk perangkat **POCO F4 GT** dengan codename **`[codename_device, misal: ingres]`**.

---

## ⚠️ PERINGATAN (DISCLAIMER)

> **Garansi Anda mungkin hangus.**
> Saya tidak bertanggung jawab atas perangkat yang brick (mati total), SD card yang rusak, perang termonuklir, atau Anda dipecat karena alarm tidak berbunyi. Silakan lakukan riset terlebih dahulu jika Anda memiliki kekhawatiran tentang fitur-fitur yang disertakan di dalam kernel atau recovery ini sebelum melakukan instalasi (flashing). ANDA yang memilih untuk melakukan modifikasi ini.

---

## 📚 Memahami Konsep Dasar

Bagi Anda yang baru terjun ke dunia modifikasi Android, berikut adalah penjelasan lengkap mengenai komponen-komponen yang ada di repositori ini:

### 1. Apa itu KERNEL?
Kernel adalah program inti (core) dari sistem operasi Android yang bertindak sebagai "jembatan" antara perangkat keras (hardware) dan perangkat lunak (software). 
* **Fungsi Utama:** Mengatur bagaimana CPU, GPU, RAM, dan baterai bekerja. 
* **Custom Kernel:** Adalah kernel bawaan pabrik yang telah dimodifikasi oleh developer (seperti di repositori ini) untuk membuka potensi maksimal perangkat. Modifikasi ini memungkinkan fitur seperti *Overclocking* (meningkatkan kecepatan prosesor), *Underclocking/Undervolting* (menghemat baterai dan mengurangi panas), pengaturan warna layar kustom, dan optimasi performa gaming.

### 2. Apa itu TWRP (Team Win Recovery Project)?
Secara bawaan, setiap HP Android memiliki mode "Recovery" bawaan pabrik yang fiturnya sangat terbatas (biasanya hanya untuk Factory Reset). **TWRP** adalah Custom Recovery open-source yang menggantikan recovery bawaan tersebut.
* **Fitur Utama:** Berbasis layar sentuh (touch interface), memungkinkan pengguna menginstal (flash) Custom ROM, Custom Kernel, Magisk/KernelSU (untuk akses Root), serta melakukan backup dan restore sistem secara menyeluruh (Nandroid Backup).

### 3. Apa itu OrangeFox Recovery?
OrangeFox adalah salah satu Custom Recovery paling populer saat ini yang pada dasarnya dibangun dari source code TWRP, namun diberikan "steroid".
* **Kelebihan dibanding TWRP biasa:** Memiliki antarmuka (UI) yang jauh lebih modern dan bisa dikustomisasi, pembaruan yang lebih rutin, dukungan bawaan untuk pembaruan OTA (Over-The-Air) pada Custom ROM tertentu, dukungan script in-built (seperti Magisk uninstaller/installer), dan fitur keamanan tambahan seperti proteksi password/PIN.

---

## ✨ Fitur-Fitur di Repositori Ini

### ⚡ Fitur Custom Kernel
* Di-compile menggunakan *toolchain* terbaru (misal: Proton Clang / GCC).
* Optimasi manajemen RAM (*Low Memory Killer*).
* Penambahan *CPU/GPU Governor* kustom untuk performa gaming (mengurangi stutter/lag).
* Dukungan Fast Charging kustom (opsional).
* Mendukung **KernelSU** secara bawaan (in-built).

### 🦊 Fitur Custom Recovery (OrangeFox/TWRP)
* Mendukung Dekripsi Data (FBE / FDE) untuk Android versi terbaru.
* Mendukung MTP dan USB OTG.
* Desain UI yang mulus dan interaktif.
* Flash `.img` dan `.zip` dengan lancar.

---

## 📋 Persyaratan (Prerequisites)

Sebelum menginstal apapun dari repositori ini, pastikan:
1. Bootloader perangkat Anda **SUDAH DIBUKA (Unlocked Bootloader)**.
2. Anda menggunakan perangkat yang tepat (Hanya untuk **`[Codename_Device]`**).
3. Baterai minimal 50% untuk mencegah perangkat mati saat proses instalasi.
4. Anda sudah membackup seluruh data penting Anda.

---

## 🛠️ Panduan Instalasi (Flashing Guide)

### Bagian 1: Instalasi Recovery (OrangeFox / TWRP)
Jika Anda menggunakan PC dan belum memiliki Custom Recovery:
1. Unduh file `recovery.img` dari bagian [Releases](#).
2. Reboot perangkat Anda ke mode **Fastboot** (Tekan dan tahan tombol `Power` + `Volume Bawah`).
3. Hubungkan perangkat ke PC menggunakan kabel USB.
4. Buka Terminal/CMD di PC Anda dan ketikkan perintah berikut:
   ```bash
   fastboot flash recovery recovery.img
   fastboot boot recovery.img
