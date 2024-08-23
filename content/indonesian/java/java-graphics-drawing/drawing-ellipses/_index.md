---
title: Menggambar Elips di Java
linktitle: Menggambar Elips di Java
second_title: Asumsikan.PSD Java API
description: Pelajari cara menggambar elips di Java menggunakan Aspose.PSD untuk desain grafis dan manipulasi gambar yang tepat. Kuasai tutorial langkah demi langkah.
type: docs
weight: 15
url: /id/java/java-graphics-drawing/drawing-ellipses/
---
## Perkenalan
Dalam tutorial ini, Anda akan belajar cara menggambar elips menggunakan Aspose.PSD untuk Java. Aspose.PSD adalah perpustakaan canggih yang memungkinkan pengembang Java bekerja dengan file PSD dan memanipulasi gambar dengan mudah. Menggambar bentuk seperti elips adalah tugas mendasar dalam pemrosesan gambar dan desain grafis. Dengan mengikuti panduan ini, Anda akan mendapatkan pengalaman langsung dalam membuat elips secara terprogram menggunakan Aspose.PSD.
## Prasyarat
Sebelum memulai, pastikan Anda memiliki hal berikut:
- Pengetahuan dasar tentang pemrograman Java.
- JDK (Java Development Kit) diinstal pada sistem Anda.
- Lingkungan Pengembangan Terintegrasi (IDE) seperti IntelliJ IDEA atau Eclipse.
-  Aspose.PSD untuk perpustakaan Java. Anda dapat mengunduhnya dari[Di Sini](https://releases.aspose.com/psd/java/).
## Paket Impor
Pertama, Anda perlu mengimpor paket yang diperlukan dari Aspose.PSD:
```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.Pen;
import com.aspose.psd.Rectangle;
import com.aspose.psd.brushes.SolidBrush;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.BmpOptions;
```
## Langkah 1: Siapkan proyek Java Anda
Sebelum Anda memulai coding, pastikan proyek Java Anda sudah diatur dengan benar dengan Aspose.PSD disertakan sebagai dependensi.
## Langkah 2: Buat instance PsdImage
Inisialisasi instance baru PsdImage dengan lebar dan tinggi yang diinginkan.
```java
Image image = new PsdImage(100, 100);
```
## Langkah 3: Inisialisasi objek Grafik
Membuat dan menginisialisasi instance Grafik untuk bekerja dengan gambar.
```java
Graphics graphics = new Graphics(image);
```
## Langkah 4: Hapus permukaan Grafik
Sebelum menggambar, bersihkan permukaan grafis dengan warna tertentu (opsional).
```java
graphics.clear(Color.getYellow());
```
## Langkah 5: Gambarlah elips bertitik
Gunakan objek Pena dengan warna merah dan gambar elips bertitik di dalam Persegi Panjang yang ditentukan.
```java
graphics.drawEllipse(new Pen(Color.getRed()), new Rectangle(30, 10, 40, 80));
```
## Langkah 6: Gambarlah elips yang berkesinambungan
Buat objek Pena dengan kuas biru solid dan gambar elips kontinu di dalam Persegi Panjang lainnya.
```java
graphics.drawEllipse(new Pen(new SolidBrush(Color.getBlue())), new Rectangle(10, 30, 80, 40));
```
## Langkah 7: Simpan gambar
Terakhir, simpan gambar yang dihasilkan dalam format BMP ke jalur tertentu.
```java
String outputPath = "Your Document Directory/Ellipse.bmp";
BmpOptions saveOptions = new BmpOptions();
saveOptions.setBitsPerPixel(32);
image.save(outputPath, saveOptions);
```

## Kesimpulan
Selamat! Anda telah berhasil mempelajari cara menggambar elips secara terprogram menggunakan Aspose.PSD untuk Java. Tutorial ini mencakup pengaturan proyek Anda, menginisialisasi grafik, menggambar elips bertitik dan kontinu, dan menyimpan gambar yang dihasilkan. Sekarang Anda dapat mengintegrasikan teknik ini ke dalam aplikasi Java Anda untuk berbagai tugas desain grafis dan manipulasi gambar.
## FAQ
### Bisakah saya menggunakan Aspose.PSD secara gratis?
Aspose.PSD menawarkan versi uji coba gratis, memungkinkan Anda mengevaluasi fitur-fiturnya sebelum membeli.
### Di mana saya dapat menemukan lebih banyak contoh dan dokumentasi?
 Mengunjungi[Dokumentasi Aspose.PSD](https://reference.aspose.com/psd/java/) untuk panduan dan contoh yang komprehensif.
### Bagaimana saya bisa mendapatkan lisensi sementara untuk Aspose.PSD?
 Lisensi sementara dapat diperoleh dari[Lisensi Sementara Aspose.PSD](https://purchase.aspose.com/temporary-license/).
### Dalam format apa Aspose.PSD dapat menyimpan gambar?
Aspose.PSD mendukung penyimpanan gambar ke berbagai format termasuk BMP, PNG, JPEG, dan PSD.
### Apakah Aspose.PSD cocok untuk penggunaan perusahaan?
Ya, Aspose.PSD dirancang untuk tugas pemrosesan gambar tingkat profesional dan perusahaan.