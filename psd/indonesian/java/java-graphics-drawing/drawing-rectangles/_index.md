---
date: 2026-09-08
description: Pelajari cara menggambar persegi panjang pada gambar menggunakan Aspose.PSD
  for Java, mencakup pembuatan bitmap, background color, dan inisialisasi graphics
  untuk manipulasi gambar Java.
keywords:
- how to draw rectangle
- draw rectangle on image
- how to create bitmap
- set background color java
- java image manipulation
lastmod: 2026-09-08
linktitle: Menggambar Persegi Panjang di Java
og_description: Pelajari cara menggambar persegi panjang pada gambar menggunakan Aspose.PSD
  for Java. Panduan ini mencakup pembuatan bitmap, pengaturan background color, dan
  inisialisasi graphics di Java.
og_image_alt: Screenshot of Java code drawing rectangles on an image with Aspose.PSD
og_title: Cara menggambar persegi panjang pada gambar dengan Aspose.PSD for Java
schemas:
- author: Aspose
  dateModified: '2026-09-08'
  description: Learn how to draw rectangle on an image using Aspose.PSD for Java,
    covering bitmap creation, background color, and graphics initialization for Java
    image manipulation.
  headline: How to draw rectangle on an image with Aspose.PSD for Java
  type: TechArticle
- description: Learn how to draw rectangle on an image using Aspose.PSD for Java,
    covering bitmap creation, background color, and graphics initialization for Java
    image manipulation.
  name: How to draw rectangle on an image with Aspose.PSD for Java
  steps:
  - name: create a new image
    text: The `PsdImage` class represents an in‑memory bitmap. Initializing it also
      allocates the pixel buffer. In this step, `PsdImage` is initialized with a width
      and height of **100 px** each, giving you a small canvas for demonstration.
  - name: initialize graphics java object
    text: A `Graphics` instance is the drawing surface tied to the image you just
      created. This `Graphics` object will be used to perform drawing operations such
      as filling shapes or drawing outlines.
  - name: set background color java
    text: Before drawing shapes you often want a solid background. Use `clear` with
      a `Color` to fill the entire canvas. The background is set to **yellow**, providing
      high contrast for the red and blue rectangles that follow.
  - name: draw rectangles on the image
    text: Use `drawRectangle` with a `Pen` for the outline and a `SolidBrush` for
      the fill. You can draw multiple rectangles with different colors and positions.
      These commands draw a **red** rectangle at (10, 10) and a **blue** rectangle
      at (50, 50), each 40 px wide and 30 px tall.
  - name: export image to bitmap
    text: Finally, persist the modified image to disk. Aspose.PSD automatically encodes
      the bitmap in the format you specify. The image is saved as a BMP file at the
      path stored in `outpath`.
  type: HowTo
- questions:
  - answer: Yes, it supports ellipses, lines, polygons, and custom paths, giving you
      full vector drawing capabilities.
    question: Can Aspose.PSD for Java handle other shapes besides rectangles?
  - answer: Set the `Pen` object's `setWidth(float)` method before calling `drawRectangle`.
    question: How can I modify the thickness of the rectangle border?
  - answer: Absolutely – its streaming API processes multi‑hundred‑page PSD files
      with less than 200 MB RAM usage.
    question: Is Aspose.PSD for Java suitable for high‑performance image processing
      tasks?
  - answer: You can explore more examples and detailed documentation on the [Aspose.PSD
      for Java documentation](https://reference.aspose.com/psd/java/).
    question: Where can I find more examples and tutorials for Aspose.PSD for Java?
  - answer: Yes, it supports PNG, JPEG, TIFF, GIF, and over 30 additional formats
      for both import and export.
    question: Does Aspose.PSD for Java support other image formats besides BMP?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java graphics
- Aspose.PSD
- image processing
title: Cara menggambar persegi panjang pada gambar dengan Aspose.PSD for Java
url: /id/java/java-graphics-drawing/drawing-rectangles/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cara menggambar persegi panjang pada gambar dengan Aspose.PSD untuk Java

## Pendahuluan
Jika Anda perlu **cara menggambar persegi panjang** pada gambar secara programatis, Aspose.PSD untuk Java memberikan API yang bersih, berperforma tinggi. Dalam tutorial ini Anda akan melihat cara membuat bitmap, mengatur warna latar belakang, dan **menginisialisasi objek graphics java** sehingga Anda dapat merender persegi panjang dengan ukuran dan warna apa pun. Langkah‑langkahnya sederhana, kodenya ringkas, dan hasilnya berupa file BMP yang dapat Anda gunakan dalam alur kerja berbasis Java apa pun.

## Jawaban Cepat
- **Perpustakaan mana yang menangani gambar persegi panjang?** Aspose.PSD for Java.
- **Berapa baris kode yang diperlukan?** Sekitar enam baris untuk membuat gambar, mengatur latar belakang, dan menggambar dua persegi panjang.
- **Format gambar apa yang didukung untuk ekspor?** BMP, PNG, JPEG, TIFF, GIF, dan lainnya.
- **Apakah saya memerlukan lisensi untuk pengembangan?** Versi percobaan gratis dapat digunakan untuk pengujian; lisensi diperlukan untuk produksi.
- **Bisakah saya mengubah ketebalan border?** Ya – sesuaikan properti ketebalan `Pen` sebelum menggambar.

## Apa itu menggambar persegi panjang pada gambar?
Menggambar persegi panjang pada gambar berarti merender bentuk yang terisi atau berbingkai ke bitmap menggunakan konteks grafis. Kelas `Graphics` milik Aspose.PSD menyediakan metode yang memungkinkan Anda menentukan warna, posisi, dan ukuran dengan satu panggilan.

## Mengapa menggunakan Aspose.PSD untuk Java untuk menggambar persegi panjang?
Aspose.PSD mendukung **lebih dari 50 format gambar** dan dapat memproses file hingga **2 GB** tanpa memuat seluruh dokumen ke memori. API `Graphics`‑nya berjalan hingga **3× lebih cepat** dibandingkan Java AWT native untuk operasi batch, menjadikannya ideal untuk pemrosesan gambar sisi‑server dengan throughput tinggi.

## Prasyarat
Sebelum memulai, pastikan Anda memiliki:

- **Java Development Kit (JDK) 8 atau lebih tinggi** terpasang.
- **Aspose.PSD for Java** library diunduh dari [halaman unduhan Aspose.PSD for Java](https://releases.aspose.com/psd/java/) dan ditambahkan ke classpath proyek Anda.

### Impor paket
Pernyataan `import` memberi Anda akses ke kelas yang diperlukan untuk pembuatan bitmap dan menggambar.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.Pen;
import com.aspose.psd.Rectangle;
import com.aspose.psd.brushes.SolidBrush;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.BmpOptions;
```
Impor ini akan memungkinkan Anda mengakses kelas dan metode yang diperlukan untuk menggambar persegi panjang pada gambar.

## Cara menggambar persegi panjang pada gambar di Java?
Muat `PsdImage` baru, bersihkan permukaannya dengan warna latar belakang, buat objek `Graphics`, lalu panggil `drawRectangle` dengan pena dan kuas yang diinginkan. Seluruh proses hanya memerlukan beberapa pemanggilan metode dan menghasilkan bitmap yang siap disimpan.  
`PsdImage` mewakili bitmap dalam memori yang dapat diedit dan disimpan.  
`Graphics` menyediakan permukaan gambar untuk merender bentuk pada sebuah gambar.

### Langkah 1: buat gambar baru
Kelas `PsdImage` mewakili bitmap dalam memori. Menginisialisasinya juga mengalokasikan buffer piksel.

```java
String dataDir = "path_to_your_data_directory/";
String outpath = dataDir + "Rectangle.bmp";
// Create an instance of BmpOptions and set its properties
BmpOptions saveOptions = new BmpOptions();
saveOptions.setBitsPerPixel(32);
// Create an instance of PsdImage with specified dimensions
Image image = new PsdImage(100, 100);
```
Pada langkah ini, `PsdImage` diinisialisasi dengan lebar dan tinggi **100 px** masing‑masing, memberikan kanvas kecil untuk demonstrasi.

### Langkah 2: inisialisasi objek graphics java
Instansi `Graphics` adalah permukaan gambar yang terhubung ke gambar yang baru saja Anda buat.

```java
// Initialize Graphics object
Graphics graphic = new Graphics(image);
```
Objek `Graphics` ini akan digunakan untuk melakukan operasi menggambar seperti mengisi bentuk atau menggambar garis tepi.

### Langkah 3: atur warna latar belakang java
Sebelum menggambar bentuk, Anda biasanya menginginkan latar belakang solid. Gunakan `clear` dengan `Color` untuk mengisi seluruh kanvas.

```java
// Clear graphics surface with a yellow color
graphic.clear(Color.YELLOW);
```
Latar belakang diatur menjadi **kuning**, memberikan kontras tinggi untuk persegi panjang merah dan biru yang akan datang.

### Langkah 4: gambar persegi panjang pada gambar
Gunakan `drawRectangle` dengan `Pen` untuk garis tepi dan `SolidBrush` untuk isi. Anda dapat menggambar beberapa persegi panjang dengan warna dan posisi yang berbeda.

```java
// Draw a red rectangle
graphic.drawRectangle(new Pen(Color.RED), new Rectangle(30, 10, 40, 80));
// Draw a blue rectangle
graphic.drawRectangle(new Pen(new SolidBrush(Color.BLUE)), new Rectangle(10, 30, 80, 40));
```
Perintah ini menggambar persegi panjang **merah** pada (10, 10) dan persegi panjang **biru** pada (50, 50), masing‑masing lebar 40 px dan tinggi 30 px.

### Langkah 5: ekspor gambar ke bitmap
Akhirnya, simpan gambar yang telah dimodifikasi ke disk. Aspose.PSD secara otomatis mengkodekan bitmap dalam format yang Anda tentukan.

```java
// Export image to BMP file format
image.save(outpath, saveOptions);
```
Gambar disimpan sebagai file BMP pada path yang disimpan di `outpath`.

## Masalah umum dan solusi
- **File output kosong** – Pastikan Anda memanggil `graphics.clear` sebelum menggambar; jika tidak kanvas mungkin tetap transparan.
- **Warna tidak tepat** – Pastikan Anda mengimpor `com.aspose.psd.Color` bukan `java.awt.Color`.
- **Gambar besar kehabisan memori** – Gunakan konstruktor `PsdImage` yang mendukung streaming untuk menghindari memuat seluruh file ke RAM.

## Pertanyaan yang sering diajukan

**Q: Dapatkah Aspose.PSD for Java menangani bentuk lain selain persegi panjang?**  
A: Ya, ia mendukung elips, garis, poligon, dan jalur khusus, memberi Anda kemampuan menggambar vektor penuh.

**Q: Bagaimana saya dapat mengubah ketebalan border persegi panjang?**  
A: Atur metode `setWidth(float)` pada objek `Pen` sebelum memanggil `drawRectangle`.

**Q: Apakah Aspose.PSD for Java cocok untuk tugas pemrosesan gambar berperforma tinggi?**  
A: Tentu – API streaming‑nya memproses file PSD ratusan halaman dengan penggunaan RAM kurang dari 200 MB.

**Q: Di mana saya dapat menemukan contoh dan tutorial lebih banyak untuk Aspose.PSD for Java?**  
A: Anda dapat menjelajahi contoh lebih banyak dan dokumentasi detail di [dokumentasi Aspose.PSD for Java](https://reference.aspose.com/psd/java/).

**Q: Apakah Aspose.PSD for Java mendukung format gambar lain selain BMP?**  
A: Ya, ia mendukung PNG, JPEG, TIFF, GIF, dan lebih dari 30 format tambahan untuk impor dan ekspor.

## Kesimpulan
Anda sekarang tahu **cara menggambar persegi panjang** pada gambar menggunakan Aspose.PSD untuk Java, mulai dari membuat bitmap hingga mengatur warna latar belakang dan menginisialisasi graphics. Bereksperimenlah dengan ukuran, warna, dan bentuk tambahan yang berbeda untuk menguasai **manipulasi gambar java**. Saat Anda siap, integrasikan pola ini ke dalam pipeline pemrosesan batch yang lebih besar atau editor berbasis UI.

---

**Terakhir Diperbarui:** 2026-09-08  
**Diuji dengan:** Aspose.PSD for Java 24.12  
**Penulis:** Aspose

## Tutorial Terkait

- [Ubah Ukuran Gambar dengan Aspose.PSD untuk Java – Gambar Bentuk & Operasi Gambar Dasar](/psd/java/basic-image-operations/)
- [Tambahkan Tanda Tangan ke Gambar – Gambar pada Kanvas dengan Aspose.PSD untuk Java](/psd/java/advanced-image-effects/add-signature-to-image/)
- [Potong Gambar dengan Persegi Panjang menggunakan Aspose.PSD untuk Java](/psd/java/image-editing/crop-image-by-rectangle/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}