---
title: Ekstrak Thumbnail dari PSD di Java
linktitle: Ekstrak Thumbnail dari PSD di Java
second_title: Asumsikan.PSD Java API
description: Pelajari cara mengekstrak thumbnail dari file PSD menggunakan Aspose.PSD untuk Java. Panduan langkah demi langkah ini mencakup semuanya mulai dari pengaturan hingga menyimpan gambar yang diekstraksi.
type: docs
weight: 15
url: /id/java/java-jpeg-image-processing/extract-thumbnail-from-psd-java/
---
## Perkenalan
Dalam tutorial ini, kita akan mempelajari cara mengekstrak thumbnail dari file PSD menggunakan Aspose.PSD untuk Java. Thumbnail dapat berguna untuk pratinjau cepat atau untuk membuat versi gambar lebih kecil yang tertanam dalam dokumen PSD. Mari selami langkah-langkah yang diperlukan untuk mencapai hal ini menggunakan Aspose.PSD.
## Prasyarat
Sebelum kita mulai, pastikan Anda telah menyiapkan yang berikut:
- Java Development Kit (JDK) diinstal pada sistem Anda.
-  Aspose.PSD untuk perpustakaan Java. Anda dapat mengunduhnya dari[Di Sini](https://releases.aspose.com/psd/java/).
- Pengetahuan dasar tentang pemrograman Java.
## Paket Impor
Untuk memulai, sertakan paket Aspose.PSD yang diperlukan di kelas Java Anda:
```java
import com.aspose.psd.Image;
import com.aspose.psd.examples.Utils.Utils;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
import com.aspose.psd.imageoptions.JpegOptions;
```
## Langkah 1: Muat File PSD
Pertama, muat file PSD yang berisi thumbnail yang ingin Anda ekstrak.
```java
String dataDir = "Your_Document_Directory/";
PsdImage image = (PsdImage)Image.load(dataDir + "your_file.psd");
```
 Mengganti`"Your_Document_Directory/"` dengan jalur direktori tempat file PSD Anda berada, dan`"your_file.psd"` dengan nama file PSD Anda.
## Langkah 2: Ulangi Sumber Daya Gambar
Ulangi sumber daya gambar untuk menemukan sumber gambar mini.
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource) {
        ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
        
        // Ekstrak data gambar kecil
        int[] data = thumbnail.getThumbnailArgb32Data();
        
        // Buat gambar baru dengan data thumbnail yang diekstraksi
        PsdImage extractedThumbnailImage = new PsdImage(thumbnail.getWidth(), thumbnail.getHeight());
        extractedThumbnailImage.saveArgb32Pixels(extractedThumbnailImage.getBounds(), data);
        
        // Simpan thumbnail yang diekstrak sebagai file JPEG terpisah
        extractedThumbnailImage.save(dataDir + "extracted_thumbnail.jpg", new JpegOptions());
        
        // Keluarkan pesan sukses
        System.out.println("Thumbnail extracted and saved successfully.");
        
        break; // Keluar dari loop setelah thumbnail ditemukan dan diproses
    }
}
```
## Langkah 3: Simpan Thumbnail yang Diekstraksi
Simpan thumbnail yang diekstrak sebagai file gambar terpisah (dalam hal ini, sebagai file JPEG).
## Langkah 4: Menangani Berbagai Jenis Gambar Kecil
 Jika file PSD Anda mungkin berisi beberapa jenis thumbnail, seperti`Thumbnail4Resource`, Anda dapat memperluas logika untuk menangani kasus tersebut dengan cara yang sama.

## Kesimpulan
Dalam tutorial ini, kita menjelajahi cara mengekstrak thumbnail dari file PSD menggunakan Aspose.PSD untuk Java. Dengan mengikuti langkah-langkah yang diuraikan di atas, Anda dapat mengambil dan menyimpan thumbnail yang tertanam dalam dokumen PSD Anda secara efisien.

## FAQ
### Apa itu Aspose.PSD?
Aspose.PSD adalah perpustakaan Java yang memungkinkan pengembang untuk bekerja dengan PSD dan format file gambar lainnya secara terprogram.
### Di mana saya dapat menemukan dokumentasi lebih lanjut tentang Aspose.PSD untuk Java?
 Anda dapat merujuk ke[dokumentasi](https://reference.aspose.com/psd/java/) untuk referensi dan contoh API terperinci.
### Bisakah saya mencoba Aspose.PSD secara gratis sebelum membeli?
 Ya, Anda dapat mengunduh a[uji coba gratis](https://releases.aspose.com/) untuk mengevaluasi kemampuan perpustakaan.
### Bagaimana saya bisa mendapatkan lisensi sementara untuk Aspose.PSD?
 Lisensi sementara dapat diperoleh dari[Di Sini](https://purchase.aspose.com/temporary-license/).
### Apakah Aspose.PSD cocok untuk penggunaan komersial?
Ya, Aspose.PSD dapat digunakan untuk proyek pribadi dan komersial berdasarkan ketentuan lisensinya.