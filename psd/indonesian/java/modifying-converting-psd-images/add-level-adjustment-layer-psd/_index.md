---
title: Tambahkan Lapisan Penyesuaian Level di PSD
linktitle: Tambahkan Lapisan Penyesuaian Level di PSD
second_title: Asumsikan.PSD Java API
description: Pelajari cara menambahkan Lapisan Penyesuaian Level secara efektif di file PSD Anda menggunakan Aspose.PSD untuk Java. Tingkatkan keterampilan mengedit gambar Anda.
type: docs
weight: 16
url: /id/java/modifying-converting-psd-images/add-level-adjustment-layer-psd/
---
## Perkenalan
Dalam hal pengeditan gambar, mengelola level dapat membuat perbedaan besar dalam kecerahan dan kejernihan foto Anda. Salah satu alat praktis di gudang Photoshop adalah "Level Adjustment Layer," yang memungkinkan Anda mengubah rentang nada dan keseimbangan warna gambar Anda. Dalam panduan ini, kami akan memandu Anda tentang cara mengimplementasikan Lapisan Penyesuaian Level dalam file PSD menggunakan Aspose.PSD untuk Java. Jadi, ambil IDE Java Anda.
## Prasyarat
Sebelum terjun ke dunia penyesuaian level, Anda perlu menyiapkan beberapa hal untuk memastikan pengendaraan lancar:
1.  Java Development Kit (JDK): Pastikan Anda telah menginstal JDK di mesin Anda. Jika Anda tidak memilikinya, Anda dapat mengambilnya dari[situs web Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) atau gunakan OpenJDK.
2.  Aspose.PSD untuk Perpustakaan Java: Untuk memanipulasi file PSD, Anda perlu mengunduh perpustakaan Aspose.PSD. Anda bisa mendapatkan versi terbaru dari ini[tautan unduhan](https://releases.aspose.com/psd/java/) dan pastikan Anda telah memasukkan JAR ke perpustakaan proyek Anda.
3. Pengetahuan Dasar Java: Memiliki pemahaman mendasar tentang pemrograman Java akan membantu, karena kita akan mendalami cuplikan kode sepanjang tutorial ini.
4. Penyiapan IDE: Anda dapat menggunakan IDE Java apa pun yang Anda sukai—seperti IntelliJ IDEA, Eclipse, atau NetBeans—untuk menulis dan menjalankan kode Anda. Pastikan Anda telah menyiapkan proyek Java Anda dan menambahkan perpustakaan Aspose.PSD.

## Paket Impor
Sebelum kita mulai menulis kode, kita perlu mengimpor paket yang diperlukan dari perpustakaan Aspose.PSD. Inilah cara Anda melakukannya:
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.LevelsLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.LevelChannel;
```
Dengan mengimpor paket-paket ini, kita akan memiliki akses ke kelas-kelas yang diperlukan untuk memuat, memodifikasi, dan menyimpan file PSD kita.

Sekarang, mari kita bagi prosesnya menjadi langkah-langkah yang mudah dicerna. Ikuti terus saat kami memuat file PSD, menyesuaikan level, dan kemudian menyimpan perubahan Anda. 
## Langkah 1: Siapkan Jalur File Anda
Langkah pertama adalah menentukan di mana file PSD kita berada dan di mana kita ingin menyimpan hasil modifikasi. Anda dapat menyesuaikan jalur direktori sesuai kebutuhan Anda.
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "LevelsAdjustmentLayer.psd";
String psdPathAfterChange = dataDir + "LevelsAdjustmentLayerChanged.psd";
```
 Ini, ganti`"Your Document Directory"`dengan jalur sebenarnya di sistem Anda tempat file PSD Anda disimpan. Ini menetapkan landasan untuk segala sesuatu yang akan kami lakukan selanjutnya.
## Langkah 2: Muat File PSD
 Sekarang, mari kita memuat file PSD menggunakan`PsdImage` kelas. Langkah ini penting karena memungkinkan kita mengakses dan memanipulasi lapisan.
```java
PsdImage im = (PsdImage) Image.load(sourceFileName);
```
 Saat Anda menelepon`Image.load()` , itu akan membaca file PSD dan membuat sebuah instance`PsdImage` yang dapat Anda kerjakan.
## Langkah 3: Iterasi Melalui Lapisan
Karena kita ingin menyesuaikan Layer Penyesuaian Level, kita perlu mengulang setiap layer dalam file PSD kita. Ini membantu kita menemukan lapisan spesifik yang ingin kita modifikasi.
```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof LevelsLayer) {
        LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
        // Manipulasi lebih lanjut akan dilakukan di sini...
    }
}
```
 Dalam lingkaran ini,`instanceof LevelsLayer` memeriksa apakah lapisan saat ini adalah Lapisan Penyesuaian Tingkat. Jika ya, kita dapat melanjutkan untuk mengubah propertinya.
## Langkah 4: Sesuaikan Pengaturan Saluran Level
Setelah kami mengidentifikasi lapisan yang benar, kami dapat mengubah level input dan outputnya. Di sinilah keajaiban terjadi! Sesuaikan parameter yang berbeda untuk melihat pengaruhnya terhadap gambar.
```java
LevelChannel channel = levelsLayer.getChannel(0);
channel.setInputMidtoneLevel(2.0f);
channel.setInputShadowLevel((short) 10);
channel.setInputHighlightLevel((short) 230);
channel.setOutputShadowLevel((short) 20);
channel.setOutputHighlightLevel((short) 200);
```
Inilah yang dilakukan setiap parameter:
- Input Midtone Level: Menyesuaikan nada tengah.
- Input Shadow Level: Mengubah area gambar yang lebih gelap.
- Input Highlight Level: Mengubah area terang pada gambar.
- Tingkat Bayangan Keluaran: Mengatur bagaimana bayangan gelap akan muncul.
- Tingkat Sorotan Keluaran: Mengatur bagaimana sorotan cahaya akan muncul.
Jangan ragu untuk bereksperimen dengan nilai yang berbeda!
## Langkah 5: Simpan File PSD yang Dimodifikasi
Sekarang kita telah melakukan penyesuaian, sekarang saatnya menyimpan file PSD yang dimodifikasi. Langkah ini penting untuk memastikan bahwa perubahan Anda diterapkan dan disimpan.
```java
im.save(psdPathAfterChange);
```
 Anda sekarang dapat menemukan file PSD yang telah disesuaikan di tempat yang ditentukan`psdPathAfterChange`. 
## Kesimpulan
Anda baru saja mempelajari cara menambahkan Lapisan Penyesuaian Level ke file PSD menggunakan Aspose.PSD untuk Java! Dengan mengikuti panduan ini, Anda dapat menyesuaikan kualitas nada gambar Anda dengan mudah, sehingga membuka jalan bagi hasil yang lebih hidup dan menarik secara visual. Ingat, latihan membuat sempurna, jadi silakan sesuaikan penyesuaian dan jelajahi berbagai file PSD untuk melihat efek perubahan Anda.
## FAQ
### Apa itu Lapisan Penyesuaian Level?
Lapisan Penyesuaian Level memungkinkan Anda mengoreksi rentang nada pada gambar Anda, menyeimbangkan bayangan, nada tengah, dan sorotan.
### Bisakah saya menggunakan Aspose.PSD tanpa pembelian?
Ya! Aspose menawarkan uji coba gratis untuk menguji perpustakaan sebelum membeli.
### Di mana saya dapat menemukan dokumentasi untuk Aspose.PSD?
 Anda dapat menemukan dokumentasinya[Di Sini](https://reference.aspose.com/psd/java/).
### Apakah ada dukungan komunitas untuk produk Aspose?
 Sangat! Anda dapat mengajukan pertanyaan dan mendapatkan dukungan di[Asumsikan forum](https://forum.aspose.com/c/psd/34).
### Bagaimana saya bisa mendapatkan lisensi sementara untuk Aspose.PSD?
 Anda dapat mengajukan permohonan izin sementara[Di Sini](https://purchase.aspose.com/temporary-license/).