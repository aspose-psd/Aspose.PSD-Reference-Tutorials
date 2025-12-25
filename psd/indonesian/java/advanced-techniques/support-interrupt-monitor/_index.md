---
date: 2025-12-25
description: Pelajari cara mengonversi PSD ke PNG menggunakan Aspose.PSD untuk Java
  dengan dukungan monitor interupsi, termasuk contoh interupsi thread Java dan tips
  menyimpan PSD sebagai PNG.
linktitle: Support for Interrupt Monitor
second_title: Aspose.PSD Java API
title: Cara Mengonversi PSD ke PNG dengan Dukungan Interrupt Monitor di Aspose.PSD
  untuk Java
url: /id/java/advanced-techniques/support-interrupt-monitor/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Mengonversi PSD ke PNG dengan Interrupt Monitor di Aspose.PSD untuk Java

## Pendahuluan

Jika Anda perlu **mengonversi PSD ke PNG** sambil mempertahankan kontrol penuh atas konversi gambar yang memakan waktu lama, Interrupt Monitor Aspose.PSD untuk Java adalah alat yang Anda cari. Dalam tutorial ini kami akan membahas contoh **java thread interrupt** dunia nyata yang memungkinkan Anda menghentikan konversi di tengah proses, memberi Anda fleksibilitas untuk mengelola sumber daya, menerapkan batas waktu, atau merespons pembatalan pengguna.

## Jawaban Cepat
- **Apa yang dilakukan Interrupt Monitor?** Ini memungkinkan Anda memberi sinyal pada konversi gambar yang sedang berlangsung untuk berhenti dengan aman.  
- **Bisakah saya mengonversi PSD ke PNG dengan itu?** Ya – monitor bekerja dengan operasi penyimpanan apa pun, termasuk PNG.  
- **Apakah diperlukan thread terpisah?** Biasanya Anda menjalankan konversi di thread terpisah sehingga dapat menginterupsi.  
- **Versi Aspose.PSD mana yang diperlukan?** Versi terbaru apa pun yang menyertakan `com.aspose.psd.multithreading.InterruptMonitor`.  
- **Apakah saya memerlukan lisensi untuk produksi?** Ya, lisensi Aspose.PSD yang valid diperlukan untuk penggunaan non‑trial.

## Apa itu “mengonversi PSD ke PNG” dengan Interrupt Monitor?

Mengonversi dokumen Photoshop besar (PSD/PSB) menjadi gambar PNG dapat memakan banyak CPU. Dengan melampirkan **Interrupt Monitor** ke pekerja konversi, Anda memperoleh kemampuan untuk menghentikan proses secara programatik—ideal untuk layanan web, pekerjaan batch, atau aplikasi UI di mana pengguna dapat membatalkan operasi.

## Mengapa menggunakan Interrupt Monitor?

- **UI Responsif:** Mencegah aplikasi Anda membeku saat file besar sedang diproses.  
- **Manajemen Sumber Daya:** Menghentikan konversi yang melebihi batas waktu atau memori.  
- **Penanganan Kesalahan:** Membersihkan file output parsial secara elegan ketika terjadi interupsi.

## Prasyarat

- Lingkungan Pengembangan Java (JDK 8 atau lebih baru).  
- Perpustakaan Aspose.PSD untuk Java – unduh **[di sini](https://releases.aspose.com/psd/java/)**.  
- Folder yang berisi file PSD/PSB yang ingin Anda kerjakan.

## Impor Paket

Mulailah dengan mengimpor kelas yang diperlukan. Ini memberi Anda akses ke opsi gambar, interrupt monitor, dan utilitas threading.

```java
import com.aspose.psd.ImageOptionsBase;

import static com.aspose.psd.examples.Utils.Utils.getDateTime;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.multithreading.InterruptMonitor;
import com.aspose.psd.system.Threading.ThreadStart;
import java.io.File;
```

## Panduan Langkah‑per‑Langkah

### Langkah 1: Atur Direktori Dokumen Anda

```java
String dataDir = "Your Document Directory";
```

Ganti `"Your Document Directory"` dengan jalur absolut tempat file PSD Anda berada.

### Langkah 2: Tentukan Opsi Gambar dan Jalur Output

```java
ImageOptionsBase saveOptions = new PngOptions();
String source = dataDir + "big2.psb";
String output = dataDir + "big_out.png";
```

Di sini kami **menyimpan PSD sebagai PNG** dengan menggunakan `PngOptions`. Sesuaikan nama file sesuai kebutuhan.

### Langkah 3: Inisialisasi Interrupt Monitor dan SaveImageWorker

```java
InterruptMonitor monitor = new InterruptMonitor();
SaveImageWorker worker = new SaveImageWorker(source, output, saveOptions, monitor);
```

Instansi `InterruptMonitor` akan digunakan nanti untuk menghentikan konversi. `SaveImageWorker` mengaitkan monitor dengan tugas konversi.

### Langkah 4: Mulai Konversi Gambar di Thread Terpisah

```java
Thread thread = new Thread(worker.ThreadProc());
try {
    thread.start();
    // Add a timeout to allow for potential interruption
    Thread.sleep(3000);
```

Kami meluncurkan konversi pada thread latar belakang sehingga thread utama dapat tetap responsif. Pemanggilan `Thread.sleep(3000)` mensimulasikan skenario batas waktu.

### Langkah 5: Interupsi Proses (Contoh Interupsi Thread Java)

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

Pemanggilan `monitor.interrupt()` memicu logika **cara menginterupsi monitor**. Setelah interupsi kami membersihkan file PNG yang ditulis sebagian.

## Masalah Umum dan Solusinya

| Masalah | Alasan | Solusi |
|---------|--------|--------|
| Konversi tidak pernah berhenti | Monitor tidak terhubung ke worker | Pastikan `SaveImageWorker` menerima instance `InterruptMonitor` yang sama. |
| File output tetap ada setelah interupsi | Kode pembersihan tidak dijalankan | Verifikasi blok `finally` dijalankan dan jalur file sudah benar. |
| `OutOfMemoryError` pada file PSB besar | Tidak menggunakan opsi streaming | Gunakan `PsdImage` dengan `LoadOptions` yang memungkinkan pemuatan efisien memori. |

## Pertanyaan yang Sering Diajukan

### Q1: Apa itu Interrupt Monitor di Aspose.PSD untuk Java?

A1: Interrupt Monitor memungkinkan pengembang **mengelola dan menginterupsi proses konversi gambar**, memberi Anda kontrol detail atas tugas yang memakan waktu lama.

### Q2: Bagaimana cara mendapatkan perpustakaan Aspose.PSD untuk Java?

A2: Anda dapat mengunduh perpustakaan Aspose.PSD untuk Java **[di sini](https://releases.aspose.com/psd/java/)**.

### Q3: Apakah ada percobaan gratis untuk Aspose.PSD untuk Java?

A3: Ya, Anda dapat menjelajahi percobaan gratis Aspose.PSD **[di sini](https://releases.aspose.com/)**.

### Q4: Di mana saya dapat menemukan dukungan untuk Aspose.PSD untuk Java?

A4: Kunjungi forum dukungan Aspose.PSD untuk Java **[di sini](https://forum.aspose.com/c/psd/34)**.

### Q5: Bagaimana cara membeli lisensi untuk Aspose.PSD untuk Java?

A5: Anda dapat membeli lisensi untuk Aspose.PSD untuk Java **[di sini](https://purchase.aspose.com/buy)**.

---

**Terakhir Diperbarui:** 2025-12-25  
**Diuji Dengan:** Aspose.PSD 24.11 untuk Java  
**Penulis:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}