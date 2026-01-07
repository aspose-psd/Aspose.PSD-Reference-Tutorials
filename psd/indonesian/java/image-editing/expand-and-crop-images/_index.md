---
date: 2026-01-07
description: Pelajari cara memotong gambar menggunakan Java dengan Aspose.PSD untuk
  Java. Panduan langkah demi langkah untuk memotong gambar, mengubah ukuran, dan mengonversi
  dari PSD ke JPEG.
linktitle: Expand and Crop Images
second_title: Aspose.PSD Java API
title: 'Potong Gambar Java: Perluas dan Potong Gambar dengan Aspose.PSD untuk Java'
url: /id/java/image-editing/expand-and-crop-images/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Crop Image Java: Memperluas dan Memotong Gambar dengan Aspose.PSD untuk Java

## Introduction

Dalam tutorial ini Anda akan menemukan cara **crop image java** dengan perpustakaan Aspose.PSD. Baik Anda perlu memperluas kanvas, memotong tepi yang tidak diinginkan, atau mengonversi file PSD ke JPEG, langkah‑langkah di bawah ini akan memandu Anda melalui proses yang bersih dan dapat diulang. Kami akan membahas prasyarat, pernyataan impor, dan setiap langkah kode dengan penjelasan yang jelas sehingga Anda dapat menerapkan teknik ini pada proyek dunia nyata.

## Quick Answers
- **What library handles crop image java?** Aspose.PSD for Java.  
- **Do I need a license for development?** Versi percobaan gratis dapat digunakan untuk pengujian; lisensi komersial diperlukan untuk produksi.  
- **Can I convert PSD to JPEG while cropping?** Ya, dengan menggunakan `JpegOptions` bersama dengan persegi panjang pemotongan.  
- **Is Java 8 supported?** Aspose.PSD mendukung Java 8 dan versi yang lebih baru.  
- **How long does the implementation take?** Biasanya kurang dari 10 menit untuk operasi pemotongan dasar.

## What is “crop image java”?

Memotong gambar di Java berarti memilih area persegi panjang dari gambar sumber dan membuang sisanya. Dengan Aspose.PSD Anda dapat mendefinisikan area ini menggunakan objek `Rectangle`, lalu menyimpan hasilnya dalam format berbeda seperti JPEG.

## Why use Aspose.PSD for Java image cropping?

- **Full PSD support** – bekerja langsung dengan file PSD berlapis tanpa harus mengonversinya terlebih dahulu.  
- **High‑performance raster handling** – penggunaan memori yang efisien untuk gambar berukuran besar.  
- **Built‑in conversion** – mudah mengekspor ke JPEG, PNG, BMP, dll., sambil menerapkan pemotongan atau perluasan kanvas.  
- **Cross‑platform** – berfungsi pada sistem apa pun yang menjalankan Java.

## Prerequisites

Sebelum kita mulai, pastikan Anda memiliki:

1. **Java Development Kit (JDK)** – Java 8 atau yang lebih baru terpasang.  
2. **Aspose.PSD for Java** – unduh perpustakaan dari situs resmi **[here](https://releases.aspose.com/psd/java/)**.  

> **Pro tip:** Tambahkan JAR Aspose.PSD ke classpath proyek Anda atau ke dependensi Maven/Gradle untuk menghindari `ClassNotFoundException`.

## Import Packages

Tambahkan impor yang diperlukan ke file sumber Java Anda. Kelas‑kelas ini memberi Anda akses ke pemuatan gambar, manipulasi raster, definisi persegi panjang, dan opsi ekspor JPEG.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;

import com.aspose.psd.imageoptions.JpegOptions;
```

## Step 1: Set Your Document Directory

Tentukan folder yang berisi file PSD sumber. Ganti placeholder dengan jalur aktual di mesin Anda.

```java
String dataDir = "Your Document Directory";
```

## Step 2: Specify Source and Destination Paths

Definisikan lokasi untuk membaca PSD dan tempat menulis JPEG yang telah dipotong.

```java
String sourceFile = dataDir + "example1.psd";
String destName = dataDir + "jpeg_out.jpg";
```

## Step 3: Load and Cache the Image

Muat PSD ke objek `RasterImage`. Caching meningkatkan kinerja untuk operasi selanjutnya seperti pemotongan.

```java
RasterImage rasterImage = (RasterImage)Image.load(sourceFile);
rasterImage.cacheData();
```

## Step 4: Create Rectangle for Cropping

Buat `Rectangle` yang menggambarkan area yang ingin Anda pertahankan. Koordinat dapat bernilai negatif untuk **memperluas** kanvas sebelum pemotongan, yang berguna untuk menambahkan batas di sekitar gambar asli.

```java
Rectangle destRect = new Rectangle(-200, -200, 300, 300);
```

> **Why use negative coordinates?**  
> Nilai X/Y negatif menggeser area pemotongan ke kiri/atas, secara efektif menambahkan ruang kosong (memperluas) di sekitar konten asli sebelum pemotongan akhir.

## Step 5: Save the Cropped Image

Akhirnya, simpan gambar hasil menggunakan `JpegOptions`. Langkah ini juga memperlihatkan **convert psd jpeg** sambil menerapkan persegi panjang pemotongan.

```java
rasterImage.save(destName, new JpegOptions(), destRect);
```

> **Result:** `jpeg_out.jpg` kini berisi gambar berukuran 300 × 300 piksel yang telah diperluas sebesar 200 px di setiap sisi dan kemudian dipotong sesuai persegi panjang yang ditentukan.

Selamat! Anda telah berhasil melakukan **java image cropping**, memperluas kanvas, dan mengonversi file PSD ke JPEG—semua dalam beberapa baris kode yang singkat.

## Common Use Cases

- **Preparing assets for web** – memotong dan mengubah ukuran screenshot atau desain sebelum diunggah.  
- **Generating thumbnails** – mengekstrak area tertentu dari PSD besar untuk keperluan pratinjau.  
- **Automated batch processing** – memproses folder berisi file PSD, menerapkan persegi panjang pemotongan yang sama pada setiap file.

## Troubleshooting & Tips

| Issue | Suggested Fix |
|-------|----------------|
| `OutOfMemoryError` ketika memuat PSD besar | Panggil `rasterImage.cacheData()` lebih awal dan pertimbangkan meningkatkan ukuran heap JVM (`-Xmx`). |
| Area yang dipotong tidak berada di tengah | Periksa offset X/Y pada persegi panjang; ingat nilai negatif memperluas kanvas. |
| JPEG output terlihat buram | Sesuaikan pengaturan kualitas `JpegOptions` (misalnya, `new JpegOptions { Quality = 90 }`). |

## Frequently Asked Questions

### Q1: Is Aspose.PSD compatible with different Java versions?

A1: Ya, Aspose.PSD mendukung berbagai versi Java, memastikan kompatibilitas dengan beragam lingkungan pengembangan.

### Q2: Can I use Aspose.PSD for commercial projects?

A2: Tentu saja, Aspose.PSD menyediakan lisensi komersial untuk pengembang, memungkinkan penggunaannya dalam proyek pribadi maupun komersial.

### Q3: Are there any limitations on the image file formats supported?

A3: Aspose.PSD mendukung berbagai format file gambar, termasuk PSD, JPEG, PNG, dan lainnya. Lihat [documentation](https://reference.aspose.com/psd/java/) untuk daftar lengkap.

### Q4: How can I get support for Aspose.PSD-related queries?

A4: Kunjungi [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) untuk mendapatkan bantuan dari komunitas atau tim dukungan Aspose.

### Q5: Is there a free trial available?

A5: Ya, Anda dapat menjelajahi Aspose.PSD dengan versi percobaan gratis. Unduh [here](https://releases.aspose.com/).

---

**Last Updated:** 2026-01-07  
**Tested With:** Aspose.PSD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}