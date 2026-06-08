---
date: 2026-06-08
description: Pelajari cara menyimpan PSD sebagai PNG menggunakan Aspose.PSD untuk
  Java dan menghentikan konversi bila diperlukan. Kelola alur kerja gambar secara
  efisien.
keywords:
- save psd as png
- how to interrupt conversion
- psd to png conversion
- manage image workflow
linktitle: Dukungan untuk Interrupt Monitor
schemas:
- author: Aspose
  dateModified: '2026-06-08'
  description: Learn how to save PSD as PNG using Aspose.PSD for Java and interrupt
    conversion when needed. Manage image workflow efficiently.
  headline: How to Save PSD as PNG with Interrupt Monitor in Aspose.PSD for Java
  type: TechArticle
- description: Learn how to save PSD as PNG using Aspose.PSD for Java and interrupt
    conversion when needed. Manage image workflow efficiently.
  name: How to Save PSD as PNG with Interrupt Monitor in Aspose.PSD for Java
  steps:
  - name: Set Your Document Directory
    text: Ensure to replace “Your Document Directory” with the actual path where your
      PSD documents are stored.
  - name: Define Image Options and Output Path
    text: Specify the image options, source PSD file, and the desired output path
      for the converted image.
  - name: Initialize Interrupt Monitor and SaveImageWorker
    text: The `InterruptMonitor` class watches a running conversion and can interrupt
      it when `requestInterrupt()` is called. Create instances of `InterruptMonitor`
      and `SaveImageWorker`, linking the monitor to the image conversion worker.
  - name: Start Image Conversion Thread
    text: Initiate a new thread for the image conversion process and introduce a timeout
      period to anticipate interruption.
  - name: Interrupt the Process
    text: Calling `monitor.requestInterrupt()` signals the monitor to abort the ongoing
      conversion. Interrupt the image conversion process using the `InterruptMonitor`
      and wait for the interruption to complete. Finally, clean up by deleting the
      output file.
  type: HowTo
- questions:
  - answer: Yes, use `InterruptMonitor` to stop the process on demand.
    question: Can I interrupt a PSD‑to‑PNG conversion?
  - answer: Call `save(outputPath, new PngOptions())`.
    question: Which method saves a PSD as PNG?
  - answer: A commercial license is required; a free trial is available.
    question: Do I need a license for production?
  - answer: Java 8 and later are fully supported.
    question: What Java version is supported?
  - answer: Conversions can run in separate threads; the monitor handles interruptions
      safely.
    question: Is the library thread‑safe?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Cara Menyimpan PSD sebagai PNG dengan Interrupt Monitor di Aspose.PSD untuk
  Java
url: /id/java/advanced-techniques/support-interrupt-monitor/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Simpan PSD sebagai PNG dengan Interrupt Monitor di Aspose.PSD untuk Java

## Pendahuluan

Jika Anda perlu **save PSD as PNG** sambil mempertahankan kontrol penuh atas konversi yang berjalan lama, Interrupt Monitor Aspose.PSD untuk Java memberikan hal itu. Dalam tutorial ini kami akan menjelaskan cara menyiapkan monitor, mengonversi file PSD ke PNG, dan menghentikan operasi dengan aman ketika diperlukan. Anda juga akan melihat bagaimana ini cocok dalam alur kerja pemrosesan gambar tipikal dan mengapa ini menjadi keharusan untuk aplikasi yang kuat.

## Jawaban Cepat
- **Bisakah saya menghentikan konversi PSD‑to‑PNG?** Ya, gunakan `InterruptMonitor` untuk menghentikan proses sesuai permintaan.  
- **Metode apa yang menyimpan PSD sebagai PNG?** Panggil `save(outputPath, new PngOptions())`.  
- **Apakah saya memerlukan lisensi untuk produksi?** Lisensi komersial diperlukan; versi percobaan gratis tersedia.  
- **Versi Java apa yang didukung?** Java 8 dan yang lebih baru didukung sepenuhnya.  
- **Apakah perpustakaan ini thread‑safe?** Konversi dapat dijalankan di thread terpisah; monitor menangani interupsi dengan aman.

## Prasyarat

Sebelum menyelami seluk‑beluk penggunaan Interrupt Monitor, pastikan Anda memiliki prasyarat berikut:

- **Java Development Environment:** Siapkan lingkungan pengembangan Java di sistem Anda.  
- **Aspose.PSD Library:** Dapatkan pustaka Aspose.PSD untuk Java. Anda dapat mengunduhnya [here](https://releases.aspose.com/psd/java/). Anda juga dapat mengunjungi situs utama Aspose [here](https://releases.aspose.com/).  
- **Document Directory:** Miliki direktori yang ditentukan untuk dokumen PSD Anda.

## Impor Paket

Mulailah dengan mengimpor paket yang diperlukan ke dalam proyek Java Anda. Ini memastikan Anda memiliki akses ke fungsionalitas Aspose.PSD.

```java
import com.aspose.psd.ImageOptionsBase;

import static com.aspose.psd.examples.Utils.Utils.getDateTime;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.multithreading.InterruptMonitor;
import com.aspose.psd.system.Threading.ThreadStart;
import java.io.File;
```

Sekarang, mari kita uraikan contoh kode menjadi panduan langkah‑demi‑langkah untuk mengintegrasikan Interrupt Monitor dalam proyek Aspose.PSD untuk Java Anda.

## Cara menyimpan PSD sebagai PNG menggunakan Interrupt Monitor?

`PsdImage` mewakili dokumen PSD yang dimuat ke memori.  
`SaveImageWorker` melakukan konversi gambar di thread terpisah.  

Muat file PSD Anda dengan `new PsdImage("source.psd")`, lampirkan `InterruptMonitor` ke `SaveImageWorker`, dan panggil `save("output.png", new PngOptions())`. Monitor memantau permintaan pembatalan dan menghentikan konversi dengan bersih, mengembalikan kontrol ke aplikasi Anda dalam hitungan milidetik.

### Langkah 1: Atur Direktori Dokumen Anda

```java
String dataDir = "Your Document Directory";
```

Pastikan untuk mengganti “Your Document Directory” dengan jalur sebenarnya tempat dokumen PSD Anda disimpan.

### Langkah 2: Tentukan Opsi Gambar dan Jalur Output

```java
ImageOptionsBase saveOptions = new PngOptions();
String source = dataDir + "big2.psb";
String output = dataDir + "big_out.png";
```

Tentukan opsi gambar, file PSD sumber, dan jalur output yang diinginkan untuk gambar yang dikonversi.

### Langkah 3: Inisialisasi Interrupt Monitor dan SaveImageWorker

Kelas `InterruptMonitor` memantau konversi yang sedang berjalan dan dapat menginterupsi ketika `requestInterrupt()` dipanggil.  

```java
InterruptMonitor monitor = new InterruptMonitor();
SaveImageWorker worker = new SaveImageWorker(source, output, saveOptions, monitor);
```

Buat instance `InterruptMonitor` dan `SaveImageWorker`, menghubungkan monitor ke pekerja konversi gambar.

### Langkah 4: Mulai Thread Konversi Gambar

```java
Thread thread = new Thread(worker.ThreadProc());
try {
    thread.start();
    // Add a timeout to allow for potential interruption
    Thread.sleep(3000);
```

Inisialisasi thread baru untuk proses konversi gambar dan perkenalkan periode timeout untuk mengantisipasi interupsi.

### Langkah 5: Interupsi Proses

Memanggil `monitor.requestInterrupt()` memberi sinyal kepada monitor untuk menghentikan konversi yang sedang berlangsung.  

```java
    // Interrupt the process
    monitor.interrupt();
    System.out.println("Interrupting the save thread #" + thread.getId() + " at " + getDateTime().toString());

    // Wait for interruption...
    thread.join();
} finally {
    // Delete the output file if it exists
    File f = new File(output);
    if (f.exists()) {
        f.delete();
    }
}
```

Interupsi proses konversi gambar menggunakan `InterruptMonitor` dan tunggu hingga interupsi selesai. Akhirnya, bersihkan dengan menghapus file output.

## Mengapa menggunakan Interrupt Monitor untuk konversi PSD‑to‑PNG?

Aspose.PSD mendukung **30+ format output**, termasuk PNG, JPEG, BMP, dan TIFF, serta dapat memproses file hingga **500 MB** tanpa memuat seluruh dokumen ke memori. Dengan menambahkan interrupt monitor Anda mengurangi pemborosan CPU dan meningkatkan responsifitas dalam pipeline pemrosesan batch, terutama ketika konversi melebihi batas waktu yang diharapkan.

## Masalah Umum dan Solusinya

- **Konversi menggantung tanpa batas:** Pastikan monitor terpasang **sebelum** memanggil `save`.  
- **File output rusak setelah interupsi:** Monitor menghentikan dengan bersih; namun, selalu periksa apakah file ada sebelum menggunakannya.  
- **Kekhawatiran thread‑safety:** Jalankan setiap konversi di thread masing‑masing; monitor hanya memengaruhi pekerja yang terkait.

## Pertanyaan yang Sering Diajukan

**Q1: Apa itu Interrupt Monitor di Aspose.PSD untuk Java?**  
A: Interrupt Monitor memungkinkan pengembang menjeda atau membatalkan konversi gambar yang berjalan lama, memberikan kontrol waktu nyata atas penggunaan sumber daya.

**Q2: Bagaimana saya dapat memperoleh pustaka Aspose.PSD untuk Java?**  
A: Anda dapat mengunduh pustaka Aspose.PSD untuk Java [here](https://releases.aspose.com/psd/java/).

**Q3: Apakah tersedia percobaan gratis untuk Aspose.PSD untuk Java?**  
A: Ya, Anda dapat menjelajahi percobaan gratis Aspose.PSD [here](https://releases.aspose.com/).

**Q4: Di mana saya dapat menemukan dukungan untuk Aspose.PSD untuk Java?**  
A: Kunjungi forum dukungan Aspose.PSD untuk Java [here](https://forum.aspose.com/c/psd/34).

**Q5: Bagaimana saya dapat membeli lisensi untuk Aspose.PSD untuk Java?**  
A: Anda dapat membeli lisensi untuk Aspose.PSD untuk Java [here](https://purchase.aspose.com/buy).

**Q6: Bisakah saya mengonversi beberapa file PSD ke PNG secara paralel?**  
A: Ya, buat thread terpisah untuk setiap file dan lampirkan `InterruptMonitor` individual ke setiap pekerja konversi.

**Q7: Apakah pustaka menangani profil warna selama konversi PSD‑to‑PNG?**  
A: Tentu saja; Aspose.PSD mempertahankan profil ICC yang tertanam dan menerapkannya ke PNG output secara otomatis.

---

**Terakhir Diperbarui:** 2026-06-08  
**Diuji Dengan:** Aspose.PSD 23.12 untuk Java  
**Penulis:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Tutorial Terkait

- [Save PSD as PNG and Apply Rendering Drop Shadow in Aspose.PSD for Java](/psd/java/advanced-image-manipulation/rendering-drop-shadow/)
- [Export PSD to PNG & Add a New Regular Layer using Aspose.PSD for Java](/psd/java/advanced-image-effects/add-new-regular-layer/)
- [Support for Interrupt Monitor in PSD Files - Java](/psd/java/psd-layer-management-effects/support-interrupt-monitor-psd-files/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}