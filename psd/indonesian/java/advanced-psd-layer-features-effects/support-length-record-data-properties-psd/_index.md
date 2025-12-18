---
date: 2025-12-17
description: Pelajari cara memodifikasi bentuk vektor PSD dengan mendukung properti
  data rekaman panjang menggunakan Aspose.PSD untuk Java. Panduan langkah demi langkah
  dengan contoh kode.
linktitle: Support Length Record Data Properties in PSD - Java
second_title: Aspose.PSD Java API
title: Cara memodifikasi bentuk vektor PSD – Dukung Properti Data Rekaman Panjang
  di Java
url: /id/java/advanced-psd-layer-features-effects/support-length-record-data-properties-psd/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Dukung Properti Data Rekaman Panjang dalam PSD - Java

## Pendahuluan
Jika Anda perlu **memodifikasi vektor PSD** secara programatik, pustaka Aspose.PSD untuk Java memberikan kontrol penuh atas file Photoshop langsung dari kode Java Anda. Dalam tutorial ini kami akan membahas semua yang perlu Anda ketahui untuk mendukung properti data rekaman panjang—langkah penting ketika Anda ingin mengedit lapisan bentuk vektor. Pada akhir tutorial, Anda akan dapat membuka file PSD, menyesuaikan properti bentuk vektornya, dan menyimpan file yang diperbarui tanpa meninggalkan IDE Anda. Mari kita mulai!

## Jawaban Cepat
- **Apa arti “memodifikasi vektor PSD”?** Menyesuaikan geometri, operasi jalur, atau properti lain dari lapisan berbasis vektor di dalam file PSD.  
- **Pustaka mana yang menangani ini?** Aspose.PSD untuk Java.  
- **Apakah saya memerlukan lisensi?** Versi percobaan gratis dapat digunakan untuk evaluasi; lisensi komersial diperlukan untuk produksi.  
- **Berapa lama implementasinya?** Sekitar 10‑15 menit untuk skrip modifikasi bentuk dasar.  
- **Apa prasyarat utama?** Java JDK, Aspose.PSD untuk Java, dan file PSD contoh.

## Apa itu “modify PSD vector shapes”?
Memodifikasi vektor PSD melibatkan perubahan data jalur vektor yang mendasarinya—seperti rekaman panjang dan operasi jalur—sehingga tampilan visual bentuk berubah sesuai. Ini sangat berguna untuk pipeline grafis otomatis, pemrosesan batch, atau alat desain khusus.

## Mengapa menggunakan Aspose.PSD for Java untuk memodifikasi vektor PSD?
- **Tidak memerlukan Photoshop** – bekerja langsung dengan file PSD di server mana pun.  
- **API kaya** – mengakses lapisan, sumber daya, dan data vektor dengan kelas yang bertipe kuat.  
- **Lintas‑platform** – berjalan di Windows, Linux, atau macOS dengan JDK apa pun.  
- **Berfokus pada kinerja** – penanganan memori yang efisien dan operasi penyimpanan yang cepat.

## Prasyarat
1. **Java Development Kit (JDK)** – unduh dari [Oracle's website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) atau gunakan manajer paket pilihan Anda.  
2. **Aspose.PSD for Java** – dapatkan JAR terbaru dari [Aspose releases page](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse, atau editor Java‑compatible lainnya.  
4. **File PSD** – buat satu di Photoshop atau ambil contoh PSD untuk percobaan.  
5. **Pengetahuan dasar Java** – familiaritas dengan kelas, objek, dan penanganan pengecualian.

## Impor Paket
Pertama, impor kelas yang diperlukan untuk bekerja dengan file PSD dan sumber daya bentuk vektor.

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.LayerResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.VsmsResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.LengthRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.PathOperations;
```

## Langkah 1: Siapkan Direktori Sumber dan Output Anda
Tentukan di mana PSD asli berada dan ke mana file yang dimodifikasi akan disimpan.

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

## Langkah 3: Temukan Resource Vsms di Layer
Data bentuk vektor berada di dalam `VsmsResource`. Loop melalui sumber daya lapisan kedua untuk menemukannya.

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

## Langkah 5: Modifikasi Properti Operasi Path
Sekarang Anda dapat **memodifikasi vektor PSD** dengan mengubah `PathOperations` mereka. Ini menentukan bagaimana bentuk berinteraksi (misalnya, eksklusi, interseksi, pengurangan).

```java
lengthRecord0.setPathOperations(PathOperations.ExcludeOverlappingShapes);
lengthRecord1.setPathOperations(PathOperations.IntersectShapeAreas);
lengthRecord2.setPathOperations(PathOperations.SubtractFrontShape);
```

## Langkah 6: Simpan File PSD yang Dimodifikasi
Persist perubahan Anda ke file baru.

```java
psdImage.save(outPsdFilePath);
```

## Langkah 7: Bersihkan Sumber Daya
Dispose `PsdImage` untuk membebaskan memori.

```java
psdImage.dispose();
```

## Kesalahan Umum & Tips
- **Pemeriksaan null** – selalu pastikan `resource` tidak `null` sebelum mengakses jalur.  
- **Batas indeks jalur** – pastikan indeks yang Anda gunakan (`[2]`, `[7]`, `[11]`) ada untuk PSD spesifik yang Anda edit.  
- **Lisensi** – menjalankan tanpa lisensi yang valid akan menambahkan watermark pada PSD yang disimpan.  

## Kesimpulan
Anda kini memiliki contoh lengkap end‑to‑end tentang cara **memodifikasi vektor PSD** dengan mendukung properti data rekaman panjang menggunakan Aspose.PSD untuk Java. Baik Anda mengotomatisasi pipeline aset atau membangun alat desain khusus, API ini memberi fleksibilitas untuk memanipulasi lapisan vektor tanpa pekerjaan manual di Photoshop. Jelajahi lebih lanjut dengan bereksperimen pada `PathOperations` lain atau menggabungkan beberapa edit `LengthRecord` untuk bentuk yang kompleks.

## Pertanyaan yang Sering Diajukan

**Q: Bagaimana cara menangani PSD yang tidak memiliki lapisan bentuk vektor?**  
A: `VsmsResource` tidak akan ada, sehingga `resource` akan tetap `null`. Tambahkan pemeriksaan dan lewati langkah modifikasi atau beri tahu pengguna.

**Q: Bisakah saya mengubah properti lain seperti warna isi atau lebar garis?**  
A: Ya, `LengthRecord` menyediakan setter tambahan untuk isi, garis, dan opasitas. Lihat dokumentasi API untuk detail lengkap.

**Q: Apakah memungkinkan memproses batch beberapa file PSD?**  
A: Tentu saja. Bungkus kode dalam loop yang iterasi melalui direktori berisi file PSD, sesuaikan jalur input dan output setiap kali.

**Q: Apakah saya perlu menutup stream secara manual saat memuat dari jalur file?**  
A: Metode `Image.load` menangani stream file secara internal, tetapi jika Anda memuat dari `InputStream`, ingatlah untuk menutupnya setelah selesai.

**Q: Versi Aspose.PSD apa yang diperlukan untuk API ini?**  
A: Kelas `LengthRecord` dan `PathOperations` tersedia sejak Aspose.PSD 20.10. Disarankan menggunakan versi terbaru.

---

**Last Updated:** 2025-12-17  
**Tested With:** Aspose.PSD for Java 24.11  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}