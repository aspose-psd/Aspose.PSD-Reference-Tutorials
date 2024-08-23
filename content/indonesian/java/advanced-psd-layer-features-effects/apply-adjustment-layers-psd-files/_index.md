---
title: Terapkan Lapisan Penyesuaian di File PSD menggunakan Java
linktitle: Terapkan Lapisan Penyesuaian di File PSD menggunakan Java
second_title: Asumsikan.PSD Java API
description: Pelajari cara menerapkan lapisan penyesuaian dalam file PSD menggunakan Aspose.PSD untuk Java dalam panduan langkah demi langkah lengkap untuk pengembang ini.
type: docs
weight: 15
url: /id/java/advanced-psd-layer-features-effects/apply-adjustment-layers-psd-files/
---
## Perkenalan
Apakah Anda seorang pengembang Java yang ingin menyempurnakan gambar yang disimpan dalam file PSD? Jika demikian, Anda berada di tempat yang tepat! Pada artikel ini, kita akan mempelajari cara menerapkan lapisan penyesuaian dalam file PSD menggunakan perpustakaan Aspose.PSD untuk Java. Baik Anda sedang mengerjakan proyek pribadi atau aplikasi profesional, memahami cara memanipulasi file PSD dapat meningkatkan kemampuan perangkat lunak Anda secara signifikan. 

## Prasyarat
Sebelum kita beralih ke kode dan mulai menerapkan lapisan penyesuaian tersebut, ada beberapa prasyarat yang Anda perlukan:
1. Java Development Kit (JDK): Pastikan Anda telah menginstal JDK di mesin Anda. Anda dapat mengunduhnya dari[situs web Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
2.  Perpustakaan Aspose.PSD: Jika Anda belum melakukannya, Anda perlu mengunduh perpustakaan Aspose.PSD untuk Java. Anda dapat menemukannya[Di Sini](https://releases.aspose.com/psd/java/).
3. Lingkungan Pengembangan: Siapkan lingkungan pengembangan terintegrasi (IDE) Java seperti IntelliJ IDEA atau Eclipse tempat Anda akan menulis dan menjalankan kode Anda.
4. Keakraban Dasar dengan Java: Pemahaman umum tentang pemrograman Java akan membantu Anda mengikutinya dengan lancar.
5. File PSD: Miliki beberapa file PSD untuk tujuan pengujian. Anda dapat membuatnya menggunakan Adobe Photoshop atau mengunduh file contoh dari internet.
## Paket Impor
Sebelum kita mulai coding, mari kita perjelas paket mana yang perlu kita impor. Aspose.PSD memungkinkan kita bekerja dengan file Photoshop dalam berbagai cara, jadi mari ambil kelas yang diperlukan untuk menangani gambar PSD dan lapisan penyesuaian.
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.AdjustmentLayer;
```
Sekarang kita sudah memiliki paketnya, mari kita uraikan contohnya langkah demi langkah!
## Langkah 1: Muat File PSD
Langkah pertama dalam perjalanan kita adalah memuat file PSD. Ini adalah file yang akan kita gunakan untuk menerapkan lapisan penyesuaian.
```java
String dataDir = "Your Document Directory";
String sourceFileName1 = dataDir + "ChannelMixerAdjustmentLayer.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName1);
```
 Dalam cuplikan ini, kita menentukan direktori tempat file PSD kita berada dan memuat file tertentu yang ingin kita manipulasi. Pastikan untuk mengganti`"Your Document Directory"` dengan jalur sebenarnya ke file PSD di mesin Anda.
## Langkah 2: Ulangi Lapisan
Sekarang kita telah memuat file PSD, kita ingin mengulangi lapisannya untuk menemukan lapisan penyesuaian.
```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof AdjustmentLayer) {
        AdjustmentLayer adjustmentLayer = (AdjustmentLayer) im.getLayers()[i];
        
        if (adjustmentLayer != null) {
            adjustmentLayer.mergeLayerTo(im.getLayers()[0]);
        }
    }
}
```
 Pada langkah ini, kita mengulang setiap lapisan dalam file PSD untuk mengidentifikasi lapisan apa pun yang termasuk dalam file PSD`AdjustmentLayer` jenis. Jika kita menemukannya, kita gabungkan dengan lapisan dasar, yang biasanya merupakan lapisan pertama (`im.getLayers()[0]`). Proses penggabungan ini secara efektif menerapkan penyesuaian pada gambar kita. 
## Langkah 3: Simpan File PSD yang Dimodifikasi
Setelah memodifikasi layer, penting untuk menyimpan perubahan yang telah kita buat. Mari kita lakukan ini pada langkah berikutnya.
```java
String exportPath1 = dataDir + "ChannelMixerAdjustmentLayerChanged.psd";
im.save(exportPath1);
```
 Di sini, kami menentukan jalur ekspor untuk file PSD kami yang telah diubah dan memanggil`save()` metode untuk menulis perubahan kami ke disk.
## Langkah 4: Lapisan Penyesuaian Level
Mari kita ulangi proses untuk jenis lapisan penyesuaian yang berbeda: lapisan penyesuaian Levels. 
### Muat PSD Lapisan Penyesuaian Level
```java
String sourceFileName2 = dataDir + "LevelsAdjustmentLayerRgb.psd";
PsdImage img = (PsdImage) Image.load(sourceFileName2);
```
Seperti sebelumnya, kita memuat file PSD yang berisi lapisan penyesuaian Levels kita. 
### Iterasi Melalui Lapisan Level
Selanjutnya, kita akan mengulang lapisannya lagi, sama seperti yang kita lakukan sebelumnya, tapi sekarang kita bekerja dengan file PSD lain.
```java
for (int i = 0; i < img.getLayers().length; i++) {
    if (img.getLayers()[i] instanceof AdjustmentLayer) {
        AdjustmentLayer adjustmentLayer = (AdjustmentLayer) img.getLayers()[i];
        
        if (adjustmentLayer != null) {
            adjustmentLayer.mergeLayerTo(img.getLayers()[0]);
        }
    }
}
```
Kode ini bertindak serupa dengan iterasi sebelumnya; itu mencari lapisan penyesuaian dalam file PSD saat ini, memungkinkan kita untuk menerapkan penyesuaian apa pun yang tersedia.
## Simpan PSD Lapisan Penyesuaian Level
Terakhir, kami akan menyimpan file baru ini setelah menerapkan penyesuaian.
```java
String exportPath2 = dataDir + "LevelsAdjustmentLayerRgbChanged.psd";
img.save(exportPath2);
```
Sekarang, kita telah berhasil memproses lapisan penyesuaian Levels!
## Kesimpulan
Selamat! Anda baru saja mempelajari cara menerapkan lapisan penyesuaian dalam file PSD menggunakan Java dan perpustakaan Aspose.PSD. Baik Anda mengubah warna atau menyesuaikan level, kini Anda memiliki keterampilan dasar untuk memanipulasi file PSD secara terprogram.
Menggunakan Aspose.PSD dapat secara signifikan menyederhanakan alur kerja dalam pengeditan gambar, memungkinkan otomatisasi dan penyesuaian dengan cara yang mungkin tidak dilakukan oleh alat tradisional. Jangan ragu untuk menjelajahi perpustakaan lebih jauh dan bereksperimen dengan berbagai jenis lapisan untuk melihat kemungkinan kreatif apa yang ada di luar sana.
## FAQ
### Apa itu perpustakaan Aspose.PSD?
Aspose.PSD adalah perpustakaan yang memungkinkan pengembang memuat, memanipulasi, dan menyimpan file Photoshop PSD dalam aplikasi Java.
### Bisakah saya menggunakan Aspose.PSD secara gratis?
 Ya! Aspose menawarkan uji coba gratis bagi Anda untuk menjelajahi perpustakaan mereka. Anda dapat mendaftar[Di Sini](https://releases.aspose.com/).
### Apakah saya perlu menginstal Photoshop untuk menggunakan Aspose.PSD?
Tidak, Anda tidak memerlukan Photoshop. Aspose.PSD bekerja secara independen untuk memanipulasi file PSD secara terprogram.
### Di mana saya dapat menemukan dokumentasi untuk Aspose.PSD?
Anda dapat mengunjungi halaman dokumentasi[Di Sini](https://reference.aspose.com/psd/java/) untuk menjelajahi fitur, kelas, dan metode.
### Bagaimana cara mendapatkan dukungan untuk produk Aspose?
 Anda dapat mengakses dukungan melalui[Asumsikan forum](https://forum.aspose.com/c/psd/34) di mana Anda dapat mengajukan pertanyaan dan menemukan solusi.