---
title: Bagaimana Menambahkan Gradien Lapisan Stroke di Java
linktitle: Bagaimana Menambahkan Gradien Lapisan Stroke di Java
second_title: Asumsikan.PSD Java API
description: Pelajari cara menambahkan dan menyesuaikan gradien lapisan guratan dalam file PSD menggunakan Aspose.PSD untuk Java dengan tutorial langkah demi langkah yang komprehensif ini.
weight: 10
url: /id/java/java-graphics-drawing/add-stroke-layer-gradient/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Bagaimana Menambahkan Gradien Lapisan Stroke di Java

## Perkenalan
Pernah bertanya-tanya bagaimana cara menambahkan gradien lapisan guratan ke gambar Anda menggunakan Java? Nah, Anda berada di tempat yang tepat! Hari ini, kita menyelami dunia Aspose.PSD untuk Java, perpustakaan canggih yang membantu Anda memanipulasi file PSD dengan mudah. Baik Anda seorang pemula atau pengembang berpengalaman, panduan langkah demi langkah ini akan memandu Anda melalui proses menambahkan gradien lapisan guratan ke file PSD Anda. Jadi, bersiaplah dan bersiaplah untuk meningkatkan keterampilan mengedit grafis Anda!
## Prasyarat
Sebelum kita mulai, ada beberapa hal yang perlu Anda siapkan. Pastikan Anda memiliki yang berikut ini:
1.  Java Development Kit (JDK): Pastikan Anda telah menginstal JDK di sistem Anda. Anda dapat mengunduhnya dari[situs web Oracle](https://www.oracle.com/java/technologies/javase-downloads.html).
2.  Aspose.PSD untuk Perpustakaan Java: Anda dapat mengunduhnya dari[Halaman unduhan Aspose.PSD](https://releases.aspose.com/psd/java/).
3. Lingkungan Pengembangan Terpadu (IDE): IDE apa pun seperti IntelliJ IDEA, Eclipse, atau NetBeans akan berfungsi.
4.  Lisensi yang valid: Anda bisa mendapatkan a[izin sementara](https://purchase.aspose.com/temporary-license/) jika Anda tidak memiliki yang lengkap.
## Paket Impor
Hal pertama yang pertama, mari impor paket yang diperlukan. Ini akan memungkinkan kita untuk menggunakan kelas dan metode yang diperlukan untuk memanipulasi file PSD.
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
Sekarang, mari kita bagi contoh ini menjadi beberapa langkah untuk pemahaman yang lebih baik.
## Langkah 1: Muat File PSD
 Pertama, kita perlu memuat file PSD yang ingin kita modifikasi. Kami akan menggunakan`PsdLoadOptions` untuk menentukan bahwa kita ingin memuat sumber daya efek.
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
String exportPath = dataDir + "StrokeGradientChanged.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```
## Langkah 2: Akses Efek Stroke
Selanjutnya, kita perlu mengakses efek guratan dari layer yang kita minati. Di sini, kita asumsikan itu adalah layer ketiga (indeks 2) dalam file PSD.
```java
StrokeEffect gradientStroke = (StrokeEffect) im.getLayers()[2].getBlendingOptions().getEffects()[0];
```
## Langkah 3: Verifikasi Properti Efek Stroke
Sebelum membuat perubahan apa pun, mari verifikasi properti efek guratan untuk memastikan kita memodifikasi pengaturan yang benar.
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
## Langkah 4: Ubah Pengaturan Isi Gradien
Sekarang, saatnya untuk mengubah pengaturan pengisian gradien sesuai dengan kebutuhan kita. Kami akan mengubah warna, opacity, blend mode, dan properti lainnya.
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
## Langkah 5: Tambahkan dan Ubah Titik Warna dan Transparansi
Mari tambahkan titik warna dan transparansi baru dan modifikasi yang sudah ada untuk mencapai efek gradien yang diinginkan.
```java
// Tambahkan titik warna baru
GradientColorPoint colorPoint = fillSettings.addColorPoint();
colorPoint.setColor(Color.getGreen());
colorPoint.setLocation(4096);
colorPoint.setMedianPointLocation(75);
// Ubah lokasi titik sebelumnya
fillSettings.getColorPoints()[1].setLocation(1899);
// Tambahkan titik transparansi baru
GradientTransparencyPoint transparencyPoint = fillSettings.addTransparencyPoint();
transparencyPoint.setOpacity(25);
transparencyPoint.setMedianPointLocation(25);
transparencyPoint.setLocation(4096);
// Ubah lokasi titik transparansi sebelumnya
fillSettings.getTransparencyPoints()[1].setLocation(2411);
```
## Langkah 6: Simpan File PSD yang Dimodifikasi
Setelah melakukan semua modifikasi yang diperlukan, kita perlu menyimpan file PSD.
```java
im.save(exportPath);
```
## Langkah 7: Verifikasi Modifikasi
Terakhir, mari muat file PSD yang disimpan dan verifikasi bahwa perubahan kita telah diterapkan dengan benar.
```java
PsdImage img = (PsdImage) Image.load(exportPath, loadOptions);
StrokeEffect gradientStrokeEffect = (StrokeEffect) img.getLayers()[2].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Color, gradientStrokeEffect.getBlendMode());
Assert.areEqual(127, gradientStrokeEffect.getOpacity());
Assert.areEqual(true, gradientStrokeEffect.isVisible());
GradientFillSettings fillSetting = (GradientFillSettings) gradientStrokeEffect.getFillSettings();
Assert.areEqual(Color.getGreen(), fillSetting.getColor());
Assert.areEqual(FillType.Gradient, fillSetting.getFillType());
// Periksa titik warna
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
// Periksa poin transparansi
Assert.areEqual(3, fillSettings.getTransparencyPoints().length);
IGradientTransparencyPoint transparencyPoint1 = fillSettings.getTransparencyPoints()[0];
Assert.areEqual(50, transparencyPoint1.getMedianPointLocation());
Assert.areEqual(100, transparencyPoint1.getOpacity());
Assert.areEqual(0, transparencyPoint1.getLocation());
transparencyPoint1 = fillSettings.getTransparencyPoints()[1];
Assert.areEqual(50, transparencyPoint.getMedianPointLocation());
Assert.areEqual(100, transparencyPoint.getOpacity());
Assert.areEqual(2411, transparencyPoint.getLocation());
transparencyPoint1 = fillSettings.getTransparencyPoints()[2];
Assert.areEqual(25, transparencyPoint.getMedianPointLocation());
Assert.areEqual(25, transparencyPoint.getOpacity());
Assert.areEqual(4096, transparencyPoint.getLocation());
```
## Kesimpulan
Dan itu dia! Anda sekarang tahu cara menambahkan dan memanipulasi gradien lapisan guratan dalam file PSD menggunakan Aspose.PSD untuk Java. Tutorial ini mencakup memuat file PSD, mengakses dan memodifikasi efek guratan, dan menyimpan perubahan. Dengan keterampilan ini, Anda dapat membuat gradien yang menarik secara visual dan menyesuaikan file PSD agar sesuai dengan kebutuhan Anda.
## FAQ
### Apa itu Aspose.PSD untuk Java?
Aspose.PSD untuk Java adalah perpustakaan yang memungkinkan pengembang untuk bekerja dengan file PSD dalam aplikasi Java, menyediakan fitur untuk membuat, memanipulasi, dan mengkonversi file PSD.
### Apakah saya memerlukan lisensi untuk menggunakan Aspose.PSD untuk Java?
 Ya, Anda memerlukan lisensi yang valid untuk menggunakan Aspose.PSD untuk Java. Anda bisa mendapatkan[izin sementara](https://purchase.aspose.com/temporary-license/) untuk tujuan evaluasi.
### Bisakah saya menggunakan Aspose.PSD untuk Java untuk membuat file PSD dari awal?
Sangat! Aspose.PSD untuk Java menyediakan API komprehensif untuk membuat dan memanipulasi file PSD secara terprogram.
### Apakah mungkin untuk menerapkan efek lain menggunakan Aspose.PSD untuk Java?
Ya, Anda dapat menerapkan berbagai efek seperti bayangan, cahaya, dan lainnya menggunakan Aspose.PSD untuk Java.
### Di mana saya dapat menemukan dokumentasi Aspose.PSD untuk Java?
 Anda dapat menemukan dokumentasinya[Di Sini](https://reference.aspose.com/psd/java/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
