---
date: 2026-09-03
description: Pelajari cara membuat gradient stroke java dan menyesuaikan gradient
  stroke dalam file PSD menggunakan Aspose.PSD for Java. Panduan langkah demi langkah
  untuk pengembang.
keywords:
- create gradient stroke java
- add gradient stroke psd
- Aspose.PSD Java
- PSD gradient stroke
lastmod: 2026-09-03
linktitle: Cara Membuat Layer Gradient Stroke di Java
og_description: Buat gradient stroke java dengan Aspose.PSD for Java dalam hitungan
  menit. Tutorial ini menunjukkan cara menambahkan dan menyesuaikan gradient stroke
  dalam file PSD, lengkap dengan potongan kode dan praktik terbaik.
og_image_alt: Screenshot of a PSD file showing a gradient stroke applied via Aspose.PSD
  Java API
og_title: Buat gradient stroke java – Panduan tutorial Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-09-03'
  description: Learn how to create gradient stroke java and customize stroke gradients
    in PSD files using Aspose.PSD for Java. Step‑by‑step guide for developers.
  headline: Create gradient stroke java – Aspose.PSD tutorial guide
  type: TechArticle
- description: Learn how to create gradient stroke java and customize stroke gradients
    in PSD files using Aspose.PSD for Java. Step‑by‑step guide for developers.
  name: Create gradient stroke java – Aspose.PSD tutorial guide
  steps:
  - name: '**Java Development Kit (JDK)** – Install the latest JDK from [Oracle''s
      website](https://www.oracle.com/java/technologies/javase-downloads.html).'
    text: '**Java Development Kit (JDK)** – Install the latest JDK from [Oracle''s
      website](https://www.oracle.com/java/technologies/javase-downloads.html).'
  - name: '**Aspose.PSD for Java** – Download the library from the [Aspose.PSD download
      page](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD for Java** – Download the library from the [Aspose.PSD download
      page](https://releases.aspose.com/psd/java/).'
  - name: '**IDE** – IntelliJ IDEA, Eclipse, or NetBeans.'
    text: '**IDE** – IntelliJ IDEA, Eclipse, or NetBeans.'
  - name: '**License** – Obtain a [temporary license](https://purchase.aspose.com/temporary-license/)
      if you don’t have a full commercial license.'
    text: '**License** – Obtain a [temporary license](https://purchase.aspose.com/temporary-license/)
      if you don’t have a full commercial license.'
  type: HowTo
- questions:
  - answer: Aspose.PSD for Java is a pure‑Java library that lets developers create,
      edit, convert, and render Photoshop PSD files without requiring Adobe Photoshop.
    question: What is Aspose.PSD for Java?
  - answer: Yes, a valid license is required for production use. You can obtain a
      [temporary license](https://purchase.aspose.com/temporary-license/) for evaluation.
    question: Do I need a license to use Aspose.PSD for Java?
  - answer: Absolutely. Aspose.PSD provides APIs to build a new PSD document, add
      layers, apply effects, and save the file entirely programmatically.
    question: Can I create PSD files from scratch with this library?
  - answer: Yes, you can apply shadows, glows, bevels, and many other layer effects
      using the same effect‑based API.
    question: Is it possible to apply other effects besides gradient strokes?
  - answer: The official documentation is available in the [Aspose.PSD Java API reference](https://reference.aspose.com/psd/java/).
    question: Where can I find the full reference documentation?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- gradient stroke
- Aspose.PSD
- Java graphics
title: Buat gradient stroke java – Panduan tutorial Aspose.PSD
url: /id/java/java-graphics-drawing/add-stroke-layer-gradient/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cara membuat gradient stroke java dengan Aspose.PSD

## Pendahuluan
Jika Anda perlu **membuat gradient stroke java** tanpa membuka Photoshop, Anda berada di tempat yang tepat. Dalam tutorial ini Anda akan belajar cara menggunakan Aspose.PSD untuk Java—sebuah perpustakaan pure‑Java yang memberi Anda kontrol penuh secara programatik atas file PSD. Kami akan memandu proses memuat PSD, mengakses efek stroke lapisan, mengonfigurasi isian gradient, dan akhirnya menyimpan hasilnya. Pada akhir tutorial Anda akan dapat menambahkan outline gradient kelas profesional pada bentuk atau teks hanya dengan beberapa baris kode.

## Jawaban Cepat
- **Apa tujuan utama?** Membuat lapisan gradient stroke pada file PSD menggunakan Java.  
- **Perpustakaan mana yang menyediakan API?** Aspose.PSD untuk Java (mendukung Java 8 +).  
- **Apakah saya memerlukan lisensi untuk produksi?** Ya – lisensi yang valid atau sementara diperlukan.  
- **Berapa lama implementasi dasar memakan waktu?** Sekitar 10‑15 menit untuk stroke sederhana.  
- **Bisakah saya menyesuaikan tipe gradient?** Tentu – gradient linear, radial, dan berbasis sudut semuanya didukung.

## Apa itu lapisan gradient stroke?
Lapisan gradient stroke adalah outline vektor yang warnanya bertransisi mulus antara dua atau lebih nuansa. Lapisan ini dapat diterapkan pada bentuk, teks, atau mask vektor apa pun di dalam file PSD, memberikan desainer efek visual dinamis tanpa merasterkan karya.

## Mengapa menggunakan Aspose.PSD untuk Java?
Aspose.PSD untuk Java menyediakan **dukungan PSD lengkap** untuk lebih dari 100 fitur—termasuk lapisan, mask, lapisan penyesuaian, dan efek lapisan – dan dapat memproses file hingga 2 GB tanpa memuat seluruh dokumen ke memori. Perpustakaan ini berjalan pada sistem operasi apa pun yang mendukung Java, tidak memiliki dependensi native, dan diperbarui setiap bulan agar tetap kompatibel dengan spesifikasi file Photoshop terbaru.

## Prasyarat
1. **Java Development Kit (JDK)** – Instal JDK terbaru dari [situs Oracle](https://www.oracle.com/java/technologies/javase-downloads.html).  
2. **Aspose.PSD untuk Java** – Unduh perpustakaan dari [halaman unduhan Aspose.PSD](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse, atau NetBeans.  
4. **Lisensi** – Dapatkan [lisensi sementara](https://purchase.aspose.com/temporary-license/) jika Anda belum memiliki lisensi komersial penuh.

## Mengimpor paket
Pernyataan `import` membawa kelas yang diperlukan ke dalam ruang lingkup.  

```text
```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.examples.Utils.Assert;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.IGradientColorPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientColorPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientTransparencyPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientTransparencyPoint;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
```
```

Sekarang mari kita bagi proses menjadi langkah‑langkah yang jelas.

## Langkah 1: Memuat file PSD
Memuat file sumber adalah langkah pertama; Anda harus mengaktifkan sumber daya efek agar informasi stroke tersedia untuk diedit. **PsdLoadOptions** mengonfigurasi cara file PSD dimuat, memungkinkan Anda mengaktifkan atau menonaktifkan sumber daya tertentu.  

```text
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
String exportPath = dataDir + "StrokeGradientChanged.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```
```

## Langkah 2: Mengakses efek stroke
**StrokeEffect** mewakili gaya outline yang diterapkan pada sebuah lapisan, termasuk lebar, warna, dan isian gradient.  

```text
```java
StrokeEffect gradientStroke = (StrokeEffect) im.getLayers()[2].getBlendingOptions().getEffects()[0];
```
```

## Langkah 3: Memverifikasi properti efek stroke
Sebelum Anda mengubah apa pun, sebaiknya membaca properti yang ada. Ini membantu Anda memahami konfigurasi saat ini dan menghindari menimpa pengaturan penting secara tidak sengaja. **GradientFillSettings** menyimpan konfigurasi isian gradient untuk efek stroke.  

```text
```java
Assert.areEqual(BlendMode.Normal, gradientStroke.getBlendMode());
Assert.areEqual(255, gradientStroke.getOpacity());
Assert.areEqual(true, gradientStroke.isVisible());
GradientFillSettings fillSettings = (GradientFillSettings) gradientStroke.getFillSettings();
Assert.areEqual(Color.getBlack(), fillSettings.getColor());
Assert.areEqual(FillType.Gradient, fillSettings.getFillType());
Assert.areEqual(true, fillSettings.getAlignWithLayer());
Assert.areEqual(GradientType.Linear, fillSettings.getGradientType());
Assert.isTrue(Math.abs(90 - fillSettings.getAngle()) < 0.001, "Angle is incorrect");
Assert.areEqual(false, fillSettings.getDither());
Assert.isTrue(Math.abs(0 - fillSettings.getHorizontalOffset()) < 0.001, "Horizontal offset is incorrect");
Assert.isTrue(Math.abs(0 - fillSettings.getVerticalOffset()) < 0.001, "Vertical offset is incorrect");
Assert.areEqual(false, fillSettings.getReverse());
```
```

## Langkah 4: Mengubah pengaturan isian gradient
`GradientFill` mendefinisikan bagaimana warna bertransisi di sepanjang stroke. Anda dapat mengubah tipenya (linear, radial), sudut, dan mode pencampuran, kemudian menetapkan titik warna dan transparansi baru.  

```text
```java
fillSettings.setColor(Color.getGreen());
gradientStroke.setOpacity((byte) 127);
gradientStroke.setBlendMode(BlendMode.Color);
fillSettings.setAlignWithLayer(false);
fillSettings.setGradientType(GradientType.Radial);
fillSettings.setAngle(45);
fillSettings.setDither(true);
fillSettings.setHorizontalOffset(15);
fillSettings.setVerticalOffset(11);
fillSettings.setReverse(true);
```
```

## Langkah 5: Menambahkan dan mengubah titik warna serta transparansi
Gradient dibangun dari serangkaian titik henti warna dan titik henti opasitas. **GradientColorPoint** mendefinisikan titik henti warna dalam gradient, menentukan warnanya dan posisinya. **GradientTransparencyPoint** mendefinisikan titik henti opasitas dalam gradient, menentukan opasitas dan posisinya. Menambahkan atau menyesuaikan titik‑titik ini memungkinkan Anda membentuk aliran visual stroke.  

```text
```java
// Add new color point
GradientColorPoint colorPoint = fillSettings.addColorPoint();
colorPoint.setColor(Color.getGreen());
colorPoint.setLocation(4096);
colorPoint.setMedianPointLocation(75);
// Change location of previous point
fillSettings.getColorPoints()[1].setLocation(1899);
// Add new transparency point
GradientTransparencyPoint transparencyPoint = fillSettings.addTransparencyPoint();
transparencyPoint.setOpacity(25);
transparencyPoint.setMedianPointLocation(25);
transparencyPoint.setLocation(4096);
// Change location of previous transparency point
fillSettings.getTransparencyPoints()[1].setLocation(2411);
```
```

## Langkah 6: Menyimpan file PSD yang telah dimodifikasi
Setelah semua penyesuaian, tulis dokumen yang diperbarui kembali ke disk. Aspose.PSD secara otomatis mempertahankan semua lapisan dan sumber daya lainnya.  

```text
```java
im.save(exportPath);
```
```

## Langkah 7: Memverifikasi modifikasi
Muat kembali file yang disimpan dan pastikan bahwa properti gradient stroke sesuai dengan nilai yang Anda tetapkan. Langkah verifikasi ini penting untuk pipeline otomatis. **Assert** menyediakan pernyataan tes sederhana untuk memverifikasi kondisi selama runtime.  

```text
```java
PsdImage img = (PsdImage) Image.load(exportPath, loadOptions);
StrokeEffect gradientStrokeEffect = (StrokeEffect) img.getLayers()[2].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Color, gradientStrokeEffect.getBlendMode());
Assert.areEqual(127, gradientStrokeEffect.getOpacity());
Assert.areEqual(true, gradientStrokeEffect.isVisible());
GradientFillSettings fillSetting = (GradientFillSettings) gradientStrokeEffect.getFillSettings();
Assert.areEqual(Color.getGreen(), fillSetting.getColor());
Assert.areEqual(FillType.Gradient, fillSetting.getFillType());
// Check color points
Assert.areEqual(3, fillSetting.getColorPoints().length);
IGradientColorPoint point = fillSetting.getColorPoints()[0];
Assert.areEqual(50, point.getMedianPointLocation());
Assert.areEqual(Color.getBlack(), point.getColor());
Assert.areEqual(0, point.getLocation());
point = fillSettings.getColorPoints()[1];
Assert.areEqual(50, point.getMedianPointLocation());
Assert.areEqual(Color.getWhite(), point.getColor());
Assert.areEqual(1899, point.getLocation());
point = fillSettings.getColorPoints()[2];
Assert.areEqual(75, point.getMedianPointLocation());
Assert.areEqual(Color.getGreen(), point.getColor());
Assert.areEqual(4096, point.getLocation());
// Check transparency points
Assert.areEqual(3, fillSettings.getTransparencyPoints().length);
IGradientTransparencyPoint transparencyPoint1 = fillSettings.getTransparencyPoints()[0];
Assert.areEqual(50, transparencyPoint1.getMedianPointLocation());
Assert.areEqual(100, transparencyPoint1.getOpacity());
Assert.areEqual(0, transparencyPoint1.getLocation());
transparencyPoint1 = fillSettings.getTransparencyPoints()[1];
Assert.areEqual(50, transparencyPoint1.getMedianPointLocation());
Assert.areEqual(100, transparencyPoint1.getOpacity());
Assert.areEqual(2411, transparencyPoint1.getLocation());
transparencyPoint1 = fillSettings.getTransparencyPoints()[2];
Assert.areEqual(25, transparencyPoint1.getMedianPointLocation());
Assert.areEqual(25, transparencyPoint1.getOpacity());
Assert.areEqual(4096, transparencyPoint1.getLocation());
```
```

## Kesulitan umum dan tips pemecahan masalah
- **Kesalahan lisensi hilang** – Jika Anda melihat pengecualian lisensi, periksa kembali bahwa file lisensi sementara telah dimuat dengan benar sebelum panggilan API apa pun.  
- **Gradient tidak terlihat** – Pastikan flag `strokeEnabled` pada lapisan target diatur ke `true`; jika tidak efek akan diabaikan saat rendering.  
- **Kinerja pada file besar** – Untuk PSD yang lebih besar dari 500 MB, pertimbangkan menggunakan `PsdImage.load(..., LoadOptions)` dengan `loadResources = false` dan aktifkan hanya sumber daya yang Anda perlukan.

## Pertanyaan yang Sering Diajukan

**T: Apa itu Aspose.PSD untuk Java?**  
J: Aspose.PSD untuk Java adalah perpustakaan pure‑Java yang memungkinkan pengembang membuat, mengedit, mengonversi, dan merender file Photoshop PSD tanpa memerlukan Adobe Photoshop.

**T: Apakah saya memerlukan lisensi untuk menggunakan Aspose.PSD untuk Java?**  
J: Ya, lisensi yang valid diperlukan untuk penggunaan produksi. Anda dapat memperoleh [lisensi sementara](https://purchase.aspose.com/temporary-license/) untuk evaluasi.

**T: Bisakah saya membuat file PSD dari awal dengan perpustakaan ini?**  
J: Tentu. Aspose.PSD menyediakan API untuk membangun dokumen PSD baru, menambahkan lapisan, menerapkan efek, dan menyimpan file sepenuhnya secara programatik.

**T: Apakah memungkinkan menerapkan efek lain selain gradient stroke?**  
J: Ya, Anda dapat menerapkan bayangan, cahaya, bevel, dan banyak efek lapisan lainnya menggunakan API berbasis efek yang sama.

**T: Di mana saya dapat menemukan dokumentasi referensi lengkap?**  
J: Dokumentasi resmi tersedia di [referensi API Aspose.PSD Java](https://reference.aspose.com/psd/java/).

## Kesimpulan
Anda kini memiliki solusi lengkap, end‑to‑end untuk cara **membuat gradient stroke java** dalam file PSD menggunakan Aspose.PSD. Dengan memuat PSD, mengakses efek stroke, mengonfigurasi isian gradient, dan menyimpan file, Anda dapat mengotomatisasi alur kerja grafis canggih yang sebaliknya memerlukan pekerjaan manual di Photoshop. Bereksperimenlah dengan berbagai tipe gradient, mode pencampuran, dan titik opasitas untuk mencapai tampilan yang tepat bagi aplikasi Anda.

---

**Terakhir Diperbarui:** 2026-09-03  
**Diuji Dengan:** Aspose.PSD for Java 24.11  
**Penulis:** Aspose

## Tutorial Terkait

- [Buat Gradient Fill PSD dengan Java menggunakan Aspose.PSD – Tambahkan Lapisan Gradient Fill](/psd/java/psd-image-modification-conversion/add-gradient-fill-layer-psd-files/)
- [Cara Membuat Efek Gradient Radial di Aspose.PSD untuk Java](/psd/java/advanced-image-effects/add-gradient-effects/)
- [Cara Mengubah Warna Stroke Java Menggunakan Aspose.PSD](/psd/java/advanced-image-effects/add-stroke-layer-color/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}