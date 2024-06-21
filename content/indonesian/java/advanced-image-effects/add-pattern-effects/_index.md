---
title: Tambahkan Efek Pola di Aspose.PSD untuk Java
linktitle: Tambahkan Efek Pola
second_title: Asumsikan.PSD Java API
description: Sempurnakan pola gambar Java Anda dengan mudah dengan Aspose.PSD untuk Java. Ikuti tutorial langkah demi langkah kami untuk menambahkan efek pola yang menawan.
type: docs
weight: 12
url: /id/java/advanced-image-effects/add-pattern-effects/
---
## Perkenalan

Dalam dunia pengembangan Java, menyempurnakan pola gambar adalah tugas umum, dan Aspose.PSD untuk Java memberikan solusi yang kuat untuk ini. Tutorial ini akan memandu Anda melalui proses penambahan efek pola menggunakan Aspose.PSD, memastikan gambar Anda menonjol dengan overlay dan penyempurnaan yang unik.

## Prasyarat

Sebelum masuk ke tutorial, pastikan Anda memiliki prasyarat berikut:

- Java Development Kit (JDK) diinstal pada sistem Anda.
-  Aspose.PSD untuk perpustakaan Java diunduh dan ditambahkan ke proyek Anda. Anda dapat mengunduhnya dari[Situs web Aspose.PSD](https://releases.aspose.com/psd/java/).

## Paket Impor

Di proyek Java Anda, impor paket yang diperlukan untuk bekerja dengan Aspose.PSD. Sertakan kode berikut di awal kelas Java Anda:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;


import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.PatternFillSettings;
import com.aspose.psd.fileformats.psd.layers.layereffects.PatternOverlayEffect;
import com.aspose.psd.fileformats.psd.layers.layerresources.PattResource;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;

import java.util.UUID;
```

## Langkah 1: Muat Gambar

```java
// Muat gambar PSD
String sourceFileName = "YourImagePath/PatternOverlay.psd";
String exportPath = "YourExportPath/PatternOverlayChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

Pastikan untuk mengganti "YourImagePath" dan "YourExportPath" dengan jalur sebenarnya di proyek Anda.

## Langkah 2: Ekstrak Informasi Overlay Pola

```java
// Ekstrak informasi tentang hamparan pola
PatternOverlayEffect patternOverlay = (PatternOverlayEffect)im.getLayers()[1].getBlendingOptions().getEffects()[0];
```

## Langkah 3: Ubah Pengaturan Pola Overlay

```java
// Ubah pengaturan hamparan pola
PatternFillSettings settings = patternOverlay.getSettings();
settings.setColor(Color.getGreen());
patternOverlay.setOpacity((byte)193);
patternOverlay.setBlendMode(BlendMode.Difference);
settings.setHorizontalOffset(15);
settings.setVerticalOffset(11);
```

## Langkah 4: Edit Data Pola

```java
// Edit data pola
PattResource resource;
UUID guid = UUID.randomUUID();
String newPatternName = "$$/Presets/Patterns/Pattern=Some new pattern name\0";

for (int i = 0; i < im.getGlobalLayerResources().length; i++) {
    if (im.getGlobalLayerResources()[i] instanceof PattResource) {
        resource = (PattResource)im.getGlobalLayerResources()[i];
        resource.setPatternId(guid.toString());
        resource.setName(newPatternName);
        resource.setPattern(new int[]{Color.getAqua().toArgb(), Color.getRed().toArgb(),
                        Color.getRed().toArgb(), Color.getAqua().toArgb(),
                        Color.getAqua().toArgb(), Color.getWhite().toArgb(),
                        Color.getWhite().toArgb(), Color.getAqua().toArgb()}, new Rectangle(0, 0, 4, 2));
    }
}
```

## Langkah 5: Simpan Gambar yang Diedit

```java
// Simpan gambar yang telah diedit
settings.setPatternName(newPatternName);
settings.setPatternId(guid.toString() + "\0");
im.save(exportPath);
```

## Langkah 6: Verifikasi Perubahannya

```java
// Verifikasi perubahan pada file yang diedit
PsdImage img = (PsdImage)Image.load(sourceFileName, loadOptions);
PatternOverlayEffect patternOverlayEffect = (PatternOverlayEffect)img.getLayers()[1].getBlendingOptions().getEffects()[0];

// Tambahkan pernyataan untuk memastikan perubahan telah berhasil diterapkan
```

## Kesimpulan

Selamat! Anda telah berhasil mempelajari cara menambahkan efek pola menggunakan Aspose.PSD untuk Java. Pustaka canggih ini memungkinkan Anda membuat gambar yang menarik secara visual dengan pola yang disesuaikan, memberikan kemungkinan tak terbatas untuk proyek berbasis Java Anda.

## FAQ

### Q1: Dapatkah saya menggunakan Aspose.PSD untuk Java dengan pustaka pemrosesan gambar Java lainnya?

A1: Aspose.PSD untuk Java dirancang untuk bekerja secara independen, namun Anda dapat mengintegrasikannya dengan pustaka Java lainnya jika diperlukan.

### Q2: Di mana saya dapat menemukan dokumentasi terperinci untuk Aspose.PSD untuk Java?

 A2: Lihat[Aspose.PSD untuk dokumentasi Java](https://reference.aspose.com/psd/java/) untuk informasi yang komprehensif.

### Q3: Apakah tersedia uji coba gratis untuk Aspose.PSD untuk Java?

 A3: Ya, Anda dapat mengakses uji coba gratis.[Di Sini](https://releases.aspose.com/).

### Q4: Bagaimana saya bisa mendapatkan dukungan untuk Aspose.PSD untuk Java?

 A4: Kunjungi[Forum Aspose.PSD](https://forum.aspose.com/c/psd/34) untuk dukungan komunitas atau pertimbangkan untuk membeli paket dukungan.

### Q5: Bisakah saya mendapatkan lisensi sementara Aspose.PSD untuk Java?

A5: Ya, Anda bisa mendapatkan lisensi sementara.[Di Sini](https://purchase.aspose.com/temporary-license/).