---
title: Menggambar Persegi Panjang di Java
linktitle: Menggambar Persegi Panjang di Java
second_title: Asumsikan.PSD Java API
description: Belajar menggambar persegi panjang pada gambar menggunakan Aspose.PSD untuk Java. Tutorial ini memandu pengembang Java langkah demi langkah. Sempurna untuk tugas manipulasi gambar.
weight: 17
url: /id/java/java-graphics-drawing/drawing-rectangles/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Menggambar Persegi Panjang di Java

## Perkenalan
Dalam dunia pengembangan Java, memanipulasi dan menghasilkan gambar secara terprogram merupakan persyaratan umum di berbagai aplikasi. Salah satu tugas yang sering ditemui adalah menggambar bentuk seperti persegi panjang pada gambar. Aspose.PSD untuk Java menyediakan seperangkat alat dan fungsi yang kuat untuk mencapai hal ini secara efisien. Tutorial ini akan memandu Anda melalui proses menggambar persegi panjang pada gambar menggunakan Aspose.PSD untuk Java, langkah demi langkah.
## Prasyarat
Sebelum masuk ke tutorial, pastikan Anda telah menyiapkan prasyarat berikut:
### Lingkungan Pengembangan Jawa
Pastikan Anda memiliki Java Development Kit (JDK) yang terinstal di sistem Anda, sebaiknya JDK 8 atau lebih tinggi.
### Aspose.PSD untuk Java
 Anda harus memiliki Aspose.PSD untuk perpustakaan Java. Anda dapat mengunduhnya dari[Aspose.PSD untuk halaman unduh Java](https://releases.aspose.com/psd/java/) dan ikuti petunjuk instalasi yang disediakan dalam dokumentasinya.
## Paket Impor
Untuk memulai, impor paket Aspose.PSD untuk Java yang diperlukan ke dalam file Java Anda:
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
## Langkah 1: Buat Gambar Baru
 Pertama, buat instance baru dari`PsdImage` kelas dengan lebar dan tinggi tertentu.
```java
String dataDir = "path_to_your_data_directory/";
String outpath = dataDir + "Rectangle.bmp";
// Buat instance BmpOptions dan atur propertinya
BmpOptions saveOptions = new BmpOptions();
saveOptions.setBitsPerPixel(32);
// Buat instance PsdImage dengan dimensi tertentu
Image image = new PsdImage(100, 100);
```
 Pada langkah ini,`PsdImage` diinisialisasi dengan lebar dan tinggi masing-masing 100 piksel.
## Langkah 2: Inisialisasi Objek Grafik
 Selanjutnya, inisialisasi a`Graphics` objek menggunakan`image` dibuat pada langkah sebelumnya.
```java
// Inisialisasi objek Grafik
Graphics graphic = new Graphics(image);
```
 Ini`Graphics`objek akan digunakan untuk melakukan operasi menggambar pada gambar.
## Langkah 3: Hapus Permukaan Grafik
Hapus permukaan grafis gambar menggunakan warna tertentu.
```java
// Permukaan grafis jernih dengan warna kuning
graphic.clear(Color.YELLOW);
```
Ini mengatur latar belakang gambar menjadi kuning.
## Langkah 4: Gambar Persegi Panjang
Sekarang, gambarlah persegi panjang pada gambar menggunakan warna dan dimensi berbeda.
```java
// Gambarlah persegi panjang merah
graphic.drawRectangle(new Pen(Color.RED), new Rectangle(30, 10, 40, 80));
// Gambarlah persegi panjang biru
graphic.drawRectangle(new Pen(new SolidBrush(Color.BLUE)), new Rectangle(10, 30, 80, 40));
```
Perintah ini menggambar persegi panjang dengan warna dan posisi tertentu (merah dan biru) pada gambar.
## Langkah 5: Ekspor Gambar
Terakhir, simpan gambar yang dimodifikasi ke format file BMP.
```java
// Ekspor gambar ke format file BMP
image.save(outpath, saveOptions);
```
 Ini menyimpan gambar dengan gambar persegi panjang ke file BMP yang ditentukan oleh`outpath`.

## Kesimpulan
Menggambar persegi panjang secara terprogram pada gambar di Java menggunakan Aspose.PSD untuk Java sangatlah mudah dengan alat dan pustaka yang tepat. Dengan mengikuti tutorial ini, Anda telah mempelajari cara menginisialisasi gambar, memanipulasi objek grafik, menggambar bentuk, dan menyimpan gambar yang dimodifikasi ke file. Bereksperimen dengan berbagai bentuk, warna, dan dimensi akan semakin meningkatkan pemahaman Anda tentang manipulasi gambar di Java.
## FAQ
### Bisakah Aspose.PSD untuk Java menangani bentuk lain selain persegi panjang?
Aspose.PSD untuk Java mendukung menggambar berbagai bentuk seperti elips, garis, dan poligon selain persegi panjang.
### Bagaimana cara mengubah ketebalan batas persegi panjang?
 Anda dapat mengatur ketebalan batas persegi panjang dengan mengatur`Pen` properti ketebalan.
### Apakah Aspose.PSD untuk Java cocok untuk tugas pemrosesan gambar berkinerja tinggi?
Ya, Aspose.PSD untuk Java dirancang untuk pemrosesan gambar berkinerja tinggi dengan fitur ekstensif untuk pengoperasian sederhana dan kompleks.
### Di mana saya dapat menemukan lebih banyak contoh dan tutorial untuk Aspose.PSD untuk Java?
 Anda dapat menjelajahi lebih banyak contoh dan dokumentasi terperinci di[Aspose.PSD untuk dokumentasi Java](https://reference.aspose.com/psd/java/).
### Apakah Aspose.PSD untuk Java mendukung format gambar lain selain BMP?
Ya, Aspose.PSD untuk Java mendukung berbagai format gambar termasuk PNG, JPEG, TIFF, dan GIF.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
