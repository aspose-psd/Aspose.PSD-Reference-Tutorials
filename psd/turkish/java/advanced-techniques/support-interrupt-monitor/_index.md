---
date: 2026-06-08
description: Aspose.PSD for Java kullanarak PSD'yi PNG olarak nasıl kaydedeceğinizi
  ve gerektiğinde dönüşümü nasıl durduracağınızı öğrenin. Görüntü iş akışını verimli
  bir şekilde yönetin.
keywords:
- save psd as png
- how to interrupt conversion
- psd to png conversion
- manage image workflow
linktitle: Interrupt Monitor Desteği
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
title: Aspose.PSD for Java'da Interrupt Monitor ile PSD'yi PNG olarak kaydetme
url: /tr/java/advanced-techniques/support-interrupt-monitor/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD'yi PNG Olarak Kaydet ve Aspose.PSD for Java'da Kesinti İzleyicisi

## Giriş

Eğer **PSD'yi PNG olarak kaydetmek** ve uzun süren dönüşümler üzerinde tam kontrol sağlamak istiyorsanız, Aspose.PSD for Java’nın Kesinti İzleyicisi tam da bunu sunar. Bu öğreticide izleyiciyi kurmayı, bir PSD dosyasını PNG'ye dönüştürmeyi ve gerektiğinde işlemi güvenli bir şekilde iptal etmeyi adım adım göstereceğiz. Ayrıca bunun tipik bir görüntü‑işleme iş akışına nasıl uyduğunu ve sağlam uygulamalar için neden vazgeçilmez olduğunu göreceksiniz.

## Hızlı Yanıtlar
- **Bir PSD‑to‑PNG dönüşümünü kesintiye uğratabilir miyim?** Evet, `InterruptMonitor` kullanarak isteğe bağlı olarak işlemi durdurabilirsiniz.  
- **PSD'yi PNG olarak kaydeden yöntem hangisidir?** `save(outputPath, new PngOptions())` çağrısını yapın.  
- **Üretim için lisansa ihtiyacım var mı?** Ticari bir lisans gereklidir; ücretsiz deneme sürümü mevcuttur.  
- **Hangi Java sürümü destekleniyor?** Java 8 ve üzeri tam olarak desteklenir.  
- **Kütüphane çok iş parçacıklı (thread‑safe) mı?** Dönüşümler ayrı iş parçacıklarında çalıştırılabilir; izleyici kesintileri güvenli bir şekilde yönetir.

## Ön Koşullar

Kesinti İzleyicisi kullanımının inceliklerine girmeden önce aşağıdaki ön koşulların sağlandığından emin olun:

- **Java Geliştirme Ortamı:** Sisteminizde bir Java geliştirme ortamı kurun.  
- **Aspose.PSD Kütüphanesi:** Aspose.PSD for Java kütüphanesini edinin. İndirmek için [buraya](https://releases.aspose.com/psd/java/) tıklayın. Ayrıca ana Aspose sitesini [buradan](https://releases.aspose.com/) ziyaret edebilirsiniz.  
- **Belge Dizinı:** PSD belgeleriniz için ayrılmış bir dizin oluşturun.

## Paketleri İçe Aktar

Gerekli paketleri Java projenize dahil ederek Aspose.PSD işlevlerine erişim sağlayın.

```java
import com.aspose.psd.ImageOptionsBase;

import static com.aspose.psd.examples.Utils.Utils.getDateTime;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.multithreading.InterruptMonitor;
import com.aspose.psd.system.Threading.ThreadStart;
import java.io.File;
```

Şimdi, örnek kodu adım adım inceleyerek Aspose.PSD for Java projenize Kesinti İzleyicisini nasıl entegre edeceğinizi görelim.

## Kesinti İzleyicisini Kullanarak PSD'yi PNG Olarak Nasıl Kaydedilir?

`PsdImage` belleğe yüklenmiş bir PSD belgesini temsil eder.  
`SaveImageWorker` görüntü dönüşümünü ayrı bir iş parçacığında gerçekleştirir.  

`new PsdImage("source.psd")` ile PSD dosyanızı yükleyin, `SaveImageWorker`a bir `InterruptMonitor` ekleyin ve `save("output.png", new PngOptions())` çağrısını yapın. İzleyici iptal isteğini izler ve dönüşümü temiz bir şekilde durdurur, milisaniyeler içinde kontrolü uygulamanıza geri verir.

### Adım 1: Belge Dizinini Ayarlayın

```java
String dataDir = "Your Document Directory";
```

“Your Document Directory” ifadesini PSD belgelerinizin gerçek yolu ile değiştirin.

### Adım 2: Görüntü Seçeneklerini ve Çıktı Yolunu Tanımlayın

```java
ImageOptionsBase saveOptions = new PngOptions();
String source = dataDir + "big2.psb";
String output = dataDir + "big_out.png";
```

Görüntü seçeneklerini, kaynak PSD dosyasını ve dönüştürülmüş görüntünün istenen çıktı yolunu belirtin.

### Adım 3: Kesinti İzleyicisini ve SaveImageWorker'ı Başlatın

`InterruptMonitor` sınıfı çalışan bir dönüşümü izler ve `requestInterrupt()` çağrıldığında onu kesintiye uğratabilir.  

```java
InterruptMonitor monitor = new InterruptMonitor();
SaveImageWorker worker = new SaveImageWorker(source, output, saveOptions, monitor);
```

`InterruptMonitor` ve `SaveImageWorker` örneklerini oluşturun, izleyiciyi dönüşüm çalışanına bağlayın.

### Adım 4: Görüntü Dönüştürme İş Parçacığını Başlatın

```java
Thread thread = new Thread(worker.ThreadProc());
try {
    thread.start();
    // Add a timeout to allow for potential interruption
    Thread.sleep(3000);
```

Görüntü dönüşüm süreci için yeni bir iş parçacığı başlatın ve kesintiyi öngörmek için bir zaman aşımı süresi tanımlayın.

### Adım 5: İşlemi Kesintiye Uğratın

`monitor.requestInterrupt()` çağrısı, izleyiciyi devam eden dönüşümü iptal etmesi için işaretler.  

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

`InterruptMonitor` kullanarak görüntü dönüşüm sürecini kesintiye uğratın ve kesintinin tamamlanmasını bekleyin. Son olarak, çıktı dosyasını silerek temizlik yapın.

## PSD‑to‑PNG Dönüştürmesi İçin Kesinti İzleyicisi Neden Kullanılmalı?

Aspose.PSD **30+ çıktı formatını** destekler; PNG, JPEG, BMP ve TIFF bunların arasındadır ve **500 MB**'a kadar dosyaları bellek içine tamamen yüklemeden işleyebilir. Bir kesinti izleyicisi ekleyerek CPU israfını azaltır ve toplu‑işleme hatlarında yanıt süresini artırırsınız, özellikle bir dönüşüm beklenen süreden uzun sürerse.

## Yaygın Sorunlar ve Çözümler

- **Dönüşüm süresiz olarak takılıyor:** `save` çağrısından **önce** izleyicinin eklendiğinden emin olun.  
- **Kesintiden sonra çıktı dosyası bozuk:** İzleyici temiz bir şekilde durur; ancak dosyanın varlığını her zaman kontrol edin.  
- **İş parçacığı güvenliği endişeleri:** Her dönüşümü kendi iş parçacığında çalıştırın; izleyici yalnızca ilişkili çalışanı etkiler.

## Sıkça Sorulan Sorular

**S1: Aspose.PSD for Java'da Kesinti İzleyicisi nedir?**  
C: Kesinti İzleyicisi, geliştiricilerin uzun süren görüntü dönüşümlerini duraklatmasına veya iptal etmesine olanak tanır, kaynak kullanımını gerçek zamanlı kontrol eder.

**S2: Aspose.PSD for Java kütüphanesini nasıl edinebilirim?**  
C: Aspose.PSD for Java kütüphanesini [buradan](https://releases.aspose.com/psd/java/) indirebilirsiniz.

**S3: Aspose.PSD for Java için ücretsiz bir deneme sürümü var mı?**  
C: Evet, Aspose.PSD'nin ücretsiz deneme sürümünü [buradan](https://releases.aspose.com/) keşfedebilirsiniz.

**S4: Aspose.PSD for Java için destek nereden alınır?**  
C: Aspose.PSD for Java destek forumunu [buradan](https://forum.aspose.com/c/psd/34) ziyaret edin.

**S5: Aspose.PSD for Java için lisans nasıl satın alınır?**  
C: Aspose.PSD for Java lisansını [buradan](https://purchase.aspose.com/buy) alabilirsiniz.

**S6: Birden fazla PSD dosyasını paralel olarak PNG'ye dönüştürebilir miyim?**  
C: Evet, her dosya için ayrı bir iş parçacığı başlatın ve her dönüşüm çalışanına ayrı bir `InterruptMonitor` ekleyin.

**S7: Kütüphane PSD‑to‑PNG dönüşümünde renk profillerini yönetiyor mu?**  
C: Kesinlikle; Aspose.PSD gömülü ICC profillerini korur ve çıktıyı PNG'ye otomatik olarak uygular.

---

**Son Güncelleme:** 2026-06-08  
**Test Edilen Sürüm:** Aspose.PSD 23.12 for Java  
**Yazar:** Aspose  

{{< blocks/products/products-backtop-button >}}

## İlgili Eğitimler

- [Save PSD as PNG and Apply Rendering Drop Shadow in Aspose.PSD for Java](/psd/java/advanced-image-manipulation/rendering-drop-shadow/)
- [Export PSD to PNG & Add a New Regular Layer using Aspose.PSD for Java](/psd/java/advanced-image-effects/add-new-regular-layer/)
- [Support for Interrupt Monitor in PSD Files - Java](/psd/java/psd-layer-management-effects/support-interrupt-monitor-psd-files/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}