---
date: 2026-09-03
description: Pelajari cara java graphics menggambar busur menggunakan Aspose.PSD untuk
  Java. Panduan langkah demi langkah dengan potongan kode untuk membuat busur dalam
  file PSD.
keywords:
- java graphics draw arc
- how to draw arcs java
- Aspose.PSD arc drawing
lastmod: 2026-09-03
linktitle: Menggambar Busur di Java
og_description: Pelajari cara java graphics menggambar busur dengan Aspose.PSD untuk
  Java. Tutorial ini menunjukkan prasyarat, langkah kode, dan tips untuk membuat busur
  dalam file PSD.
og_image_alt: Screenshot of a Java program drawing an arc using Aspose.PSD
og_title: Cara java graphics menggambar busur di Java – Panduan Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-09-03'
  description: Learn how to java graphics draw arc using Aspose.PSD for Java. Step‑by‑step
    guide with code snippets for creating arcs in PSD files.
  headline: How to java graphics draw arc in Java
  type: TechArticle
- description: Learn how to java graphics draw arc using Aspose.PSD for Java. Step‑by‑step
    guide with code snippets for creating arcs in PSD files.
  name: How to java graphics draw arc in Java
  steps:
  - name: set up your Java project
    text: Create a new Java project in your favourite IDE and add the Aspose.PSD JAR
      to the build path. Ensure the JAR is referenced correctly so the compiler can
      locate the library classes.
  - name: import required packages
    text: 'To begin, import the necessary packages from Aspose.PSD for Java: The `Pen`
      class defines the colour, width, and style of the line used to draw the arc.
      These imports expose the `PsdImage`, `Graphics`, `Pen`, and colour classes needed
      for arc drawing.'
  - name: initialise image and graphics objects
    text: 'Create an instance of `PsdImage` and obtain a `Graphics` object to draw
      on: Replace `"Your Document Directory"` with the folder where you want the output
      files saved.'
  - name: define arc parameters
    text: 'Set the geometry and style of the arc—its bounding rectangle, start angle,
      sweep angle, colour, and thickness: Adjust the values to match the visual design
      you need; for example, a 200 px radius arc starting at 45° and sweeping 270°.'
  - name: draw the arc and save the image
    text: 'Invoke `drawArc` on the `Graphics` object and persist the PSD (or export
      to another format): The `drawArc` method of the `Graphics` class renders an
      arc defined by a bounding rectangle, start angle, and sweep angle using the
      specified `Pen`. The snippet draws the arc on the canvas and saves it as a '
  type: HowTo
- questions:
  - answer: Yes, the library can draw rectangles, ellipses, lines, polygons, and custom
      paths using the same `Graphics` API.
    question: Can Aspose.PSD for Java handle other shapes besides arcs?
  - answer: Create a `Pen` with the desired `Color` and width, then pass that `Pen`
      instance to `drawArc`.
    question: How do I change the arc colour and thickness?
  - answer: Absolutely. Aspose.PSD supports PNG, JPEG, TIFF, GIF and many more – just
      change the file extension in the `save` method.
    question: Is it possible to export the PSD to a format other than BMP?
  - answer: Visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) for tutorials,
      code samples, and assistance from other developers.
    question: Where can I find more examples and community support?
  - answer: Yes, it can process files up to 2 GB and render arcs without loading the
      entire document into memory, thanks to its streaming architecture.
    question: Does the library work with large PSD files?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java graphics
- Aspose.PSD
- arc drawing
- PSD manipulation
title: Cara java graphics menggambar busur di Java
url: /id/java/java-graphics-drawing/drawing-arcs/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cara menggambar busur dengan Java graphics di Java

## Pendahuluan
Dalam tutorial ini Anda akan menemukan cara **java graphics draw arc** menggunakan pustaka Aspose.PSD untuk Java. Menggambar busur secara programatik adalah kebutuhan umum untuk komponen UI khusus, visualisasi data, dan laporan yang kaya grafis. Aspose.PSD untuk Java memberi Anda kontrol penuh atas file PSD (Photoshop Document), memungkinkan Anda membuat, mengedit, dan mengekspor gambar tanpa harus menginstal Photoshop.

## Jawaban Cepat
- **Perpustakaan mana yang mendukung menggambar busur di Java?** Aspose.PSD for Java.
- **Apakah saya memerlukan lisensi untuk penggunaan produksi?** Yes, a commercial license is required for non‑trial deployments.
- **Format file apa yang dapat saya ekspor?** BMP, PNG, JPEG, TIFF, GIF and more.
- **Bisakah saya mengubah ketebalan dan warna busur?** Yes, via the `Pen` object passed to `drawArc`.
- **Apakah API kompatibel dengan Java 8 dan versi selanjutnya?** Fully compatible with Java 8‑21.

## Apa itu Java graphics draw arc?
`java graphics draw arc` mengacu pada proses merender segmen garis melengkung—sebuah busur—ke permukaan grafis menggunakan API menggambar Java. Dalam konteks Aspose.PSD, operasi ini dilakukan pada objek `Graphics` yang mewakili lapisan di dalam file PSD.

## Mengapa menggunakan Aspose.PSD untuk Java untuk menggambar busur?
Aspose.PSD mendukung **50+** format gambar dan dokumen, dapat menangani file PSD dengan **ukuran hingga 2 GB**, dan memproses dokumen ratusan halaman tanpa memuat seluruh file ke memori. Kinerja terukur ini menjadikannya ideal untuk pembuatan grafis sisi server di mana kecepatan dan penggunaan memori penting.

## Prasyarat
1. **Java Development Environment** – Instal Java dari [Oracle's website](https://www.oracle.com/java/).  
2. **Aspose.PSD for Java Library** – Unduh JAR terbaru dari [download page](https://releases.aspose.com/psd/java/). Ikuti instruksi yang diberikan untuk menambahkan JAR ke classpath proyek Anda.

## Cara Java graphics draw arc di Java?
Muat sebuah `PsdImage` baru, dapatkan permukaan `Graphics`-nya, konfigurasikan sebuah `Pen` dengan warna dan ketebalan yang diinginkan, lalu panggil `drawArc`. Urutan singkat ini membuat busur dan menyimpan hasilnya dalam satu rantai metode. Dengan menyesuaikan persegi pembatas dan parameter sudut, Anda dapat mengontrol ukuran, posisi, dan rentang busur agar sesuai dengan kebutuhan desain Anda.

### Langkah 1: siapkan proyek Java Anda
Buat proyek Java baru di IDE favorit Anda dan tambahkan JAR Aspose.PSD ke jalur build. Pastikan JAR direferensikan dengan benar sehingga kompiler dapat menemukan kelas pustaka.

### Langkah 2: impor paket yang diperlukan
Untuk memulai, impor paket yang diperlukan dari Aspose.PSD untuk Java:
Kelas `Pen` mendefinisikan warna, lebar, dan gaya garis yang digunakan untuk menggambar busur.
```java
import com.aspose.psd.Color;
import static com.aspose.psd.ColorAdjustType.Pen;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.Pen;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.BmpOptions;
```  
Impor ini memperlihatkan kelas `PsdImage`, `Graphics`, `Pen`, dan kelas warna yang dibutuhkan untuk menggambar busur.

### Langkah 3: inisialisasi objek gambar dan grafis
Buat sebuah instance `PsdImage` dan dapatkan objek `Graphics` untuk menggambar:
```java
String dataDir = "Your Document Directory";
// Initialize PsdImage object
PsdImage image = new PsdImage(100, 100);
// Initialize Graphics object and clear surface
Graphics graphics = new Graphics(image);
graphics.clear(Color.getYellow());
```  
Ganti `"Your Document Directory"` dengan folder tempat Anda ingin menyimpan file output.

### Langkah 4: definisikan parameter busur
Atur geometri dan gaya busur—persegi pembatas, sudut mulai, sudut rentang, warna, dan ketebalan:
```java
int width = 100;
int height = 200;
int startAngle = 45;
int sweepAngle = 270;
```  
Sesuaikan nilai-nilai agar cocok dengan desain visual yang Anda butuhkan; misalnya, busur dengan radius 200 px yang dimulai pada 45° dan menyapu 270°.

### Langkah 5: gambar busur dan simpan gambar
Panggil `drawArc` pada objek `Graphics` dan simpan PSD (atau ekspor ke format lain):
Metode `drawArc` dari kelas `Graphics` merender sebuah busur yang didefinisikan oleh persegi pembatas, sudut mulai, dan sudut rentang menggunakan `Pen` yang ditentukan.
```java
// Draw arc with specified Pen object (black color) and parameters
graphics.drawArc(new Pen(Color.getBlack()), 0, 0, width, height, startAngle, sweepAngle);
// Save the image in BMP format
String outputPath = dataDir + "Arc.bmp";
BmpOptions saveOptions = new BmpOptions();
saveOptions.setBitsPerPixel(32);
image.save(outputPath, saveOptions);
```  
Potongan kode ini menggambar busur pada kanvas dan menyimpannya sebagai file BMP. Ubah ekstensi file di `outputPath` untuk mengekspor ke PNG, JPEG, atau TIFF.

## Kesalahan umum dan pemecahan masalah
- **Incorrect angle units** – Aspose.PSD mengharapkan sudut dalam derajat, bukan radian. Memberikan radian akan menghasilkan hasil yang tidak terduga.
- **Pen thickness too large** – Pena yang sangat tebal dapat menyebabkan busur melampaui batas gambar; kurangi ketebalan atau perbesar kanvas.
- **File path issues** – Gunakan path absolut atau pastikan direktori kerja memiliki izin menulis untuk menghindari `IOException`.

## Pertanyaan yang Sering Diajukan

**Q: Apakah Aspose.PSD untuk Java dapat menangani bentuk lain selain busur?**  
A: Ya, pustaka ini dapat menggambar persegi panjang, elips, garis, poligon, dan jalur khusus menggunakan API `Graphics` yang sama.

**Q: Bagaimana cara mengubah warna dan ketebalan busur?**  
A: Buat sebuah `Pen` dengan `Color` dan lebar yang diinginkan, lalu berikan instance `Pen` tersebut ke `drawArc`.

**Q: Apakah memungkinkan mengekspor PSD ke format selain BMP?**  
A: Tentu saja. Aspose.PSD mendukung PNG, JPEG, TIFF, GIF, dan banyak lagi – cukup ubah ekstensi file dalam metode `save`.

**Q: Di mana saya dapat menemukan contoh lebih banyak dan dukungan komunitas?**  
A: Kunjungi [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) untuk tutorial, contoh kode, dan bantuan dari pengembang lain.

**Q: Apakah pustaka ini bekerja dengan file PSD besar?**  
A: Ya, dapat memproses file hingga 2 GB dan merender busur tanpa memuat seluruh dokumen ke memori, berkat arsitektur streaming-nya.

---

**Terakhir Diperbarui:** 2026-09-03  
**Diuji Dengan:** Aspose.PSD for Java 24.11  
**Penulis:** Aspose

## Tutorial Terkait

- [Menggambar dan Menyimpan Persegi Panjang dalam PSD menggunakan Aspose.PSD untuk Java](/psd/java/basic-image-operations/simple-drawing/)
- [Ubah Ukuran Gambar dengan Aspose.PSD untuk Java – Menggambar Bentuk & Operasi Gambar Dasar](/psd/java/basic-image-operations/)
- [Cara Mengubah Warna Garis Java Menggunakan Aspose.PSD](/psd/java/advanced-image-effects/add-stroke-layer-color/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}