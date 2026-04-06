---
date: 2026-01-14
description: Pelajari cara membuat lapisan goresan gradien dan menyesuaikan gradien
  goresan dalam file PSD menggunakan Aspose.PSD untuk Java dengan tutorial langkah
  demi langkah ini.
linktitle: How to Create Gradient Stroke Layer in Java
second_title: Aspose.PSD Java API
title: Cara Membuat Lapisan Garis Gradien di Java
url: /id/java/java-graphics-drawing/add-stroke-layer-gradient/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cara Membuat Lapisan Stroke Gradien di Java

## Pendahuluan
Pernah bertanya-tanya bagaimana cara **membuat lapisan stroke gradien** dalam file PSD Anda menggunakan Java? Anda berada di tempat yang tepat! Hari ini kami akan menyelami Aspose.PSD untuk Java—sebuah perpustakaan kuat yang memungkinkan Anda memanipulasi file PSD dengan mudah. Baik Anda baru dalam pemrograman grafis atau ingin menyempurnakan desain yang ada, panduan ini akan memandu Anda menambahkan dan menyesuaikan gradien stroke langkah demi langkah.

## Jawaban Cepat
- **Apa tujuan utama?** Membuat lapisan stroke gradien pada file PSD.  
- **Perpustakaan apa yang diperlukan?** Aspose.PSD untuk Java.  
- **Apakah saya memerlukan lisensi?** Ya, lisensi yang valid (atau sementara) diperlukan untuk produksi.  
- **Versi Java apa yang didukung?** Java 8 atau lebih tinggi.  
- **Berapa lama implementasinya?** Sekitar 10‑15 menit untuk stroke gradien dasar.

## Apa Itu Lapisan Stroke Gradien?
Lapisan stroke gradien adalah kontur vektor di sekitar bentuk atau teks yang berubah secara halus antara warna. Menggunakan Aspose.PSD Anda dapat secara programatik menentukan warna, opasitas, sudut, dan tipe (linear, radial, dll.) dari stroke.

## Mengapa Menggunakan Aspose.PSD untuk Java?
- **Dukungan PSD lengkap** – membaca, mengedit, dan menulis file PSD tanpa Photoshop.  
- **API efek yang kaya** – mengakses stroke, bayangan, cahaya, dan banyak efek lapisan lainnya.  
- **Lintas platform** – bekerja pada sistem operasi apa pun yang mendukung Java.  
- **Tanpa ketergantungan native** – Java murni, mudah diintegrasikan ke pipeline CI.

## Prasyarat
1. **Java Development Kit (JDK)** – Instal JDK terbaru dari [situs web Oracle](https://www.oracle.com/java/technologies/javase-downloads.html).  
2. **Aspose.PSD untuk Java** – Unduh perpustakaan dari [halaman unduhan Aspose.PSD](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse, atau NetBeans.  
4. **Lisensi** – Dapatkan [lisensi sementara](https://purchase.aspose.com/temporary-license/) jika Anda belum memiliki lisensi penuh.

## Impor Paket
Pertama, impor kelas yang akan kita gunakan untuk memuat PSD, mengakses efek, dan mengonfigurasi isian gradien.

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

Sekarang mari kita bagi proses menjadi langkah‑langkah yang jelas.

## Langkah 1: Muat File PSD
Kami memuat PSD sumber dan mengaktifkan sumber daya efek sehingga efek stroke tersedia.

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
String exportPath = dataDir + "StrokeGradientChanged.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```

## Langkah 2: Akses Efek Stroke
Dengan asumsi stroke yang ingin kami ubah berada pada lapisan ketiga (indeks 2), kami mengambil `StrokeEffect`‑nya.

```java
StrokeEffect gradientStroke = (StrokeEffect) im.getLayers()[2].getBlendingOptions().getEffects()[0];
```

## Langkah 3: Verifikasi Properti Efek Stroke
Sebelum melakukan perubahan, kami mengonfirmasi pengaturan yang ada agar tahu persis apa yang akan diperbarui.

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

## Langkah 4: Modifikasi Pengaturan Isian Gradien
Di sini kami mengubah warna, opasitas, mode campuran, dan properti lainnya untuk mencapai tampilan yang diinginkan.

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

## Langkah 5: Tambah dan Modifikasi Titik Warna serta Transparansi
Kami menambahkan titik warna dan transparansi baru, lalu menyesuaikan yang sudah ada untuk membentuk gradien.

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

## Langkah 6: Simpan File PSD yang Telah Dimodifikasi
Setelah semua penyesuaian, kami menulis file yang diperbarui kembali ke disk.

```java
im.save(exportPath);
```

## Langkah 7: Verifikasi Modifikasi
Muat file yang disimpan dan pastikan setiap properti mencerminkan perubahan yang kami terapkan.

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
Assert.areEqual(50, transparencyPoint.getMedianPointLocation());
Assert.areEqual(100, transparencyPoint.getOpacity());
Assert.areEqual(2411, transparencyPoint.getLocation());
transparencyPoint1 = fillSettings.getTransparencyPoints()[2];
Assert.areEqual(25, transparencyPoint.getMedianPointLocation());
Assert.areEqual(25, transparencyPoint.getOpacity());
Assert.areEqual(4096, transparencyPoint.getLocation());
```

## Kesimpulan
Anda kini tahu cara **membuat lapisan stroke gradien** dalam file PSD menggunakan Aspose.PSD untuk Java. Dengan memuat PSD, mengakses efek stroke, menyesuaikan pengaturan isian gradien, dan menyimpan hasilnya, Anda dapat secara programatik menghasilkan grafis kelas profesional tanpa pernah membuka Photoshop.

## FAQ
### Apa itu Aspose.PSD untuk Java?
Aspose.PSD untuk Java adalah perpustakaan yang memungkinkan pengembang bekerja dengan file PSD dalam aplikasi Java, menyediakan fitur untuk membuat, memanipulasi, dan mengonversi file PSD.

### Apakah saya memerlukan lisensi untuk menggunakan Aspose.PSD untuk Java?
Ya, Anda memerlukan lisensi yang valid untuk menggunakan Aspose.PSD untuk Java. Anda dapat mendapatkan [lisensi sementara](https://purchase.aspose.com/temporary-license/) untuk tujuan evaluasi.

### Bisakah saya menggunakan Aspose.PSD untuk Java untuk membuat file PSD dari awal?
Tentu saja! Aspose.PSD untuk Java menyediakan API lengkap untuk membuat dan memanipulasi file PSD secara programatik.

### Apakah memungkinkan menerapkan efek lain menggunakan Aspose.PSD untuk Java?
Ya, Anda dapat menerapkan berbagai efek seperti bayangan, cahaya, dan lainnya menggunakan Aspose.PSD untuk Java.

### Di mana saya dapat menemukan dokumentasi untuk Aspose.PSD untuk Java?
Anda dapat menemukan dokumentasi [di sini](https://reference.aspose.com/psd/java/).

---

**Terakhir Diperbarui:** 2026-01-14  
**Diuji Dengan:** Aspose.PSD untuk Java 24.11  
**Penulis:** Aspose

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
