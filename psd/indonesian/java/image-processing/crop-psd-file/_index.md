---
date: 2026-08-17
description: Pelajari cara memotong file PSD Java dengan Aspose.PSD untuk Java – cara
  cepat dan tepat untuk memangkas dokumen Photoshop dalam aplikasi Java Anda.
keywords:
- crop psd file java
- aspose.psd java
- java image cropping
lastmod: 2026-08-17
linktitle: Potong File PSD
og_description: Potong file PSD Java menggunakan Aspose.PSD untuk Java. Panduan ini
  menunjukkan langkah demi langkah cara memangkas file Photoshop secara efisien, dengan
  penjelasan tanpa kode dan tip praktik terbaik.
og_image_alt: Guide showing how to crop a PSD file in Java using Aspose.PSD
og_title: Potong file PSD Java dengan Aspose.PSD – pemotongan gambar cepat
schemas:
- author: Aspose
  dateModified: '2026-08-17'
  description: Learn how to crop psd file java with Aspose.PSD for Java – a fast,
    precise way to trim Photoshop documents in your Java applications.
  headline: Crop psd file java using Aspose.PSD
  type: TechArticle
- description: Learn how to crop psd file java with Aspose.PSD for Java – a fast,
    precise way to trim Photoshop documents in your Java applications.
  name: Crop psd file java using Aspose.PSD
  steps:
  - name: set document directory
    text: Replace “Your Document Directory” with the absolute or relative path that
      contains the PSD you want to process.
  - name: load PSD file
    text: The `RasterImage` class is Aspose.PSD’s entry point for raster‑based operations
      on a PSD file. Loading the file creates an in‑memory representation that you
      can manipulate.
  - name: define crop area
    text: '`Rectangle` defines the X and Y coordinates together with width and height
      of the region to keep. This class is part of the standard Java AWT package and
      is used by Aspose.PSD to specify cropping bounds.'
  - name: save cropped PSD
    text: After applying the crop, you can persist the result back to PSD format.
      The library writes only the cropped pixels, keeping the original color mode
      and bit depth.
  - name: save cropped image as PNG
    text: If you need a web‑friendly version, export the cropped raster to PNG. Aspose.PSD
      provides PNG save options that let you control compression level and interlacing.
  type: HowTo
- questions:
  - answer: Aspose.PSD for Java.
    question: What library handles PSD cropping in Java?
  - answer: Two API calls after loading the image.
    question: How many lines of code are required for a basic crop?
  - answer: Yes, using the built‑in PNG save options.
    question: Can I export the cropped area as PNG?
  - answer: A commercial license is needed beyond the trial period.
    question: Is a license required for production use?
  - answer: Java 8 and later, including Java 11, 17, and 21.
    question: What Java versions are supported?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- crop psd
- aspose.psd
- java image processing
title: Potong file PSD Java menggunakan Aspose.PSD
url: /id/java/image-processing/crop-psd-file/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Memotong file psd java menggunakan Aspose.PSD

## Pendahuluan

Jika Anda perlu memangkas dokumen Photoshop secara programatis, **crop psd file java** adalah tugas umum bagi pengembang Java yang bekerja dengan pipeline grafis, pipeline aset, atau alur kerja desain otomatis. Aspose.PSD untuk Java menyediakan API khusus yang memungkinkan Anda mendefinisikan sebuah persegi panjang dan mengekstrak wilayah yang Anda butuhkan hanya dalam beberapa baris kode. Dalam tutorial ini Anda akan mempelajari mengapa perpustakaan ini dibangun untuk pemotongan berperforma tinggi, cara menyiapkan lingkungan Anda, dan langkah‑langkah tepat untuk menghasilkan hasil PSD dan PNG.

## Jawaban Cepat
- **Perpustakaan apa yang menangani pemotongan PSD di Java?** Aspose.PSD for Java.
- **Berapa baris kode yang diperlukan untuk pemotongan dasar?** Dua panggilan API setelah memuat gambar.
- **Bisakah saya mengekspor area yang dipotong sebagai PNG?** Ya, menggunakan opsi penyimpanan PNG bawaan.
- **Apakah lisensi diperlukan untuk penggunaan produksi?** Lisensi komersial diperlukan setelah periode percobaan.
- **Versi Java apa yang didukung?** Java 8 dan yang lebih baru, termasuk Java 11, 17, dan 21.

## Apa itu crop psd file java?

Crop psd file java mengacu pada proses memotong secara programatis sebuah wilayah persegi panjang dari Dokumen Photoshop (.psd) menggunakan kode Java. Dengan Aspose.PSD Anda dapat melakukan operasi ini tanpa meluncurkan Photoshop, menjadikannya ideal untuk pipeline gambar sisi server.

## Mengapa menggunakan Aspose.PSD untuk Java?

Aspose.PSD mendukung **30+ format input dan output** dan dapat memproses file PSD hingga **500 MB** tanpa memuat seluruh dokumen ke dalam memori, berkat arsitektur streaming‑nya. Perpustakaan ini mempertahankan lapisan, masker, dan profil warna, menghasilkan hasil potongan yang cocok dengan output asli Photoshop. Kinerja terukur ini memungkinkan Anda menangani pekerjaan batch pada perangkat keras standar dengan penggunaan memori yang dapat diprediksi.

## Prasyarat

- **Lingkungan pengembangan Java** – JDK 8 atau yang lebih baru terpasang dan dikonfigurasi.
- **Aspose.PSD untuk Java** – unduh JAR terbaru dan dokumentasi [Dokumentasi Aspose.PSD untuk Java](https://reference.aspose.com/psd/java/).
- **File PSD contoh** – letakkan file .psd di dalam direktori proyek Anda sehingga kode dapat menemukannya.

## Cara memotong file PSD di Java?

Muat file sumber, definisikan persegi panjang yang ingin Anda pertahankan, terapkan pemotongan, dan akhirnya simpan hasilnya dalam format yang diinginkan. Seluruh alur kerja hanya memerlukan lima langkah sederhana, masing‑masing diilustrasikan dengan placeholder tempat Anda akan menyisipkan kode Anda sendiri.

### Langkah 1: atur direktori dokumen

Ganti “Your Document Directory” dengan jalur absolut atau relatif yang berisi PSD yang ingin Anda proses.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.xmp.types.complex.colorant.ColorType;
```

### Langkah 2: muat file PSD

Kelas `RasterImage` adalah titik masuk Aspose.PSD untuk operasi berbasis raster pada file PSD. Memuat file membuat representasi dalam memori yang dapat Anda manipulasi.

```java
String dataDir = "Your Document Directory";
```

### Langkah 3: definisikan area pemotongan

`Rectangle` mendefinisikan koordinat X dan Y bersama dengan lebar serta tinggi wilayah yang akan dipertahankan. Kelas ini merupakan bagian dari paket standar Java AWT dan digunakan oleh Aspose.PSD untuk menentukan batas pemotongan.

```java
String sourceFileName = dataDir + "1.psd";
RasterImage image = (RasterImage)Image.load(sourceFileName);
```

### Langkah 4: simpan PSD yang dipotong

Setelah menerapkan pemotongan, Anda dapat menyimpan kembali hasilnya ke format PSD. Perpustakaan hanya menulis piksel yang dipotong, mempertahankan mode warna dan kedalaman bit asli.

```java
image.crop(new Rectangle(10, 30, 100, 100));
```

### Langkah 5: simpan gambar yang dipotong sebagai PNG

Jika Anda memerlukan versi yang ramah web, ekspor raster yang dipotong ke PNG. Aspose.PSD menyediakan opsi penyimpanan PNG yang memungkinkan Anda mengontrol tingkat kompresi dan interlacing.

```java
String exportPathPsd = dataDir + "CropTest.psd";
image.save(exportPathPsd, new PsdOptions());
```

## Masalah umum dan solusi

- **Koordinat persegi panjang tidak tepat** – Pastikan nilai X/Y dimulai dari 0 untuk sudut kiri atas; nilai negatif akan menyebabkan `ArgumentException`.
- **Lonjakan memori pada file besar** – Gunakan opsi `loadOptions.setLoadOnlyVisibleLayers(true)` untuk mengurangi penggunaan memori ketika Anda tidak memerlukan lapisan tersembunyi.
- **Kehilangan profil warna** – Pertahankan profil ICC asli dengan memanggil `image.getColorProfile()` sebelum pemotongan dan menetapkannya kembali setelah operasi.

## Pertanyaan yang sering diajukan

### Q1: dapatkah saya menggunakan Aspose.PSD untuk Java untuk memotong gambar dalam format lain?

A1: Aspose.PSD terutama menargetkan file PSD, tetapi juga mendukung BMP, GIF, JPEG, PNG, TIFF dan beberapa format raster lainnya untuk input maupun output.

### Q2: apakah Aspose.PSD untuk Java cocok untuk pemrosesan gambar skala besar?

A2: Ya. Arsitektur streaming perpustakaan memproses file PSD berukuran ratusan halaman dengan jejak memori di bawah 100 MB, menjadikannya ideal untuk pekerjaan batch.

### Q3: apakah ada pertimbangan lisensi untuk menggunakan Aspose.PSD untuk Java?

A3: Lisensi komersial diperlukan untuk penyebaran produksi. Detail tersedia di [halaman pembelian Aspose.PSD untuk Java](https://purchase.aspose.com/buy).

### Q4: bagaimana saya dapat mendapatkan dukungan untuk masalah terkait Aspose.PSD untuk Java?

A4: Kunjungi [forum Aspose.PSD untuk Java](https://forum.aspose.com/c/psd/34) untuk mengajukan pertanyaan, berbagi potongan kode, dan menerima bantuan dari komunitas serta insinyur produk.

### Q5: dapatkah saya mencoba Aspose.PSD untuk Java sebelum membeli?

A5: Ya, percobaan gratis yang berfungsi penuh dapat diunduh di [unduhan percobaan gratis Aspose.PSD](https://releases.aspose.com/).

{{< blocks/products/products-backtop-button >}}

```java
String exportPathPng = dataDir + "CropTest.png";
PngOptions options = new PngOptions();
options.setColorType(PngColorType.TruecolorWithAlpha);
image.save(exportPathPng, options);
```

## Tutorial Terkait

- [Memotong Gambar dengan Persegi Panjang di Aspose.PSD untuk Java](/psd/java/image-editing/crop-image-by-rectangle/)
- [Memotong Gambar dengan Pergeseran di Aspose.PSD untuk Java](/psd/java/image-editing/crop-image-by-shifts/)
- [Cara Memutar Gambar di Java dengan Aspose.PSD](/psd/java/advanced-image-manipulation/rotate-image/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}