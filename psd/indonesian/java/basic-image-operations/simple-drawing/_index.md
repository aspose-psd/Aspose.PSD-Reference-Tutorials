---
date: 2026-06-13
description: Pelajari cara menggambar persegi panjang dalam file PSD menggunakan Aspose.PSD
  for Java. Panduan ini menampilkan kode langkah‑demi‑langkah, penambahan layer, pemrosesan
  gambar di sisi server, dan menggambar bentuk.
keywords:
- how to draw rectangle
- how to create psd
- java graphics draw rectangle
- server side image processing
- add layer to psd
linktitle: Lakukan Penggambaran Sederhana
schemas:
- author: Aspose
  dateModified: '2026-06-13'
  description: Learn how to draw rectangle in PSD files using Aspose.PSD for Java.
    This guide shows step‑by‑step code, adding layers, server‑side image processing
    and shape drawing.
  headline: How to Draw Rectangle in PSD with Aspose.PSD for Java
  type: TechArticle
- questions:
  - answer: Yes, the `Graphics` class also supports drawing ellipses, lines, and custom
      paths via the `drawPath` method.
    question: Can I draw other shapes besides rectangles?
  - answer: Absolutely; you can use `SolidBrush` with an ARGB color to include alpha
      transparency, enabling semi‑transparent overlays.
    question: Does Aspose.PSD support transparency in drawn shapes?
  - answer: Yes, each `Layer` object has a `setOpacity` method that accepts a value
      from 0 to 255, allowing fine‑grained control over layer transparency.
    question: Is it possible to edit the opacity of a layer?
  - answer: Use `PsdImage image = (PsdImage)Image.load("path/to/file.psd");` before
      manipulating layers. The loaded image retains all original layers and masks.
    question: How do I load an existing PSD file instead of creating a new one?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Cara Menggambar Persegi Panjang di PSD dengan Aspose.PSD for Java
url: /id/java/basic-image-operations/simple-drawing/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cara Menggambar Persegi Panjang di PSD dengan Aspose.PSD untuk Java

## Pendahuluan

Dalam tutorial ini Anda akan menemukan **cara menggambar persegi panjang** di dalam file Photoshop PSD menggunakan library Aspose.PSD murni‑Java. Apakah Anda sedang membangun pipeline aset sisi‑server, mengotomatisasi pembuatan thumbnail, atau menambahkan grafik dinamis ke desain yang ada, langkah‑langkah di bawah ini memberikan solusi lengkap yang siap produksi. Kami akan membahas cara membuat dokumen PSD baru, menambahkan lapisan, membersihkan latar belakang, dan akhirnya menggambar persegi panjang merah dan biru—semua tanpa pernah membuka Photoshop.

## Jawaban Cepat
- **Apa kelas utama untuk membuat file PSD?** `PsdImage`
- **Metode mana yang membersihkan warna latar belakang lapisan?** `Graphics.clear(Color)`
- **Bagaimana cara menggambar persegi panjang merah?** `graphic.drawRectangle(new Pen(Color.getRed()), new Rectangle(...))`
- **Apakah saya memerlukan lisensi untuk pengembangan?** Versi percobaan gratis dapat digunakan untuk pengujian; lisensi diperlukan untuk produksi.
- **Apakah saya dapat memanipulasi file PSD yang ada dengan API yang sama?** Ya, Aspose.PSD mendukung pengeditan PSD secara penuh.

## Apa itu menggambar persegi panjang merah dalam file PSD?

Menggambar persegi panjang merah berarti menggunakan objek `Graphics` untuk merender bentuk persegi panjang yang diisi atau digarisbawahi dengan warna merah pada lapisan tertentu dari gambar PSD. Operasi ini umum untuk menyorot area, membuat placeholder, atau menambahkan grafik sederhana secara programatik.

## Mengapa menggunakan Aspose.PSD untuk Java untuk memanipulasi file PSD?

Aspose.PSD untuk Java mendukung **lebih dari 50 format input dan output**, dapat memproses file PSD berukuran ratusan halaman tanpa memuat seluruh file ke memori, dan berjalan pada platform apa pun yang mendukung Java 8 atau lebih tinggi. Mesin pemrosesan gambar sisi‑servernya menghilangkan kebutuhan akan Photoshop, mengurangi biaya lisensi, dan memungkinkan alur kerja otomatis yang menangani hingga **10 GB** data gambar per jam pada VM yang sederhana.

## Prasyarat

- Java Development Kit (JDK) 8 atau yang lebih baru terpasang di mesin Anda.  
- Perpustakaan Aspose.PSD untuk Java. Anda dapat mengunduhnya dari [Aspose.PSD for Java Documentation](https://reference.aspose.com/psd/java/).

## Mengimpor Paket

Pernyataan `import` membawa kelas yang diperlukan ke dalam ruang lingkup sehingga Anda dapat bekerja dengan gambar PSD, lapisan, warna, dan grafik.

Kelas `PsdImage` adalah objek tingkat‑atas Aspose.PSD yang mewakili satu file PSD dalam memori.  
`Graphics` menyediakan primitif menggambar seperti garis, persegi panjang, dan elips.  
`Color` dan `Pen` memungkinkan Anda menentukan warna goresan dan ketebalan.  
Kelas `Layer` mewakili lapisan gambar individu dalam dokumen PSD.  
Kelas `Rectangle` mendefinisikan posisi dan ukuran area persegi panjang yang digunakan untuk operasi menggambar.  
Kelas `SolidBrush` mengisi bentuk dengan warna solid.

## Apa langkah pertama untuk membuat dokumen PSD?

Anda menginstansiasi `PsdImage` dengan memberikan lebar dan tinggi kanvas dalam piksel, yang membuat struktur file PSD kosong. Setelah menyiapkan lapisan atau latar belakang awal, panggil metode `save` dengan jalur file untuk menulis dokumen ke disk. Ini menyiapkan gambar untuk operasi penyuntingan selanjutnya.

## Langkah 1: Buat Dokumen Baru

Pertama, buat dokumen PSD baru dengan ukuran kanvas yang diinginkan. Dokumen ini akan menampung lapisan tempat kita akan menggambar.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Pen;
import com.aspose.psd.Rectangle;
import com.aspose.psd.brushes.SolidBrush;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
```

## Bagaimana cara menambahkan lapisan kosong baru ke gambar PSD?

Pertama, buat instance `Layer` baru dengan lebar dan tinggi yang sama dengan `PsdImage` induk. Kemudian tambahkan lapisan ini ke koleksi `Layers` gambar menggunakan metode `add`. Setelah lapisan menjadi bagian dari gambar, dapatkan objek `Graphics`-nya untuk melakukan operasi menggambar; tanpa langkah ini gambar tidak akan muncul.

## Langkah 2: Tambahkan Lapisan

Selanjutnya, tambahkan lapisan kosong baru yang mencakup lebar dan tinggi penuh gambar. Lapisan penting untuk memisahkan operasi menggambar.

```java
//ExStart:CreateDocument
String outputDir = "Your Document Directory";
String outPsdFilePath = outputDir + "output.psd";
int width = 100;
int height = 100;

PsdImage image = new PsdImage(width, height);
//ExEnd:CreateDocument
```

## Apa tujuan membersihkan warna latar belakang lapisan?

Memanggil `Graphics.clear` dengan `Color` tertentu mengisi seluruh lapisan dengan warna tersebut, secara efektif mengatur ulang semua data piksel. Ini memastikan bahwa konten sebelumnya dihapus dan lapisan dimulai dari latar belakang yang diketahui, yang menghindari transparansi atau pencampuran warna yang tidak terduga ketika PSD dibuka atau diedit di Photoshop nanti.

## Langkah 3: Gambar Bentuk

Kami akan menggunakan kelas `Graphics` untuk memanipulasi data piksel lapisan. Di bawah ini tiga contoh yang menggambarkan pembersihan latar belakang dan menggambar persegi panjang dengan warna berbeda.

### Bersihkan Warna Lapisan (atur latar belakang menjadi kuning)

```java
//ExStart:AddLayer
Layer layer = new Layer();
layer.setBottom(height);
layer.setRight(width);
image.addLayer(layer);
//ExEnd:AddLayer
```

### Gambar Persegi Panjang Merah (fokus utama)

```java
//ExStart:DrawRectangleYellow
Graphics graphic = new Graphics(layer);
graphic.clear(Color.getYellow());
//ExEnd:DrawRectangleYellow
```

### Gambar Persegi Panjang Biru (contoh tambahan)

```java
//ExStart:DrawRedRectangle
graphic.drawRectangle(new Pen(Color.getRed()), new Rectangle(30, 10, 40, 80));
//ExEnd:DrawRedRectangle
```

## Bagaimana cara menyimpan file PSD yang telah diedit ke disk?

Gunakan metode `save` pada objek `PsdImage`, dengan memberikan jalur file lengkap dan opsional menentukan format gambar yang diinginkan (PSD secara default). Ini menulis semua lapisan, masker, dan perintah menggambar ke dalam satu file PSD yang mematuhi spesifikasi Photoshop, memungkinkan file dibuka tanpa peringatan.

## Langkah 4: Simpan Perubahan

Akhirnya, tulis gambar PSD yang dimodifikasi ke disk. File akan berisi lapisan baru dan bentuk yang digambar.

```java
//ExStart:DrawBlueRectangle
graphic.drawRectangle(new Pen(new SolidBrush(Color.getBlue())), new Rectangle(10, 30, 80, 40));
//ExEnd:DrawBlueRectangle
```

## Masalah Umum dan Solusinya

- **Lapisan tidak terlihat setelah menggambar:** Pastikan lapisan ditambahkan ke gambar **sebelum** membuat objek `Graphics`. Permukaan gambar harus terhubung ke lapisan yang valid.
- **Warna muncul tidak tepat:** Verifikasi Anda menggunakan `Color.getRed()` (atau `Color.getBlue()`) bukan membuat nilai RGB khusus yang melebihi rentang 0‑255.
- **File tidak tersimpan:** Pastikan jalur `outputDir` ada dan aplikasi memiliki izin menulis. Pada Linux, Anda mungkin perlu menyesuaikan kepemilikan folder atau menggunakan `Files.createDirectories`.
- **Penurunan kinerja pada file besar:** Gunakan `setLoadOptions` milik `PsdImage` untuk memuat hanya saluran yang diperlukan, mengurangi konsumsi memori untuk PSD lebih besar dari 200 MB.

## Pertanyaan yang Sering Diajukan

**Q1: Apakah saya dapat menggunakan Aspose.PSD untuk Java untuk memanipulasi file PSD yang ada?**  
A1: Ya, Aspose.PSD untuk Java menyediakan fungsionalitas luas untuk mengedit dan memanipulasi file PSD yang ada, termasuk penataan ulang lapisan, penyesuaian masker, dan gambar vektor.

**Q2: Di mana saya dapat menemukan dukungan untuk Aspose.PSD untuk Java?**  
A2: Anda dapat mengunjungi [Aspose.PSD for Java Forum](https://forum.aspose.com/c/psd/34) untuk bantuan komunitas dan respons resmi dari Aspose.

**Q3: Apakah tersedia versi percobaan gratis untuk Aspose.PSD untuk Java?**  
A3: Ya, Anda dapat mengakses versi percobaan gratis [di sini](https://releases.aspose.com/). Versi percobaan mencakup semua fitur tetapi menambahkan watermark pada file yang disimpan.

**Q4: Bagaimana cara membeli lisensi untuk Aspose.PSD untuk Java?**  
A4: Anda dapat membeli lisensi dari [Aspose.PSD Purchase Page](https://purchase.aspose.com/buy). Opsi lisensi meliputi perpetual, subscription, dan lisensi situs.

**Q5: Apakah lisensi sementara tersedia untuk Aspose.PSD untuk Java?**  
A5: Ya, Anda dapat memperoleh lisensi sementara dari [di sini](https://purchase.aspose.com/temporary-license/).

## Pertanyaan Tambahan yang Sering Diajukan

**Q: Bisakah saya menggambar bentuk lain selain persegi panjang?**  
A: Ya, kelas `Graphics` juga mendukung menggambar elips, garis, dan jalur khusus melalui metode `drawPath`.

**Q: Apakah Aspose.PSD mendukung transparansi pada bentuk yang digambar?**  
A: Tentu saja; Anda dapat menggunakan `SolidBrush` dengan warna ARGB untuk menyertakan transparansi alfa, memungkinkan lapisan semi‑transparent.

**Q: Apakah memungkinkan mengedit opasitas sebuah lapisan?**  
A: Ya, setiap objek `Layer` memiliki metode `setOpacity` yang menerima nilai dari 0 hingga 255, memungkinkan kontrol halus atas transparansi lapisan.

**Q: Bagaimana cara memuat file PSD yang ada alih-alih membuat yang baru?**  
A: Gunakan `PsdImage image = (PsdImage)Image.load("path/to/file.psd");` sebelum memanipulasi lapisan. Gambar yang dimuat mempertahankan semua lapisan dan masker asli.

## Kesimpulan

Anda kini telah menguasai **cara menggambar persegi panjang** dan memanipulasi lapisan di dalam file PSD menggunakan Aspose.PSD untuk Java. Dengan membuat dokumen, menambahkan lapisan, membersihkan latar belakangnya, dan menggambar dengan API `Graphics`, Anda dapat mengotomatiskan tak terhitung tugas desain grafis di sisi server. Bereksperimenlah dengan berbagai pena, kuas, dan efek lapisan untuk memperluas fondasi ini menjadi pipeline generasi gambar lengkap.

```java
//ExStart:SaveChanges
image.save(outPsdFilePath);
//ExEnd:SaveChanges
```

{{< blocks/products/products-backtop-button >}}

## Tutorial Terkait

- [Cara Menggambar Bentuk Java – Operasi Gambar Dasar](/psd/java/basic-image-operations/)
- [Pengubahan Ukuran Sederhana dengan Aspose.PSD – Perpustakaan Manipulasi Gambar Java](/psd/java/basic-image-operations/simple-resizing/)
- [Memotong Gambar dengan Persegi Panjang di Aspose.PSD untuk Java](/psd/java/image-editing/crop-image-by-rectangle/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

---

**Terakhir Diperbarui:** 2026-06-13  
**Diuji Dengan:** Aspose.PSD for Java 24.12 (terbaru pada saat penulisan)  
**Penulis:** Aspose