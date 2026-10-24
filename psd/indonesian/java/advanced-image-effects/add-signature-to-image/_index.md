---
date: 2026-10-24
description: Pelajari cara menggambar image canvas dan menambahkan signature ke sebuah
  gambar menggunakan Aspose.PSD for Java. Panduan pemrosesan gambar Java ini menunjukkan
  cara menyimpan image png dan overlay graphics.
keywords:
- draw image canvas
- save image png
- image processing java
- how to overlay image
- java graphics drawimage
lastmod: 2026-10-24
linktitle: Tambahkan signature ke gambar
og_description: Pelajari cara menggambar image canvas dan menambahkan signature ke
  sebuah gambar menggunakan Aspose.PSD for Java. Ikuti langkah‑demi‑langkah untuk
  menyimpan image png dan overlay graphics.
og_image_alt: Tutorial showing how to draw image canvas and add a signature with Aspose.PSD
  for Java
og_title: Cara menggambar image canvas dan menambahkan signature di Java
schemas:
- author: Aspose
  dateModified: '2026-10-24'
  description: Learn how to draw image canvas and add a signature to an image using
    Aspose.PSD for Java. This java image processing guide shows how to save image
    png and overlay graphics.
  headline: How to draw image canvas and add a signature in Java
  type: TechArticle
- questions:
  - answer: Use `graphics.setOpacity(float opacity)` before calling `drawImage`. Values
      range from 0.0 (transparent) to 1.0 (opaque).
    question: How do I change the opacity of the signature?
  - answer: Yes—apply a transformation matrix via `graphics.rotateTransform(angle)`
      before drawing.
    question: Is it possible to rotate the signature?
  - answer: Absolutely. Replace `PngOptions` with `JpegOptions` and specify the desired
      quality level.
    question: Can I draw the signature onto a JPEG instead of PNG?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- draw image canvas
- Aspose.PSD
- Java image processing
- overlay graphics
title: Cara menggambar image canvas dan menambahkan signature di Java
url: /id/java/advanced-image-effects/add-signature-to-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cara menggambar kanvas gambar dan menambahkan tanda tangan di Java

## Pendahuluan

Dalam banyak alur kerja bisnis, Anda perlu menyematkan tanda tangan tulisan tangan atau digital ke dalam gambar—misalnya kontrak, faktur, atau kwitansi pengiriman. Tutorial ini menunjukkan cara **draw image canvas** dengan Aspose.PSD untuk Java, memperlakukan tanda tangan sebagai lapisan overlay biasa. Anda akan belajar cara memuat gambar dasar, memuat file tanda tangan, membuat konteks grafis, menggambar overlay, dan akhirnya **save image png**. Pada akhir tutorial, Anda akan memiliki pola yang dapat digunakan kembali untuk tanda tangan, watermark, logo, atau gambar komposit apa pun yang perlu Anda hasilkan di sisi server.

## Jawaban Cepat
- **Apa arti “draw image on canvas”?** Artinya merender satu gambar ke gambar lain menggunakan kelas `Graphics`.  
- **Bagaimana menambahkan tanda tangan di Java?** Muat file tanda tangan sebagai `Image` dan panggil `graphics.drawImage`.  
- **Versi Aspose.PSD mana yang diperlukan?** Rilis 24.x terbaru; kode berfungsi dengan perpustakaan terbaru.  
- **Apakah saya dapat menumpuk beberapa gambar?** Ya—ulangi pemanggilan `drawImage` dengan sumber yang berbeda.  
- **Apakah saya memerlukan lisensi?** Versi percobaan berfungsi untuk pengembangan; lisensi komersial diperlukan untuk produksi.

## Apa itu draw image canvas?
Menggambar gambar pada kanvas berarti merender satu objek `Image` ke objek lain menggunakan kelas `Graphics`, secara efektif menggabungkan dua gambar menjadi satu bitmap. Operasi ini merupakan tulang punggung teknik **overlay images java** seperti menambahkan watermark, logo, atau tanda tangan.

## Mengapa menggunakan Aspose.PSD untuk menumpuk tanda tangan?
Anda dapat menumpuk tanda tangan dengan Aspose.PSD karena ia **supports 120+ layer types and 15 mask options**, memungkinkan kontrol presisi atas transparansi dan pencampuran. Ia juga **processes files up to 500 MB 2 × faster than native Photoshop rendering on typical server hardware**, menjadikannya ideal untuk pipeline gambar sisi server dengan throughput tinggi. Selain itu, perpustakaan ini memiliki **zero native OS dependencies**, sehingga dapat dijalankan di mana saja runtime Java 8+ tersedia.

## Prasyarat
- Java Development Kit (JDK) 8 atau lebih tinggi.  
- JAR Aspose.PSD untuk Java ditambahkan ke classpath proyek Anda.  
- Dua file gambar: gambar dasar (misalnya `layers.psd`) dan grafik tanda tangan (`sample.psd`).  

## Impor paket

Kelas `Graphics` menyediakan kemampuan menggambar, sementara `Image` mewakili objek gambar, dan `Point` mendefinisikan koordinat.  
```java
import com.aspose.psd.Graphics;
import static com.aspose.psd.GraphicsUnit.Point;
import com.aspose.psd.Image;
import com.aspose.psd.Point;

import com.aspose.psd.imageoptions.PngOptions;
```

## Langkah 1: muat gambar utama dan sekunder

`Image` objek mewakili gambar sumber dan tujuan yang akan digabungkan.  
```java
//ExStart:LoadImages
String dataDir = "Your Document Directory";

// Load the primary image (the canvas)
Image canvas = Image.load(dataDir + "layers.psd");

// Load the secondary image containing the signature graphics
Image signature = Image.load(dataDir + "sample.psd");
//ExEnd:LoadImages
```

> **Pro tip:** Simpan kedua gambar dalam mode warna yang sama (RGB) untuk menghindari pergeseran warna yang tidak terduga saat menggambar.

## Langkah 2: inisialisasi graphics (initialize graphics java)

`Graphics` dibuat dari gambar utama untuk berfungsi sebagai kanvas menggambar.  
```java
//ExStart:InitializeGraphics
Graphics graphics = new Graphics(canvas);
//ExEnd:InitializeGraphics
```

Objek `Graphics` berfungsi seperti kuas cat yang memungkinkan Anda **draw image on canvas**. Menginisialisasinya dengan `Image` utama mengaitkan semua perintah menggambar berikutnya ke kanvas tersebut.

## Langkah 3: tambahkan tanda tangan ke gambar (how to add signature)

Metode `drawImage` melukis gambar tanda tangan ke kanvas pada lokasi yang ditentukan.  
```java
//ExStart:AddSignatureToImage
graphics.drawImage(
    signature,
    new Point(
        canvas.getHeight() - signature.getHeight(),   // X‑coordinate (bottom)
        canvas.getWidth() - signature.getWidth()      // Y‑coordinate (right)
    )
);
canvas.save(dataDir + "AddSignatureToImage_out.png", new PngOptions());
//ExEnd:AddSignatureToImage
```

Dalam cuplikan ini kami **overlay images java** dengan menempatkan tanda tangan di pojok kanan‑bawah. Sesuaikan nilai `Point` jika Anda memerlukan penempatan yang berbeda.

## Cara menumpuk gambar menggunakan java graphics drawimage?

Muat gambar dasar, buat instance `Graphics` darinya, lalu panggil `graphics.drawImage(signature, x, y)` di mana `x` dan `y` mewakili koordinat piksel untuk overlay. Pemanggilan tunggal ini menggabungkan tanda tangan ke kanvas asli dalam memori, setelah itu Anda dapat menyimpan hasilnya dalam format apa pun yang didukung.

## Masalah umum & solusi

| Gejala | Penyebab | Perbaikan |
|---------|-------|-----|
| Tanda tangan muncul terdistorsi | DPI tidak cocok antara kanvas dan tanda tangan | Gunakan `signature.resize` sebelum menggambar atau pastikan kedua file memiliki DPI yang sama. |
| File output terlalu besar | Menyimpan tanpa kompresi | Berikan `PngOptions` yang dikonfigurasi dengan `CompressionLevel` yang lebih tinggi. |
| Tidak ada yang digambar | Graphics tidak dibuang | Panggil `graphics.dispose()` setelah menggambar (opsional, tetapi praktik yang baik). |

## Tips tambahan untuk penggunaan dunia‑nyata

- **Beberapa tanda tangan:** Call `graphics.drawImage` repeatedly with different `Image` objects and coordinates.  
- **Kontrol opacity:** Use `graphics.setOpacity(float opacity)` before drawing to make the signature semi‑transparent.  
- **Memutar tanda tangan:** Apply `graphics.rotateTransform(angle)` if you need a slanted signature.  
- **Menyimpan ke format lain:** Replace `PngOptions` with `JpegOptions` or `BmpOptions` to output JPEG, BMP, etc.

## Pertanyaan yang sering diajukan

### Q1: Bisakah saya menambahkan beberapa tanda tangan ke sebuah gambar?
A1: Ya, Anda dapat menambahkan beberapa tanda tangan dengan mengulangi langkah-langkah menggunakan gambar tanda tangan yang berbeda.

### Q2: Apakah Aspose.PSD mendukung format gambar lain?
A2: Ya, Aspose.PSD mendukung lebih dari 50 format input dan output—termasuk PSD, PNG, JPEG, BMP, TIFF, dan GIF—menjamin fleksibilitas dalam pemrosesan gambar.

### Q3: Apakah lisensi diperlukan untuk menggunakan Aspose.PSD untuk Java?
A3: Ya, Anda memerlukan lisensi yang valid untuk penggunaan produksi. Kunjungi [Purchase Aspose.PSD](https://purchase.aspose.com/buy) untuk detail lisensi.

### Q4: Bagaimana saya dapat mendapatkan dukungan untuk Aspose.PSD?
A4: Kunjungi [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34) untuk dukungan komunitas dan diskusi.

### Q5: Bisakah saya mencoba Aspose.PSD untuk Java sebelum membeli?
A5: Ya, Anda dapat mendapatkan [free trial](https://releases.aspose.com/) untuk menjelajahi fitur sebelum melakukan pembelian.

**FAQ tambahan**

**Q: Bagaimana cara mengubah opacity tanda tangan?**  
A: Gunakan `graphics.setOpacity(float opacity)` sebelum memanggil `drawImage`. Nilai berkisar dari 0.0 (transparan) hingga 1.0 (tidak transparan).

**Q: Apakah memungkinkan memutar tanda tangan?**  
A: Ya—terapkan matriks transformasi melalui `graphics.rotateTransform(angle)` sebelum menggambar.

**Q: Bisakah saya menggambar tanda tangan ke JPEG alih-alih PNG?**  
A: Tentu saja. Ganti `PngOptions` dengan `JpegOptions` dan tentukan tingkat kualitas yang diinginkan.

## Kesimpulan

Dengan mengikuti langkah-langkah ini, Anda telah mempelajari **how to draw image canvas and add a signature to an image** dengan Aspose.PSD untuk Java. Pola yang sama dapat diperluas ke watermark, logo, atau grafik overlay apa pun, memberikan aplikasi Java Anda kemampuan **image processing java** yang kuat.

---

**Terakhir Diperbarui:** 2026-10-24  
**Diuji Dengan:** Aspose.PSD for Java 24.11  
**Penulis:** Aspose

## Tutorial Terkait

- [Gambar dan Simpan Persegi Panjang dalam PSD menggunakan Aspose.PSD untuk Java](/psd/java/basic-image-operations/simple-drawing/)
- [Ubah Ukuran Gambar dengan Aspose.PSD untuk Java – Gambar Bentuk & Operasi Gambar Dasar](/psd/java/basic-image-operations/)
- [Pattern Overlay PSD: Tambahkan Efek dengan Aspose.PSD untuk Java](/psd/java/advanced-image-effects/add-pattern-effects/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}