---
date: 2025-12-08
description: Pelajari cara mengonversi PSD ke PNG dan mengubah ukuran gambar secara
  proporsional di Java menggunakan Aspose.PSD. Tutorial langkah demi langkah ini mencakup
  caching gambar, mengubah ukuran, dan menyimpan sebagai PNG.
language: id
linktitle: Convert PSD to PNG & Resize Proportionally
second_title: Aspose.PSD Java API
title: Cara Mengonversi PSD ke PNG dan Mengubah Ukuran Secara Proporsional dengan
  Aspose.PSD untuk Java
url: /java/advanced-image-manipulation/resize-image-proportionally/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cara Mengonversi PSD ke PNG dan Mengubah Ukuran Secara Proporsional dengan Aspose.PSD untuk Java

## Pendahuluan

Jika Anda perlu **mengonversi PSD ke PNG** sambil mempertahankan rasio aspek asli, Anda berada di tempat yang tepat. Dalam tutorial ini kami akan membahas tutorial **Aspose.PSD** lengkap yang menunjukkan **cara mengubah ukuran gambar** secara proporsional di Java, menyimpan gambar dalam cache untuk kinerja optimal, dan akhirnya menyimpan hasilnya sebagai PNG. Pada akhir tutorial Anda akan dapat mengintegrasikan alur kerja ini ke dalam pipeline pemrosesan gambar berbasis Java apa pun.

## Jawaban Cepat
- **Apakah Aspose.PSD dapat mengonversi PSD ke PNG?** Ya – cukup muat PSD dan simpan dengan `PngOptions`.
- **Apakah perpustakaan mendukung pengubahan ukuran secara proporsional?** Tentu saja; gunakan `resizeWidthProportionally` dan `resizeHeightProportionally`.
- **Apakah saya harus meng-cache gambar terlebih dahulu?** Caching (`image.cacheData()`) meningkatkan kinerja untuk file PSD berukuran besar.
- **Versi Java apa yang dibutuhkan?** Java 8 atau yang lebih baru sepenuhnya didukung.
- **Apakah lisensi diperlukan untuk produksi?** Ya, lisensi komersial menghapus watermark evaluasi.

## Apa itu “convert PSD to PNG” dan mengapa penting?

Mengonversi dokumen Photoshop (PSD) ke file portable network graphics (PNG) memungkinkan Anda berbagi desain berlapis dalam format ringan yang ramah web. PNG mempertahankan transparansi dan kualitas lossless, menjadikannya ideal untuk aset UI, thumbnail, atau skenario apa pun di mana fidelitas gambar penting.

## Mengapa mengubah ukuran gambar secara proporsional di Java?

Mengubah ukuran **cara mengubah ukuran gambar** tanpa mendistorsi rasio aspeknya memastikan grafik terlihat alami di berbagai layar. API `Aspose.PSD` menyediakan metode khusus untuk skala proporsional, yang secara otomatis menghitung tinggi atau lebar yang cocok, sehingga Anda tidak perlu melakukan perhitungan manual yang rawan kesalahan.

## Prasyarat

Sebelum kita masuk ke kode, pastikan Anda memiliki:

1. **Java Development Kit (JDK)** – Java 8 atau yang lebih baru terpasang.
2. **Aspose.PSD untuk Java** – unduh JAR terbaru dari situs resmi [di sini](https://releases.aspose.com/psd/java/).
3. File PSD contoh (`sample.psd`) yang ditempatkan di direktori yang dapat Anda referensikan dari proyek Anda.

## Impor Paket

Tambahkan impor yang diperlukan ke kelas Java Anda. Kelas‑kelas ini memberi Anda akses ke pemuatan gambar, caching, pengubahan ukuran, dan opsi output PNG.

```java
import com.aspose.psd.Image;
import com.aspose.psd.imageoptions.PngOptions;
```

## Langkah 1: Muat Gambar PSD

Pertama, muat file PSD sumber. Jika file berukuran besar, meng-cache data gambar mengurangi beban memori saat Anda melakukan operasi selanjutnya.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

Image image = Image.load(sourceFile);

if (!image.isCached()) {
    // Image caching java – improves performance for large files
    image.cacheData();
}
```

## Langkah 2: Ubah Ukuran Gambar Secara Proporsional (Java)

Sekarang tentukan dimensi baru. Pada contoh ini kami memperkecil gambar menjadi **setengah** ukuran aslinya sambil mempertahankan rasio aspek. Anda dapat menyesuaikan lebar atau tinggi target sesuai kebutuhan.

```java
int newWidth = image.getWidth() / 2;
image.resizeWidthProportionally(newWidth);

int newHeight = image.getHeight() / 2;
image.resizeHeightProportionally(newHeight);
```

> **Tip profesional:** Gunakan `resizeWidthProportionally` *atau* `resizeHeightProportionally`—perpustakaan secara otomatis menghitung dimensi lainnya agar gambar tetap proporsional.

## Langkah 3: Simpan Gambar yang Diubah Ukurannya sebagai PNG

Akhirnya, ekspor gambar yang telah diubah ukurannya ke format PNG. Langkah ini menyelesaikan alur kerja **convert PSD to PNG**.

```java
String destName = dataDir + "SimpleResizeImageProportionally_out.png";
image.save(destName, new PngOptions());
```

Saat kode dijalankan, Anda akan menemukan file PNG yang berukuran setengah dari PSD asli, dengan kualitas visual yang sama dan tanpa distorsi.

## Masalah Umum & Solusi

| Masalah | Penyebab | Solusi |
|-------|-------|-----|
| **OutOfMemoryError** | PSD besar tidak di‑cache | Panggil `image.cacheData()` sebelum mengubah ukuran |
| **Output PNG kosong** | Jalur file salah | Verifikasi `dataDir` dan izin menulis |
| **Rasio aspek tampak tidak tepat** | Menggunakan lebar dan tinggi secara manual | Gunakan metode proporsional yang disediakan oleh Aspose.PSD |

## Pertanyaan yang Sering Diajukan

**T: Apakah Aspose.PSD kompatibel dengan semua format gambar?**  
J: Aspose.PSD mendukung PSD, PNG, JPEG, BMP, GIF, dan banyak lagi. Lihat daftar lengkapnya di [dokumentasi](https://reference.aspose.com/psd/java/).

**T: Bisakah saya menggunakan Aspose.PSD untuk proyek komersial?**  
J: Ya. Beli lisensi komersial di [toko Aspose](https://purchase.aspose.com/buy).

**T: Apakah tersedia lisensi sementara untuk pengujian?**  
J: Tentu – minta lisensi sementara [di sini](https://purchase.aspose.com/temporary-license/) untuk tujuan evaluasi.

**T: Di mana saya dapat menemukan dukungan komunitas?**  
J: Forum [Aspose.PSD](https://forum.aspose.com/c/psd/34) adalah tempat yang bagus untuk mengajukan pertanyaan dan berbagi solusi.

**T: Bagaimana cara mengakses referensi API lengkap?**  
J: Dokumentasi API detail tersedia [di sini](https://reference.aspose.com/psd/java/).

## Kesimpulan

Anda kini tahu cara **mengonversi PSD ke PNG**, mengubah ukuran gambar secara proporsional, dan menangani caching secara efisien menggunakan Aspose.PSD untuk Java. Integrasikan langkah‑langkah ini ke dalam aplikasi Anda untuk memberikan pemrosesan gambar yang cepat dan berkualitas tinggi tanpa bergantung pada instalasi Photoshop native.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Terakhir Diperbarui:** 2025-12-08  
**Diuji Dengan:** Aspose.PSD 24.12 untuk Java  
**Penulis:** Aspose