---
title: PSD Dosyalarında Kesinti Monitörü Desteği - Java
linktitle: PSD Dosyalarında Kesinti Monitörü Desteği - Java
second_title: Aspose.PSD Java API'si
description: Aspose.PSD'nin Interrupt Monitor'ünü kullanarak Java'da uzun süredir devam eden PSD dönüşümlerini kesintiye uğratın. Zarif kesintiyi nasıl uygulayacağınızı ve kullanıcı deneyimini nasıl geliştireceğinizi öğrenin.
weight: 24
url: /tr/java/psd-layer-management-effects/support-interrupt-monitor-psd-files/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD Dosyalarında Kesinti Monitörü Desteği - Java

## giriiş

Bu kapsamlı kılavuz, sizi Java uygulamalarınızda Interrupt Monitor'den yararlanmanız için gereken bilgilerle donatacaktır. Önkoşulları derinlemesine inceleyeceğiz, gerekli paketleri içe aktarma konusunda size yol göstereceğiz ve kod örneklerini kullanarak süreci anlaşılır, adım adım talimatlara ayıracağız. O halde kemerlerinizi bağlayın ve PSD dönüşümlerinizin kontrolünü ele almaya hazırlanın!

## Önkoşullar

Bu yolculuğa çıkmadan önce aşağıdakilere sahip olduğunuzdan emin olun:

- Java Geliştirme Kiti (JDK): Java kodunu çalıştırmak için çalışan bir JDK gereklidir. Uygun sürümü Oracle web sitesinden indirip yükleyin ([https://www.oracle.com/java/technologies/javase-downloads.html](https://www.oracle.com/java/technologies/javase-downloads.html)).
- Aspose.PSD for Java Kütüphanesi: PSD manipülasyon yeteneklerinden yararlanmak için Aspose.PSD for Java kütüphanesine ihtiyacınız olacak. Aspose web sitesinden indirebilirsiniz ([https://releases.aspose.com/psd/java/](https://releases.aspose.com/psd/java/)). Bir satın alma işlemine başlamadan önce keşif için ücretsiz deneme sürümünün mevcut olduğunu unutmayın ([https://releases.aspose.com/](https://releases.aspose.com/)).

## Gerekli Paketleri İçe Aktarma

Önkoşulları tamamladıktan sonra kodlara geçelim. İlk adım, Aspose.PSD ve kesme monitörleriyle çalışmak için gereken temel paketlerin içe aktarılmasını içerir:

```java
import com.aspose.psd.ImageOptionsBase;
import static com.aspose.psd.examples.Utils.Utils.getDateTime;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.multithreading.InterruptMonitor;
import com.aspose.psd.system.Threading.ThreadStart;
import java.io.File;
```

Artık gerekli malzemelere sahip olduğumuza göre işimize dönelim! Aspose.PSD kullanarak Java'da bir PSD dönüşümünü nasıl kesintiye uğratacağınızın adım adım dökümü aşağıda verilmiştir:

## 1. Adım: Dosya Yollarını ve Çıktı Seçeneklerini Tanımlayın

 Kaynak PSD dosyanızın yollarını ve dönüştürülen görüntü için istediğiniz hedefi ayarlayarak başlayın. Ayrıca, bir örneğini oluşturun`ImageOptionsBase`çıktı formatını (örneğin, PNG, JPEG) ve istenen kalite ayarlarını belirtmek için:

```java
String sourcePath = "your_source_psd_file.psd";
String outputPath = "converted_image.png";

ImageOptionsBase saveOptions = new PngOptions();
// SaveOptions'ı istediğiniz formata göre daha da özelleştirebilirsiniz (örneğin, JPEG kalitesinin ayarlanması)
```

## Adım 2: Kesinti Monitörü ve Çalışan İş Parçacığı Oluşturun

 Daha sonra, şunun bir örneğini oluşturacağız:`InterruptMonitor` Dönüşüm sürecini izlemek için. Ek olarak, asıl dönüştürme görevini gerçekleştirecek bir çalışan iş parçacığı oluşturacağız:

```java
InterruptMonitor monitor = new InterruptMonitor();
SaveImageWorker worker = new SaveImageWorker(sourcePath, outputPath, saveOptions, monitor);
Thread thread = new Thread(worker);
```

 Burada,`SaveImageWorker` class, görüntü dönüştürme işleminin gerçekleştirilmesinden sorumlu arka plan iş parçacığını temsil eder. Bu sınıf genellikle PSD dosyasını yükleme, dönüştürme işlemini gerçekleştirme ve çıktı görüntüsünü kaydetme mantığını kapsar. (Basitlik açısından, gerçek uygulama`SaveImageWorker` burada gösterilmemiştir ancak ayrı bir sınıf olarak tanımlanabilir).

## 3. Adım: Dönüştürmeyi Başlatın ve Zaman Aşımını Ayarlayın

Her şey ayarlandıktan sonra, çalışan iş parçacığını başlatarak dönüştürme sürecini başlatalım:

```java
thread.start();
```

Şimdi, potansiyel olarak uzun süren bir dönüşümü kesintiye uğratma özelliğini eklemek için bir zaman aşımı mekanizması tanıtacağız. Bu, dönüştürme çok uzun sürerse programın süresiz olarak takılmamasını sağlar. Kullanmak`Thread.sleep(timeout)` uygun bir zaman aşımı süresi belirlemek için (milisaniye cinsinden):

```java
Thread.sleep(300
```

## Adım 4: Dönüşümü Durdurun

 Belirtilen zaman aşımından sonra, işçi iş parçacığına aşağıdaki komutu kullanarak bir kesme sinyali göndereceğiz:`InterruptMonitor`:

```java
// Dönüştürme sürecini kesintiye uğratın
monitor.interrupt();
System.out.println("Interrupting the save thread #" + thread.getId() + " at " + getDateTime().toString());
```

 Bu sinyal, dönüşüm sürecini zarif bir şekilde kesintiye uğratacaktır.`SaveImageWorker` sınıf.

## Adım 5: Konu Tamamlanmasını ve Temizlenmesini Bekleyin

 Dönüştürme işleminin tamamen durdurulduğundan emin olmak için şunu kullanacağız:`thread.join()`:

```java
thread.join();
```

Son olarak, işlem sırasında oluşturulan geçici dosyaları temizlemek iyi bir uygulamadır:

```java
File outputFile = new File(outputPath);
if (outputFile.exists()) {
    outputFile.delete();
}
```

## Çözüm

 Bu adımları izleyerek ve gerekli mantığı uygulamanıza dahil ederek`SaveImageWorker`sınıfında, Aspose.PSD'nin Interrupt Monitor'ünü kullanarak Java uygulamalarınızda uzun süredir devam eden PSD dönüşümlerini etkili bir şekilde kesebilirsiniz. Bu özellik, kullanıcılarınıza daha duyarlı ve kullanıcı dostu bir deneyim sunmanıza olanak tanır.

 Unutmayın,`SaveImageWorker` Sınıf bu sürecin temel taşıdır. Kesintileri zarif ve verimli bir şekilde ele alan sağlam bir uygulama oluşturmaya zaman ayırın. 

## SSS'ler

### Aspose.PSD ile her türlü görüntü dönüştürmeyi kesebilir miyim?

Örnek PSD'den PNG'ye dönüştürmeye odaklanırken Interrupt Monitor, desteklenen diğer görüntü formatlarıyla da kullanılabilir. Temel prensip aynı kalır.

###  Nasıl`InterruptMonitor` work internally?

`InterruptMonitor` esas olarak çalışan iş parçacığına bir kesinti sinyali vermek için bir mekanizma sağlar. Java'nın iş parçacığı kesinti mekanizması kullanılarak uygulanır.

###  Eğer kesintiyi halledemezsem ne olur?`SaveImageWorker` class?

 Eğer`SaveImageWorker`Kesintileri açıkça kontrol etmezse, dönüştürme süreci süresiz olarak devam edebilir ve potansiyel olarak kaynakların tükenmesine veya uygulamaların yanıt vermemesine yol açabilir.

### Zaman aşımı süresini özelleştirebilir miyim?

 Kesinlikle! Zaman aşımı değerini şuradan ayarlayabilirsiniz:`Thread.sleep()` özel gereksinimlerinize uyacak şekilde arayın.

### Interrupt Monitor'ü kullanmanın herhangi bir performans etkisi var mı?

 Kesinti Monitörü'nü kullanmanın performans yükü genellikle minimum düzeydedir. Ancak, kesinti kontrollerinin sıklığı`SaveImageWorker` performansı etkileyebilir. Hızlı yanıt verme ve verimlilik arasında bir denge kurmak önemlidir.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
