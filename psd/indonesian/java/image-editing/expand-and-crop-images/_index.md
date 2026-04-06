---
date: 2026-01-07
description: Pelajari cara memotong gambar menggunakan Java dengan Aspose.PSD untuk
  Java. Panduan langkah demi langkah untuk memotong gambar, mengubah ukuran, dan mengonversi
  dari PSD ke JPEG.
linktitle: Expand and Crop Images
second_title: Aspose.PSD Java API
title: 'Potong Gambar Java - Perluas dan Potong Gambar dengan Aspose.PSD untuk Java'
url: /id/java/image-editing/expand-and-crop-images/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Crop Image Java: Memperluas dan Memotong Gambar dengan Aspose.PSD untuk Java

## Perkenalan

Dalam tutorial ini Anda akan menemukan cara **crop image java** dengan perpustakaan Aspose.PSD. Baik Anda perlu memperluas kanvas, memotong tepi yang tidak diinginkan, atau mengubah file PSD ke JPEG, langkah‑langkah di bawah ini akan memandu Anda melalui proses yang bersih dan dapat diulang. Kami akan membahas persyaratan, pernyataan impor, dan setiap langkah kode dengan penjelasan yang jelas sehingga Anda dapat menerapkan teknik ini pada proyek dunia nyata.

## Jawaban Cepat
- **Perpustakaan apa yang menangani pemotongan gambar java?** Aspose.PSD untuk Java.
- **Apakah saya memerlukan lisensi untuk pengembangan?** Versi percobaan gratis dapat digunakan untuk pengujian; lisensi komersial diperlukan untuk produksi.
- **Dapatkah saya mengonversi PSD ke JPEG sambil memotong?** Ya, dengan menggunakan `JpegOptions` bersama dengan potongan panjang.
- **Apakah Java 8 didukung?** Aspose.PSD mendukung Java 8 dan versi yang lebih baru.
- **Berapa lama waktu penerapannya?** Biasanya kurang dari 10menit untuk operasi pemotongan dasar.

## Apa itu “pangkas gambar java”?

Memotong gambar di Java berarti memilih area persegi panjang dari sumber gambar dan membuang sisa. Dengan Aspose.PSD Anda dapat mendefinisikan area ini menggunakan objek `Rectangle`, lalu menyimpan hasilnya dalam format berbeda seperti JPEG.

## Mengapa menggunakan Aspose.PSD untuk pemotongan gambar Java?

- **Dukungan PSD penuh** – bekerja langsung dengan file PSD berlapis tanpa harus mengonversinya terlebih dahulu.
- **Penanganan raster berkinerja tinggi** – penggunaan memori yang efisien untuk gambar berukuran besar.
- **Konversi bawaan** – mudah mengekspor ke JPEG, PNG, BMP, dll., sambil menerapkan pemotongan atau perluasan kanvas.
- **Cross‑platform** – berfungsi pada sistem apa pun yang menjalankan Java.

## Prasyarat

Sebelum kita mulai, pastikan Anda memiliki:

1. **Java Development Kit (JDK)** – Java8 atau yang lebih baru terpasang.
2. **Aspose.PSD untuk Java** – unduh perpustakaan dari situs resmi **[di sini](https://releases.aspose.com/psd/java/)**.

> **Tips pro:** Tambahkan JAR Aspose.PSD ke proyek classpath Anda atau ke dependensi Maven/Gradle untuk menghindari `ClassNotFoundException`.

## Impor Paket

Tambahkan impor yang diperlukan ke file sumber Java Anda. Kelas‑kelas ini memberi Anda akses untuk memuat gambar, manipulasi raster, resolusi persegi panjang, dan opsi ekspor JPEG.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;

import com.aspose.psd.imageoptions.JpegOptions;
```

## Langkah 1: Tetapkan Direktori Dokumen Anda

Tentukan folder yang berisi file PSD sumber. Ganti placeholder dengan jalur aktual di mesin Anda.

```java
String dataDir = "Your Document Directory";
```

## Langkah 2: Tentukan Jalur Sumber dan Tujuan

Definisikan lokasi untuk membaca PSD dan tempat menulis JPEG yang telah dipotong.

```java
String sourceFile = dataDir + "example1.psd";
String destName = dataDir + "jpeg_out.jpg";
```

## Langkah 3: Muat dan Simpan Gambar dalam Cache

Muat PSD ke objek `RasterImage`. Caching meningkatkan kinerja untuk operasi selanjutnya seperti pemotongan.

```java
RasterImage rasterImage = (RasterImage)Image.load(sourceFile);
rasterImage.cacheData();
```

## Langkah 4: Buat Persegi Panjang untuk Pemotongan

Buat `Rectangle` yang menggambarkan area yang ingin Anda pertahankan. Koordinat dapat bernilai negatif untuk **memperluas** kanvas sebelum pemotongan, yang berguna untuk menambahkan batas di sekitar gambar asli.

```java
Rectangle destRect = new Rectangle(-200, -200, 300, 300);
```

> **Why use negative coordinates?**  
> Nilai X/Y negatif menggeser area pemotongan ke kiri/atas, secara efektif menambahkan ruang kosong (memperluas) di sekitar konten asli sebelum pemotongan akhir.

## Langkah 5: Simpan Gambar yang Telah Dipotong

Akhirnya, simpan gambar hasil menggunakan `JpegOptions`. Langkah ini juga memperlihatkan **convert psd jpeg** sambil menerapkan persegi panjang pemotongan.

```java
rasterImage.save(destName, new JpegOptions(), destRect);
```

> **Result:** `jpeg_out.jpg` kini berisi gambar berukuran 300 × 300 piksel yang telah diperluas sebesar 200 px di setiap sisi dan kemudian dipotong sesuai persegi panjang yang ditentukan.

Selamat! Anda telah berhasil melakukan **java image cropping**, memperluas kanvas, dan mengonversi file PSD ke JPEG—semua dalam beberapa baris kode yang singkat.

## Kasus Penggunaan Umum

- **Mempersiapkan aset untuk web** – memotong dan mengubah ukuran tangkapan layar atau desain sebelum diunggah.
- **Menghasilkan thumbnail** – mengekstrak area tertentu dari PSD besar untuk mencapai tujuan.
- **Pemrosesan batch otomatis** – memproses folder berisi file PSD, menerapkan serangkaian panjang pemotongan yang sama pada setiap file.

## Pemecahan Masalah & Tip

| Edisi | Perbaikan yang Disarankan |
|-------|----------------|
| `OutOfMemoryError` ketika memuat PSD besar | Panggil `rasterImage.cacheData()` lebih awal dan mempengaruhi peningkatan ukuran heap JVM (`-Xmx`). |
| Area yang dipotong tidak berada di tengah | Periksa offset X/Y pada panjang tertentu; ingat nilai negatif memperluas kanvas. |
| Output JPEG terlihat buram | Sesuaikan pengaturan kualitas `JpegOptions` (misalnya, `JpegOptions baru { Kualitas = 90 }`). |

## Pertanyaan yang Sering Diajukan

### Q1: Apakah Aspose.PSD kompatibel dengan versi Java yang berbeda?

A1: Ya, Aspose.PSD mendukung berbagai versi Java, memastikan kompatibilitas dengan beragam lingkungan pengembangan.

### Q2: Bisakah saya menggunakan Aspose.PSD untuk proyek komersial?

A2: Tentu saja, Aspose.PSD menyediakan lisensi komersial untuk pengembang, memungkinkan penggunaannya dalam proyek pribadi maupun komersial.

### Q3: Apakah ada batasan pada format file gambar yang didukung?

A3: Aspose.PSD mendukung berbagai format file gambar, termasuk PSD, JPEG, PNG, dan lainnya. Lihat [dokumentasi](https://reference.aspose.com/psd/java/) untuk daftar lengkap.

### Q4: Bagaimana cara mendapatkan dukungan untuk pertanyaan terkait Aspose.PSD?

A4: Kunjungi [Forum Aspose.PSD](https://forum.aspose.com/c/psd/34) untuk mendapatkan bantuan dari komunitas atau tim dukungan Aspose.

### Q5: Apakah tersedia uji coba gratis?

A5: Ya, Anda dapat menjelajahi Aspose.PSD dengan versi percobaan gratis. Unduh [di sini](https://releases.aspose.com/).

---

**Terakhir Diperbarui:** 07-01-2026
**Diuji Dengan:** Aspose.PSD untuk Java 24.12
**Penulis:** Beranggapan  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}