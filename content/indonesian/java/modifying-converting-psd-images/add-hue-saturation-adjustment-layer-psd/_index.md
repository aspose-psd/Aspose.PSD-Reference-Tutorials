---
title: Tambahkan Lapisan Penyesuaian Saturasi Hue ke PSD
linktitle: Tambahkan Lapisan Penyesuaian Saturasi Hue ke PSD
second_title: Asumsikan.PSD Java API
description: Pelajari cara menambahkan lapisan penyesuaian saturasi rona ke PSD menggunakan Aspose.PSD untuk Java dalam tutorial langkah demi langkah yang komprehensif ini. Tingkatkan alur kerja desain grafis Anda.
type: docs
weight: 14
url: /id/java/modifying-converting-psd-images/add-hue-saturation-adjustment-layer-psd/
---
## Perkenalan
Dalam hal desain grafis, manipulasi warna memainkan peran penting—khususnya, mengubah corak, saturasi, dan kecerahan dapat mengubah suasana dan kualitas gambar secara drastis. Salah satu cara efektif untuk mencapai hal ini adalah melalui penggunaan lapisan penyesuaian di Photoshop (file PSD). Jika Anda ingin menyempurnakan file PSD Anda secara terprogram menggunakan Java, perpustakaan Aspose.PSD siap membantu! Tutorial ini akan membawa Anda melalui langkah-langkah untuk menambahkan Lapisan Penyesuaian Saturasi Hue ke file PSD Anda, menjadikan alur kerja Anda lebih produktif dan efisien.
Dalam panduan ini, kami akan membahas semuanya mulai dari mengimpor paket yang diperlukan hingga detail seluk beluk contoh kode.
## Prasyarat
Sebelum kita beralih ke kode, pastikan Anda memiliki yang berikut ini:
1.  Java Development Kit (JDK): Pastikan Anda telah menginstal JDK 8 atau lebih tinggi di mesin Anda. Anda dapat mengunduhnya dari[Unduhan Kit Pengembangan Java SE](https://www.oracle.com/java/technologies/javase-downloads.html).
2.  Aspose.PSD untuk Perpustakaan Java: Anda harus memiliki perpustakaan Aspose.PSD, yang Anda bisa[unduh di sini](https://releases.aspose.com/psd/java/). 
3. IDE: Lingkungan Pengembangan Terpadu (IDE) yang cocok seperti IntelliJ IDEA atau Eclipse untuk pengembangan Java.
4. Pengetahuan Dasar Java: Keakraban dengan pemrograman Java merupakan nilai tambah, tapi jangan khawatir; kami akan memandu Anda melalui kode langkah demi langkah.
Sekarang setelah prasyarat kita beres, mari beralih ke bagian yang menyenangkan—coding!
## Paket Impor
Untuk mulai bekerja dengan perpustakaan Aspose.PSD, langkah pertama adalah mengimpor kelas yang diperlukan. Inilah cara Anda melakukannya di file Java Anda:
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.HueSaturationLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.ColorRangeHsl;
```
Pastikan Anda memiliki perpustakaan yang sesuai yang ditambahkan ke proyek Anda sehingga impor ini berfungsi dengan lancar.
## Langkah 1: Siapkan Direktori Dokumen Anda
Setiap proyek membutuhkan titik awal, tidak terkecuali proyek kami. Anda perlu menentukan direktori tempat file PSD Anda disimpan. Ini penting untuk memuat dan menyimpan gambar dengan benar.
```java
String dataDir = "Your Document Directory"; // Perbarui jalur ini ke direktori Anda yang sebenarnya
```
## Langkah 2: Muat File PSD yang Ada
Untuk memanipulasi file PSD yang ada, pertama-tama kita perlu memuatnya ke dalam program kita. Inilah cara Anda melakukannya:
```java
String sourceFileName = dataDir + "HueSaturationAdjustmentLayer.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```
 Dalam kode ini, perbarui`"HueSaturationAdjustmentLayer.psd"` ke nama file PSD yang ada yang ingin Anda edit.
## Langkah 3: Edit Lapisan Hue/Saturation
Selanjutnya, kita akan menelusuri lapisan gambar PSD yang dimuat untuk menemukan dan mengedit lapisan Hue/Saturation yang ada. Langkah ini melibatkan modifikasi nilai rona, saturasi, dan kecerahan.
```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof HueSaturationLayer) {
        HueSaturationLayer hueLayer = (HueSaturationLayer) im.getLayers()[i];
        hueLayer.setHue((short) -25);
        hueLayer.setSaturation((short) -12);
        hueLayer.setLightness((short) 67);
        ColorRangeHsl colorRange = hueLayer.getRange(2);
        colorRange.setHue((short) -40);
        colorRange.setSaturation((short) 50);
        colorRange.setLightness((short) -20);
        colorRange.setMostLeftBorder((short) 300);
    }
}
```
Dalam contoh ini:
- Kami menyesuaikan rona ke -25, saturasi ke -12, dan kecerahan ke +67.
-  Itu`getRange(2)` Metode ini memungkinkan kita mengubah rentang warna tertentu sesuai keinginan.
## Langkah 4: Simpan File PSD yang Dimodifikasi
Setelah melakukan penyesuaian, langkah selanjutnya adalah menyimpan file. Ini adalah bagian penting dari proses kami, memastikan bahwa perubahan yang telah kami lakukan tidak hilang.
```java
String psdPathAfterChange = dataDir + "HueSaturationAdjustmentLayerChanged.psd";
im.save(psdPathAfterChange);
```
## Langkah 5: Tambahkan Layer Hue/Saturation Baru
Selanjutnya, Anda mungkin ingin menambahkan lapisan penyesuaian Hue/Saturation baru ke file PSD lainnya. Ikuti saja pendekatan yang sama yang Anda gunakan sebelumnya tetapi dengan file PSD berbeda.
```java
sourceFileName = dataDir + "PhotoExample.psd";
PsdImage img = (PsdImage) Image.load(sourceFileName);
HueSaturationLayer hueLayerNew = img.addHueSaturationAdjustmentLayer();
```
## Langkah 6: Tetapkan Nilai Hue/Saturation Baru untuk Layer Baru
Sekarang setelah Anda membuat layer baru ini, terapkan pengaturan rona, saturasi, dan kecerahan yang diinginkan seperti sebelumnya.
```java
hueLayerNew.setHue((short) -25);
hueLayerNew.setSaturation((short) -12);
hueLayerNew.setLightness((short) 67);
ColorRangeHsl newColorRange = hueLayerNew.getRange(2);
newColorRange.setHue((short) -160);
newColorRange.setSaturation((short) 100);
newColorRange.setLightness((short) 20);
newColorRange.setMostLeftBorder((short) 300);
```
## Langkah 7: Simpan File PSD yang Diperbarui
Terakhir, simpan file PSD dengan menambahkan lapisan Hue/Saturation sehingga Anda dapat melihat perubahannya.
```java
String psdPathAfterNewLayerChange = dataDir + "PhotoExampleAddedHueSaturation.psd";
img.save(psdPathAfterNewLayerChange);
```
Selamat! Anda telah berhasil memanipulasi file PSD menggunakan Aspose.PSD untuk Java. Sekarang, Anda dapat bereksperimen dengan berbagai gambar dan perubahan yang lebih dalam, sehingga proyek desain grafis Anda menjadi nyata.
## Kesimpulan
Bekerja dengan grafik secara terprogram membuka banyak kemungkinan. Menggunakan Aspose.PSD untuk Java untuk menambah dan memodifikasi Lapisan Penyesuaian Saturasi Hue memberikan fleksibilitas dan efisiensi yang dapat menyederhanakan alur kerja desain Anda. Baik Anda menyempurnakan foto untuk suatu proyek atau membuat konten visual yang menakjubkan, menguasai alat-alat ini dapat meningkatkan hasil Anda secara signifikan.
 Jangan ragu untuk menjelajahi lebih banyak fungsi Aspose.PSD dengan mendalaminya[dokumentasi](https://reference.aspose.com/psd/java/) atau pertimbangkan untuk mengambil a[izin sementara](https://purchase.aspose.com/temporary-license/) untuk menguji kekuatan penuh perpustakaan.
## FAQ
### Apa itu Lapisan Penyesuaian Saturasi Hue?
Lapisan Penyesuaian Saturasi Hue memungkinkan Anda mengubah properti warna gambar tanpa mengubah piksel aslinya secara permanen.
### Apakah saya perlu menginstal Photoshop untuk menggunakan Aspose.PSD?
Tidak, Aspose.PSD adalah perpustakaan mandiri yang bekerja secara independen dari Photoshop.
### Bisakah saya menggunakan Aspose.PSD untuk pemrosesan batch?
Ya, Anda dapat mengotomatiskan dan memproses banyak file PSD secara batch dengan Aspose.PSD.
### Apakah Aspose.PSD gratis?
Aspose.PSD menawarkan uji coba gratis, tetapi lisensi diperlukan untuk penggunaan jangka panjang. Anda dapat melihat harga[Di Sini](https://purchase.aspose.com/buy).