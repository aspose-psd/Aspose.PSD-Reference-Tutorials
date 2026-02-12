---
date: 2026-02-12
description: Pelajari cara memutar gambar pada sudut tertentu dalam Java menggunakan
  Aspose.PSD. Panduan ini menunjukkan cara memutar gambar, memutar gambar dengan derajat,
  dan menangani warna latar belakang.
linktitle: How to Rotate Image on a Specific Angle
second_title: Aspose.PSD Java API
title: Cara Memutar Gambar pada Sudut Tertentu dengan Aspose.PSD untuk Java
url: /id/java/advanced-image-manipulation/rotate-image-specific-angle/
weight: 20
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cara Memutar Gambar pada Sudut Tertentu dengan Aspose.PSD untuk Java

## Introduction

Jika Anda perlu **cara memutar gambar** secara programatis dalam aplikasi Java, Aspose.PSD untuk Java menawarkan API yang bersih, berperforma tinggi, dan menangani semua pekerjaan berat. Baik Anda sedang membangun editor foto, menghasilkan thumbnail, atau menyiapkan aset untuk layanan web, memutar gambar dengan derajat yang tepat adalah kebutuhan umum. Pada tutorial ini kami akan membahas proses lengkap—dari memuat file PSD hingga menyimpan hasil yang diputar—serta menyoroti praktik terbaik seperti caching dan penanganan latar belakang.

## Quick Answers
- **Perpustakaan apa yang terbaik untuk memutar gambar di Java?** Aspose.PSD untuk Java.  
- **Apakah saya dapat memutar dengan derajat berapa pun?** Ya, metode `rotate` menerima sudut `float` (positif atau negatif).  
- **Apakah saya memerlukan lisensi untuk pengembangan?** Versi percobaan gratis dapat digunakan untuk pengujian; lisensi diperlukan untuk produksi.  
- **Format gambar apa yang didukung?** PSD, JPEG, PNG, TIFF, GIF, BMP, dan banyak lagi.  
- **Bagaimana cara mengatur warna latar belakang untuk ruang kosong?** Berikan instance `Color` ke metode `rotate`.

## What is Image Rotation in Java?

Rotasi gambar berarti memutar matriks piksel di sekitar titik pivot (biasanya pusat) dengan sudut tertentu. Di Java, Anda dapat melakukannya secara manual dengan `Graphics2D`, tetapi Aspose.PSD menyederhanakan perhitungan, menangani kedalaman warna yang berbeda, dan mempertahankan informasi lapisan saat bekerja dengan file PSD.

## Why Use Aspose.PSD for Rotating Images?

- **Presisi:** Memutar dengan derajat pecahan apa pun tanpa kehilangan kualitas.  
- **Kinerja:** Caching bawaan (`image.cacheData()`) mempercepat pemrosesan file besar.  
- **Kontrol Latar Belakang:** Tentukan warna latar untuk mengisi celah yang terbentuk akibat rotasi.  
- **Fleksibilitas Format:** Muat PSD, keluarkan JPEG, PNG, atau format lain yang didukung.

## Prerequisites

Sebelum memulai, pastikan Anda memiliki hal‑hal berikut:

1. **Java Development Kit (JDK 8 atau lebih baru)** – IDE Java yang berfungsi atau pengaturan command‑line.  
2. **Aspose.PSD untuk Java** – unduh JAR terbaru dari [halaman Aspose.PSD Java](https://reference.aspose.com/psd/java/).  
3. **File PSD contoh** – misalnya `sample.psd` yang ditempatkan di folder yang dapat Anda referensikan dari kode.

## Import Packages

Pertama, impor kelas‑kelas yang diperlukan. Impor ini tetap sama terlepas dari sudut rotasi yang Anda pilih.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imageoptions.JpegOptions;
```

## Step‑by‑Step Guide

### Step 1: Define Your Document Directory

Tetapkan folder yang berisi PSD sumber dan tempat output akan ditulis.

```java
String dataDir = "Your Document Directory";
```

> **Tip profesional:** Gunakan path absolut atau `System.getProperty("user.dir")` untuk menghindari kejutan path relatif.

### Step 2: Specify Source and Destination File Paths

```java
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "RotatingImageOnSpecificAngle_out.jpg";
```

Anda dapat mengubah `destName` ke ekstensi yang didukung apa pun (`.png`, `.tiff`, dll.) sesuai kebutuhan output Anda.

### Step 3: Load the Image

```java
RasterImage image = (RasterImage)Image.load(sourceFile);
```

`Image.load` secara otomatis mendeteksi format file dan mengembalikan objek `RasterImage` konkret untuk operasi berbasis raster.

### Step 4: Cache Image Data (Optional but Recommended)

```java
if (!image.isCached())
{
    image.cacheData();
}
```

Caching menyimpan piksel gambar di memori, yang mempercepat transformasi selanjutnya—terutama berguna untuk file PSD berukuran besar.

### Step 5: Rotate the Image

```java
image.rotate(20f, true, Color.getRed());
```

- **20f** – sudut rotasi dalam derajat (float). Ubah nilai ini untuk memutar dengan sudut apa pun, misalnya `-45f` untuk berlawanan arah jarum jam.  
- **true** – pertahankan rasio aspek asli sambil memperluas kanvas agar muat gambar yang diputar.  
- **Color.getRed()** – warna latar yang mengisi sudut kosong yang terbentuk akibat rotasi. Ganti dengan `Color.getWhite()` atau warna khusus lain sesuai kebutuhan.

#### Rotate Image by Degrees in Java

Metode `rotate` menerima nilai floating‑point apa pun, sehingga Anda dapat **memutar gambar dengan derajat** seperti `30f`, `90f`, atau `-15f`. Nilai positif memutar searah jarum jam, sementara nilai negatif memutar berlawanan arah jarum jam.

#### Rotate Image Specific Angle Using Aspose.PSD

Karena metode ini bekerja dengan `float`, Anda dapat menentukan **sudut rotasi gambar tertentu** seperti `22.5f` untuk kontrol presisi dalam alur kerja desain grafis.

#### Rotate Image Java Example Summary

Semua langkah di atas menunjukkan alur kerja **rotate image java** yang lengkap—dari memuat file hingga menyimpan output yang diputar.

### Step 6: Save the Result

```java
image.save(destName, new JpegOptions());
```

`JpegOptions` memungkinkan Anda mengontrol kualitas, kompresi, dan pengaturan khusus JPEG lainnya. Untuk output lossless, ganti dengan `PngOptions`.

## Common Issues and Solutions

| Masalah | Penyebab | Solusi |
|---------|----------|--------|
| **Sudut kosong setelah rotasi** | Tidak ada warna latar yang diberikan | Berikan `Color` (misalnya `Color.getWhite()`) ke `rotate`. |
| **Kesalahan out‑of‑memory pada PSD besar** | Gambar tidak di‑cache | Panggil `image.cacheData()` sebelum memproses. |
| **Arah sudut tidak tepat** | Kebingungan antara nilai negatif dan positif | Gunakan nilai negatif untuk rotasi searah jarum jam (atau sebaliknya tergantung sistem koordinat Anda). |
| **Perubahan tidak tersimpan** | Lupa memanggil `save` | Pastikan `image.save(...)` dijalankan setelah rotasi. |

## Frequently Asked Questions

**Q: Bisakah saya memutar gambar dengan transparansi menggunakan Aspose.PSD untuk Java?**  
A: Ya. Perpustakaan mempertahankan kanal alfa; cukup hindari menentukan warna latar yang tidak tembus jika Anda menginginkan sudut transparan.

**Q: Apakah ada batasan pada format file gambar yang didukung untuk rotasi?**  
A: Tidak. Aspose.PSD mendukung PSD, JPEG, PNG, TIFF, GIF, BMP, JPEG2000, WMF, EMF, dan banyak lagi.

**Q: Bisakah saya memutar gambar dengan sudut negatif?**  
A: Tentu saja. Berikan nilai float negatif ke `rotate` (misalnya `-30f`) untuk memutar searah jarum jam.

**Q: Apakah Aspose.PSD menyediakan pratinjau gambar secara real‑time selama rotasi?**  
A: API ini hanya sisi server. Untuk pratinjau langsung, integrasikan bitmap yang diputar ke dalam kerangka UI (Swing, JavaFX) dan segarkan tampilan.

**Q: Apakah ada forum komunitas untuk Aspose.PSD tempat saya dapat mencari bantuan?**  
A: Ya, kunjungi [forum Aspose.PSD](https://forum.aspose.com/c/psd/34) untuk mengajukan pertanyaan dan berbagi pengalaman.

## Conclusion

Anda kini mengetahui **cara memutar gambar** pada sudut tertentu menggunakan Aspose.PSD untuk Java. Dengan memanfaatkan caching, kontrol warna latar, dan opsi output yang fleksibel, Anda dapat mengintegrasikan fungsi rotasi yang presisi ke dalam alur kerja gambar berbasis Java mana pun.

---

**Last Updated:** 2026-02-12  
**Tested With:** Aspose.PSD untuk Java 24.11 (terbaru pada saat penulisan)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}