---
date: 2025-12-27
description: Pelajari cara menggambar persegi panjang merah dan bentuk lainnya dalam
  file PSD menggunakan Aspose.PSD untuk Java. Panduan langkah demi langkah ini mencakup
  pembuatan dokumen, penambahan lapisan, dan menggambar dengan contoh kode.
linktitle: Perform Simple Drawing
second_title: Aspose.PSD Java API
title: Gambar Persegi Panjang Merah dengan Aspose.PSD untuk Java
url: /id/java/basic-image-operations/simple-drawing/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Menggambar Persegi Panjang Merah dengan Aspose.PSD untuk Java

## Pendahuluan

Selamat datang di panduan langkah‑demi‑langkah ini tentang cara **menggambar persegi panjang merah** menggunakan Aspose.PSD untuk Java! Dalam tutorial ini, kami akan menjelaskan cara membuat dokumen PSD baru, menambahkan layer, dan menggambar bentuk dengan warna khusus. Baik Anda mengotomatisasi aset grafis maupun membangun backend alat desain, tutorial ini memberikan blok‑bangunan penting yang Anda perlukan.

## Jawaban Cepat
- **Apa kelas utama untuk membuat file PSD?** `PsdImage`
- **Metode mana yang menghapus warna latar belakang layer?** `Graphics.clear(Color)`
- **Bagaimana cara menggambar persegi panjang merah?** `graphic.drawRectangle(new Pen(Color.getRed()), new Rectangle(...))`
- **Apakah saya memerlukan lisensi untuk pengembangan?** Versi percobaan gratis cukup untuk pengujian; lisensi diperlukan untuk produksi.
- **Bisakah saya memanipulasi file PSD yang sudah ada dengan API yang sama?** Ya, Aspose.PSD mendukung pengeditan PSD secara penuh.

## Apa itu menggambar persegi panjang merah pada file PSD?
Menggambar persegi panjang merah berarti menggunakan objek `Graphics` untuk merender bentuk persegi panjang yang diisi atau dioutline dengan warna merah pada layer tertentu dari gambar PSD. Operasi ini umum untuk menyorot area, membuat placeholder, atau menambahkan grafik sederhana secara programatis.

## Mengapa menggunakan Aspose.PSD untuk Java untuk memanipulasi file PSD?
Aspose.PSD menyediakan API murni‑Java yang memungkinkan Anda membaca, mengedit, dan menulis file Photoshop PSD tanpa perlu menginstal Photoshop. API ini mendukung manajemen layer, manipulasi warna, dan gambar vektor, menjadikannya ideal untuk pemrosesan gambar sisi server, pipeline aset otomatis, dan pembuatan grafik khusus.

## Prasyarat

- Java Development Kit (JDK) terpasang di mesin Anda.  
- Perpustakaan Aspose.PSD untuk Java. Anda dapat mengunduhnya dari [Aspose.PSD for Java Documentation](https://reference.aspose.com/psd/java/).

## Impor Paket

Untuk memulai, impor kelas‑kelas yang diperlukan ke dalam proyek Java Anda:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Pen;
import com.aspose.psd.Rectangle;
import com.aspose.psd.brushes.SolidBrush;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
```

## Langkah 1: Buat Dokumen Baru

Pertama, buat dokumen PSD baru dengan ukuran kanvas yang diinginkan. Dokumen ini akan menampung layer tempat kita akan menggambar.

```java
//ExStart:CreateDocument
String outputDir = "Your Document Directory";
String outPsdFilePath = outputDir + "output.psd";
int width = 100;
int height = 100;

PsdImage image = new PsdImage(width, height);
//ExEnd:CreateDocument
```

## Langkah 2: Tambahkan Layer

Selanjutnya, tambahkan layer kosong baru yang mencakup lebar dan tinggi penuh gambar. Layer penting untuk memisahkan operasi menggambar.

```java
//ExStart:AddLayer
Layer layer = new Layer();
layer.setBottom(height);
layer.setRight(width);
image.addLayer(layer);
//ExEnd:AddLayer
```

## Langkah 3: Gambar Bentuk

Kami akan menggunakan kelas `Graphics` untuk memanipulasi data piksel layer. Berikut tiga contoh yang menggambarkan cara menghapus latar belakang dan menggambar persegi panjang dengan warna berbeda.

### Hapus Warna Layer (atur latar belakang menjadi kuning)

```java
//ExStart:DrawRectangleYellow
Graphics graphic = new Graphics(layer);
graphic.clear(Color.getYellow());
//ExEnd:DrawRectangleYellow
```

### Gambar Persegi Panjang Merah (fokus utama)

```java
//ExStart:DrawRedRectangle
graphic.drawRectangle(new Pen(Color.getRed()), new Rectangle(30, 10, 40, 80));
//ExEnd:DrawRedRectangle
```

### Gambar Persegi Panjang Biru (contoh tambahan)

```java
//ExStart:DrawBlueRectangle
graphic.drawRectangle(new Pen(new SolidBrush(Color.getBlue())), new Rectangle(10, 30, 80, 40));
//ExEnd:DrawBlueRectangle
```

## Langkah 4: Simpan Perubahan

Akhirnya, tulis gambar PSD yang telah dimodifikasi ke disk. File akan berisi layer baru dan bentuk yang digambar.

```java
//ExStart:SaveChanges
image.save(outPsdFilePath);
//ExEnd:SaveChanges
```

## Masalah Umum dan Solusinya

- **Layer tidak terlihat setelah menggambar:** Pastikan layer ditambahkan ke gambar **sebelum** membuat objek `Graphics`.
- **Warna muncul tidak tepat:** Verifikasi Anda menggunakan `Color.getRed()` (atau metode statis lainnya) bukan nilai RGB khusus yang mungkin berada di luar jangkauan.
- **File tidak tersimpan:** Pastikan jalur `outputDir` ada dan aplikasi memiliki izin menulis.

## Pertanyaan yang Sering Diajukan

### Q1: Bisakah saya menggunakan Aspose.PSD untuk Java untuk memanipulasi file PSD yang sudah ada?

A1: Ya, Aspose.PSD untuk Java menyediakan fungsionalitas luas untuk mengedit dan memanipulasi file PSD yang sudah ada.

### Q2: Di mana saya dapat menemukan dukungan untuk Aspose.PSD untuk Java?

A2: Anda dapat mengunjungi [Aspose.PSD for Java Forum](https://forum.aspose.com/c/psd/34) untuk pertanyaan terkait dukungan.

### Q3: Apakah ada versi percobaan gratis untuk Aspose.PSD untuk Java?

A3: Ya, Anda dapat mengakses versi percobaan gratis [di sini](https://releases.aspose.com/).

### Q4: Bagaimana cara membeli lisensi untuk Aspose.PSD untuk Java?

A4: Anda dapat membeli lisensi dari [Halaman Pembelian Aspose.PSD](https://purchase.aspose.com/buy).

### Q5: Apakah lisensi sementara tersedia untuk Aspose.PSD untuk Java?

A5: Ya, Anda dapat memperoleh lisensi sementara [di sini](https://purchase.aspose.com/temporary-license/).

## Pertanyaan Tambahan yang Sering Diajukan

**Q: Bisakah saya menggambar bentuk lain selain persegi panjang?**  
A: Ya, kelas `Graphics` juga mendukung menggambar elips, garis, dan jalur khusus.

**Q: Apakah Aspose.PSD mendukung transparansi pada bentuk yang digambar?**  
A: Tentu saja; Anda dapat menggunakan `SolidBrush` dengan warna ARGB untuk menyertakan transparansi alfa.

**Q: Apakah memungkinkan mengedit opasitas sebuah layer?**  
A: Ya, setiap objek `Layer` memiliki metode `setOpacity` yang menerima nilai dari 0 hingga 255.

**Q: Bagaimana cara memuat file PSD yang sudah ada alih‑alih membuat yang baru?**  
A: Gunakan `PsdImage image = (PsdImage)Image.load("path/to/file.psd");` sebelum memanipulasi layer.

## Kesimpulan

Anda kini telah mempelajari cara **menggambar persegi panjang merah** dan bentuk dasar lainnya dalam file PSD menggunakan Aspose.PSD untuk Java Dengan membuat dokumen, menambahkan layer, menghapus latar belakangnya, dan menggambar menggunakan API `Graphics`, Anda dapat mengotomatisasi banyak tugas desain grafis.ajahi lebih lanjut dengan bereksperimen menggunakan kuas berbeda, efek layer, dan format file lainnya.

---

**Terakhir Diperbarui:** 2025-12-27  
**Diuji Dengan:** Aspose.PSD for Java 24.12 (terbaru pada saat penulisan)  
**Penulis:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}