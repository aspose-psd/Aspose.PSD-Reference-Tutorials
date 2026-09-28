---
date: 2026-09-28
description: Pelajari cara mengekspor PSD sebagai PNG sambil mengatur mode warna PSD
  ke grayscale 16‑bit menggunakan Aspose.PSD for Java. Panduan langkah‑demi‑langkah
  dengan contoh kode.
keywords:
- export psd as png
- how to convert psd to png
- 16-bit grayscale java
lastmod: 2026-09-28
linktitle: Ekspor PSD sebagai PNG – Grayscale 16‑bit – Java
og_description: Ekspor PSD sebagai PNG dengan grayscale 16‑bit menggunakan Aspose.PSD
  for Java. Ikuti tutorial langkah‑demi‑langkah ini untuk mempertahankan 65.536 nuansa
  abu-abu.
og_image_alt: Guide showing how to export PSD as PNG with 16-bit grayscale using Aspose.PSD
  Java
og_title: Ekspor PSD sebagai PNG dengan grayscale 16‑bit di Java – Panduan Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-09-28'
  description: Learn how to export PSD as PNG while setting PSD color mode to 16-bit
    grayscale using Aspose.PSD for Java. Step‑by‑step guide with code examples.
  headline: How to export PSD as PNG with 16‑bit grayscale color mode in Java
  type: TechArticle
- description: Learn how to export PSD as PNG while setting PSD color mode to 16-bit
    grayscale using Aspose.PSD for Java. Step‑by‑step guide with code examples.
  name: How to export PSD as PNG with 16‑bit grayscale color mode in Java
  steps:
  - name: '**Java Development Kit (JDK)** – Install the latest JDK from [Oracle''s
      site](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
    text: '**Java Development Kit (JDK)** – Install the latest JDK from [Oracle''s
      site](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
  - name: '**Aspose.PSD for Java library** – Download the JAR from the [Aspose download
      page](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD for Java library** – Download the JAR from the [Aspose download
      page](https://releases.aspose.com/psd/java/).'
  - name: '**An IDE** – IntelliJ IDEA, Eclipse, or Visual Studio Code works perfectly.'
    text: '**An IDE** – IntelliJ IDEA, Eclipse, or Visual Studio Code works perfectly.'
  - name: '**Basic Java knowledge** – You should be comfortable creating classes,
      handling exceptions, and working with file paths.'
    text: '**Basic Java knowledge** – You should be comfortable creating classes,
      handling exceptions, and working with file paths.'
  - name: '**A sample PSD file** – Create one in Adobe Photoshop or grab a free sample
      online.'
    text: '**A sample PSD file** – Create one in Adobe Photoshop or grab a free sample
      online.'
  type: HowTo
- questions:
  - answer: It provides 65 536 shades of gray, delivering far more tonal detail than
      the standard 8‑bit (256 shades).
    question: What is 16‑bit grayscale color mode?
  - answer: Absolutely! Aspose.PSD supports RGB, CMYK, Lab, Indexed, and many other
      color modes.
    question: Can I use Aspose.PSD for non‑grayscale images?
  - answer: Yes, you can try a free trial version of Aspose.PSD. Just head to the
      [Aspose download page](https://releases.aspose.com/).
    question: Is there a trial version of Aspose.PSD?
  - answer: Check the official [documentation](https://reference.aspose.com/psd/java/)
      for in‑depth tutorials, API references, and sample projects.
    question: Where can I find more Aspose.PSD examples?
  - answer: You can buy a license by visiting the [Aspose purchase page](https://purchase.aspose.com/buy).
    question: How do I purchase a license for Aspose.PSD?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- convert psd
- Aspose.PSD
- Java image processing
title: Cara mengekspor PSD sebagai PNG dengan mode warna grayscale 16‑bit di Java
url: /id/java/advanced-psd-layer-features-effects/support-16-bit-grayscale-color-mode-psd/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ekspor PSD sebagai PNG dengan mode warna grayscale 16‑bit di Java

## Pendahuluan
Mengekspor PSD sebagai PNG sambil mempertahankan mode warna grayscale 16‑bit memberi Anda kedalaman foto profesional dan kompatibilitas universal PNG. Dalam panduan ini Anda akan belajar cara **mengatur mode warna PSD menjadi grayscale 16‑bit** dan kemudian **mengekspor PSD sebagai PNG** menggunakan Aspose.PSD untuk Java. Tutorial ini mencakup semua hal mulai dari prasyarat hingga pemecahan masalah, sehingga Anda dapat mengintegrasikan alur kerja ke dalam pipeline gambar berbasis Java apa pun.

## Jawaban Cepat
- **Apa yang dimaksud dengan “ekspor PSD sebagai PNG”?** Muat sebuah PSD, opsional ubah mode warnanya, dan simpan sebagai file PNG.  
- **Kelas Aspose mana yang menangani konversi?** `PsdImage` memuat PSD dan `PngOptions` menentukan pengaturan output PNG.  
- **Apakah saya memerlukan lisensi untuk produksi?** Ya – versi percobaan dapat digunakan untuk pengujian, tetapi lisensi berbayar diperlukan untuk penggunaan komersial.  
- **Apakah kedalaman 16‑bit dapat dipertahankan dalam PNG?** Tentu saja, dengan menggunakan `PngColorType.GrayscaleWithAlpha`.  
- **IDE mana yang didukung?** Semua IDE Java – IntelliJ IDEA, Eclipse, VS Code, atau NetBeans.

## Apa itu ekspor PSD sebagai PNG?
Ekspor PSD sebagai PNG adalah proses mengonversi dokumen Adobe Photoshop (PSD) menjadi file Portable Network Graphics (PNG) sambil mempertahankan data piksel dan kedalaman warna gambar. Konversi ini biasanya digunakan untuk berbagi aset grayscale berkualitas tinggi di web tanpa kehilangan detail tonal.

## Mengapa mengekspor PSD sebagai PNG dengan grayscale 16‑bit?
Mengekspor ke PNG sambil mempertahankan grayscale 16‑bit mempertahankan 65 536 nuansa abu-abu, yang memberikan kekayaan tonal jauh lebih tinggi dibandingkan gambar 8‑bit. Dukungan universal PNG memastikan file dapat ditampilkan di browser, aplikasi seluler, dan editor desktop tanpa kehilangan, sementara kompresi lossless Aspose.PSD menjamin tidak ada artefak yang muncul.

## Prasyarat
Sebelum memulai, pastikan Anda memiliki item berikut siap:

1. **Java Development Kit (JDK)** – Instal JDK terbaru dari [Oracle's site](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. **Aspose.PSD for Java library** – Unduh JAR dari [Aspose download page](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse, atau Visual Studio Code berfungsi dengan baik.  
4. **Pengetahuan dasar Java** – Anda harus nyaman membuat kelas, menangani pengecualian, dan bekerja dengan jalur file.  
5. **File PSD contoh** – Buat satu di Adobe Photoshop atau dapatkan contoh gratis secara daring.

## Cara mengekspor PSD sebagai PNG langkah demi langkah

## Bagaimana cara mengatur mode warna PSD menjadi grayscale 16‑bit?
PsdImage adalah kelas Aspose.PSD yang memuat dan merepresentasikan file PSD dalam memori.  
ColorMode adalah enumerasi yang mendefinisikan mode warna gambar PSD.  

Muat PSD dengan `PsdImage`, ubah mode warnanya menggunakan properti `ColorMode`, lalu simpan file yang telah dimodifikasi. Operasi ini berjalan sepenuhnya dalam memori, menghilangkan kebutuhan file perantara dan memastikan konversi cepat serta efisien.

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

Impor ini memberi Anda akses ke fungsionalitas yang akan Anda gunakan untuk memanipulasi file PSD, mengatur mode warna, dan mengekspor hasilnya sebagai PNG.

## Bagaimana cara mendefinisikan direktori sumber dan output?
`File` adalah kelas java.io yang merepresentasikan jalur file atau direktori pada sistem file.  

Anda perlu memberi tahu program di mana membaca PSD asli dan di mana menulis PNG yang dikonversi. Menggunakan jalur absolut atau relatif berfungsi, tetapi pertahankan konsistensinya di seluruh lingkungan untuk menghindari kesalahan resolusi jalur.

```java
String sourceDir = "Your Source Directory"; // Change to your source directory
String outputDir = "Your Document Directory"; // Change to your output directory
```

Ganti string placeholder dengan jalur sebenarnya di mesin Anda.

## Bagaimana cara mengenkapsulasi logika konversi dalam metode yang dapat digunakan kembali?
`convertPsdToPng` adalah metode khusus yang mengenkapsulasi semua langkah yang diperlukan untuk mengonversi file PSD ke PNG dengan pengaturan opsional.  

Membuat metode khusus memungkinkan Anda menggunakan kembali langkah konversi yang sama untuk banyak file atau pengaturan berbeda. Lewatkan parameter seperti jalur sumber, folder tujuan, dan tingkat kompresi opsional, menjadikan alur kerja fleksibel dan mudah dipelihara.

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

Metode ini memungkinkan Anda **mengatur mode warna PSD** dan kemudian **mengekspor PSD sebagai PNG** dalam satu alur.

## Bagaimana cara memuat PSD dan menerapkan mode grayscale 16‑bit?
PsdImage adalah kelas Aspose.PSD yang memuat file PSD ke dalam memori.  
ColorMode.GRAYSCALE_16 adalah nilai enumerasi yang mengatur gambar menjadi grayscale 16‑bit.  
`channelBitsCount` adalah properti yang menentukan jumlah bit per kanal.  

Di dalam metode konversi, bangun jalur file lengkap, buat instance `PsdImage`, dan ubah `ColorMode`-nya menjadi `ColorMode.GRAYSCALE_16`. Properti `channelBitsCount` harus diatur ke 16 untuk mempertahankan kedalaman bit tinggi, memastikan gambar menyimpan semua informasi tonal.

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

## Bagaimana cara menggambar batas halus pada gambar (langkah opsional)?
`Graphics` adalah kelas yang menyediakan kemampuan menggambar pada kanvas `PsdImage`.  

Anda dapat secara opsional menggambar persegi panjang abu-abu di sekitar gambar untuk membuat output lebih terlihat selama pengujian. Langkah ini menunjukkan cara bekerja dengan lapisan dan objek grafis, dan persegi panjang dihitung secara dinamis sehingga tetap terpusat terlepas dari ukuran gambar.

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

Persegi panjang dihitung secara dinamis sehingga tetap terpusat terlepas dari ukuran gambar.

## Bagaimana cara menyimpan PSD yang dimodifikasi dengan mode warna baru?
`PsdOptions` adalah kelas yang mengontrol cara file PSD disimpan, termasuk pengaturan mode warna dan kedalaman bit.  

Setelah menggambar (atau melewatkan langkah tersebut), panggil `save` pada instance `PsdImage`, dengan memberikan objek `PsdOptions` yang mempertahankan konfigurasi grayscale 16‑bit. Ini memastikan PSD yang disimpan mempertahankan mode warna yang diinginkan tanpa kehilangan data.

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

## Bagaimana cara mengonversi PSD ke PNG sambil mempertahankan kedalaman 16‑bit?
`PngOptions` adalah kelas yang mendefinisikan pengaturan output PNG seperti tipe warna dan tingkat kompresi.  
`PngColorType.GrayscaleWithAlpha` adalah nilai enumerasi yang menyimpan data grayscale 16‑bit dengan saluran alfa.  

Muat PSD yang baru disimpan, konfigurasikan `PngOptions` dengan `PngColorType.GrayscaleWithAlpha`, dan panggil `save`. Ini mempertahankan data grayscale 16‑bit di dalam file PNG, memberikan gambar lossless berkualitas tinggi yang cocok untuk pemrosesan atau distribusi lebih lanjut.

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

Sekarang Anda telah berhasil **mengekspor PSD sebagai PNG** sambil mempertahankan data grayscale 16‑bit berkualitas tinggi.

## Masalah umum dan solusi
| Issue | Why it happens | Fix |
|-------|----------------|-----|
| **“Unsupported color type” exception** | Mencoba menyimpan PSD dengan konfigurasi kanal yang tidak didukung. | Pastikan `channelBitsCount` sesuai dengan kedalaman bit sebenarnya (16) dan `channelsCount` benar untuk grayscale (1). |
| **File not found** | Jalur direktori sumber tidak benar. | Periksa kembali string `sourceDir` dan pastikan file PSD ada di lokasi tersebut. |
| **Output PNG appears black** | PNG disimpan tanpa penanganan alfa yang tepat. | Gunakan `PngColorType.GrayscaleWithAlpha` seperti yang ditunjukkan di atas. |
| **Memory overflow on large PSDs** | Memuat seluruh file ke memori. | Aktifkan mode streaming via `PsdImage.load(inputStream, new LoadOptions())` untuk memproses file besar secara efisien. |

## Pertanyaan yang sering diajukan

**Q: What is 16‑bit grayscale color mode?**  
A: Memberikan 65 536 nuansa abu-abu, memberikan detail tonal jauh lebih banyak dibandingkan standar 8‑bit (256 nuansa).

**Q: Can I use Aspose.PSD for non‑grayscale images?**  
A: Tentu saja! Aspose.PSD mendukung RGB, CMYK, Lab, Indexed, dan banyak mode warna lainnya.

**Q: Is there a trial version of Aspose.PSD?**  
A: Ya, Anda dapat mencoba versi percobaan gratis Aspose.PSD. Kunjungi [Aspose download page](https://releases.aspose.com/).

**Q: Where can I find more Aspose.PSD examples?**  
A: Lihat [documentation](https://reference.aspose.com/psd/java/) resmi untuk tutorial mendalam, referensi API, dan contoh proyek.

**Q: How do I purchase a license for Aspose.PSD?**  
A: Anda dapat membeli lisensi dengan mengunjungi [Aspose purchase page](https://purchase.aspose.com/buy).

**Terakhir Diperbarui:** 2026-09-28  
**Diuji Dengan:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**Penulis:** Aspose

## Tutorial Terkait

- [Convert PSD to PNG with Specified Bit Depth Using Aspose.PSD for Java](/psd/java/optimizing-png-files/specify-png-bit-depth/)
- [Export PSD to PNG with Layer Effects using Aspose.PSD for Java](/psd/java/psd-image-modification-conversion/apply-layer-effects-psd-files/)
- [Save PSD as JPEG and Support RGB Color with Aspose.PSD Java](/psd/java/advanced-psd-layer-features-effects/support-rgb-color-psd-files/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}