---
date: 2026-07-08
description: 'Tutorial perpustakaan pengeditan gambar Java: pelajari cara crop image
  java menggunakan Aspose.PSD for Java, resize, expand canvas, dan convert PSD to
  JPEG.'
keywords:
- java image editing library
- java image processing tutorial
- how to crop image java
lastmod: 2026-07-08
linktitle: Expand dan Crop Images
og_description: Tutorial perpustakaan pengeditan gambar Java menunjukkan cara crop,
  expand canvas, dan convert PSD to JPEG menggunakan Aspose.PSD for Java dalam hitungan
  menit.
og_image_alt: 'Guide: Crop and expand images in Java with Aspose.PSD'
og_title: Perpustakaan Pengeditan Gambar Java – Crop Image dengan Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-07-08'
  description: 'Java image editing library tutorial: learn how to crop image java
    using Aspose.PSD for Java, resize, expand canvas, and convert PSD to JPEG.'
  headline: Java Image Editing Library – Crop Image with Aspose.PSD
  type: TechArticle
- questions:
  - answer: Aspose.PSD for Java.
    question: What library handles crop image java?
  - answer: A free trial works for testing; a commercial license is required for production.
    question: Do I need a license for development?
  - answer: Yes, using `JpegOptions` together with a cropping rectangle.
    question: Can I convert PSD to JPEG while cropping?
  - answer: Aspose.PSD supports Java 8 and newer versions.
    question: Is Java 8 supported?
  - answer: Typically under 10 minutes for a basic crop operation.
    question: How long does the implementation take?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java image editing
- Aspose.PSD
- image cropping
- PSD to JPEG
title: Perpustakaan Pengeditan Gambar Java – Crop Image dengan Aspose.PSD
url: /id/java/image-editing/expand-and-crop-images/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Perpustakaan Pengeditan Gambar Java: Memotong Gambar Java dengan Aspose.PSD

## Pendahuluan

Dalam tutorial ini Anda akan belajar cara menggunakan **java image editing library**—khususnya Aspose.PSD untuk Java—untuk memotong, memperluas, dan mengonversi file PSD ke JPEG. Baik Anda menyiapkan aset untuk portal web atau mengotomatiskan pembuatan thumbnail, langkah‑langkah di bawah ini memberikan alur kerja yang dapat diulang, siap produksi, yang dapat Anda integrasikan ke dalam proyek Java 8+ apa pun.

## Jawaban Cepat
- **Perpustakaan apa yang menangani crop image java?** Aspose.PSD for Java.  
- **Apakah saya perlu lisensi untuk pengembangan?** Versi percobaan gratis dapat digunakan untuk pengujian; lisensi komersial diperlukan untuk produksi.  
- **Bisakah saya mengonversi PSD ke JPEG sambil memotong?** Ya, dengan menggunakan `JpegOptions` bersama dengan rectangle pemotongan.  
- **Apakah Java 8 didukung?** Aspose.PSD mendukung Java 8 dan versi yang lebih baru.  
- **Berapa lama implementasinya?** Biasanya kurang dari 10 menit untuk operasi pemotongan dasar.

## Apa itu “crop image java”?

Crop image java berarti memilih area persegi panjang dari gambar sumber dan membuang semua yang berada di luar area tersebut. Dengan Aspose.PSD, Anda membuat sebuah `Rectangle` yang mendefinisikan area, menerapkannya ke `RasterImage`, dan kemudian menyimpan hasilnya dalam format apa pun yang didukung seperti JPEG.

## Mengapa menggunakan Aspose.PSD untuk pemotongan gambar Java?

Aspose.PSD menyediakan **java image editing library** yang menangani file PSD secara native, mendukung lebih dari 100 fitur lapisan, dan dapat memproses gambar hingga 10 000 × 10 000 piksel sambil menjaga penggunaan memori di bawah 500 MB. Ia juga menawarkan konversi bawaan ke JPEG, PNG, BMP, dan lainnya, semuanya tanpa memerlukan alat eksternal. Hal ini membuat pipeline pemrosesan massal menjadi cepat, dapat diandalkan, dan mudah dipelihara.

## Prasyarat

1. **Java Development Kit (JDK)** – Java 8 atau yang lebih baru terpasang.  
2. **Aspose.PSD for Java** – unduh perpustakaan dari situs resmi **[here](https://releases.aspose.com/psd/java/)**.  

> **Pro tip:** Tambahkan JAR Aspose.PSD ke classpath proyek Anda atau ke dependensi Maven/Gradle untuk menghindari `ClassNotFoundException`.

## Impor Paket

Tambahkan impor yang diperlukan ke file sumber Java Anda. Kelas‑kelas ini memberi Anda akses ke pemuatan gambar, manipulasi raster, definisi rectangle, dan opsi ekspor JPEG.

## Cara Memotong Gambar Java Menggunakan Aspose.PSD?

Muat PSD sumber dengan `RasterImage`, definisikan sebuah `Rectangle` yang menggambarkan area pemotongan (koordinat negatif dapat memperluas kanvas), dan akhirnya simpan hasilnya dengan `JpegOptions`. Alur tiga langkah ini menangani pemotongan serta konversi format dalam satu proses, menghilangkan kebutuhan akan file perantara.

## Langkah 1: Atur Direktori Dokumen Anda

Tentukan folder yang berisi file PSD sumber. Ganti placeholder dengan jalur aktual di mesin Anda.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;

import com.aspose.psd.imageoptions.JpegOptions;
```

## Langkah 2: Tentukan Jalur Sumber dan Tujuan

Definisikan di mana membaca PSD dan di mana menulis JPEG yang dipotong.

```java
String dataDir = "Your Document Directory";
```

## Langkah 3: Muat dan Cache Gambar

`RasterImage` mewakili versi rasterisasi dari file PSD dalam memori.  
Muat PSD ke dalam objek `RasterImage`. Caching meningkatkan kinerja untuk operasi selanjutnya seperti pemotongan.

```java
String sourceFile = dataDir + "example1.psd";
String destName = dataDir + "jpeg_out.jpg";
```

## Langkah 4: Buat Rectangle untuk Pemotongan

`Rectangle` mendefinisikan koordinat X, Y serta lebar/tinggi dari area pemotongan.  
Buat sebuah `Rectangle` yang menggambarkan wilayah yang ingin Anda pertahankan. Koordinat dapat bernilai negatif untuk **memperluas** kanvas sebelum pemotongan, yang berguna untuk menambahkan batas di sekitar gambar asli.

```java
RasterImage rasterImage = (RasterImage)Image.load(sourceFile);
rasterImage.cacheData();
```

> **Mengapa menggunakan koordinat negatif?**  
> Nilai X/Y negatif menggeser area pemotongan ke kiri/atas, secara efektif menambahkan ruang kosong (memperluas) di sekitar konten asli sebelum pemotongan akhir.

## Langkah 5: Simpan Gambar yang Dipotong

`JpegOptions` menentukan pengaturan untuk output JPEG, seperti kualitas dan kompresi.  
Akhirnya, simpan gambar yang dihasilkan menggunakan `JpegOptions`. Langkah ini juga memperlihatkan **convert psd jpeg** sambil menerapkan rectangle pemotongan.

```java
Rectangle destRect = new Rectangle(-200, -200, 300, 300);
```

> **Result:** `jpeg_out.jpg` kini berisi gambar 300 × 300 piksel yang telah diperluas 200 px di setiap sisi dan kemudian dipotong ke rectangle yang didefinisikan.

Selamat! Anda telah berhasil melakukan **java image cropping**, memperluas kanvas, dan mengonversi file PSD ke JPEG—semua dalam beberapa baris kode yang singkat.

## Kasus Penggunaan Umum

- **Menyiapkan aset untuk web** – potong dan ubah ukuran screenshot atau desain sebelum mengunggah.  
- **Membuat thumbnail** – ekstrak wilayah tertentu dari PSD besar untuk keperluan pratinjau.  
- **Pemrosesan batch otomatis** – iterasi melalui folder berisi file PSD, menerapkan rectangle pemotongan yang sama pada masing‑masing.

## Pemecahan Masalah & Tips

| Masalah | Perbaikan yang Disarankan |
|---------|---------------------------|
| `OutOfMemoryError` saat memuat PSD besar | Panggil `rasterImage.cacheData()` lebih awal dan pertimbangkan meningkatkan ukuran heap JVM (`-Xmx`). |
| Area yang dipotong tidak berada di tengah | Periksa offset X/Y pada rectangle; ingat nilai negatif memperluas kanvas. |
| Output JPEG terlihat buram | Sesuaikan pengaturan kualitas `JpegOptions` (mis., `new JpegOptions { Quality = 90 }`). |

## Pertanyaan yang Sering Diajukan

### Q1: Apakah Aspose.PSD kompatibel dengan berbagai versi Java?

A1: Ya, Aspose.PSD mendukung Java 8, 11, 17, dan rilis yang lebih baru, memastikan kompatibilitas luas di berbagai lingkungan pengembangan.

### Q2: Apakah saya dapat menggunakan Aspose.PSD untuk proyek komersial?

A2: Tentu saja, Aspose.PSD menyediakan lisensi komersial untuk pengembang, memungkinkan penggunaannya dalam aplikasi pribadi maupun komersial.

### Q3: Apakah ada batasan pada format file gambar yang didukung?

A3: Aspose.PSD mendukung lebih dari 30 format gambar, termasuk PSD, JPEG, PNG, BMP, TIFF, dan lainnya. Lihat [documentation](https://reference.aspose.com/psd/java/) untuk daftar lengkap.

### Q4: Bagaimana cara mendapatkan dukungan untuk pertanyaan terkait Aspose.PSD?

A4: Kunjungi [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) untuk meminta bantuan dari komunitas atau tim dukungan Aspose.

### Q5: Apakah tersedia versi percobaan gratis?

A5: Ya, Anda dapat menjelajahi Aspose.PSD dengan versi percobaan gratis. Unduh di [here](https://releases.aspose.com/).

---

**Last Updated:** 2026-07-08  
**Tested With:** Aspose.PSD for Java 24.12  
**Author:** Aspose  

{{< blocks/products/products-backtop-button >}}

```java
rasterImage.save(destName, new JpegOptions(), destRect);
```

## Tutorial Terkait

- [Pengubahan Ukuran Sederhana dengan Aspose.PSD – Perpustakaan Manipulasi Gambar Java](/psd/java/basic-image-operations/simple-resizing/)
- [Cara Memutar Gambar 270 Derajat dengan Aspose.PSD untuk Java](/psd/java/advanced-image-manipulation/rotate-image/)
- [Cara Menyesuaikan Gamma dalam Pemrosesan Gambar Java dengan Aspose.PSD](/psd/java/advanced-techniques/adjust-gamma/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}