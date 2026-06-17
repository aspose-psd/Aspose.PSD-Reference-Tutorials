---
date: 2026-04-08
description: Pelajari cara mengekspor PSD ke PNG dan membuat lapisan PSD baru dengan
  Aspose.PSD untuk Java menggunakan lisensi sementara Aspose. Tutorial langkah demi
  langkah ini mencakup manipulasi gambar PSD serta pengaturan posisi lapisan.
keywords:
- aspose temporary license
- set layer position
- psd image manipulation
- create new psd layer
linktitle: Tambahkan lapisan biasa baru ke PSD
second_title: Aspose.PSD Java API
title: Ekspor PSD ke PNG & Tambahkan Lapisan Reguler Baru menggunakan Aspose.PSD untuk
  Java – lisensi sementara Aspose
url: /id/java/advanced-image-effects/add-new-regular-layer/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ekspor PSD ke PNG & Tambahkan Lapisan Reguler Baru menggunakan Aspose.PSD untuk Java

## Pendahuluan

Dalam **aspose psd tutorial** ini Anda akan menemukan cara **mengekspor PSD ke PNG** sekaligus **membuat lapisan reguler baru** di dalam file yang sama, **menggunakan lisensi sementara aspose** untuk pengembangan. Apakah Anda perlu menghasilkan thumbnail siap web, menyiapkan aset untuk alur kerja desain, atau sekadar bereksperimen dengan **psd image manipulation**, Aspose.PSD untuk Java memberi Anda kontrol programatik penuh. Kami akan membimbing Anda melalui setiap langkah—dari memuat file sumber hingga menyimpan baik PSD yang diperbarui maupun salinan PNG—sehingga Anda dapat mulai memanipulasi lapisan PSD segera.

## Jawaban Cepat
- **Apakah saya dapat mengekspor PSD ke PNG dengan satu panggilan?** Ya, setelah menambahkan lapisan Anda dapat memanggil `save` dengan `PngOptions`.
- **Apakah saya memerlukan lisensi untuk pengembangan?** Lisensi sementara berfungsi untuk pengujian; lisensi penuh diperlukan untuk produksi.
- **Versi Java mana yang didukung?** Aspose.PSD bekerja dengan Java 8 dan yang lebih baru.
- **Apakah penempatan lapisan berbasis piksel?** Ya, Anda mengatur koordinat kiri, atas, kanan, bawah dalam piksel menggunakan metode **set layer position**.
- **Apakah PNG akan mempertahankan transparansi lapisan?** PNG akan berisi hasil gabungan semua lapisan yang terlihat.

## Mengapa menggunakan lisensi sementara aspose?

**Lisensi sementara aspose** memungkinkan Anda mengevaluasi seluruh rangkaian fitur Aspose.PSD tanpa batasan fungsional. Lisensi ini menghilangkan watermark evaluasi, membuka semua API—termasuk kemampuan **membuat objek psd layer** baru—dan memungkinkan Anda menguji kode dalam lingkungan mirip produksi sebelum membeli lisensi permanen.

## Prasyarat

Sebelum memulai, pastikan Anda memiliki:

- **Java Development Environment** – JDK 8+ dan alat build (Maven/Gradle) terpasang.
- **Aspose.PSD for Java** – Unduh JAR terbaru dari situs resmi [here](https://releases.aspose.com/psd/java/).
- **File PSD contoh** – Kami akan menggunakan `OneLayer.psd` dalam contoh.

## Impor Paket

Tambahkan impor yang diperlukan ke kelas Java Anda. Kelas‑kelas ini menyediakan fungsionalitas inti untuk **psd image manipulation** dan penanganan lapisan.

```java
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```

## Apa itu “set layer position” dan mengapa penting?

Saat Anda menambahkan lapisan baru, Anda harus menentukan di mana lapisan tersebut muncul di kanvas. Metode `setLeft`, `setTop`, `setRight`, dan `setBottom` **set layer position** dalam koordinat piksel. Penempatan yang tepat memastikan grafik Anda berada tepat pada posisi yang diharapkan, yang sangat penting untuk tugas seperti menggabungkan aset UI atau menyiapkan file siap cetak.

## Panduan langkah demi langkah

### Langkah 1: Muat File PSD

Pertama, muat PSD yang ada yang ingin Anda modifikasi. Ini memberi Anda objek `PsdImage` yang dapat Anda kerjakan.

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "OneLayer.psd";
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

### Langkah 2: Siapkan Data Piksel dan Persegi Panjang

Kami akan membuat dua buffer piksel (`int[]`) dan mendefinisikan area persegi panjang tempat lapisan baru akan dilukis. Ini merupakan dasar untuk **membuat lapisan psd baru**.

```java
int[] data1 = new int[2500];
int[] data2 = new int[2500];
Rectangle rect1 = new Rectangle(0, 0, 50, 50);
Rectangle rect2 = new Rectangle(0, 0, 100, 25);
```

### Langkah 3: Inisialisasi Data Lapisan

Isi buffer piksel dengan nilai ARGB default. Nilai `-10000000` mewakili warna gelap semi‑transparan.

```java
for (int i = 0; i < 2500; i++) {
    data1[i] = -10000000;
    data2[i] = -10000000;
}
```

### Langkah 4: Tambahkan Lapisan Reguler (Manipulasi Lapisan PSD)

Sekarang kami **menambahkan lapisan reguler** ke gambar PSD dan **set layer position** menggunakan properti kiri, atas, kanan, dan bawah. Ini menunjukkan cara **manipulasi lapisan PSD** secara programatik.

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

### Langkah 5: Ekspor PSD ke PNG dan Simpan PSD yang Diperbarui

Setelah lapisan berada di tempatnya, simpan dokumen yang telah dimodifikasi. Pertama kami mengekspor hasil ke PNG (langkah **export psd to png**), kemudian kami menyimpan PSD dengan lapisan baru.

```java
String exportPath = dataDir + "Updated.psd";
String exportPathPng = dataDir + "Updated.png";

im.save(exportPath, new PsdOptions());          // Save the updated PSD
im.save(exportPathPng, new PngOptions());       // Export PSD to PNG
```

> **Pro tip:** Jika Anda hanya memerlukan PNG, Anda dapat melewatkan pemanggilan `save` pada PSD dan langsung memanggil `save` dengan `PngOptions`.

## Masalah Umum & Pemecahan Masalah

| Gejala | Penyebab Kemungkinan | Perbaikan |
|---------|----------------------|-----------|
| PNG muncul kosong | Lapisan tidak terlihat atau sepenuhnya transparan | Pastikan Anda menetapkan nilai piksel yang tidak transparan atau panggil `layer.setVisible(true)`. |
| `ArrayIndexOutOfBoundsException` | Ketidaksesuaian antara ukuran persegi panjang dan panjang array piksel | Verifikasi bahwa `rect.width * rect.height == dataArray.length`. |
| LicenseException at runtime | Tidak ada lisensi yang valid dimuat | Muat lisensi sementara atau permanen sebelum memanggil metode API apa pun. |

## Pertanyaan yang Sering Diajukan

**Q: Apakah Aspose.PSD kompatibel dengan Java 8?**  
A: Ya, Aspose.PSD mendukung Java 8 dan versi yang lebih baru.

**Q: Bisakah saya menerapkan transformasi (rotasi, skala) pada lapisan yang ditambahkan?**  
A: Tentu saja! Kelas `Layer` menyediakan metode seperti `rotate`, `scale`, dan `translate` untuk kontrol transformasi penuh.

**Q: Di mana saya dapat menemukan dokumentasi Aspose.PSD tambahan?**  
A: Dokumentasi API detail tersedia [here](https://reference.aspose.com/psd/java/).

**Q: Bagaimana cara mendapatkan lisensi sementara untuk Aspose.PSD?**  
A: Kunjungi halaman lisensi sementara [here](https://purchase.aspose.com/temporary-license/).

**Q: Apakah ada forum komunitas untuk dukungan Aspose.PSD?**  
A: Ya, bergabunglah dalam diskusi di forum Aspose [here](https://forum.aspose.com/c/psd/34).

## Kesimpulan

Anda kini telah mempelajari cara **mengekspor PSD ke PNG** sambil **menambahkan lapisan reguler baru** menggunakan Aspose.PSD untuk Java, serta melihat bagaimana **lisensi sementara aspose** memungkinkan Anda mencoba alur kerja ini tanpa batasan. Tutorial ini menampilkan kemampuan inti **psd image manipulation**: memuat file, membuat lapisan, mengisi data piksel, dan mengekspor komposisi akhir. Jangan ragu untuk bereksperimen dengan ukuran persegi panjang yang berbeda, warna piksel, atau efek lapisan untuk menyesuaikan output dengan kebutuhan proyek Anda.

---

**Last Updated:** 2026-04-08  
**Tested With:** Aspose.PSD 24.11 for Java  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}