---
date: 2026-08-28
description: Tambahkan pola ke lapisan di Java dengan Aspose.PSD. Ikuti panduan langkah
  demi langkah ini untuk menerapkan efek lapisan stroke, mengonfigurasi sumber daya
  pola, dan menyimpan file PSD Anda secara efisien.
keywords:
- add pattern to layer
- java add layer effect
- Aspose.PSD stroke pattern
lastmod: 2026-08-28
linktitle: Cara Menambahkan Pola Lapisan Stroke di Java
og_description: Tambahkan pola ke lapisan di Java menggunakan Aspose.PSD. Ikuti panduan
  singkat ini untuk menerapkan efek lapisan stroke, mengonfigurasi sumber daya pola,
  dan menyimpan file PSD Anda secara efisien.
og_image_alt: Guide showing how to add pattern to layer in Java with Aspose.PSD
og_title: Tambahkan pola ke lapisan di Java – tutorial Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-08-28'
  description: Add pattern to layer in Java with Aspose.PSD. Follow this step‑by‑step
    guide to apply a stroke layer effect, configure pattern resources, and save your
    PSD files efficiently.
  headline: How to add pattern to layer in Java
  type: TechArticle
- description: Add pattern to layer in Java with Aspose.PSD. Follow this step‑by‑step
    guide to apply a stroke layer effect, configure pattern resources, and save your
    PSD files efficiently.
  name: How to add pattern to layer in Java
  steps:
  - name: load the PSD file
    text: 'Loading the document gives you access to its layer hierarchy and effect
      collection. `PsdLoadOptions` configures how the PSD is read, while `PsdImage`
      represents the loaded file in memory. java String dataDir = "Your Document Directory";
      String sourceFileName = dataDir + "Stroke.psd"; PsdLoadOptions '
  - name: prepare new pattern data
    text: Create a `PatternResource` that holds the bitmap you want to tile as a stroke
      pattern. `PatternResource` is a PSD global resource that stores a repeating
      bitmap pattern. `Rectangle` defines the bounds of the pattern, and `UUID` provides
      a unique identifier. java int[] newPattern = new int[] { Color.
  - name: access the stroke effect
    text: Identify the shape layer that already has a stroke, then retrieve its `StrokeEffect`
      object. `StrokeEffect` represents the stroke layer effect applied to a shape
      layer. java StrokeEffect patternStroke = (StrokeEffect)im.getLayers()[3].getBlendingOptions().getEffects()[0];
      Assert.areEqual(BlendMode.N
  - name: modify the stroke effect
    text: Now update the stroke’s properties to reference the new pattern resource.
  - name: apply the new pattern
    text: '`PatternFillSettings` holds the fill settings for a pattern‑based stroke
      effect. Commit the changes to the layer and write the updated PSD back to disk.
      java ((PatternFillSettings)patternStroke.getFillSettings()).setPatternName("$$/Presets/Patterns/HorizontalLine1=Horizontal
      Line 9\0"); ((PatternFil'
  - name: verify the changes
    text: 'Reload the file and inspect the stroke to confirm the pattern appears as
      expected. java PsdImage img = (PsdImage)Image.load(sourceFileName, loadOptions);
      StrokeEffect patternStrokeEffect = (StrokeEffect)img.getLayers()[3].getBlendingOptions().getEffects()[0];
      PattResource resource1 = null; for (int '
  type: HowTo
- questions:
  - answer: Aspose.PSD for Java is a library that enables developers to create, edit,
      and convert PSD (Photoshop Document) files programmatically.
    question: What is Aspose.PSD for Java?
  - answer: Yes, you can use it in commercial projects. You can purchase a license
      from the **Aspose purchase page**([Aspose purchase page](https://purchase.aspose.com/buy)).
    question: Can I use Aspose.PSD for Java in a commercial project?
  - answer: Yes, you can download a free trial version from the **Aspose releases
      page**([Aspose releases page](https://releases.aspose.com/)).
    question: Is there a free trial available for Aspose.PSD for Java?
  - answer: You can get support from the Aspose community forums **here**([Aspose
      PSD community forum](https://forum.aspose.com/c/psd/34)).
    question: How can I get support for Aspose.PSD for Java?
  - answer: You need a JDK installed and an IDE for development. The library supports
      Windows, Linux, and macOS.
    question: What are the system requirements for Aspose.PSD for Java?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java graphics
- Aspose.PSD
- layer effects
title: Cara menambahkan pola ke lapisan di Java
url: /id/java/java-graphics-drawing/add-stroke-layer-pattern/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cara menambahkan pola ke lapisan di Java

## Pendahuluan
Menambahkan pola ke lapisan di Java adalah kebutuhan umum ketika Anda perlu memperkaya file Photoshop PSD dengan efek garis tepi khusus. Dengan Aspose.PSD for Java tugas ini menjadi sederhana, bahkan jika Anda baru mengenal perpustakaan ini. Dalam tutorial ini Anda akan belajar cara memuat PSD, membuat sumber pola, melampirkannya ke efek garis tepi, dan menyimpan hasilnya—semua dengan petunjuk langkah demi langkah yang jelas.

## Jawaban Cepat
- **Library apa yang dibutuhkan?** Aspose.PSD for Java.  
- **Berapa lama implementasinya?** Sekitar 10‑15 menit untuk pola dasar.  
- **Apakah saya memerlukan lisensi?** Versi percobaan gratis dapat digunakan untuk pengembangan; lisensi komersial diperlukan untuk produksi.  
- **Versi Java mana yang didukung?** JDK 8 atau yang lebih baru.  
- **Bisakah saya menggunakan ini dalam layanan web?** Ya, API bersifat platform‑agnostic dan bekerja di lingkungan Java apa pun.

## Apa itu menambahkan pola ke lapisan?
Menambahkan pola ke lapisan berarti menetapkan bitmap berulang (tiled) ke efek garis tepi atau isi sehingga grafik tersebut berulang di sepanjang kontur bentuk. Teknik ini banyak digunakan untuk border dekoratif, tekstur, dan overlay merek, memungkinkan desainer membuat tema visual yang konsisten tanpa harus menggambar setiap elemen secara manual.

## Mengapa menggunakan Aspose.PSD untuk tugas ini?
Aspose.PSD mendukung **lebih dari 30 format gambar** dan dapat memanipulasi file PSD hingga **2 GB** tanpa harus memuat seluruh dokumen ke memori, memberikan kinerja cepat pada perangkat keras server standar. API yang fluida memungkinkan Anda bekerja dengan efek lapisan secara programatis, menghilangkan kebutuhan Photoshop dalam alur kerja otomatis.

## Prasyarat
Sebelum memulai, pastikan Anda memiliki:
- Java Development Kit (JDK) 8 atau yang lebih baru terpasang.
- Aspose.PSD for Java – unduh dari **halaman unduhan Aspose.PSD for Java**([Aspose.PSD for Java download page](https://releases.aspose.com/psd/java/)) dan tambahkan JAR ke classpath proyek Anda.
- IDE seperti IntelliJ IDEA atau Eclipse untuk mengedit dan menjalankan kode contoh.
- File PSD contoh yang berisi lapisan bentuk yang ingin Anda modifikasi.

## Mengimpor paket
Pertama, impor namespace yang menyediakan akses ke objek PSD, sumber daya, dan efek.

```
// No actual code block is added to preserve original placeholders.
```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;
import com.aspose.psd.examples.Utils.Assert;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.PatternFillSettings;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.fileformats.psd.layers.layerresources.PattResource;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import java.util.UUID;
```
```

## Cara menambahkan pola ke lapisan di Java?

Muat PSD target, buat sumber pola, lampirkan ke efek garis tepi lapisan yang diinginkan, dan akhirnya simpan file. Alur end‑to‑end ini hanya memerlukan beberapa baris kode dan bekerja dengan PSD standar apa pun yang berisi lapisan bentuk vektor.

### Langkah 1: memuat file PSD
Memuat dokumen memberi Anda akses ke hierarki lapisan dan koleksi efeknya.  
`PsdLoadOptions` mengonfigurasi cara PSD dibaca, sementara `PsdImage` mewakili file yang dimuat di memori.

```
// Placeholder for original code.
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```
```

Dengan memuat file PSD, Anda kini dapat mengakses dan memanipulasi lapisan serta efeknya.

### Langkah 2: menyiapkan data pola baru
Buat `PatternResource` yang menyimpan bitmap yang ingin Anda ubah menjadi pola garis tepi berulang.  
`PatternResource` adalah sumber daya global PSD yang menyimpan pola bitmap berulang. `Rectangle` menentukan batas pola, dan `UUID` memberikan pengidentifikasi unik.

```
// Placeholder for original code.
```java
int[] newPattern = new int[]
{
    Color.getAqua().toArgb(), Color.getRed().toArgb(), Color.getRed().toArgb(), Color.getAqua().toArgb(),
    Color.getAqua().toArgb(), Color.getWhite().toArgb(), Color.getWhite().toArgb(), Color.getAqua().toArgb(),
    Color.getAqua().toArgb(), Color.getWhite().toArgb(), Color.getWhite().toArgb(), Color.getAqua().toArgb(),
    Color.getAqua().toArgb(), Color.getRed().toArgb(), Color.getRed().toArgb(), Color.getAqua().toArgb(),
};
Rectangle newPatternBounds = new Rectangle(0, 0, 4, 4);
UUID guid = UUID.randomUUID();
```
```

Data pola ini akan digunakan untuk membuat efek garis tepi baru.

### Langkah 3: mengakses efek garis tepi
Identifikasi lapisan bentuk yang sudah memiliki garis tepi, lalu ambil objek `StrokeEffect`‑nya.  
`StrokeEffect` mewakili efek garis tepi lapisan yang diterapkan pada lapisan bentuk.

```
// Placeholder for original code.
```java
StrokeEffect patternStroke = (StrokeEffect)im.getLayers()[3].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Normal, patternStroke.getBlendMode());
Assert.areEqual(255, patternStroke.getOpacity());
Assert.areEqual(true, patternStroke.isVisible());
PatternFillSettings fillSettings = (PatternFillSettings)patternStroke.getFillSettings();
Assert.areEqual(FillType.Pattern, fillSettings.getFillType());
```
```

Ini memastikan Anda bekerja dengan lapisan dan efek yang tepat.

### Langkah 4: memodifikasi efek garis tepi
Sekarang perbarui properti garis tepi untuk merujuk ke sumber pola baru.

#### Memperbarui properti efek garis tepi
```
// Placeholder for original code.
```java
patternStroke.setOpacity((byte)127);
patternStroke.setBlendMode(BlendMode.Color);
```
```

#### Memperbarui sumber pola
`PattResource` adalah sumber daya lapisan global PSD yang menyimpan data pola.

```
// Placeholder for original code.
```java
PattResource resource;
for (int i = 0; i < im.getGlobalLayerResources().length; i++)
{
    if (im.getGlobalLayerResources()[i] instanceof PattResource)
    {
        resource = (PattResource)im.getGlobalLayerResources()[i];
        resource.setPatternId(guid.toString());
        resource.setName("$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0");
        resource.setPattern(newPattern, newPatternBounds);
    }
}
```
```

Potongan kode ini menggantikan pola yang ada dengan pola yang Anda sediakan.

### Langkah 5: menerapkan pola baru
`PatternFillSettings` menyimpan pengaturan isi untuk efek garis tepi berbasis pola. Terapkan perubahan ke lapisan dan tulis kembali PSD yang diperbarui ke disk.

```
// Placeholder for original code.
```java
((PatternFillSettings)patternStroke.getFillSettings()).setPatternName("$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0");
((PatternFillSettings)patternStroke.getFillSettings()).setPatternId(guid.toString() + "\0");
im.save(exportPath);
```
```

Ini memastikan pola baru diterapkan dengan benar dan file disimpan dengan perubahan.

### Langkah 6: memverifikasi perubahan
Muat ulang file dan periksa garis tepi untuk memastikan pola muncul seperti yang diharapkan.

```
// Placeholder for original code.
```java
PsdImage img = (PsdImage)Image.load(sourceFileName, loadOptions);
StrokeEffect patternStrokeEffect = (StrokeEffect)img.getLayers()[3].getBlendingOptions().getEffects()[0];
PattResource resource1 = null;
for (int i = 0; i < img.getGlobalLayerResources().length; i++)
{
    if (img.getGlobalLayerResources()[i] instanceof PattResource)
    {
        resource1 = (PattResource)img.getGlobalLayerResources()[i];
    }
}
try
{
    Assert.areEqual(newPattern, resource1.getPatternData());
    Assert.areEqual(newPatternBounds, new Rectangle(0, 0, resource1.getWidth(), resource1.getHeight()));
    Assert.areEqual(guid.toString(), resource1.getPatternId());
    Assert.areEqual(BlendMode.Color, patternStrokeEffect.getBlendMode());
    Assert.areEqual(127, patternStrokeEffect.getOpacity());
    Assert.areEqual(true, patternStrokeEffect.isVisible());
    PatternFillSettings fillSettings1 = (PatternFillSettings)patternStrokeEffect.getFillSettings();
    Assert.areEqual(FillType.Pattern, fillSettings1.getFillType());
}
catch (Exception e)
{
    System.out.println(e.getMessage());
}
```
```

Langkah ini memverifikasi bahwa data pola telah diterapkan dengan benar pada efek garis tepi.

## Masalah umum dan pemecahan masalah
- **Pola tidak terlihat:** Pastikan DPI gambar pola cocok dengan resolusi PSD, dan flag `Enabled` pada garis tepi diatur ke `true`.  
- **File PSD besar menyebabkan OutOfMemoryError:** Gunakan `PsdImage.load(..., LoadOptions)` dengan `LoadOptions.setLoadAllLayers(false)` untuk memuat lapisan sesuai permintaan.  
- **Lapisan yang dipilih tidak tepat:** Verifikasi indeks atau nama lapisan sebelum mengakses efeknya; Anda dapat menenumerasi `psdImage.getLayers()` untuk melihat lapisan yang tersedia.

## Pertanyaan yang sering diajukan

**Q: Apa itu Aspose.PSD for Java?**  
A: Aspose.PSD for Java adalah perpustakaan yang memungkinkan pengembang membuat, mengedit, dan mengonversi file PSD (Photoshop Document) secara programatis.

**Q: Bisakah saya menggunakan Aspose.PSD for Java dalam proyek komersial?**  
A: Ya, Anda dapat menggunakannya dalam proyek komersial. Anda dapat membeli lisensi dari **halaman pembelian Aspose**([Aspose purchase page](https://purchase.aspose.com/buy)).

**Q: Apakah tersedia versi percobaan gratis untuk Aspose.PSD for Java?**  
A: Ya, Anda dapat mengunduh versi percobaan gratis dari **halaman rilis Aspose**([Aspose releases page](https://releases.aspose.com/)).

**Q: Bagaimana saya dapat mendapatkan dukungan untuk Aspose.PSD for Java?**  
A: Anda dapat memperoleh dukungan dari forum komunitas Aspose **di sini**([Aspose PSD community forum](https://forum.aspose.com/c/psd/34)).

**Q: Apa persyaratan sistem untuk Aspose.PSD for Java?**  
A: Anda memerlukan JDK yang terpasang dan IDE untuk pengembangan. Perpustakaan ini mendukung Windows, Linux, dan macOS.

## Kesimpulan
Anda kini telah mempelajari cara menambahkan pola ke lapisan di Java menggunakan Aspose.PSD. Dengan mengikuti langkah‑langkah di atas, Anda dapat secara programatis meningkatkan file PSD dengan pola garis tepi khusus, mengotomatisasi alur kerja branding, dan mengintegrasikan pemrosesan grafis ke dalam aplikasi berbasis Java apa pun. Jelajahi fitur Aspose.PSD lainnya seperti penggabungan lapisan, penyesuaian warna, dan ekspor ke PNG atau JPEG untuk memperluas toolkit pemrosesan gambar Anda.

---

**Terakhir Diperbarui:** 2026-08-28  
**Diuji Dengan:** Aspose.PSD 24.11 for Java  
**Penulis:** Aspose

## Tutorial Terkait

- [Render Pattern Fill Layer Psd Files](/psd/java/advanced-psd-layer-features-effects/render-pattern-fill-layer-psd-files/)
- [Pattern Overlay PSD: Tambahkan Efek dengan Aspose.PSD for Java](/psd/java/advanced-image-effects/add-pattern-effects/)
- [Cara Mengubah Warna Garis Tepi Java Menggunakan Aspose.PSD](/psd/java/advanced-image-effects/add-stroke-layer-color/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}
{{< blocks/products/products-backtop-button >}}