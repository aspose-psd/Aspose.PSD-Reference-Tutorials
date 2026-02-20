---
date: 2026-02-20
description: Pelajari cara mendukung properti rekaman panjang dan memproses batch
  file PSD menggunakan Aspose.PSD untuk Java. Panduan langkah demi langkah dengan
  contoh kode.
linktitle: Support Length Record Data Properties in PSD - Java
second_title: Aspose.PSD Java API
title: Dukungan Properti Rekaman Panjang – Modifikasi Bentuk Vektor PSD (Java)
url: /id/java/advanced-psd-layer-features-effects/support-length-record-data-properties-psd/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Dukungan Properti Rekaman Panjang – Modifikasi Bentuk Vektor PSD (Java)

## Pendahuluan
Jika Anda perlu **memodifikasi bentuk vektor PSD** secara programatis, perpustakaan Aspose.PSD untuk Java memberi Anda kontrol penuh atas file Photoshop langsung dari kode Java Anda. Dalam tutorial ini kami akan membahas semua yang perlu Anda ketahui untuk **mendukung properti rekaman panjang**—langkah penting ketika Anda ingin mengedit lapisan bentuk vektor. Pada akhir tutorial, Anda akan dapat membuka file PSD, menyesuaikan properti bentuk vektornya, dan menyimpan file yang diperbarui tanpa meninggalkan IDE Anda. Mari kita mulai!

## Jawaban Cepat
- **Apa arti “memodifikasi bentuk vektor PSD”?** Menyesuaikan geometri, operasi jalur, atau properti lain dari lapisan berbasis vektor di dalam file PSD.  
- **Perpustakaan mana yang menangani ini?** Aspose.PSD untuk Java.  
- **Apakah saya memerlukan lisensi?** Versi percobaan gratis dapat digunakan untuk evaluasi; lisensi komersial diperlukan untuk produksi.  
- **Berapa lama implementasinya?** Sekitar 10‑15 menit untuk skrip modifikasi bentuk dasar.  
- **Apa prasyarat utama?** Java JDK, Aspose.PSD untuk Java, dan file PSD contoh.

## Apa itu “dukungan properti rekaman panjang”?
Mendukung properti rekaman panjang berarti mengakses dan memperbarui objek `LengthRecord` yang mendeskripsikan setiap jalur vektor di dalam PSD. Mengubah rekaman ini memungkinkan Anda mengontrol bagaimana bentuk-bentuk digabungkan, berpotongan, atau dikurangkan satu sama lain.

## Mengapa menggunakan Aspose.PSD untuk Java untuk mendukung properti rekaman panjang?
- **Tidak memerlukan Photoshop** – bekerja langsung dengan file PSD di server mana pun.  
- **API kaya** – mengakses lapisan, sumber daya, dan data vektor dengan kelas yang bertipe kuat.  
- **Lintas platform** – berjalan di Windows, Linux, atau macOS dengan JDK apa pun.  
- **Berfokus pada kinerja** – penanganan memori yang efisien dan operasi penyimpanan yang cepat.  

## Prasyarat
1. **Java Development Kit (JDK)** – unduh dari [situs Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) atau **gunakan manajer paket pilihan Anda**.  
2. **Aspose.PSD untuk Java** – dapatkan JAR terbaru dari [halaman rilis Aspose](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse, atau editor yang kompatibel dengan Java.  
4. **File PSD** – buat satu di Photoshop atau ambil contoh PSD untuk bereksperimen.  
5. **Pengetahuan dasar Java** – familiaritas dengan kelas, objek, dan penanganan pengecualian.

## Mengimpor Paket
Pertama, impor kelas yang Anda perlukan untuk bekerja dengan file PSD dan sumber daya bentuk vektor.

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.LayerResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.VsmsResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.LengthRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.PathOperations;
```

## Langkah 1: Siapkan Direktori Sumber dan Output Anda
Tentukan di mana PSD asli berada dan di mana Anda ingin file yang dimodifikasi disimpan.

```java
String sourceDir = "Your Source Directory";
String outputDir = "Your Document Directory";
String inPsdFilePath = sourceDir + "PathOperationsShape.psd";
String outPsdFilePath = outputDir + "out_PathOperationsShape.psd";
```

## Langkah 2: Muat File PSD
Gunakan `Image.load` untuk membuka file dan cast ke `PsdImage` untuk fitur khusus PSD.

```java
PsdImage psdImage = (PsdImage) Image.load(inPsdFilePath);
```

## Langkah 3: Temukan Sumber Vsms di Lapisan
Data bentuk vektor berada di dalam `VsmsResource`. Lakukan loop pada sumber daya lapisan kedua untuk menemukannya.

```java
VsmsResource resource = null;
for (LayerResource layerResource : psdImage.getLayers()[1].getResources()) {
    if (layerResource instanceof VsmsResource) {
        resource = (VsmsResource) layerResource;
        break;
    }
}
```

## Langkah 4: Akses Rekaman Panjang
Setiap `LengthRecord` mewakili jalur vektor yang berbeda. Ambil yang ingin Anda modifikasi.

```java
LengthRecord lengthRecord0 = (LengthRecord) resource.getPaths()[2];
LengthRecord lengthRecord1 = (LengthRecord) resource.getPaths()[7];
LengthRecord lengthRecord2 = (LengthRecord) resource.getPaths()[11];
```

## Langkah 5: Modifikasi Properti Operasi Jalur
Sekarang Anda dapat **memodifikasi bentuk vektor PSD** dengan mengubah `PathOperations` mereka. Ini menentukan bagaimana bentuk berinteraksi (mis., eksklusi, interseksi, pengurangan).

```java
lengthRecord0.setPathOperations(PathOperations.ExcludeOverlappingShapes);
lengthRecord1.setPathOperations(PathOperations.IntersectShapeAreas);
lengthRecord2.setPathOperations(PathOperations.SubtractFrontShape);
```

## Langkah 6: Simpan File PSD yang Dimodifikasi
Simpan perubahan Anda ke file baru.

```java
psdImage.save(outPsdFilePath);
```

## Langkah 7: Bersihkan Sumber Daya
Buang `PsdImage` untuk membebaskan memori.

```java
psdImage.dispose();
```

## Cara memproses batch file PSD dengan dukungan properti rekaman panjang
Jika Anda perlu menerapkan penyesuaian bentuk vektor yang sama ke banyak PSD, bungkus kode di atas dalam loop yang mengiterasi direktori file. Perbarui `inPsdFilePath` dan `outPsdFilePath` untuk setiap iterasi, dan Anda akan dapat **memproses batch file PSD** secara efisien.

## Kesalahan Umum & Tips
- **Pemeriksaan null** – selalu pastikan `resource` tidak `null` sebelum mengakses jalur.  
- **Batas indeks jalur** – pastikan indeks yang Anda gunakan (`[2]`, `[7]`, `[11]`) ada untuk PSD spesifik yang Anda edit.  
- **Lisensi** – menjalankan tanpa lisensi yang valid akan menambahkan watermark pada PSD yang disimpan.  

## Kesimpulan
Anda sekarang memiliki contoh lengkap, end‑to‑end tentang cara **memodifikasi bentuk vektor PSD** dengan mendukung properti rekaman panjang menggunakan Aspose.PSD untuk Java. Baik Anda mengotomatisasi pipeline aset atau membangun alat desain khusus, API ini memberi Anda fleksibilitas untuk memanipulasi lapisan vektor tanpa pekerjaan manual Photoshop. Jelajahi lebih lanjut dengan bereksperimen dengan `PathOperations` lain atau menggabungkan beberapa edit `LengthRecord` untuk bentuk yang kompleks.

## Pertanyaan yang Sering Diajukan

**T: Bagaimana saya menangani PSD yang tidak berisi lapisan bentuk vektor?**  
J: `VsmsResource` tidak ada, sehingga `resource` akan tetap `null`. Tambahkan pemeriksaan dan lewati langkah modifikasi atau beri tahu pengguna.

**T: Bisakah saya mengubah properti lain seperti warna isi atau lebar garis?**  
J: Ya, `LengthRecord` menyediakan setter tambahan untuk isi, garis, dan opasitas. Lihat dokumentasi API untuk detail lengkap.

**T: Apakah memungkinkan memproses batch beberapa file PSD?**  
J: Tentu saja. Bungkus kode dalam loop yang mengiterasi direktori file PSD, menyesuaikan jalur input dan output setiap kali.

**T: Apakah saya perlu menutup stream secara manual saat memuat dari jalur file?**  
J: Metode `Image.load` menangani stream file secara internal, tetapi jika Anda memuat dari `InputStream`, ingat untuk menutupnya setelah digunakan.

**T: Versi Aspose.PSD apa yang diperlukan untuk API ini?**  
J: Kelas `LengthRecord` dan `PathOperations` tersedia sejak Aspose.PSD 20.10. Disarankan menggunakan versi terbaru.

---

**Terakhir Diperbarui:** 2026-02-20  
**Diuji Dengan:** Aspose.PSD untuk Java 24.11  
**Penulis:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}