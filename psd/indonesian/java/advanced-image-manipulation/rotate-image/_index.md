---
date: 2026-05-19
description: Pelajari cara mengonversi PSD ke JPEG dan rotate image 270 degrees menggunakan
  Aspose.PSD for Java. Panduan ini menunjukkan cara rotate file PSD, flip images,
  dan mengonversi PSD ke JPEG.
keywords:
- convert psd to jpeg
- how to rotate psd
- flip image java
- rotate psd layer
- rotate image without photoshop
linktitle: Rotate Image 270 Degrees
schemas:
- author: Aspose
  dateModified: '2026-05-19'
  description: Learn how to convert PSD to JPEG and rotate image 270 degrees using
    Aspose.PSD for Java. This guide shows how to rotate PSD files, flip images, and
    convert PSD to JPEG.
  headline: Convert PSD to JPEG & Rotate 270° with Aspose.PSD for Java
  type: TechArticle
- description: Learn how to convert PSD to JPEG and rotate image 270 degrees using
    Aspose.PSD for Java. This guide shows how to rotate PSD files, flip images, and
    convert PSD to JPEG.
  name: Convert PSD to JPEG & Rotate 270° with Aspose.PSD for Java
  steps:
  - name: Load the PSD File
    text: '`Image` is Aspose.PSD''s core class that represents a single PSD document
      in memory. Instantiating it reads only the header information, keeping memory
      usage low.'
  - name: Rotate the Image 270 Degrees
    text: '`rotateFlip` performs the specified rotation and optional flip on the image.
      `RotateFlipType.Rotate270FlipNone` rotates the canvas 270 degrees clockwise
      while leaving the image orientation unchanged. > **Pro tip:** If you also need
      to flip the image horizontally or vertically, choose a different `Ro'
  - name: Convert PSD to JPEG and Save
    text: '`JpegOptions` defines JPEG‑specific parameters such as compression quality.
      The `save` method writes the transformed image to disk in the desired format.
      The file `RotatedImage_out.jpg` now contains the original PSD content rotated
      270 degrees and saved as a JPEG.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.PSD supports PSD, JPEG, PNG, BMP, GIF, TIFF, and many other
      raster formats.
    question: Is Aspose.PSD compatible with different image formats?
  - answer: Absolutely! While `RotateFlipType` provides common angles, you can chain
      multiple calls or use transformation matrices for arbitrary angles.
    question: Can I apply custom rotations, not just predefined flips?
  - answer: Replace `JpegOptions` with `PngOptions` (or the appropriate options class)
      in the `save` method.
    question: How do I convert the rotated PSD to another format, such as PNG?
  - answer: For community help, visit the [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34).
    question: Where can I find additional support or assistance?
  - answer: Yes, you can explore Aspose.PSD with a [free trial](https://releases.aspose.com/).
    question: Is there a free trial available?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Konversi PSD ke JPEG & Rotate 270° dengan Aspose.PSD for Java
url: /id/java/advanced-image-manipulation/rotate-image/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Konversi PSD ke JPEG & Putar Gambar 270 Derajat dengan Aspose.PSD untuk Java

## Pendahuluan

Dalam **tutorial pemrosesan gambar Java** ini, Anda akan belajar cara **mengonversi PSD ke JPEG** sambil memutar gambar 270 derajat menggunakan Aspose.PSD untuk Java. Baik Anda membangun pipeline pemrosesan batch, editor berbasis web, atau utilitas desktop, perpustakaan ini memungkinkan Anda memanipulasi lapisan PSD tanpa Photoshop. Kami juga akan membahas pembalikan opsional dan menunjukkan alur end‑to‑end lengkap dari memuat file PSD hingga menyimpan JPEG.

## Jawaban Cepat
- **Perpustakaan apa yang menangani rotasi?** Aspose.PSD for Java  
- **Sudut rotasi apa yang digunakan contoh?** 270 derajat  
- **Bisakah saya juga membalikkan gambar?** Ya – gunakan opsi `RotateFlipType` seperti `Rotate90FlipX`  
- **Bagaimana cara menyimpan hasilnya?** Pada contoh kami menyimpan sebagai JPEG menggunakan `JpegOptions`  
- **Apakah saya memerlukan lisensi untuk produksi?** Lisensi Aspose.PSD yang valid diperlukan untuk penggunaan komersial  

## Apa itu “rotate image 270 degrees”?

Memutar gambar 270 derajat berarti memutar gambar tiga perempat lingkaran penuh searah jarum jam (atau 90 derajat berlawanan arah jarum jam). Orientasi ini sering mengembalikan tata letak potret asli setelah transformasi sebelumnya, dan biasanya digunakan ketika gambar diambil dalam mode lanskap tetapi perlu ditampilkan dalam mode potret. Hasilnya adalah visual yang terorientasi dengan benar tanpa kehilangan kualitas.

## Mengapa menggunakan Aspose.PSD untuk tugas ini?

Aspose.PSD mendukung **lebih dari 50 format input dan output**—termasuk PSD, JPEG, PNG, BMP, GIF, dan TIFF—dan dapat memproses file hingga **2 GB** tanpa memuat seluruh dokumen ke memori. API ini bekerja pada runtime Java apa pun (JDK 8+), tidak memerlukan instalasi Photoshop native, dan menyediakan satu panggilan `rotateFlip` yang menangani rotasi dan pembalikan dalam satu langkah.

## Prasyarat

Sebelum Anda memulai, pastikan Anda memiliki:

- Perpustakaan **Aspose.PSD for Java** terpasang. Anda dapat mengunduhnya dan melihat referensi API lengkap [di sini](https://reference.aspose.com/psd/java/).  
- Lingkungan pengembangan Java (JDK 8 atau lebih tinggi).  
- File PSD contoh yang ingin Anda putar. Perbarui variabel `sourceFile` dalam kode dengan jalur yang benar ke file Anda.

## Impor Paket

Kelas `Image`, `RotateFlipType`, dan `JpegOptions` diperlukan untuk memuat, mengubah, dan menyimpan file.  
`Image` adalah kelas inti yang mewakili dokumen PSD dalam memori.  
`RotateFlipType` mencantumkan operasi rotasi dan pembalikan yang didukung.  
`JpegOptions` mengonfigurasi pengaturan output JPEG seperti kualitas.  

```java
import com.aspose.psd.Image;
import com.aspose.psd.RotateFlipType;

import com.aspose.psd.imageoptions.JpegOptions;
```

## Cara Mengonversi PSD ke JPEG setelah memutar?

Muat PSD sumber, terapkan rotasi 270 derajat, dan segera simpan sebagai JPEG. Alur tiga langkah ini selesai dalam kurang dari satu detik untuk gambar 10 MP tipikal pada CPU modern, menjadikannya ideal untuk pekerjaan batch dengan throughput tinggi. Dengan memproses hanya data gambar yang diperlukan, konsumsi memori tetap rendah, dan JPEG yang dihasilkan mempertahankan kesetiaan visual sambil mengurangi ukuran file.

### Langkah 1: Muat File PSD

`Image` adalah kelas inti Aspose.PSD yang mewakili satu dokumen PSD dalam memori. Menginstansiasinya hanya membaca informasi header, sehingga penggunaan memori tetap rendah.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
Image image = Image.load(sourceFile);
```

### Langkah 2: Putar Gambar 270 Derajat

`rotateFlip` melakukan rotasi yang ditentukan serta pembalikan opsional pada gambar. `RotateFlipType.Rotate270FlipNone` memutar kanvas 270 derajat searah jarum jam sementara orientasi gambar tetap tidak berubah.

```java
image.rotateFlip(RotateFlipType.Rotate270FlipNone);
```

> **Tip pro:** Jika Anda juga perlu membalikkan gambar secara horizontal atau vertikal, pilih `RotateFlipType` yang berbeda seperti `Rotate90FlipX` atau `Rotate180FlipY`.

### Langkah 3: Konversi PSD ke JPEG dan Simpan

`JpegOptions` mendefinisikan parameter khusus JPEG seperti kualitas kompresi. Metode `save` menulis gambar yang telah diubah ke disk dalam format yang diinginkan.

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
A: Ya, Aspose.PSD mendukung PSD, JPEG, PNG, BMP, GIF, TIFF, dan banyak format raster lainnya.

**Q: Bisakah saya menerapkan rotasi khusus, bukan hanya flip yang telah ditentukan?**  
A: Tentu! Meskipun `RotateFlipType` menyediakan sudut umum, Anda dapat menambahkan beberapa panggilan atau menggunakan matriks transformasi untuk sudut arbitrer.

**Q: Bagaimana cara mengonversi PSD yang diputar ke format lain, seperti PNG?**  
A: Ganti `JpegOptions` dengan `PngOptions` (atau kelas opsi yang sesuai) dalam metode `save`.

**Q: Di mana saya dapat menemukan dukungan atau bantuan tambahan?**  
A: Untuk bantuan komunitas, kunjungi [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34).

**Q: Apakah ada percobaan gratis yang tersedia?**  
A: Ya, Anda dapat menjelajahi Aspose.PSD dengan [percobaan gratis](https://releases.aspose.com/).

**Q: Bagaimana cara mendapatkan lisensi sementara?**  
A: Jika Anda memerlukan lisensi sementara, Anda dapat memperolehnya [di sini](https://purchase.aspose.com/temporary-license/).

---

**Terakhir Diperbarui:** 2026-05-19  
**Diuji Dengan:** Aspose.PSD for Java 24.12  
**Penulis:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Tutorial Terkait

- [Konversi PSD ke Format Gambar Raster dengan Aspose.PSD untuk Java](/psd/java/advanced-techniques/convert-psd-to-raster-formats/)
- [Konversi PSD ke PNG dan Putar Lapisan dalam File PSD menggunakan Java](/psd/java/advanced-psd-layer-features-effects/rotate-layers-psd-files/)
- [Cara Memutar Gambar di Java dengan Aspose.PSD](/psd/java/advanced-image-manipulation/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}