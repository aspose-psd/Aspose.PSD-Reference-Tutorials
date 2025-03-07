---
title: Lapisan Penyesuaian Tingkat Render dalam File PSD - Java
linktitle: Lapisan Penyesuaian Tingkat Render dalam File PSD - Java
second_title: Asumsikan.PSD Java API
description: Pelajari cara meningkatkan kontras dan kecerahan gambar dengan mudah menggunakan Aspose.PSD untuk Java. Lapisan Penyesuaian Tingkat Master dengan panduan langkah demi langkah ini.
weight: 17
url: /id/java/psd-layer-management-effects/render-level-adjustment-layer-psd/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Lapisan Penyesuaian Tingkat Render dalam File PSD - Java

## Perkenalan

Pernahkah Anda membuka file PSD hanya untuk menemukan gambarnya kurang kontras atau cerah? Jangan takut, pejuang pengeditan gambar! Aspose.PSD untuk Java hadir untuk menyelamatkan dengan kemampuan manipulasi Lapisan Penyesuaian Level yang kuat. Panduan ini akan membekali Anda dengan pengetahuan untuk menyempurnakan gambar Anda menggunakan Level dengan mudah. 

## Prasyarat

- Java Development Kit (JDK): Pastikan Anda menginstal JDK versi terbaru di sistem Anda. Anda dapat mengunduhnya dari situs web Oracle ([https://www.oracle.com/java/technologies/javase-downloads.html](https://www.oracle.com/java/technologies/javase-downloads.html)).
- Aspose.PSD untuk Perpustakaan Java: Unduh perpustakaan Aspose.PSD untuk Java dari halaman unduh ([https://releases.aspose.com/psd/java/](https://releases.aspose.com/psd/java/)). Anda memerlukan lisensi yang valid untuk menggunakan fitur lengkap, namun uji coba gratis tersedia untuk Anda mulai ([https://releases.aspose.com/](https://releases.aspose.com/)).

## Paket Impor

Sebelum mendalami kodenya, kita perlu mengimpor kelas Aspose.PSD yang diperlukan untuk berinteraksi dengan file PSD. Inilah yang Anda perlukan:

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.LevelsLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.LevelChannel;
import com.aspose.psd.imageoptions.PngOptions;
```

 Itu`com.aspose.psd` paket menyediakan akses ke fungsi manipulasi PSD, sementara`com.aspose.psd.imaging.PngOptions` memungkinkan kita menentukan opsi saat menyimpan gambar sebagai PNG.

Sekarang, mari kita memulai petualangan penyesuaian Level:

## Langkah 1: Menyiapkan Jalur File:

- Tentukan variabel untuk direktori dokumen Anda (`dataDir`), nama file PSD sumber (`sourceFileName`), target nama file PSD setelah modifikasi (`psdPathAfterChange`), dan jalur ekspor PNG terakhir (`pngExportPath`). Pertimbangkan untuk menggunakan nama deskriptif untuk meningkatkan keterbacaan kode.

```java
String dataDir = "Your Document Directory";

String sourceFileName = dataDir + "LevelsAdjustmentLayer.psd";
String psdPathAfterChange = dataDir + "LevelsAdjustmentLayerChanged.psd";
String pngExportPath = dataDir + "LevelsAdjustmentLayerChanged.png";
```

## Langkah 2: Memuat Gambar PSD:

-  Gunakan`Image.load` metode untuk membuka file PSD sumber dan menyimpannya di a`PsdImage`objek (`im`). Aspose.PSD secara otomatis mendeteksi format file.

```java
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

## Langkah 3: Iterasi Melalui Lapisan:

- Kita perlu menemukan Layer Penyesuaian Level dalam PSD Anda. Aspose menyediakan cara mudah untuk melakukan iterasi melalui semua lapisan menggunakan loop.

```java
for (int i = 0; i < im.getLayers().length; i++) {
   // ... (kode untuk memeriksa Lapisan Level akan ditambahkan di sini)
}
```

## Langkah 4: Mengidentifikasi Lapisan Level:

- Di dalam loop, periksa apakah lapisan saat ini (`im.getLayers()[i]` ) adalah contoh dari`LevelsLayer` kelas menggunakan`instanceof` operator. 
-  Jika ya, pindahkan layer ke a`LevelsLayer` objek untuk manipulasi lebih lanjut.

```java
for (int i = 0; i < im.getLayers().length; i++) {
   if (im.getLayers()[i] instanceof LevelsLayer) {
	   LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
	   // ... (kode untuk menyesuaikan level akan ditambahkan di sini)
   }
}
```
## Langkah 5: Penyempurnaan Level (Lanjutan):

-  Sesuaikan level output menggunakan`setOutputShadowLevel` Dan`setOutputHighlightLevel` untuk mengontrol gelap dan terang gambar yang dihasilkan. Nilai-nilai ini menentukan rentang level input yang akan dipetakan ke rentang output.

```java
for (int i = 0; i < im.getLayers().length; i++) {
   if (im.getLayers()[i] instanceof LevelsLayer) {
	   LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
	   LevelChannel channel = levelsLayer.getChannel(0);

	   // Sesuaikan Level Input (0-255):
	   channel.setInputShadowLevel((short) 10); // Gelapkan bayangan sedikit
	   channel.setInputMidtoneLevel(2.0f);     // Tingkatkan nada tengah
	   channel.setInputHighlightLevel((short) 230); // Kurangi sorotan

	   // Sesuaikan Tingkat Output (0-255):
	   channel.setOutputShadowLevel((short) 20); // Gelapkan bayangan lebih jauh
	   channel.setOutputHighlightLevel((short) 200); //Mencerahkan sorotan
   }
}
```

## Langkah 6: Menyimpan PSD yang Dimodifikasi:

-  Gunakan`save` metode`PsdImage` objek untuk menyimpan gambar yang dimodifikasi ke jalur yang ditentukan (`psdPathAfterChange`).

```java
im.save(psdPathAfterChange);
```

## Langkah 7: Mengekspor sebagai PNG (Opsional):

-  Jika Anda memerlukan versi PNG dari gambar yang disesuaikan, buatlah`PngOptions` objek dan atur jenis warnanya`TruecolorWithAlpha` . Kemudian, gunakan`save` metode lagi dengan jalur dan opsi ekspor PNG.

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
im.save(pngExportPath, saveOptions);
```

Dan itu dia! Anda telah berhasil menyesuaikan Lapisan Penyesuaian Level di file PSD Anda menggunakan Aspose.PSD untuk Java. Dengan memahami langkah-langkah ini dan bereksperimen dengan nilai yang berbeda, Anda dapat meningkatkan kontras dan tampilan gambar secara keseluruhan.

## Kesimpulan

Aspose.PSD untuk Java memberdayakan Anda untuk mengendalikan proses pengeditan gambar Anda. Dengan menguasai Lapisan Penyesuaian Level, Anda dapat memberikan kehidupan baru ke dalam foto dan desain Anda. Ingat, latihan membuat sempurna, jadi jangan ragu untuk bereksperimen dan mengeksplorasi potensi penuh dari alat canggih ini.
 
## FAQ

### Dapatkah saya menyesuaikan saluran warna individual (RGB) secara terpisah? 
Ya, Anda dapat mengakses setiap saluran warna menggunakan`getChannel` metode`LevelsLayer` objek dan memodifikasi levelnya secara mandiri.

### Bagaimana cara menangani beberapa Lapisan Penyesuaian Level di PSD?
Kode tersebut mengulangi semua lapisan, sehingga secara otomatis akan memproses lapisan Level tambahan apa pun yang ditemukan pada gambar.

### Apakah ada cara lain untuk mengatur kontras gambar selain Level?
Sangat! Aspose.PSD menawarkan berbagai alat penyesuaian gambar seperti Kurva, Kecerahan/Kontras, dan banyak lagi.

### Bisakah saya mengotomatiskan proses ini untuk banyak gambar? 
Ya, Anda dapat memasukkan kode ini ke dalam skrip pemrosesan loop atau batch untuk memproses beberapa file PSD secara efisien.

### Di mana saya dapat menemukan informasi dan dukungan lebih lanjut?
Aspose menyediakan dokumentasi ekstensif ([https://reference.aspose.com/psd/java/](https://reference.aspose.com/psd/java/)) dan forum dukungan ([https://forum.aspose.com/c/psd/34](https://forum.aspose.com/c/psd/34)) untuk pertanyaan atau masalah apa pun yang mungkin Anda temui.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
