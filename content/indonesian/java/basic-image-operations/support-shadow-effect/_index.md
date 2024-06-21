---
title: Mendukung Efek Bayangan di Aspose.PSD untuk Java
linktitle: Mendukung Efek Bayangan
second_title: Asumsikan.PSD Java API
description: Pelajari cara menambahkan efek bayangan menawan ke gambar menggunakan Aspose.PSD untuk Java. Tingkatkan desain grafis Anda dengan tutorial langkah demi langkah ini.
type: docs
weight: 13
url: /id/java/basic-image-operations/support-shadow-effect/
---
## Perkenalan

Meningkatkan gambar dengan efek bayangan adalah praktik umum dalam desain grafis, menambah kedalaman dan realisme. Aspose.PSD untuk Java memberikan dukungan kuat untuk efek bayangan, memungkinkan pengembang dengan mudah mengintegrasikan efek ini ke dalam aplikasi Java mereka. Dalam tutorial ini, kita akan mengeksplorasi cara mendukung efek bayangan menggunakan Aspose.PSD, langkah demi langkah.

## Prasyarat

Sebelum masuk ke tutorial, pastikan Anda memiliki prasyarat berikut:

- Pengetahuan dasar tentang pemrograman Java.
-  Aspose.PSD untuk Java diinstal. Anda dapat mengunduhnya[Di Sini](https://releases.aspose.com/psd/java/).

## Paket Impor

Pastikan Anda telah mengimpor paket yang diperlukan untuk memanfaatkan fungsionalitas Aspose.PSD di aplikasi Java Anda. Gunakan cuplikan kode berikut sebagai panduan:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;


import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.layereffects.DropShadowEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
```

## Langkah 1: Muat Gambar PSD

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Shadow.psd";
String psdPathAfterChange = dataDir + "ShadowChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

## Langkah 2: Ambil Efek Bayangan

```java
DropShadowEffect shadowEffect = (DropShadowEffect)(im.getLayers()[1].getBlendingOptions().getEffects()[0]);
```

## Langkah 3: Verifikasi Pengaturan Default

```java
Assert.areEqual(Color.getBlack(), shadowEffect.getColor());
Assert.areEqual(255, shadowEffect.getOpacity());
Assert.areEqual(3, shadowEffect.getDistance());
Assert.areEqual(7, shadowEffect.getSize());
Assert.areEqual(true, shadowEffect.getUseGlobalLight());
Assert.areEqual(90, shadowEffect.getAngle());
Assert.areEqual(0, shadowEffect.getSpread());
Assert.areEqual(0, shadowEffect.getNoise());
```

## Langkah 4: Sesuaikan Efek Bayangan

```java
shadowEffect.setColor(Color.getGreen());
shadowEffect.setOpacity((byte)128);
shadowEffect.setDistance(11);
shadowEffect.setUseGlobalLight(false);
shadowEffect.setSize(9);
shadowEffect.setAngle(45);
shadowEffect.setSpread(3);
shadowEffect.setNoise(50);
```

## Langkah 5: Simpan Gambar yang Dimodifikasi

```java
im.save(psdPathAfterChange);
```

## Kesimpulan

Dengan langkah sederhana ini, Anda dapat dengan mudah mendukung efek bayangan di Aspose.PSD untuk Java, sehingga meningkatkan daya tarik visual gambar Anda.

## FAQ

### Q1: Apakah Aspose.PSD untuk Java cocok untuk proyek desain grafis profesional?

A1: Tentu saja! Aspose.PSD untuk Java adalah perpustakaan canggih yang dirancang untuk tugas desain grafis profesional.

### Q2: Dapatkah saya menggunakan Aspose.PSD untuk Java dalam aplikasi komersial?

 A2: Ya, Aspose.PSD untuk Java adalah produk komersial. Anda dapat membelinya[Di Sini](https://purchase.aspose.com/buy).

### Q3: Apakah tersedia uji coba gratis?

 A3: Ya, Anda dapat menjelajahi versi uji coba gratis.[Di Sini](https://releases.aspose.com/).

### Q4: Di mana saya dapat menemukan dokumentasi terperinci?

 A4: Lihat dokumentasi komprehensif[Di Sini](https://reference.aspose.com/psd/java/).

### Q5: Bagaimana saya bisa mendapatkan dukungan untuk Aspose.PSD untuk Java?

 A5: Bergabunglah dengan forum komunitas.[Di Sini](https://forum.aspose.com/c/psd/34) untuk pertanyaan dukungan apa pun.