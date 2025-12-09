---
date: 2025-12-06
description: Pelajari cara memutar gambar 270 derajat menggunakan Aspose.PSD untuk
  Java. Panduan ini menunjukkan cara memutar file PSD, membalik gambar, dan mengonversi
  PSD ke JPEG.
linktitle: Rotate Image 270 Degrees
second_title: Aspose.PSD Java API
title: Cara Memutar Gambar 270 Derajat dengan Aspose.PSD untuk Java
url: /id/java/advanced-image-manipulation/rotate-image/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Putar Gambar 270 Derajat dengan Aspose.PSD untuk Java

## Pendahuluan

Dalam **tutorial pemrosesan gambar java** ini, Anda akan menemukan cara **rotate image 270 degrees** dengan cepat dan dapat diandalkan menggunakan Aspose.PSD untuk Java. Baik Anda sedang membangun alat pengeditan foto, mengotomatiskan konversi batch, atau hanya perlu mengubah orientasi lapisan PSD, perpustakaan ini membuat tugas tersebut menjadi mudah. Kami juga akan membahas membalik gambar dan mengonversi PSD yang diputar ke JPEG, sehingga Anda mendapatkan alur kerja end‑to‑end yang lengkap.

## Jawaban Cepat
- **Perpustakaan apa yang menangani rotasi?** Aspose.PSD for Java  
- **Sudut rotasi apa yang digunakan contoh?** 270 degrees  
- **Apakah saya juga dapat membalik gambar?** Yes – use `RotateFlipType` options like `Rotate90FlipX`  
- **Bagaimana cara menyimpan hasilnya?** In the example we save as JPEG using `JpegOptions`  
- **Apakah saya memerlukan lisensi untuk produksi?** A valid Aspose.PSD license is required for commercial use  

## Apa itu “rotate image 270 degrees”?
Memutar gambar 270 derajat berarti memutar gambar tiga perempat lingkaran penuh searah jarum jam (atau 90 derajat berlawanan arah jarum jam). Dalam banyak skenario pengeditan grafis, orientasi ini cocok dengan tata letak potret asli setelah serangkaian transformasi.

## Mengapa menggunakan Aspose.PSD untuk tugas ini?
- **Full PSD support** – bekerja dengan lapisan, masker, dan objek penyesuaian.  
- **No native Photoshop required** – dapat dijalankan pada runtime Java apa pun.  
- **Simple API** – satu pemanggilan metode (`rotateFlip`) menangani rotasi dan pembalikan.  
- **Easy format conversion** – mengekspor langsung ke JPEG, PNG, atau format umum lainnya.  

## Prasyarat

Sebelum Anda memulai, pastikan Anda memiliki:

- **Aspose.PSD for Java** library terpasang. Anda dapat mengunduhnya dan melihat referensi API lengkap [di sini](https://reference.aspose.com/psd/java/).  
- Lingkungan pengembangan Java (JDK 8 atau lebih tinggi).  
- File PSD contoh yang ingin Anda putar. Perbarui variabel `sourceFile` dalam kode dengan jalur yang benar ke file Anda.

## Impor Paket

Mulailah dengan mengimpor kelas yang diperlukan dari paket Aspose.PSD:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RotateFlipType;

import com.aspose.psd.imageoptions.JpegOptions;
```

## Cara Memutar PSD – Langkah 1: Muat Gambar

Buat instance `Image` yang menunjuk ke file PSD sumber Anda:

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
Image image = Image.load(sourceFile);
```

## Cara Memutar PSD – Langkah 2: Putar Gambar 270 Derajat

Gunakan metode `rotateFlip` dengan `RotateFlipType.Rotate270FlipNone` untuk mencapai rotasi 270 derajat tanpa pembalikan apa pun:

```java
image.rotateFlip(RotateFlipType.Rotate270FlipNone);
```

> **Pro tip:** Jika Anda juga perlu membalik gambar secara horizontal atau vertikal, pilih `RotateFlipType` yang berbeda seperti `Rotate90FlipX` atau `Rotate180FlipY`.

## Cara Memutar PSD – Langkah 3: Konversi PSD ke JPEG dan Simpan

Setelah diputar, Anda dapat **convert PSD to JPEG** (atau format lain yang didukung) menggunakan kelas opsi yang sesuai:

```java
String destName = dataDir + "RotatedImage_out.jpg";
image.save(destName, new JpegOptions());
```

File `RotatedImage_out.jpg` kini berisi konten PSD asli yang diputar 270 derajat dan disimpan sebagai JPEG.

## Masalah Umum dan Solusinya

| Masalah | Solusi |
|-------|----------|
| **Gambar muncul terbalik** | Pastikan Anda menggunakan `Rotate270FlipNone`. Untuk rotasi 90 derajat searah jarum jam gunakan `Rotate90FlipNone`. |
| **File output rusak** | Pastikan folder tujuan ada dan Anda memiliki izin menulis. |
| **Pengecualian lisensi** | Instal lisensi Aspose.PSD sementara atau permanen sebelum memuat gambar dalam produksi. |

## Pertanyaan yang Sering Diajukan

**Q: Apakah Aspose.PSD kompatibel dengan berbagai format gambar?**  
A: Ya, Aspose.PSD mendukung PSD, JPEG, PNG, BMP, GIF, dan banyak format raster lainnya.

**Q: Apakah saya dapat menerapkan rotasi khusus, tidak hanya flip yang telah ditentukan?**  
A: Tentu saja! Meskipun `RotateFlipType` menyediakan sudut umum, Anda dapat menggabungkan beberapa pemanggilan atau menggunakan matriks transformasi untuk sudut arbitrer.

**Q: Bagaimana cara mengonversi PSD yang diputar ke format lain, seperti PNG?**  
A: Ganti `JpegOptions` dengan `PngOptions` (atau kelas opsi yang sesuai) dalam metode `save`.

**Q: Di mana saya dapat menemukan dukungan atau bantuan tambahan?**  
A: Untuk bantuan komunitas, kunjungi [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34).

**Q: Apakah ada percobaan gratis yang tersedia?**  
A: Ya, Anda dapat menjelajahi Aspose.PSD dengan [free trial](https://releases.aspose.com/).

**Q: Bagaimana cara mendapatkan lisensi sementara?**  
A: Jika Anda memerlukan lisensi sementara, Anda dapat mendapatkannya [di sini](https://purchase.aspose.com/temporary-license/).

## Kesimpulan

Anda kini telah mempelajari cara **rotate image 270 degrees** menggunakan Aspose.PSD untuk Java, membalik gambar bila diperlukan, dan mengekspor hasilnya ke JPEG. Alur kerja sederhana ini dapat diintegrasikan ke dalam pipeline pemrosesan gambar berbasis Java yang lebih besar, memberi Anda kontrol penuh atas manipulasi PSD tanpa bergantung pada Photoshop.

---

**Terakhir Diperbarui:** 2025-12-06  
**Diuji Dengan:** Aspose.PSD for Java 24.12  
**Penulis:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}