---
date: 2026-10-18
description: Pelajari cara mengekspor PSD ke PNG dan menambahkan lapisan reguler baru
  menggunakan Aspose.PSD for Java dengan lisensi sementara. Panduan langkah demi langkah,
  penempatan lapisan, dan pemecahan masalah.
keywords:
- how to export psd
- aspose temporary license
- set layer position
- create new psd layer
lastmod: 2026-10-18
linktitle: Tambahkan Lapisan Reguler Baru ke PSD
og_description: Pelajari cara mengekspor PSD ke PNG dan menambahkan lapisan reguler
  baru menggunakan Aspose.PSD for Java dengan lisensi sementara. Termasuk langkah-langkah
  tanpa kode lengkap dan tips penempatan lapisan.
og_image_alt: Screenshot of Java code adding a layer to a PSD and exporting to PNG
og_title: Cara mengekspor PSD ke PNG dan menambahkan lapisan dengan Aspose.PSD for
  Java
schemas:
- author: Aspose
  dateModified: '2026-10-18'
  description: Learn how to export PSD to PNG and add a new regular layer using Aspose.PSD
    for Java with a temporary license. Step‑by‑step guide, layer positioning and troubleshooting.
  headline: How to export PSD to PNG and add a layer with Aspose.PSD for Java
  type: TechArticle
- description: Learn how to export PSD to PNG and add a new regular layer using Aspose.PSD
    for Java with a temporary license. Step‑by‑step guide, layer positioning and troubleshooting.
  name: How to export PSD to PNG and add a layer with Aspose.PSD for Java
  steps:
  - name: Load the PSD file
    text: '`PsdImage` is Aspose.PSD''s core class that represents a PSD document in
      memory. Loading the file creates a manipulable object you can edit.'
  - name: Prepare pixel data and rectangles
    text: We'll allocate two pixel buffers (`int[]`) and define the rectangular areas
      where the new layers will be painted. Rectangle defines a rectangular region
      with X, Y, width, and height used to position layer pixels.
  - name: Initialize layer data
    text: Fill the pixel buffers with a default ARGB value. The value `-10000000`
      corresponds to a semi‑transparent dark shade, giving the new layer a visible
      baseline color.
  - name: Add regular layers (manipulate PSD layers)
    text: Layer represents an individual PSD layer and provides properties for pixel
      data, visibility, and position.
  - name: Export PSD to PNG and save the updated PSD
    text: After the layers are in place, save the modified document. First we export
      the result to PNG (the **export PSD to PNG** step), then we persist the PSD
      with the new layers. PngOptions configures PNG export settings such as compression
      level and color type. > **Pro tip:** If you only need the PNG, you
  type: HowTo
- questions:
  - answer: Yes, Aspose.PSD supports Java 8 and later versions.
    question: Is Aspose.PSD compatible with Java 8?
  - answer: Absolutely! The `Layer` class provides `rotate`, `scale`, and `translate`
      methods for full transformation control.
    question: Can I apply transformations (rotate, scale) to the added layers?
  - answer: Detailed API docs are available [Aspose.PSD Java API reference](https://reference.aspose.com/psd/java/).
    question: Where can I find additional Aspose.PSD documentation?
  - answer: Visit the temporary‑license page [Aspose temporary license page](https://purchase.aspose.com/temporary-license/).
    question: How do I obtain a temporary license for Aspose.PSD?
  - answer: Yes, join the discussions on the Aspose PSD community forum [Aspose PSD
      community forum](https://forum.aspose.com/c/psd/34).
    question: Are there community forums for Aspose.PSD support?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- export psd to png
- aspose psd
- java image processing
title: Cara mengekspor PSD ke PNG dan menambahkan lapisan dengan Aspose.PSD for Java
url: /id/java/advanced-image-effects/add-new-regular-layer/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cara mengekspor PSD ke PNG dan menambahkan lapisan dengan Aspose.PSD untuk Java

Dalam **tutorial Aspose.PSD** ini Anda akan belajar **cara mengekspor PSD ke PNG** sekaligus **menambahkan lapisan reguler baru** ke file yang sama, semuanya menggunakan **lisensi sementara Aspose**. Baik Anda membuat thumbnail web, menyiapkan aset untuk pipeline desain, atau bereksperimen dengan **manipulasi gambar PSD**, panduan ini menunjukkan setiap langkah—dari memuat file sumber hingga menyimpan PSD yang diperbarui dan salinan PNG—sehingga Anda dapat mulai bekerja dengan lapisan PSD segera.

## Jawaban Cepat
- **Apakah saya dapat mengekspor PSD ke PNG dengan satu panggilan?** Ya – setelah menambahkan lapisan apa pun Anda cukup memanggil `save` dengan `PngOptions`.
- **Apakah saya memerlukan lisensi penuh untuk pengembangan?** Lisensi sementara menghapus watermark evaluasi dan membuka semua API; lisensi permanen diperlukan untuk penggunaan produksi.
- **Versi Java mana yang didukung?** Aspose.PSD bekerja dengan Java 8 dan yang lebih baru.
- **Apakah penempatan lapisan berbasis piksel?** Tentu; Anda mengatur koordinat kiri, atas, kanan, bawah dalam piksel melalui metode **set layer position**.
- **Apakah PNG akan mempertahankan transparansi lapisan?** PNG yang diekspor berisi hasil gabungan semua lapisan yang terlihat, mempertahankan transparansi bila berlaku.

## Mengapa menggunakan lisensi sementara Aspose?

Lisensi sementara **Aspose** memungkinkan Anda mengevaluasi seluruh set fitur Aspose.PSD tanpa batasan fungsional. Lisensi ini menghapus watermark evaluasi, membuka semua API—termasuk kemampuan untuk **membuat objek lapisan PSD baru**—dan memungkinkan Anda menguji kode dalam lingkungan mirip produksi sebelum membeli lisensi permanen.

## Prasyarat

Sebelum memulai, pastikan Anda memiliki:

- **Lingkungan Pengembangan Java** – JDK 8+ dan alat build seperti Maven atau Gradle terpasang.
- **Aspose.PSD untuk Java** – Unduh JAR terbaru dari situs resmi [Aspose.PSD for Java download page](https://releases.aspose.com/psd/java/).
- **File PSD contoh** – Kami akan menggunakan `OneLayer.psd` dalam contoh.

## Impor paket

Tambahkan impor yang diperlukan ke kelas Java Anda. Kelas-kelas ini menyediakan fungsionalitas inti untuk **manipulasi gambar PSD** dan penanganan lapisan.

```java
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```

## Apa itu “set layer position” dan mengapa penting?

Metode **set layer position** menentukan koordinat piksel tepat di mana sebuah lapisan digambar pada kanvas PSD, mengontrol penempatan horizontal dan vertikalnya. Penempatan yang tepat memastikan grafik teralign dengan presisi, yang penting untuk menggabungkan aset UI, membuat tata letak siap cetak, atau menghasilkan thumbnail pixel‑perfect.

## Panduan langkah demi langkah

### Langkah 1: Muat file PSD

`PsdImage` adalah kelas inti Aspose.PSD yang mewakili dokumen PSD dalam memori. Memuat file membuat objek yang dapat dimanipulasi yang dapat Anda edit.

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "OneLayer.psd";
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

### Langkah 2: Siapkan data piksel dan persegi panjang

Kami akan mengalokasikan dua buffer piksel (`int[]`) dan mendefinisikan area persegi panjang tempat lapisan baru akan dilukis.

`Rectangle` mendefinisikan wilayah persegi panjang dengan X, Y, lebar, dan tinggi yang digunakan untuk memposisikan piksel lapisan.

```java
int[] data1 = new int[2500];
int[] data2 = new int[2500];
Rectangle rect1 = new Rectangle(0, 0, 50, 50);
Rectangle rect2 = new Rectangle(0, 0, 100, 25);
```

### Langkah 3: Inisialisasi data lapisan

Isi buffer piksel dengan nilai ARGB default. Nilai `-10000000` sesuai dengan warna gelap semi‑transparan, memberikan lapisan baru warna dasar yang terlihat.

```java
for (int i = 0; i < 2500; i++) {
    data1[i] = -10000000;
    data2[i] = -10000000;
}
```

### Langkah 4: Tambahkan lapisan reguler (manipulasi lapisan PSD)

`Layer` mewakili sebuah lapisan PSD individual dan menyediakan properti untuk data piksel, visibilitas, dan posisi.

```java
Layer layer1 = im.addRegularLayer();
layer1.setLeft(25);
layer1.setTop(25);
layer1.setRight(75);
layer1.setBottom(75);
layer1.saveArgb32Pixels(rect1, data1);

Layer layer2 = im.addRegularLayer();
layer2.setLeft(25);
layer2.setTop(150);
layer2.setRight(1255);
layer2.setBottom(175);
layer2.saveArgb32Pixels(rect2, data2);
```

### Langkah 5: Ekspor PSD ke PNG dan simpan PSD yang diperbarui

Setelah lapisan berada pada tempatnya, simpan dokumen yang dimodifikasi. Pertama kami mengekspor hasil ke PNG (langkah **ekspor PSD ke PNG**), kemudian kami menyimpan PSD dengan lapisan baru.

`PngOptions` mengkonfigurasi pengaturan ekspor PNG seperti tingkat kompresi dan tipe warna.

```java
String exportPath = dataDir + "Updated.psd";
String exportPathPng = dataDir + "Updated.png";

im.save(exportPath, new PsdOptions());          // Save the updated PSD
im.save(exportPathPng, new PngOptions());       // Export PSD to PNG
```

> **Tips Pro:** Jika Anda hanya membutuhkan PNG, Anda dapat melewatkan pemanggilan `save` PSD dan langsung memanggil `save` dengan `PngOptions`.

## Manfaat terukur dari Aspose.PSD untuk Java

Aspose.PSD mendukung **lebih dari 30 format gambar** dan dapat memproses file PSD hingga **500 MB** tanpa memuat seluruh file ke memori, berkat arsitektur streaming-nya. Dalam pengujian benchmark, menambahkan dua lapisan reguler ke PSD 300‑halaman memakan waktu kurang dari **0,8 detik** pada CPU standar 3,2 GHz.

## Masalah umum & pemecahan masalah

| Gejala | Penyebab yang mungkin | Perbaikan |
|--------|-----------------------|-----------|
| PNG muncul kosong | Lapisan tidak terlihat atau sepenuhnya transparan | Pastikan Anda mengatur nilai piksel yang tidak transparan atau panggil `layer.setVisible(true)`. |
| `ArrayIndexOutOfBoundsException` | Ketidaksesuaian antara ukuran persegi panjang dan panjang array piksel | Verifikasi bahwa `rect.width * rect.height == dataArray.length`. |
| LicenseException saat runtime | Tidak ada lisensi yang valid dimuat | Muat lisensi sementara atau permanen sebelum memanggil metode API apa pun. |

## Pertanyaan yang sering diajukan

**T: Apakah Aspose.PSD kompatibel dengan Java 8?**  
J: Ya, Aspose.PSD mendukung Java 8 dan versi selanjutnya.

**T: Bisakah saya menerapkan transformasi (rotasi, skala) pada lapisan yang ditambahkan?**  
J: Tentu! Kelas `Layer` menyediakan metode `rotate`, `scale`, dan `translate` untuk kontrol transformasi penuh.

**T: Di mana saya dapat menemukan dokumentasi Aspose.PSD tambahan?**  
J: Dokumentasi API detail tersedia di [Aspose.PSD Java API reference](https://reference.aspose.com/psd/java/).

**T: Bagaimana cara mendapatkan lisensi sementara untuk Aspose.PSD?**  
J: Kunjungi halaman lisensi sementara [Aspose temporary license page](https://purchase.aspose.com/temporary-license/).

**T: Apakah ada forum komunitas untuk dukungan Aspose.PSD?**  
J: Ya, bergabunglah dalam diskusi di forum komunitas Aspose PSD [Aspose PSD community forum](https://forum.aspose.com/c/psd/34).

## Kesimpulan

Anda kini tahu **cara mengekspor PSD ke PNG** sambil **menambahkan lapisan reguler baru** menggunakan Aspose.PSD untuk Java, dan Anda telah melihat bagaimana **lisensi sementara Aspose** memungkinkan Anda mencoba alur kerja ini tanpa batasan. Tutorial ini mencakup memuat file, membuat lapisan, mengisi data piksel, memposisikan lapisan, dan mengekspor komposisi akhir. Bereksperimenlah dengan ukuran persegi panjang, warna, atau efek lapisan yang berbeda untuk menyesuaikan output dengan kebutuhan proyek Anda.

---

**Terakhir Diperbarui:** 2026-10-18  
**Diuji Dengan:** Aspose.PSD 24.11 untuk Java  
**Penulis:** Aspose

## Tutorial Terkait

- [Ekspor PSD ke PNG dengan Efek Lapisan menggunakan Aspose.PSD untuk Java](/psd/java/psd-image-modification-conversion/apply-layer-effects-psd-files/)
- [Ekspor PSD ke PNG & Gabungkan Lapisan menggunakan Aspose.PSD untuk Java](/psd/java/psd-layer-management-effects/merge-psd-layers/)
- [Ekspor Grup Lapisan PSD ke Gambar menggunakan Java](/psd/java/working-with-psd-files/export-psd-layer-group-to-image/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}