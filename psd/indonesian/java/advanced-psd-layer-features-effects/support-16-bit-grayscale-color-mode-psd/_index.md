---
date: 2025-12-17
description: Pelajari cara mengonversi PSD ke PNG sambil mengatur mode warna PSD menjadi
  grayscale 16‑bit menggunakan Aspose.PSD untuk Java. Panduan langkah demi langkah
  dengan contoh kode.
linktitle: Convert PSD to PNG – 16-bit Grayscale – Java
second_title: Aspose.PSD Java API
title: Cara Mengonversi PSD ke PNG dengan Mode Warna Grayscale 16-bit di Java
url: /id/java/advanced-psd-layer-features-effects/support-16-bit-grayscale-color-mode-psd/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Mengonversi PSD ke PNG dengan Mode Warna Grayscale 16-bit di Java

## Introduction
Saat Anda menyelami dunia desain grafis dan manipulasi gambar, memahami cara **convert PSD to PNG** seperti memiliki senjata rahasia. Khususnya, menggunakan mode grayscale 16‑bit memberikan gambar Anda kedalaman dan detail yang menakjubkan sehingga benar‑benar menonjol. Dalam tutorial ini kami akan menjelaskan cara **set PSD color mode** ke grayscale 16‑bit dan kemudian **export PSD as PNG** menggunakan Aspose.PSD untuk Java. Siap meningkatkan alur kerja gambar Anda? Mari kita mulai.

## Quick Answers
- **Apa yang dimaksud dengan “convert PSD to PNG”?** Memuat sebuah PSD, opsional mengubah mode warnanya, dan menyimpannya sebagai file PNG.  
- **Kelas Aspose mana yang menangani konversi?** `PsdImage` memuat dan `PngOptions` untuk menyimpan.  
- **Apakah saya memerlukan lisensi khusus?** Versi trial dapat digunakan untuk pengujian; lisensi berbayar diperlukan untuk produksi.  
- **Bisakah saya mempertahankan kedalaman 16‑bit di PNG?** Ya, dengan menggunakan `PngColorType.GrayscaleWithAlpha`.  
- **IDE apa yang didukung?** Semua IDE Java – IntelliJ IDEA, Eclipse, VS Code, dll.

## Prerequisites
Sebelum kita mulai, pastikan Anda memiliki semua yang diperlukan untuk mendapatkan hasil terbaik dari tutorial ini. Berikut yang Anda perlukan:

1. **Java Development Kit (JDK)** – Pastikan Anda memiliki versi terbaru yang terpasang. Anda dapat mengunduhnya dari [Oracle's site](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. **Aspose.PSD for Java Library** – Ini adalah mesin yang memungkinkan kita memanipulasi file PSD. Dapatkan dari [Aspose download page](https://releases.aspose.com/psd/java/).  
3. **Sebuah IDE** – IntelliJ IDEA, Eclipse, atau Visual Studio Code akan berfungsi dengan baik.  
4. **Pengetahuan dasar Java** – Familiaritas dengan sintaks Java akan membuat langkah‑langkah lebih lancar.  
5. **File PSD contoh** – Buat satu di Adobe Photoshop atau unduh contoh gratis secara daring.

Siap? Bagus! Mari kita impor paket yang diperlukan dan mulai menulis kode.

## Import Packages
Untuk memulai, tambahkan impor Aspose.PSD yang diperlukan ke file Java Anda:

```java
import com.aspose.psd.*;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.ColorModes;
import com.aspose.psd.fileformats.psd.CompressionMethod;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.system.Enum;
```

## Step 1: Define Your Directories
Pertama, siapkan folder sumber dan output. Ini memberi tahu program di mana membaca PSD asli dan di mana menulis file yang telah dikonversi.

```java
String sourceDir = "Your Source Directory"; // Change to your source directory
String outputDir = "Your Document Directory"; // Change to your output directory
```

Ganti string placeholder dengan jalur sebenarnya di mesin Anda.

## Step 2: Create a Method to Handle Image Processing
Kami akan membungkus logika konversi dalam sebuah metode yang dapat digunakan kembali. Metode ini menerima semua parameter yang mungkin ingin Anda ubah, seperti mode warna, kedalaman bit, dan kompresi.

```java
class LocalScopeExtension {
    void saveToPsdThenLoadAndSaveToPng(
        String file,
        short colorMode,
        short channelBitsCount,
        short channelsCount,
        short compression,
        int layerNumber) {
```

Metode ini memungkinkan Anda **set PSD color mode** dan kemudian **export PSD as PNG** dalam satu alur.

## Step 3: Define File Paths and Load the PSD
Di dalam metode, bangun jalur file lengkap dan muat PSD grayscale 16‑bit asli:

```java
String filePath = sourceDir + file + ".psd";
String postfix = Enum.getName(ColorModes.class, colorMode) + channelBitsCount + "_" +
                 channelsCount + "_" + Enum.getName(CompressionMethod.class, compression);
String exportPath = outputDir + file + postfix + ".psd";
String pngExportPath = outputDir + file + postfix + ".png";
// Load a predefined 16-bit grayscale PSD
PsdImage image = (PsdImage)Image.load(filePath);
```

`postfix` membantu Anda melacak pengaturan yang digunakan untuk setiap file yang diekspor.

## Step : Process the Layer or Full Image
Sekarang kita dapat menggambar pada lapisan tertentu atau pada seluruh gambar. Pada contoh ini kami menambahkan batas abu-abu halus agar hasilnya lebih terlihat.

```java
try {
    RasterCachedImage raster = layerNumber >= 0 ? image.getLayers()[layerNumber] : image;
    // Draw a gray inner border around the perimeter of the layer
    Graphics graphics = new Graphics(raster);
    int width = raster.getWidth();
    int height = raster.getHeight();
    Rectangle rect = new Rectangle(
        width / 3,
        height / 3,
        width - (2 * (width / 3)) - 1,
        height - (2 * (height / 3)) - 1);
    graphics.drawRectangle(new Pen(Color.getDarkGray(), 1), rect);
```

Persegi panjang dihitung secara dinamis sehingga tetap berada di tengah terlepas dari ukuran gambar.

## Step 5: Save the Modified PSD File
Setelah menggambar, kami menyimpan PSD dengan mode warna dan kedalaman bit yang tepat seperti yang Anda tentukan. Ini adalah inti dari **setting PSD color mode** sebelum konversi.

```java
    // Save a copy of PSD with specific characteristics
    PsdOptions psdOptions = new PsdOptions();
    psdOptions.setColorMode(colorMode);
    psdOptions.setChannelBitsCount(channelBitsCount);
    psdOptions.setChannelsCount(channelsCount);
    psdOptions.setCompressionMethod(compression);
    image.save(exportPath, psdOptions);
}
```

## Step 6: Convert the PSD to PNG
Akhirnya, kami memuat PSD yang baru disimpan dan mengekspornya sebagai PNG. Dengan menggunakan `PngColorType.GrayscaleWithAlpha` kami mempertahankan kedalaman 16‑bit dalam file PNG.

```java
finally {
    image.dispose();
}
// Load the saved PSD
PsdImage image1 = (PsdImage)Image.load(exportPath);
try {
    // Convert the saved PSD to a grayscale PNG image
    PngOptions pngOptions = new PngOptions();
    pngOptions.setColorType(PngColorType.GrayscaleWithAlpha);
    image1.save(pngExportPath, pngOptions); // here should be no exception
}
finally {
    image1.dispose();
}
```

Sekarang Anda telah berhasil **converted PSD to PNG** sambil mempertahankan data grayscale 16‑bit berkualitas tinggi.

## Common Issues and Solutions
| Masalah | Mengapa Terjadi | Solusi |
|-------|----------------|-----|
| **“Unsupported color type” exception** | Mencoba menyimpan PSD dengan konfigurasi kanal yang tidak didukung. | Pastikan `channelBitsCount` sesuai dengan kedalaman bit sebenarnya (16) dan `channelsCount` benar untuk grayscale (1). |
| **File not found** | Jalur direktori sumber tidak benar. | Periksa kembali string `sourceDir` dan pastikan file PSD ada. |
| **Output PNG appears black** | PNG disimpan tanpa penanganan kanal alfa. | Gunakan `PngColorType.GrayscaleWithAlpha` seperti yang ditunjukkan di atas. |

## Frequently Asked Questions

**Q: Apa itu mode warna grayscale 16-bit?**  
A: Memberikan 65 536 tingkat abu-abu, memberikan detail tonal jauh lebih banyak dibandingkan standar 8‑bit (256 tingkat).

**Q: Bisakah saya menggunakan Aspose.PSD untuk gambar non‑grayscale?**  
A: Tentu saja! Aspose.PSD mendukung RGB, CMYK, Lab, dan banyak mode warna lainnya.

**Q: Apakah ada versi trial dari Aspose.PSD?**  
A: Ya, Anda dapat mencoba versi trial gratis Aspose.PSD. Kunjungi [Aspose download page](https://releases.aspose.com/).

**Q: Di mana saya dapat menemukan contoh lebih banyak tentang penggunaan Aspose.PSD?**  
A: Anda dapat melihat [documentation](https://reference.aspose.com/psd/java/) untuk contoh dan tutorial yang lebih mendalam.

**Q: Bagaimana cara membeli lisensi untuk Aspose.PSD?**  
A: Anda dapat membeli lisensi dengan mengunjungi [Aspose purchase page](https://purchase.aspose.com/buy).

---

**Terakhir Diperbarui:** 2025-12-17  
**Diuji Dengan:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**Penulis:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}