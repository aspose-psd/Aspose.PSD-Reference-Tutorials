---
title: Konversi PSB ke JPG di Java
linktitle: Konversi PSB ke JPG di Java
second_title: Asumsikan.PSD Java API
description: Konversi PSB ke JPG dengan mudah di Java dengan Aspose.PSD. Ikuti panduan terperinci kami untuk konversi gambar yang lancar. Unduh, coba, dan beli Aspose.PSD.
type: docs
weight: 10
url: /id/java/java-psb-to-image-format-conversion/convert-psb-to-jpg-java/
---
## Perkenalan
Selamat datang di panduan komprehensif kami tentang mengonversi file PSB ke format JPG menggunakan Aspose.PSD untuk Java! Jika Anda berurusan dengan file PSB—file Photoshop yang besar dan berlapis—dan perlu mengonversinya ke format JPG yang lebih didukung secara universal, Anda berada di tempat yang tepat. Dalam tutorial ini, kami akan memandu Anda melalui proses langkah demi langkah. Pada akhirnya, Anda akan dapat dengan mudah mengonversi file PSB Anda ke JPG.
## Prasyarat
Sebelum kita mendalami tutorialnya, mari kita bahas prasyaratnya. Inilah yang Anda perlukan untuk memulai:
-  Java Development Kit (JDK): Pastikan Anda telah menginstal JDK di sistem Anda. Anda dapat mengunduhnya dari[situs web Oracle](https://www.oracle.com/java/technologies/javase-downloads.html).
-  Aspose.PSD untuk Perpustakaan Java: Unduh perpustakaan Aspose.PSD untuk Java dari[Unduh Halaman](https://releases.aspose.com/psd/java/).
- Lingkungan Pengembangan: IDE seperti IntelliJ IDEA, Eclipse, atau editor teks pilihan Anda.
- File PSB: File PSB yang ingin Anda konversi.
## Mengimpor Paket
Hal pertama yang pertama, mari impor paket yang diperlukan. Impor ini penting untuk bekerja dengan perpustakaan Aspose.PSD dan menangani konversi gambar.
```java
import com.aspose.psd.Image;
import com.aspose.psd.examples.Utils.Utils;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.JpegOptions;
```
## Langkah 1: Siapkan Proyek Anda
Sebelum Anda mulai membuat kode, siapkan proyek Java Anda. Buat proyek baru di IDE Anda dan tambahkan perpustakaan Aspose.PSD untuk Java ke jalur pembangunan proyek Anda. Ini akan memungkinkan Anda untuk menggunakan kelas dan metode yang disediakan oleh Aspose.PSD.
## Langkah 2: Muat File PSB
 Untuk memuat file PSB, Anda harus menentukan jalur ke file Anda dan menggunakan`PsdLoadOptions` untuk mengkonfigurasi proses pemuatan. Inilah cara Anda melakukannya:
```java
String dataDir = "Your Document Directory"; // Ganti dengan jalur direktori Anda
String sourceFileName = dataDir + "Simple.psb";
PsdLoadOptions options = new PsdLoadOptions();
PsdImage image = (PsdImage) Image.load(sourceFileName, options);
```
 Pada langkah ini, kami mengatur direktori tempat file PSB Anda berada dan memuat file ke dalam a`PsdImage` objek menggunakan`PsdLoadOptions`.
## Langkah 3: Konfigurasikan Opsi JPG
Sekarang file PSB Anda dimuat, Anda perlu mengatur opsi untuk konversi JPG. Ini termasuk menentukan kualitas keluaran JPG.
```java
JpegOptions jpgOptions = new JpegOptions();
jpgOptions.setQuality(95);
```
 Di sini, kami membuat a`JpegOptions` objek dan mengatur kualitasnya ke 95. Anda dapat menyesuaikan nilai ini untuk mengontrol kompresi dan kualitas gambar keluaran.
## Langkah 4: Simpan Gambar sebagai JPG
Dengan pilihan yang ditetapkan, Anda siap menyimpan file PSB Anda sebagai JPG. Di sinilah konversi sebenarnya terjadi.
```java
image.save(dataDir + "Simple_output.jpg", jpgOptions);
```
Perintah ini menyimpan gambar PSB yang dimuat sebagai JPG di direktori yang ditentukan dengan pengaturan kualitas yang ditentukan.
## Langkah 5: Simpan Gambar sebagai PSB (Opsional)
Jika Anda juga ingin menyimpan kembali gambar yang dimodifikasi sebagai file PSB, Anda dapat melakukannya dengan perintah serupa:
```java
image.save(dataDir + "Simple_output.psb");
```
Langkah ini opsional tetapi berguna jika Anda perlu mempertahankan format berlapis dari file PSB asli bersama dengan JPG yang dikonversi.
## Kesimpulan
Selamat! Anda telah berhasil mengonversi file PSB ke JPG menggunakan Aspose.PSD untuk Java. Tutorial ini telah memandu Anda dalam menyiapkan proyek, memuat file PSB, mengonfigurasi opsi JPG, dan menyimpan gambar yang dikonversi. Dengan mengikuti langkah-langkah ini, Anda dapat dengan mudah menangani konversi PSB ke JPG di aplikasi Java Anda.
Baik Anda seorang pengembang yang mengerjakan aplikasi pemrosesan gambar atau hanya perlu mengonversi file PSB sesekali, Aspose.PSD untuk Java memberikan solusi tangguh untuk kebutuhan Anda.
## FAQ
### Apa itu Aspose.PSD untuk Java?
Aspose.PSD untuk Java adalah perpustakaan yang memungkinkan pengembang memanipulasi dan mengonversi file PSD dan PSB dalam aplikasi Java. Ini mendukung berbagai fitur termasuk memuat, mengedit, dan menyimpan file Photoshop.
### Bisakah saya mencoba Aspose.PSD untuk Java sebelum membeli?
 Ya, Anda dapat mengunduh uji coba gratis Aspose.PSD untuk Java dari[Unduh Halaman](https://releases.aspose.com/). Ini memungkinkan Anda mengevaluasi perpustakaan dan fitur-fiturnya sebelum melakukan pembelian.
### Bagaimana cara mendapatkan lisensi sementara Aspose.PSD untuk Java?
Anda dapat memperoleh lisensi sementara dari[halaman lisensi sementara](https://purchase.aspose.com/temporary-license/). Ini akan memungkinkan Anda untuk menggunakan seluruh fitur perpustakaan untuk jangka waktu terbatas.
### Apakah ada dukungan yang tersedia jika saya mengalami masalah?
 Sangat! Anda dapat mengakses dukungan melalui[Forum dukungan Aspose.PSD](https://forum.aspose.com/c/psd/34). Tim dukungan responsif dan siap membantu Anda dengan masalah atau pertanyaan apa pun yang mungkin Anda miliki.
### Bisakah saya menyesuaikan kualitas keluaran JPG?
 Ya, Anda dapat mengatur kualitas keluaran JPG dengan mengatur`Quality` properti di`JpegOptions` obyek. Nilainya berkisar dari 0 hingga 100, dengan nilai yang lebih tinggi menunjukkan kualitas yang lebih baik dan kompresi yang lebih rendah.