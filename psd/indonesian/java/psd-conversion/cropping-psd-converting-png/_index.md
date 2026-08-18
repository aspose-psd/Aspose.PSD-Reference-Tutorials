---
date: 2026-03-21
description: Pelajari cara mengonversi PSD ke PNG dan memotong file PSD menggunakan
  Aspose.PSD untuk Java. Panduan ini menunjukkan pemrosesan gambar langkah demi langkah
  dalam aplikasi Java.
linktitle: Cropping PSD when Converting to PNG
second_title: Aspose.PSD Java API
title: Cara mengonversi PSD ke PNG sambil memotong dengan Aspose.PSD untuk Java
url: /id/java/psd-conversion/cropping-psd-converting-png/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cara mengonversi psd ke png sambil memotong dengan Aspose.PSD untuk Java

## Pendahuluan
Di dunia Java yang dinamis, menguasai pemrosesan gambar yang efisien sangat penting. Pada tutorial ini Anda akan belajar **cara mengonversi psd ke png** dan memotong gambar dalam satu alur kerja menggunakan pustaka kuat Aspose.PSD untuk Java. Pada akhir panduan langkah‑demi‑langkah ini, Anda akan dapat menambahkan pemotongan yang tepat pada ekspor PNG Anda dan membuat aplikasi Java Anda menangani aset PSD dengan percaya diri.

## Jawaban Cepat
- **Apa yang dilakukan kode ini?** Memuat PSD, memotong sebuah persegi panjang, dan menyimpannya sebagai PNG.  
- **Perpustakaan apa yang diperlukan?** Aspose.PSD untuk Java (versi terbaru).  
- **Apakah saya memerlukan lisensi?** Ya, lisensi komersial diperlukan untuk penggunaan produksi.  
- **Bisakah saya menentukan wilayah pemotongan apa pun?** Tentu – Anda mengatur X, Y, lebar, dan tinggi yang Anda butuhkan.  
- **Apakah pendekatan ini cepat untuk file besar?** Ya, Aspose.PSD dioptimalkan untuk pemrosesan berperforma tinggi.

## Apa itu mengonversi psd ke png?
Mengonversi PSD ke PNG berarti mengambil dokumen Photoshop berlapis dan meratakannya menjadi gambar PNG lossless. Format ini ideal untuk pengiriman web, thumbnail, atau skenario apa pun di mana Anda membutuhkan gambar raster tanpa lapisan asli.

## Mengapa memotong PSD sebelum mengonversi ke PNG?
Pemotongan memungkinkan Anda mengekstrak hanya bagian desain yang diperlukan, mengurangi ukuran file dan memfokuskan pada konten visual yang relevan. Ini sangat berguna untuk menghasilkan thumbnail, aset UI, atau menyiapkan gambar untuk tata letak responsif.

## Prasyarat
Sebelum menyelam ke tutorial, pastikan Anda memiliki prasyarat berikut:
- Pengetahuan dasar tentang pemrograman Java.  
- Java Development Kit (JDK) terpasang di sistem Anda.  
- Perpustakaan Aspose.PSD untuk Java diunduh dan ditambahkan ke proyek Anda.  
- File PSD contoh untuk percobaan.

## Impor Paket
Dalam proyek Java Anda, pastikan untuk mengimpor paket yang diperlukan untuk menggunakan fungsionalitas Aspose.PSD:
```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;
import com.aspose.psd.imageoptions.PngOptions;
```

## Langkah 1: Siapkan Proyek Anda
Mulailah dengan membuat proyek Java dan menambahkan pustaka Aspose.PSD untuk Java ke classpath proyek Anda. Ini memberi Anda akses ke semua kelas pemrosesan gambar yang diperlukan.

## Langkah 2: Muat Gambar PSD
```java
String dataDir = "Your Document Directory";
String srcPath = dataDir + "sample.psd";
// Load an existing PSD image
RasterImage image = (RasterImage)Image.load(srcPath);
```
*Di sini kami memuat file PSD sumber ke dalam objek `RasterImage`, yang menyediakan operasi berbasis raster seperti pemotongan.*

## Langkah 3: Tentukan Wilayah Pemotongan
```java
// Create an instance of Rectangle class by passing x, y, width, and height
Rectangle cropRegion = new Rectangle(0, 0, 350, 450);
```
*`Rectangle` mendefinisikan area yang ingin Anda pertahankan. Sesuaikan nilai `x`, `y`, `width`, dan `height` agar cocok dengan desain Anda. Langkah ini secara langsung menjawab kata kunci “define crop region”.*

## Langkah 4: Potong Gambar PSD
```java
// Call the crop method of Image class and pass the Rectangle instance
image.crop(cropRegion);
```
*Memanggil `crop` mengubah gambar di memori, menghapus semua yang berada di luar persegi panjang yang ditentukan.*

## Langkah 5: Atur Opsi Ekspor PNG
```java
// Create an instance of PngOptions class
PngOptions pngOptions = new PngOptions();
```
*`PngOptions` memungkinkan Anda mengontrol pengaturan khusus PNG seperti tingkat kompresi, tipe warna, dan lainnya.*

## Langkah 6: Simpan Gambar yang Dipotong sebagai PNG
```java
// Provide output path and PngOptions to convert the PSD file to PNG and save the output
String destName = dataDir + "export.png";
image.save(destName, pngOptions);
```
*Metode `save` melakukan operasi **convert psd to png** sambil mempertahankan pemotongan yang Anda definisikan.*

## Kesalahan Umum & Tips
- **Dimensi persegi panjang tidak tepat:** Pastikan lebar dan tinggi tidak melebihi ukuran gambar asli, jika tidak akan terjadi pengecualian.  
- **Penggunaan memori dengan PSD besar:** Buang objek `RasterImage` (`image.dispose()`) setelah menyimpan untuk membebaskan sumber daya native.  
- **Lisensi tidak diatur:** Jika Anda menjalankan kode tanpa lisensi yang valid, watermark akan muncul pada PNG output.

## Pertanyaan yang Sering Diajukan
### Bisakah saya memotong file PSD dengan bentuk tidak beraturan menggunakan Aspose.PSD untuk Java?
Ya, Aspose.PSD untuk Java memungkinkan Anda menentukan wilayah pemotongan khusus, sehingga dapat memotong gambar ke dalam berbagai bentuk.

### Apakah Aspose.PSD untuk Java cocok untuk tugas pemrosesan gambar skala besar?
Tentu! Aspose.PSD dirancang untuk menangani gambar besar secara efisien, menjadikannya ideal untuk proyek dengan kebutuhan pemrosesan gambar yang luas.

### Apakah saya memerlukan lisensi untuk Aspose.PSD untuk Java?
Ya, lisensi yang valid diperlukan untuk penggunaan komersial. Anda dapat memperolehnya dari [Aspose Purchase](https://purchase.aspose.com/buy).

### Bagaimana saya dapat mencari bantuan atau melaporkan masalah dengan Aspose.PSD untuk Java?
Kunjungi [forum Aspose.PSD](https://forum.aspose.com/c/psd/34) untuk meminta bantuan, berbagi pengalaman, dan melaporkan masalah apa pun yang Anda temui.

### Bisakah saya mencoba Aspose.PSD untuk Java sebelum membeli?
Tentu! Jelajahi fitur perpustakaan dengan percobaan gratis yang tersedia [di sini](https://releases.aspose.com/).

---

**Last Updated:** 2026-03-21  
**Tested With:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}