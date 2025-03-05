---
title: Tambahkan Tanda Air Diagonal ke File PSD dengan Java
linktitle: Tambahkan Tanda Air Diagonal ke File PSD dengan Java
second_title: Asumsikan.PSD Java API
description: Pelajari cara mudah menambahkan tanda air diagonal ke file PSD menggunakan Java dengan Aspose.PSD. Panduan langkah demi langkah untuk menyempurnakan gambar Anda dengan percaya diri.
type: docs
weight: 12
url: /id/java/modifying-converting-psd-images/add-diagonal-watermark-psd-files/
---
## Perkenalan
Di dunia digital saat ini, memiliki visual yang mencolok dapat membuat perbedaan besar. Baik Anda seorang desainer yang ingin melindungi karya Anda atau pemasar yang ingin menambahkan merek pada gambar, menerapkan tanda air sangatlah penting. Dalam tutorial ini, kita akan mempelajari cara menambahkan tanda air diagonal ke file PSD menggunakan Java dengan bantuan Aspose.PSD, perpustakaan yang kuat untuk memanipulasi file PSD.
## Prasyarat
Sebelum kita beralih ke bagian pengkodean yang menarik, Anda harus memastikan bahwa Anda telah menyiapkan beberapa hal:
### 1. Lingkungan Pengembangan Java
 Pastikan Anda telah menginstal Java di mesin Anda. Anda dapat mengunduh versi terbaru dari[situs web Jawa](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
### 2. Perpustakaan Aspose.PSD
 Untuk bekerja dengan file PSD, Anda memerlukan perpustakaan Aspose.PSD. Anda dapat mengunduhnya dari[Asumsikan halaman Unduhan](https://releases.aspose.com/psd/java/)Bergantung pada struktur proyek Anda, Anda mungkin menggunakan Maven atau alat manajemen ketergantungan lainnya, jadi jangan ragu untuk menggabungkannya sesuai kebutuhan Anda.
### 3. Pemahaman Dasar Tentang Java
Pemahaman yang kuat tentang Java akan membantu Anda mengikuti tutorial ini dengan lancar. Pastikan Anda merasa nyaman dengan kelas, objek, dan penanganan file dasar di Java.
### 4. Pengaturan IDE
Gunakan Lingkungan Pengembangan Terintegrasi (IDE) apa pun seperti IntelliJ IDEA, Eclipse, atau NetBeans untuk membuat kode. Itu membuat pengkodean menjadi lebih mudah, bukan?
## Paket Impor
Untuk memanipulasi file PSD, Anda perlu mengimpor paket tertentu dari Aspose.PSD. Berikut adalah paket yang perlu Anda sertakan di bagian atas file Java Anda:
```java
import com.aspose.psd.Color;
import com.aspose.psd.Font;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.Matrix;
import com.aspose.psd.PointF;
import com.aspose.psd.RectangleF;
import com.aspose.psd.StringAlignment;
import com.aspose.psd.StringFormat;
import com.aspose.psd.brushes.SolidBrush;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```
Sekarang setelah prasyarat kita diurutkan dan paket yang diperlukan telah diimpor, mari ikuti langkah-langkah untuk menambahkan tanda air diagonal ke file PSD.
## Langkah 1: Siapkan Direktori Anda
```java
String dataDir = "Your Document Directory";
```
Pertama, Anda harus menentukan direktori tempat file PSD Anda berada. Direktori ini akan menjadi titik awal untuk memuat gambar. Jadi ganti`"Your Document Directory"` dengan jalur sebenarnya tempat file PSD Anda berada.
## Langkah 2: Muat File PSD
```java
PsdImage psdImage = (PsdImage)Image.load(dataDir + "layers.psd");
```
 Sekarang, kami akan memuat file PSD yang ingin Anda kerjakan. Itu`Image.load` metode membaca file dan melemparkannya ke a`PsdImage` obyek. Pastikan untuk memberikan nama persis file PSD Anda, yang dalam hal ini adalah`"layers.psd"`.
## Langkah 3: Buat Objek Grafik
```java
Graphics graphics = new Graphics(psdImage);
```
 Pada langkah ini, kita membuat a`Graphics` objek yang memungkinkan kita melakukan operasi menggambar pada gambar yang dimuat. Anggap saja seperti menyiapkan kanvas tempat kita bisa melukis tanda air kita.
## Langkah 4: Buat Font untuk Tanda Air
```java
Font font = new Font("Arial", 20.0f);
```
Di sini, kita menentukan gaya font dan ukuran untuk teks tanda air kita. Dalam hal ini, kami memilih Arial dengan ukuran 20. Silakan memilih font apa pun yang terinstal di sistem Anda — percantik sedikit!
## Langkah 5: Buat Kuas untuk Tanda Air
```java
SolidBrush brush = new SolidBrush(Color.fromArgb(50, 128, 128, 128));
```
 Selanjutnya, kita membuat a`SolidBrush` objek, yang akan mewarnai watermark kita. Itu`Color.fromArgb`metode mengambil empat parameter: alpha, merah, hijau, dan biru. Nilai alpha mengontrol transparansi (0 sepenuhnya transparan dan 255 sepenuhnya buram). Kami telah menetapkannya ke 50 untuk efek semi-transparan yang bagus.
## Langkah 6: Siapkan Matriks Transformasi
```java
graphics.setTransform(new Matrix());
graphics.getTransform().rotateAt(45, new PointF(psdImage.getWidth() / 2, psdImage.getHeight() / 2));
```
 Di sinilah keajaiban terjadi! Kami membuat matriks transformasi untuk memutar tanda air. Itu`rotateAt` Fungsi ini mengambil dua parameter: sudut (45 derajat untuk tampilan diagonal) dan titik sekitar untuk memutar (yang merupakan pusat gambar dalam kasus kita).
## Langkah 7: Tentukan Penyelarasan String
```java
StringFormat sf = new StringFormat();
sf.setAlignment(StringAlignment.Center);
```
 Kita perlu memastikan tanda air kita berada di tengah. Itu`StringFormat` class membantu kita dalam hal itu, menyelaraskan teks dengan sempurna di tengah gambar. Lagi pula, siapa yang suka penempatan yang berantakan?
## Langkah 8: Gambarkan Tanda Air
```java
graphics.drawString("Some watermark text", font, brush, new RectangleF(0, psdImage.getHeight() / 2, psdImage.getWidth(), psdImage.getHeight() / 2), sf);
```
 Sekarang, saatnya menggambar tanda air! Menggunakan`drawString`Metodenya, kami menentukan konten tanda air kami (silakan sesuaikan teksnya), font, kuas, area di mana kami ingin menggambarnya, dan pengaturan perataannya. Tanda air Anda akan diterapkan menggunakan parameter yang kami atur di persegi panjang!
## Langkah 9: Simpan Gambar
```java
psdImage.save(dataDir + "AddDiagnolWatermark_output.png", new PngOptions());
```
 Terakhir, kami menyimpan gambar kami yang telah dimodifikasi. Di sini, kami mengekspornya sebagai file PNG. Pastikan untuk memberi nama unik pada file keluaran Anda sehingga tidak menimpa file yang sudah ada. Itu`PngOptions` kelas membantu menentukan format gambar.
## Kesimpulan
Dan begitu saja, Anda berhasil menambahkan tanda air diagonal ke file PSD Anda menggunakan Java! Ini adalah proses yang mudah, namun dapat meningkatkan profesionalisme gambar Anda secara signifikan. Baik Anda melindungi karya seni atau mempromosikan merek Anda, tanda air adalah solusi sederhana namun efektif.

## FAQ
### Apa itu Aspose.PSD?
Aspose.PSD adalah perpustakaan Java yang digunakan untuk bekerja dengan dan memanipulasi file PSD tanpa memerlukan Adobe Photoshop.
### Bisakah saya menggunakan font lain untuk memberi tanda air?
Ya, Anda dapat memilih font apa pun yang diinstal pada sistem Anda untuk diberi tanda air.
### Apakah ada cara untuk menyesuaikan transparansi tanda air?
Sangat! Anda dapat menyesuaikan nilai alpha di SolidBrush untuk mengubah transparansi.
### Bisakah saya menambahkan banyak tanda air?
 Ya, Anda dapat menghubungi`drawString` metode beberapa kali dengan parameter berbeda untuk menambahkan lebih banyak tanda air.
### Di mana saya dapat menemukan informasi lebih lanjut tentang Aspose.PSD?
 Anda dapat memeriksa dokumentasinya[Di Sini](https://reference.aspose.com/psd/java/).