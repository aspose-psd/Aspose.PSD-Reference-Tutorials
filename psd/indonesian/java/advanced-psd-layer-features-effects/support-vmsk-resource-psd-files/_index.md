---
title: Mendukung Sumber Daya Vmsk dalam File PSD dengan Java
linktitle: Mendukung Sumber Daya Vmsk dalam File PSD dengan Java
second_title: Asumsikan.PSD Java API
description: Kelola sumber daya Vmsk dengan mudah dalam file PSD menggunakan Aspose.PSD untuk Java. Tutorial komprehensif langkah demi langkah yang ideal untuk pengembang dan desainer.
weight: 23
url: /id/java/advanced-psd-layer-features-effects/support-vmsk-resource-psd-files/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Mendukung Sumber Daya Vmsk dalam File PSD dengan Java

## Perkenalan
Ketika bekerja dengan file PSD (Photoshop Document), mengelola sumber daya sangatlah penting, terutama ketika mengintegrasikan fitur-fitur khusus seperti sumber daya Vmsk (Vector Mask). Sumber daya Vmsk dapat memberdayakan desainer dengan menambahkan bentuk vektor yang kompleks, memungkinkan mereka membuat grafik yang menakjubkan dengan mudah. Dalam panduan ini, kami akan melakukan pendekatan langsung untuk menunjukkan kepada Anda cara mendukung sumber daya Vmsk dalam file PSD menggunakan Aspose.PSD untuk Java. Baik Anda seorang pengembang yang ingin menyempurnakan aplikasi Anda atau seorang desainer yang mencari otomatisasi, tutorial ini akan memandu Anda melalui proses langkah demi langkah, sehingga mudah untuk diikuti dan diterapkan.
## Prasyarat
Sebelum kita menyelami detail menarik dalam menangani sumber daya Vmsk, pastikan Anda telah menyiapkan segalanya untuk pengalaman yang lancar.
### Apa yang Anda Butuhkan
-  Java Development Kit (JDK): Pastikan Anda telah menginstal JDK di mesin Anda. Jika belum, Anda dapat mendownloadnya dari[situs web Oracle](https://www.oracle.com/java/technologies/javase-downloads.html).
- Aspose.PSD untuk Java Library: Ini adalah perpustakaan yang kuat untuk mengelola file PSD. Anda dapat mengunduhnya dari[Asumsikan halaman rilis](https://releases.aspose.com/psd/java/) . Bagi yang ingin mencoba sebelum membeli, bisa juga memulainya[uji coba gratis](https://releases.aspose.com/).
- IDE: Semua IDE untuk Java (seperti IntelliJ IDEA, Eclipse, dll.) akan berfungsi untuk proyek ini.
### Menyiapkan Ruang Kerja Anda
1. Buat Proyek Java Baru: Mulai IDE pilihan Anda dan buat proyek Java baru. Ini adalah tempat bermain Anda untuk bekerja dengan kode.
2. Tambahkan Perpustakaan Aspose: Setelah mengunduh perpustakaan Aspose, tambahkan file jar ke perpustakaan proyek Anda. Langkah ini sangat penting karena memungkinkan kita memanfaatkan semua fitur menarik dari Aspose.PSD.
Dengan adanya prasyarat ini, Anda siap untuk mulai membuat, memodifikasi, dan mengelola file PSD dengan sumber daya Vmsk. Mari langsung ke pemrogramannya!
## Paket Impor
Sebelum kita dapat mengerjakan file PSD, kita perlu mengimpor paket yang diperlukan. Ini adalah tulang punggung kode kita, memberi kita akses ke berbagai kelas dan metode yang ditawarkan perpustakaan Aspose.PSD.
```java
import com.aspose.psd.Image;
import com.aspose.psd.Point;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.fileformats.psd.layers.LayerResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.VmskResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.BezierKnotRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.InitialFillRuleRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.LengthRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.PathFillRuleRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathType;
```
Sekarang kita telah menyiapkan panggungnya, saatnya bertindak! Di bagian ini, kami akan memecah kode menjadi langkah-langkah yang dapat dikelola. Langkah-langkah ini akan memandu Anda dalam membaca file PSD, menangani sumber daya Vmsk, dan bahkan mengeditnya.
## Langkah 1: Muat File PSD Anda
Hal pertama yang ingin Anda lakukan adalah memuat file PSD Anda. Di sinilah semua keajaiban dimulai.
```java
String dataDir = "Your Document Directory"; // Perbarui jalur ini
String sourceFileName = dataDir + "Rectangle.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

-  Kami mengatur`dataDir` ke direktori file PSD Anda. 
-  Kami membuat string untuk`sourceFileName`, menggabungkan direktori dengan nama file PSD.
-  Terakhir, kami memuat file PSD ke dalam a`PsdImage` objek menggunakan`Image.load()`.
## Langkah 2: Ambil Sumber Daya Vmsk
Sekarang setelah gambar PSD kita dimuat, mari ambil sumber daya Vmsk.
```java
VmskResource resource = getVmskResource(im);
```

-  Kami memanggil`getVmskResource()` metode yang menangani pencarian dan pengambilan sumber daya Vmsk dari gambar.
## Langkah 3: Validasi Properti Sumber Daya Vmsk
Sebelum melanjutkan dengan modifikasi, penting untuk memvalidasi bahwa sumber daya Vmsk kita berada dalam kondisi yang diharapkan.
```java
if (resource.isDisabled() != false ||
	resource.isInverted() != false ||
	resource.isNotLinked() != false ||
	resource.getPaths().length != 7) {
	throw new RuntimeException("VmskResource was read wrong");
}
```

- Di sini, kami memeriksa berbagai properti sumber daya Vmsk. Kami ingin memastikannya tidak dinonaktifkan, dibalik, atau tidak ditautkan, dan memiliki jumlah jalur yang tepat.
## Langkah 4: Akses Setiap Jalur dan Validasi
Mari kita gali lebih dalam dan periksa jalur dalam sumber daya Vmsk.
```java
PathFillRuleRecord pathFillRule = (PathFillRuleRecord) resource.getPaths()[0];
InitialFillRuleRecord initialFillRule = (InitialFillRuleRecord) resource.getPaths()[1];
LengthRecord subpathLength = (LengthRecord) resource.getPaths()[2];
if (pathFillRule.getType() != VectorPathType.PathFillRuleRecord ||
	initialFillRule.getType() != VectorPathType.InitialFillRuleRecord ||
	initialFillRule.isFillStartsWithAllPixels() != false ||
	subpathLength.getType() != VectorPathType.ClosedSubpathLengthRecord ||
	subpathLength.isClosed() != true) {
	throw new RuntimeException("VmskResource paths were read wrong");
}
```

- Kami mengekstrak tiga catatan jalur tertentu dan memvalidasi jenis dan propertinya untuk memastikannya memenuhi kriteria kami.
## Langkah 5: Edit Sumber Daya Vmsk
Sekarang kita masuk ke bagian modifikasi! Anda dapat mengubah properti sumber daya Vmsk sesuai kebutuhan.
```java
resource.setDisabled(true);
resource.setInverted(true);
resource.setNotLinked(true);
```

- Di blok ini, kami mengubah berbagai properti sumber daya Vmsk. Dengan menyetelnya ke true, kita dapat mengontrol perilaku mask di file PSD.
## Langkah 6: Ubah Titik Simpul Bezier
Simpul Bezier sangat penting untuk jalur vektor. Mari kita ubah beberapa nilai di sini.
```java
BezierKnotRecord bezierKnot = (BezierKnotRecord) resource.getPaths()[3];
bezierKnot.getPoints()[0] = new Point(0, 0);
bezierKnot = (BezierKnotRecord) resource.getPaths()[4];
bezierKnot.getPoints()[0] = new Point(8039797, 10905190);
```

-  Kami mengakses secara spesifik`BezierKnotRecord` jalur dan mengubah titiknya untuk berpotensi membentuk kembali topeng vektor.
## Langkah 7: Simpan File PSD yang Dimodifikasi
Setelah semua pengeditan selesai, saatnya menyimpan file PSD yang dimodifikasi. 
```java
String exportPath = dataDir + "Rectangle_changed.psd";
im.save(exportPath);
```

-  Kami menetapkan jalur untuk file PSD yang diekspor dan kemudian menelepon`im.save()` untuk menulis perubahan pada file baru ini.
## Langkah 8: Bersihkan Sumber Daya
Terakhir, kami perlu memastikan bahwa kami membuang gambar tersebut dengan benar untuk mengosongkan sumber daya.
```java
im.dispose();
```

- Itu selalu merupakan praktik yang baik untuk membuang sumber daya apa pun setelah Anda selesai. Ini membantu menghindari kebocoran memori pada aplikasi Anda.
## Kesimpulan
Selamat! Anda baru saja melangkah melalui proses mendetail dalam mendukung sumber daya Vmsk dalam file PSD menggunakan Aspose.PSD untuk Java. Dari memuat gambar, mengambil dan memvalidasi sumber daya Vmsk, mengedit propertinya, dan kemudian menyimpan PSD Anda yang telah dimodifikasi, Anda telah membahas hal-hal penting. Dengan keterampilan ini, Anda dapat secara efisien mengelola dan memanfaatkan berbagai sumber daya dalam file PSD, menyempurnakan proyek desain grafis atau skrip otomatisasi Anda.
## FAQ
### Apa itu sumber daya Vmsk?
Sumber daya Vmsk adalah topeng vektor dalam file PSD yang memungkinkan bentuk vektor kompleks dan fitur pengeditan.
### Bisakah saya menggunakan Aspose.PSD dalam proyek Maven?
Ya, Anda dapat memasukkan Aspose.PSD sebagai ketergantungan dalam proyek Maven Anda menggunakan koordinatnya dari repositori.
### Dalam format apa saya dapat menyimpan file PSD saya yang telah dimodifikasi?
Anda dapat menyimpannya kembali sebagai file PSD atau mengekspornya ke format lain seperti PNG, JPEG, dll.
### Apakah ada uji coba gratis yang tersedia untuk Aspose.PSD?
 Ya, Anda dapat mengakses uji coba gratis Aspose.PSD untuk menguji fitur-fiturnya. Kunjungi[tautan uji coba gratis](https://releases.aspose.com/).
### Bagaimana saya bisa mendapatkan dukungan untuk Aspose.PSD?
 Anda dapat bergabung dengan[Asumsikan forum](https://forum.aspose.com/c/psd/34)untuk dukungan dan bantuan pemecahan masalah.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
