---
date: 2026-11-04
description: Pelajari cara menggunakan Aspose.PSD untuk Java untuk menerapkan lapisan
  penyesuaian invert, memproses gambar PSD secara batch, dan membuat file PSD gambar
  negatif.
keywords:
- how to use aspose
- batch process psd images
- create negative image psd
- image processing java library
- apply multiple adjustment layers
lastmod: 2026-11-04
linktitle: Lapisan Penyesuaian Invert
og_description: Cara menggunakan Aspose.PSD untuk Java untuk menambahkan lapisan penyesuaian
  invert, memproses gambar PSD secara batch, dan membuat PSD gambar negatif. Ikuti
  panduan langkah demi langkah.
og_image_alt: Screenshot showing Aspose.PSD Java code adding an invert adjustment
  layer
og_title: Cara menggunakan Aspose.PSD untuk menambahkan lapisan penyesuaian invert
  di Java
schemas:
- author: Aspose
  dateModified: '2026-11-04'
  description: Learn how to use Aspose.PSD for Java to apply an invert adjustment
    layer, batch process PSD images, and create negative image PSD files.
  headline: How to use Aspose.PSD to add an invert adjustment layer in Java
  type: TechArticle
- questions:
  - answer: Yes, it supports Java 6.0 and later, including Java 8, 11, and 17.
    question: Is Aspose.PSD compatible with all Java versions?
  - answer: Absolutely. After adding the invert layer you can call `addBrightnessAdjustmentLayer()`,
      `addHueSaturationAdjustmentLayer()`, etc., to stack effects.
    question: Can I apply multiple adjustment layers in a single operation?
  - answer: The complete documentation is available [Aspose.PSD Java API reference](https://reference.aspose.com/psd/java/).
    question: Where can I find the full API reference?
  - answer: Yes, you can download a trial version [Aspose.PSD trial download](https://releases.aspose.com/).
    question: Is there a free trial for Aspose.PSD?
  - answer: Request a temporary license [temporary license request page](https://purchase.aspose.com/temporary-license/).
    question: How do I obtain a temporary license for testing?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- aspose psd
- java image processing
- invert adjustment layer
- batch psd processing
title: Cara menggunakan Aspose.PSD untuk menambahkan lapisan penyesuaian invert di
  Java
url: /id/java/advanced-image-manipulation/invert-adjustment-layer/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cara Menggunakan Aspose.PSD untuk Menambahkan Lapisan Penyesuaian Invert di Java

## Pendahuluan

Jika Anda mencari **image processing java library** yang kuat, Aspose.PSD untuk Java adalah salah satu opsi paling serbaguna di pasar. Dalam tutorial ini Anda akan melihat **cara menggunakan Aspose** untuk menyisipkan **Invert Adjustment Layer** ke dalam file PSD, menumpuknya dengan penyesuaian lain, dan bahkan menjalankan operasi pada puluhan file. Baik Anda membangun alat pemrosesan batch, layanan gambar sisi server, atau editor gambar tunggal, langkah-langkah di bawah ini akan membawa Anda dari PSD sumber ke gambar negatif yang dapat diedit sepenuhnya dalam hitungan menit.

## Jawaban Cepat
- **Apa yang dilakukan Invert Adjustment Layer?** Itu membalik setiap nilai RGB di area yang dipilih, mengubah gambar menjadi negatif fotografis.  
- **Perpustakaan mana yang menyediakan fitur ini?** Aspose.PSD, sebuah **image processing java library** terkemuka.  
- **Bisakah saya menumpuknya dengan penyesuaian lain?** Ya – Anda dapat **menerapkan multiple adjustment layers** seperti Brightness/Contrast, Hue/Saturation, dan lainnya.  
- **Apakah saya memerlukan lisensi untuk pengembangan?** Versi percobaan gratis tersedia; lisensi diperlukan untuk penggunaan produksi.  
- **Berapa lama implementasinya?** Biasanya kurang dari 10 menit untuk kasus penggunaan dasar.

## Apa Itu Invert Adjustment Layer?

Invert Adjustment Layer adalah penyuntingan non‑destruktif yang membalik nilai warna setiap piksel yang dipengaruhinya. Karena berada di atas tumpukan lapisan, Anda dapat mengubah visibilitasnya atau mengubah urutannya tanpa mengubah data gambar asli secara permanen. Ini adalah cara tercepat untuk **membuat file PSD gambar negatif** atau mencapai tampilan negatif film klasik.

## Mengapa Menggunakan Aspose.PSD sebagai image processing java library Anda?

Aspose.PSD mendukung **lebih dari 200 fitur PSD**, dapat membaca dan menulis file Photoshop tanpa memerlukan Photoshop, dan memproses dokumen ratusan halaman dengan menggunakan kurang dari 500 MB memori heap. Ia berjalan pada runtime Java apa pun (Java 6+), menjadikannya ideal untuk **batch process psd images** di server Windows, Linux, atau macOS.

## Prasyarat

1. **Aspose.PSD for Java** – unduh JAR terbaru dari situs resmi [Aspose.PSD for Java download page](https://releases.aspose.com/psd/java/).  
2. **Java Development Kit** – JDK 6.0 atau lebih baru terinstal dan dikonfigurasi di `PATH`.  

Sekarang Anda siap menulis kode.

## Impor paket

Kelas `PsdImage` mewakili seluruh dokumen Photoshop dalam memori, sementara kelas lapisan penyesuaian berada di paket `com.aspose.psd.layers.adjustments`.

Kelas `PsdImage` adalah objek tingkat atas Aspose.PSD yang mengenkapsulasi struktur dan data piksel file PSD. Impor namespace, kemudian Anda akan dapat memuat, mengedit, dan menyimpan file PSD.

## Langkah 1: Siapkan Direktori Dokumen

Tentukan folder yang berisi file PSD sumber Anda dan tempat output akan disimpan. Menggunakan path absolut menghindari `NullPointerException` ketika direktori kerja berubah.

## Langkah 2: Muat File PSD

Muat file sumber ke dalam objek `PsdImage`. Objek ini menyimpan hierarki lapisan lengkap dalam memori, memungkinkan penyuntingan non‑destruktif.

Kelas `PsdImage` menyediakan metode statis `load` yang membaca header file, memvalidasi format, dan membangun representasi dalam memori yang siap untuk dimanipulasi.

## Langkah 3: Tambahkan Invert Adjustment Layer

Panggil metode bawaan untuk menyisipkan Invert Adjustment Layer di atas tumpukan lapisan saat ini. Anda kemudian dapat menambahkan lebih banyak lapisan (mis., Brightness, Hue) untuk **apply multiple adjustment layers** dalam satu alur kerja.

`addInvertAdjustmentLayer()` menambahkan Invert Adjustment Layer ke koleksi lapisan PSD.

## Langkah 4: Simpan Output

Simpan PSD yang telah dimodifikasi ke disk.  

`save()` menulis file PSD, termasuk semua lapisan dan metadata, ke path yang ditentukan.

Penyimpanan menggunakan metode `save` yang sama yang menulis dokumen lengkap, termasuk semua lapisan penyesuaian, masker, dan metadata, ke format yang ditentukan.

### Apa yang Baru Saja Terjadi?

File PSD dimuat ke dalam objek `PsdImage`, sebuah `InvertAdjustmentLayer` dibuat dan ditambahkan sebagai lapisan teratas, dan dokumen disimpan. Urutan ini mempertahankan data gambar asli sambil menambahkan efek invert non‑destruktif yang dapat diaktifkan atau diubah urutannya nanti.

Anda kini telah berhasil menggunakan Aspose.PSD, sebuah **image processing java library**, untuk memanipulasi file PSD.

## Cara Memproses Batch Gambar PSD dengan Penyesuaian Invert?

Muat setiap file di dalam loop `for`, terapkan langkah yang sama, dan panggil `save` untuk setiap iterasi. Karena Aspose.PSD memproses file secara streaming, Anda dapat menangani **ratusan PSD** sambil menjaga penggunaan memori di bawah 300 MB dengan menggunakan kembali instance `PsdImage` yang sama.

## Cara Mengonversi PSD menjadi Gambar Negatif?

Tambahkan Invert Adjustment Layer sebagai item teratas dan simpan dokumen – operasi itu setara dengan **convert PSD to negative**. Anda kemudian dapat menonaktifkan atau menghapus lapisan untuk kembali ke tampilan asli tanpa memuat ulang file sumber.

## Masalah Umum & Tips

| Masalah | Penyebab | Solusi |
|-------|-------|----------|
| **NullPointerException pada `Image.load`** | Path file tidak benar atau file tidak ada | Verifikasi `dataDir` dan nama file; gunakan path absolut untuk pengujian |
| **Urutan lapisan tidak seperti yang diharapkan** | Menambahkan lapisan setelah yang ada mengubah tumpukan | Sisipkan lapisan invert sebelum penyesuaian lain, atau ubah urutan via `psdImage.getLayers().move()` |
| **Penurunan kinerja pada PSD besar** | Memuat file sangat besar ke memori | Tingkatkan heap JVM (`-Xmx2g`) atau proses file dalam potongan menggunakan `psdImage.getPages().get(0).getResources().setMemoryOptimized(true)` |

## Pertanyaan yang Sering Diajukan

**Q: Apakah Aspose.PSD kompatibel dengan semua versi Java?**  
A: Ya, mendukung Java 6.0 dan yang lebih baru, termasuk Java 8, 11, dan 17.

**Q: Apakah saya dapat menerapkan multiple adjustment layers dalam satu operasi?**  
A: Tentu saja. Setelah menambahkan lapisan invert Anda dapat memanggil `addBrightnessAdjustmentLayer()`, `addHueSaturationAdjustmentLayer()`, dll., untuk menumpuk efek.

**Q: Di mana saya dapat menemukan referensi API lengkap?**  
A: Dokumentasi lengkap tersedia [Aspose.PSD Java API reference](https://reference.aspose.com/psd/java/).

**Q: Apakah ada trial gratis untuk Aspose.PSD?**  
A: Ya, Anda dapat mengunduh versi trial [Aspose.PSD trial download](https://releases.aspose.com/).

**Q: Bagaimana cara mendapatkan lisensi sementara untuk pengujian?**  
A: Minta lisensi sementara [temporary license request page](https://purchase.aspose.com/temporary-license/).

**Terakhir Diperbarui:** 2026-11-04  
**Diuji Dengan:** Aspose.PSD 24.12 for Java  
**Penulis:** Aspose  






```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
```

```java
String dataDir = "Your Document Directory";
```

```java
String filePath = dataDir + "InvertStripes_before.psd";
String outputPath = dataDir + "InvertStripes_after.psd";

PsdImage im = (PsdImage)Image.load(filePath);
```

```java
im.addInvertAdjustmentLayer();
```

```java
im.save(outputPath);
```

## Tutorial Terkait

- [Tambahkan Lapisan Penyesuaian Level ke File PSD dengan Aspose.PSD untuk Java](/psd/java/modifying-converting-psd-images/add-level-adjustment-layer-psd/)
- [Cara Menambahkan Adjustment Layer – Channel Mixer di PSD (Java)](/psd/java/modifying-converting-psd-images/add-channel-mixer-adjustment-layer-psd/)
- [Cara Mengedit PSD - Tambahkan Curves Adjustment Layer Menggunakan Java](/psd/java/modifying-converting-psd-images/add-curves-adjustment-layer-psd/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}