---
date: 2025-12-25
description: Aspose.PSD for Java kullanarak, kesinti izleyici desteğiyle PSD'yi PNG'ye
  dönüştürmeyi, bir Java iş parçacığı kesinti örneği ve PSD'yi PNG olarak kaydetme
  ipuçlarını öğrenin.
linktitle: Support for Interrupt Monitor
second_title: Aspose.PSD Java API
title: Aspose.PSD for Java'da Kesinti İzleyici Desteğiyle PSD'yi PNG'ye Nasıl Dönüştürülür
url: /tr/java/advanced-techniques/support-interrupt-monitor/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java’da Interrupt Monitor ile PSD’yi PNG’ye Dönüştürme

## Giriş

Uzun süren görüntü dönüşümlerini tam kontrol altında tutarken **PSD’yi PNG’ye dönüştürmeniz** gerekiyorsa, Aspose.PSD for Java’nın Interrupt Monitor’ı aradığınız araçtır. Bu öğreticide, dönüşümü süreç ortasında durdurmanıza olanak tanıyan gerçek bir **java thread interrupt örneği** üzerinden adım adım ilerleyeceğiz; bu sayede kaynakları yönetme, zaman aşımını uygulama veya kullanıcı iptallerine yanıt verme esnekliğine sahip olacaksınız.

## Hızlı Yanıtlar
- **Interrupt Monitor ne işe yarar?** Devam eden bir görüntü dönüşümünü güvenli bir şekilde durdurmanızı sağlar.  
- **Bununla PSD’yi PNG’ye dönüştürebilir miyim?** Evet – monitor, PNG dahil herhangi bir kaydetme işlemiyle çalışır.  
- **Ayrı bir iş parçacığı gerekli mi?** Genellikle dönüşümü, kesebileceğiniz bir ayrı iş parçacığında çalıştırırsınız.  
- **Hangi Aspose.PSD sürümü gerekiyor?** `com.aspose.psd.multithreading.InterruptMonitor` sınıfını içeren herhangi bir yeni sürüm.  
- **Üretim için lisansa ihtiyacım var mı?** Evet, deneme dışı kullanım için geçerli bir Aspose.PSD lisansı gereklidir.

## Interrupt Monitor ile “PSD’yi PNG’ye dönüştürmek” nedir?

Büyük bir Photoshop belgesini (PSD/PSB) PNG görüntüsüne dönüştürmek CPU‑yoğun olabilir. Dönüşüm çalışanına bir **Interrupt Monitor** ekleyerek, işlemi programatik olarak durdurma yeteneği kazanırsınız—web servisleri, toplu işler veya kullanıcıların işlemleri iptal edebileceği UI uygulamaları için mükemmeldir.

## Neden Interrupt Monitor kullanmalı?

- **Duyarlı UI:** Büyük bir dosya işlenirken uygulamanızın donmasını önler.  
- **Kaynak Yönetimi:** Zaman veya bellek bütçesini aşan dönüşümleri durdurur.  
- **Hata Yönetimi:** Kesinti gerçekleştiğinde kısmi çıktı dosyalarını zarif bir şekilde temizler.

## Ön Koşullar

- Java Geliştirme Ortamı (JDK 8 veya daha yeni).  
- Aspose.PSD for Java kütüphanesi – **[buradan](https://releases.aspose.com/psd/java/)** indirin.  
- Üzerinde çalışmak istediğiniz PSD/PSB dosyalarını içeren bir klasör.

## Paketleri İçe Aktarma

Start by importing the required classes. This gives you access to image options, the interrupt monitor, and threading utilities.

```java
import com.aspose.psd.ImageOptionsBase;

import static com.aspose.psd.examples.Utils.Utils.getDateTime;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.multithreading.InterruptMonitor;
import com.aspose.psd.system.Threading.ThreadStart;
import java.io.File;
```

## Adım Adım Kılavuz

### Adım 1: Belge Dizinini Ayarlayın

```java
String dataDir = "Your Document Directory";
```

`"Your Document Directory"` ifadesini PSD dosyalarınızın bulunduğu mutlak yol ile değiştirin.

### Adım 2: Görüntü Seçeneklerini ve Çıktı Yolunu Tanımlayın

```java
ImageOptionsBase saveOptions = new PngOptions();
String source = dataDir + "big2.psb";
String output = dataDir + "big_out.png";
```

Burada `PngOptions` kullanarak **PSD’yi PNG olarak kaydediyoruz**. Dosya adlarını ihtiyacınıza göre ayarlayın.

### Adım 3: Interrupt Monitor ve SaveImageWorker’ı Başlatın

```java
InterruptMonitor monitor = new InterruptMonitor();
SaveImageWorker worker = new SaveImageWorker(source, output, saveOptions, monitor);
```

`InterruptMonitor` örneği daha sonra dönüşümü durdurmak için kullanılacak. `SaveImageWorker` monitor’ü dönüşüm görevine bağlar.

### Adım 4: Görüntü Dönüşümünü Ayrı Bir İş Parçacığında Başlatın

```java
Thread thread = new Thread(worker.ThreadProc());
try {
    thread.start();
    // Add a timeout to allow for potential interruption
    Thread.sleep(3000);
```

Dönüşümü arka plan iş parçacığında başlatıyoruz, böylece ana iş parçacığı yanıt vermeye devam eder. `Thread.sleep(3000)` çağrısı bir zaman aşımı senaryosunu taklit eder.

### Adım 5: İşlemi Kesintiye Uğratın (Java Thread Interrupt Örneği)

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

`monitor.interrupt()` çağrısı **monitor’ü nasıl kesintiye uğratılır** mantığını tetikler. Kesintiden sonra kısmen yazılmış olabilecek PNG dosyasını temizliyoruz.

## Yaygın Sorunlar ve Çözümleri

| Sorun | Sebep | Çözüm |
|-------|--------|-----|
| Dönüşüm hiç durmuyor | Monitor işçiye bağlanmamış | `SaveImageWorker` aynı `InterruptMonitor` örneğini almalı. |
| Kesintiden sonra çıktı dosyası kalıyor | Temizleme kodu çalıştırılmadı | `finally` bloğunun çalıştığını ve dosya yolunun doğru olduğunu doğrulayın. |
| `OutOfMemoryError` büyük PSB dosyalarında | Akış seçenekleri kullanılmıyor | Bellek‑verimli yüklemeyi etkinleştiren `LoadOptions` ile `PsdImage` kullanın. |

## Sıkça Sorulan Sorular

### S1: Aspose.PSD for Java’da Interrupt Monitor nedir?

Interrupt Monitor, geliştiricilerin **görüntü dönüşüm süreçlerini yönetip kesintiye uğratmalarını** sağlar; uzun süren görevler üzerinde ayrıntılı kontrol sunar.

### S2: Aspose.PSD for Java kütüphanesini nasıl edinebilirim?

Aspose.PSD for Java kütüphanesini **[buradan](https://releases.aspose.com/psd/java/)** indirebilirsiniz.

### S3: Aspose.PSD for Java için ücretsiz deneme mevcut mu?

Evet, Aspose.PSD’nin ücretsiz denemesini **[buradan](https://releases.aspose.com/)** inceleyebilirsiniz.

### S4: Aspose.PSD for Java desteğini nerede bulabilirim?

Aspose.PSD for Java destek forumunu **[buradan](https://forum.aspose.com/c/psd/34)** ziyaret edin.

### S5: Aspose.PSD for Java için lisans nasıl satın alabilirim?

Aspose.PSD for Java için lisansı **[buradan](https://purchase.aspose.com/buy)** satın alabilirsiniz.

---

**Son Güncelleme:** 2025-12-25  
**Test Edilen Versiyon:** Aspose.PSD 24.11 for Java  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}