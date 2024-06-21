---
title: Bagaimana Menambahkan Pola Lapisan Stroke di Java
linktitle: Bagaimana Menambahkan Pola Lapisan Stroke di Java
second_title: Asumsikan.PSD Java API
description: Pelajari cara menambahkan pola lapisan guratan ke file PSD menggunakan Aspose.PSD untuk Java. Ikuti panduan langkah demi langkah ini untuk menyempurnakan gambar Anda dengan mudah.
type: docs
weight: 11
url: /id/java/java-graphics-drawing/add-stroke-layer-pattern/
---
## Perkenalan
Menambahkan pola lapisan guratan ke gambar di Java mungkin terdengar seperti tugas yang menakutkan, namun dengan Aspose.PSD untuk Java, ini lebih mudah dari yang Anda kira. Baik Anda mendesain grafis atau mengerjakan aplikasi pengeditan foto, panduan ini akan memandu Anda melalui prosesnya langkah demi langkah. Siap untuk memulai? Ayo selami!
## Prasyarat
Sebelum memulai, Anda memerlukan beberapa hal:
- Java Development Kit (JDK): Pastikan Anda telah menginstal JDK di sistem Anda.
-  Aspose.PSD untuk Java: Unduh perpustakaan dari[Di Sini](https://releases.aspose.com/psd/java/) dan sertakan dalam proyek Anda.
- Sebuah IDE: Gunakan Lingkungan Pengembangan Terpadu (IDE) favorit Anda seperti IntelliJ IDEA atau Eclipse.
## Paket Impor
Hal pertama yang pertama, Anda perlu mengimpor paket yang diperlukan ke proyek Java Anda. Paket-paket ini penting untuk bekerja dengan Aspose.PSD.
```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;
import com.aspose.psd.examples.Utils.Assert;
import com.aspose.psd.examples.Utils.Utils;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.PatternFillSettings;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.fileformats.psd.layers.layerresources.PattResource;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import java.util.UUID;
```
## Langkah 1: Muat File PSD
Langkah pertama dalam menambahkan pola layer stroke adalah memuat file PSD yang ingin Anda edit.
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```
Dengan memuat file PSD, kini Anda dapat mengakses dan memanipulasi lapisan dan efeknya.
## Langkah 2: Siapkan Data Pola Baru
Selanjutnya, Anda perlu menyiapkan data pola baru yang akan Anda terapkan pada layer stroke.
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
Data pola ini akan digunakan untuk membuat efek guratan baru.
## Langkah 3: Akses Efek Stroke
Untuk mengubah efek guratan, Anda perlu mengakses lapisan tertentu dan opsi pencampurannya.
```java
StrokeEffect patternStroke = (StrokeEffect)im.getLayers()[3].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Normal, patternStroke.getBlendMode());
Assert.areEqual(255, patternStroke.getOpacity());
Assert.areEqual(true, patternStroke.isVisible());
PatternFillSettings fillSettings = (PatternFillSettings)patternStroke.getFillSettings();
Assert.areEqual(FillType.Pattern, fillSettings.getFillType());
```
Ini memastikan Anda bekerja dengan lapisan dan efek yang benar.
## Langkah 4: Ubah Efek Stroke
Sekarang, mari kita modifikasi efek guratan dengan data pola baru.
### Perbarui Properti Efek Stroke
```java
patternStroke.setOpacity((byte)127);
patternStroke.setBlendMode(BlendMode.Color);
```
### Perbarui Sumber Daya Pola
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
Cuplikan kode ini memperbarui sumber daya pola dengan data pola baru.
## Langkah 5: Terapkan Pola Baru
Terakhir, terapkan pola baru pada efek guratan dan simpan perubahannya.
```java
((PatternFillSettings)patternStroke.getFillSettings()).setPatternName("$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0");
((PatternFillSettings)patternStroke.getFillSettings()).setPatternId(guid.toString() + "\0");
im.save(exportPath);
```
Ini memastikan pola baru diterapkan dengan benar dan file disimpan dengan perubahan.
## Langkah 6: Verifikasi Perubahannya
Untuk memastikan semuanya berfungsi dengan benar, muat kembali file dan verifikasi perubahannya.
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
Langkah ini memverifikasi bahwa data pola telah diterapkan dengan benar pada efek guratan.
## Kesimpulan
Dan itu dia! Anda telah berhasil menambahkan pola lapisan guratan ke file PSD menggunakan Aspose.PSD untuk Java. Dengan mengikuti langkah-langkah ini, Anda dapat menyesuaikan dan menyempurnakan gambar Anda dengan mudah. Selamat membuat kode!
## FAQ
### Apa itu Aspose.PSD untuk Java?
Aspose.PSD untuk Java adalah perpustakaan yang memungkinkan pengembang membuat, mengedit, dan mengonversi file PSD (Photoshop Document) secara terprogram.
### Bisakah saya menggunakan Aspose.PSD untuk Java dalam proyek komersial?
 Ya, Anda dapat menggunakannya dalam proyek komersial. Anda dapat membeli lisensi dari[Di Sini](https://purchase.aspose.com/buy).
### Apakah ada uji coba gratis yang tersedia untuk Aspose.PSD untuk Java?
 Ya, Anda dapat mengunduh versi uji coba gratis dari[Di Sini](https://releases.aspose.com/).
### Bagaimana saya bisa mendapatkan dukungan untuk Aspose.PSD untuk Java?
 Anda bisa mendapatkan dukungan dari forum komunitas Aspose[Di Sini](https://forum.aspose.com/c/psd/34).
### Apa saja persyaratan sistem untuk Aspose.PSD untuk Java?
Anda perlu menginstal JDK dan IDE untuk pengembangan. Perpustakaan mendukung beberapa sistem operasi termasuk Windows, Linux, dan macOS.