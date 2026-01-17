---
date: 2026-01-17
description: Pelajari cara menambahkan pola goresan java dengan Aspose.PSD untuk Java.
  Ikuti panduan langkah demi langkah ini untuk meningkatkan gambar PSD Anda dengan
  cepat.
linktitle: How to Add Stroke Layer Pattern in Java
second_title: Aspose.PSD Java API
title: Cara Menambahkan Pola Goresan di Java Menggunakan Aspose.PSD
url: /id/java/java-graphics-drawing/add-stroke-layer-pattern/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cara Menambahkan Pola Garis Stroke Java Menggunakan Aspose.PSD

## Pendahuluan
Jika Anda perlu **menambahkan pola stroke java** ke file Photoshop, Aspose.PSD untuk Java membuatnya sangat sederhana. Baik Anda sedang membangun alat desain grafis, mengotomatiskan penyuntingan batch, atau sekadar bereksperimen dengan efek lapisan, tutorial ini akan memandu Anda melalui setiap langkah—dari memuat PSD hingga memverifikasi pola baru. Mari kita mulai dan lihat betapa cepatnya Anda dapat meningkatkan gambar Anda.

## Jawaban Cepat
- **Perpustakaan apa yang saya perlukan?** Aspose.PSD untuk Java  
- **Versi Java mana yang didukung?** JDK 8 atau yang lebih baru  
- **Apakah saya memerlukan lisensi untuk pengujian?** Versi percobaan gratis cukup untuk pengembangan; lisensi diperlukan untuk produksi  
- **Berapa lama implementasinya?** Sekitar 10‑15 menit untuk pola stroke dasar  
- **Bisakah saya menggunakan kembali pola pada beberapa lapisan?** Ya, cukup tetapkan `PattResource` yang sama ke lapisan lain  

## Apa itu menambahkan pola stroke java?
Menambahkan pola stroke dalam Java berarti menerapkan isian khusus (biasanya bitmap berulang) ke efek stroke sebuah lapisan. Teknik ini memungkinkan Anda membuat outline yang bergaya—misalnya garis putus-putus, tekstur batu bata, atau border grafis khusus—langsung di dalam file PSD tanpa membuka Photoshop.

## Mengapa Menggunakan Aspose.PSD untuk menambahkan pola stroke java?
- **Kesetiaan PSD penuh** – Semua efek lapisan, sumber daya, dan mode perpaduan dipertahankan.  
- **Tidak memerlukan Photoshop asli** – Berfungsi di semua OS dengan JDK.  
- **Kontrol programatik** – Otomatiskan pemrosesan batch atau integrasikan ke layanan sisi‑server.  
- **API kaya** – Akses ke sumber daya global, isian pola, dan mode perpaduan dalam satu antarmuka yang fluida.

## Prasyarat
- **Java Development Kit (JDK)** – Pastikan JDK 8 atau yang lebih baru telah terpasang.  
- **Aspose.PSD untuk Java** – Unduh perpustakaan dari [here](https://releases.aspose.com/psd/java/) dan tambahkan JAR ke classpath proyek Anda.  
- **IDE** – IntelliJ IDEA, Eclipse, atau editor apa pun yang Anda sukai.

## Mengimpor Paket
Pertama, impor kelas‑kelas yang diperlukan untuk menangani file PSD, warna, persegi panjang, dan efek stroke.

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

## Langkah 1: Memuat File PSD
Muat PSD sumber sehingga Anda dapat bekerja dengan lapisan dan sumber dayanya.

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

## Langkah 2: Menyiapkan Data Pola Baru
Buat pola sederhana berukuran 4 × 4 piksel yang akan digunakan untuk stroke.

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

## Langkah 3: Mengakses Efek Stroke
Temukan efek stroke pada lapisan target (dalam contoh ini, lapisan keempat).

```java
StrokeEffect patternStroke = (StrokeEffect)im.getLayers()[3].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Normal, patternStroke.getBlendMode());
Assert.areEqual(255, patternStroke.getOpacity());
Assert.areEqual(true, patternStroke.isVisible());
PatternFillSettings fillSettings = (PatternFillSettings)patternStroke.getFillSettings();
Assert.areEqual(FillType.Pattern, fillSettings.getFillType());
```

## Langkah 4: Memodifikasi Efek Stroke
### Memperbarui Properti Efek Stroke
Sesuaikan opacity dan mode perpaduan untuk melihat dampak visual pola baru.

```java
patternStroke.setOpacity((byte)127);
patternStroke.setBlendMode(BlendMode.Color);
```

### Memperbarui Sumber Daya Pola
Ganti sumber daya pola global yang ada dengan yang baru saja Anda buat.

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

## Langkah 5: Menerapkan Pola Baru
Hubungkan sumber daya pola yang diperbarui ke efek stroke dan simpan PSD.

```java
((PatternFillSettings)patternStroke.getFillSettings()).setPatternName("$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0");
((PatternFillSettings)patternStroke.getFillSettings()).setPatternId(guid.toString() + "\0");
im.save(exportPath);
```

## Langkah 6: Memverifikasi Perubahan
Muat ulang file dan pastikan bahwa pola baru, opacity, serta mode perpaduan telah diterapkan dengan benar.

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

## Masalah Umum dan Solusinya
| Masalah | Penyebab | Solusi |
|-------|-------|-----|
| Pola tidak muncul | Referensi `PatternId` salah | Pastikan `PatternId` yang ditetapkan pada `PattResource` cocok dengan yang digunakan di `PatternFillSettings`. |
| Stroke menghilang setelah disimpan | Opacity diatur ke 0 atau efek disembunyikan | Verifikasi `setOpacity` berada di antara 0‑255 dan `isVisible()` mengembalikan `true`. |
| Warna tidak sesuai harapan | Mode perpaduan tidak cocok | Gunakan `BlendMode.Color` (atau mode lain) yang sesuai dengan tujuan desain Anda. |

## FAQ
### Apa itu Aspose.PSD untuk Java?
Aspose.PSD untuk Java adalah perpustakaan yang memungkinkan pengembang membuat, mengedit, dan mengonversi file PSD (Photoshop Document) secara programatik.

### Bisakah saya menggunakan Aspose.PSD untuk Java dalam proyek komersial?
Ya, Anda dapat menggunakannya dalam proyek komersial. Anda dapat membeli lisensi dari [here](https://purchase.aspose.com/buy).

### Apakah tersedia versi percobaan gratis untuk Aspose.PSD untuk Java?
Ya, Anda dapat mengunduh versi percobaan gratis dari [here](https://releases.aspose.com/).

### Bagaimana cara mendapatkan dukungan untuk Aspose.PSD untuk Java?
Anda dapat mendapatkan dukungan melalui forum komunitas Aspose [here](https://forum.aspose.com/c/psd/34).

### Apa saja persyaratan sistem untuk Aspose.PSD untuk Java?
Anda memerlukan JDK terpasang dan IDE untuk pengembangan. Perpustakaan ini mendukung berbagai sistem operasi termasuk Windows, Linux, dan macOS.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Terakhir Diperbarui:** 2026-01-17  
**Diuji Dengan:** Aspose.PSD untuk Java 24.12 (versi terbaru pada saat penulisan)  
**Penulis:** Aspose