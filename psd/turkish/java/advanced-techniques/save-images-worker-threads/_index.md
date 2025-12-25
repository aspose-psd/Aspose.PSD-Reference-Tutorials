---
date: 2025-12-25
description: İşçi iş parçacıklarını kullanarak PSD dosyalarını JPG olarak kaydetme
  üzerine bir Java görüntü işleme öğreticisini öğrenin. Bu rehber, görüntüleri iş
  parçacıklarıyla verimli bir şekilde kaydetmeyi gösterir.
linktitle: Save Images using Worker Threads
second_title: Aspose.PSD Java API
title: Java Görüntü İşleme Öğreticisi – İşçi İş Parçacıklarıyla Görüntüleri Kaydet
url: /tr/java/advanced-techniques/save-images-worker-threads/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java Image Processing Öğreticisi – İşçi İplikleriyle Görüntü Kaydetme

## Introduction

Bu **java image processing tutorial**'a hoş geldiniz; burada Aspose.PSD for Java'da **worker threads** kullanarak PSD dosyalarını JPG (veya diğer formatlar) olarak nasıl kaydedeceğinizi göstereceğiz. Çok‑işlemcili (multi‑threaded) görüntü işleme, özellikle büyük bir dosya topluluğunu dönüştürmeniz gerektiğinde yürütme süresini önemli ölçüde azaltabilir. Önümüzdeki birkaç dakikada, iş parçacıklarının neden önemli olduğunu, güvenli bir şekilde nasıl kurulacağını öğrenecek ve tamamen çalıştırılabilir bir kod örneği göreceksiniz.

## Quick Answers
- **What does this tutorial cover?** Aspose.PSD for Java kullanarak worker threads ile görüntü kaydetme.  
- **Why use threads?** Birden fazla görüntüyü paralel işleyerek verimliliği artırmak.  
- **Do I need a license?** Üretim ortamı için geçici bir lisans gerekir; test için ücretsiz deneme sürümü yeterlidir.  
- **Which Java version is supported?** Java 8 ve üzeri.  
- **Can I convert PSD to JPG?** Evet – öğreticide herhangi bir desteklenen formatta kaydetme gösterilmektedir.

## What is java image processing tutorial?

Bir *java image processing tutorial*, Java’da programatik olarak görüntü dosyalarını nasıl manipüle edeceğinizi, dönüştüreceğinizi ve dışa aktaracağınızı öğretir. Bu rehberde odak, yoğun I/O işini arka plan iş parçacıklarına devrederek **görüntüleri verimli bir şekilde kaydetmek** üzerinedir.

## Why use worker threads for saving images?

- **Performance:** Paralel yürütme, birden çok CPU çekirdeğini kullanarak toplam işleme süresini azaltır.  
- **Responsiveness:** Büyük dosyalar kaydedilirken ana uygulamanız yanıt vermeye devam eder.  
- **Scalability:** Yaklaşımı, toplu işlerde binlerce dosyayı işlemek için kolayca genişletebilirsiniz.

## Prerequisites

Başlamadan önce aşağıdaki ön koşulların sağlandığından emin olun:

- Java programlama temelleri.  
- Aspose.PSD for Java kütüphanesi yüklü. Kütüphaneyi [buradan](https://releases.aspose.com/psd/java/) indirebilirsiniz.  
- Java (JDK 8 veya daha yeni) yüklü bir geliştirme ortamı.

## Import Packages

Java projenizde Aspose.PSD ile çalışmak için gerekli paketleri içe aktararak başlayın:

```java
import com.aspose.psd.Image;
import com.aspose.psd.ImageOptionsBase;
import com.aspose.psd.coreexceptions.OperationInterruptedException;
import static com.aspose.psd.examples.Utils.Utils.getDateTime;
import com.aspose.psd.multithreading.InterruptMonitor;
import java.text.DateFormat;
import java.text.SimpleDateFormat;
import java.util.Date;
```

### Step 1: Initialize `SaveImageWorker`

`SaveImageWorker` adında bir sınıf oluşturun ve gerekli değişkenleri başlatın. Bu worker, tek bir kaydetme işlemi için gereken tüm verileri kapsül eder.

```java
public class SaveImageWorker {
    // ... (Refer to provided code for variable declarations)
    
    public SaveImageWorker(String inputPath, String outputPath, ImageOptionsBase saveOptions, InterruptMonitor monitor) {
        // Constructor logic
    }
    
    // ... (Refer to provided code for additional methods)
}
```

### Step 2: Define `ThreadProc` Method

`ThreadProc` metodunu uygulayarak bir görüntüyü bir formattan diğerine dönüştürün ve kesintileri (interrupt) sorunsuz bir şekilde yönetin.

```java
public String ThreadProc() {
    Image image = Image.load(this.inputPath);

    InterruptMonitor.setThreadLocalInstance(this.monitor);

    try {
        image.save(this.outputPath, this.saveOptions);
    } catch (OperationInterruptedException e) {
        System.out.println("The save thread #" + Thread.currentThread().getId() + " finishes at " + getDateTime().toString());
        System.out.println(e);
    } catch (Exception e) {
        System.out.println(e);
    } finally {
        InterruptMonitor.setThreadLocalInstance(null);
    }

    return "Hello Aspose";
}
```

### Step 3: Utilize `SaveImageWorker` in Your Application

Ana uygulamanızda bir `SaveImageWorker` örneği oluşturun ve arka plan iş parçacığında kaydetme işlemini gerçekleştirmek için `ThreadProc` metodunu çağırın.

```java
public class MainApplication {
    public static void main(String[] args) {
        // ... (Initialize inputPath, outputPath, saveOptions, and monitor)
        
        SaveImageWorker saveImageWorker = new SaveImageWorker(inputPath, outputPath, saveOptions, monitor);
        String result = saveImageWorker.ThreadProc();
        
        // ... (Handle the result as needed)
    }
}
```

## Common Issues and Solutions

| Issue | Why it Happens | How to Fix |
|-------|----------------|------------|
| **Thread hangs** | `InterruptMonitor` temizlenmemiş | `finally` bloğunda `InterruptMonitor.setThreadLocalInstance(null)` çağrıldığından emin olun. |
| **Unsupported format** | Yanlış `ImageOptionsBase` alt sınıfı kullanılmış | İstenen çıktıya uygun `JpegOptions`, `PngOptions` vb. kullanın. |
| **Out‑of‑memory** | Büyük PSD UI iş parçacığında yüklenmiş | İşlem ve kaydetme işlemlerini worker iş parçacığında yapın; çok büyük dosyalar için akış (streaming) yöntemini düşünün. |

## Frequently Asked Questions

### Q1: Is Aspose.PSD for Java suitable for multi‑threaded image processing?

A1: Yes, Aspose.PSD for Java provides built‑in support for multi‑threading, allowing you to enhance performance in image processing tasks.

### Q2: Where can I find detailed documentation for Aspose.PSD for Java?

A2: You can refer to the documentation [here](https://reference.aspose.com/psd/java/) for comprehensive information on Aspose.PSD for Java.

### Q3: How can I obtain a temporary license for Aspose.PSD for Java?

A3: You can get a temporary license [here](https://purchase.aspose.com/temporary-license/) to explore the full capabilities of Aspose.PSD for Java.

### Q4: What support options are available for Aspose.PSD for Java?

A4: For any assistance or queries, visit the [Aspose.PSD for Java forum](https://forum.aspose.com/c/psd/34) to connect with the community and experts.

### Q5: Where can I purchase Aspose.PSD for Java?

A5: To purchase Aspose.PSD for Java, visit the [purchase page](https://purchase.aspose.com/buy).

### Q6: Can I convert a PSD to JPG using this approach?

A6: Absolutely. Use `JpegOptions` as the `saveOptions` argument when calling `image.save(...)`.

### Q7: How many threads should I spawn for optimal performance?

A7: A good rule of thumb is to match the number of available CPU cores (`Runtime.getRuntime().availableProcessors()`), but always test with your workload.

## Conclusion

Artık Aspose.PSD for Java kullanarak **threads** ile **görüntü kaydetme** yöntemini gösteren bir **java image processing tutorial**'ını başarıyla tamamladınız. Kaydetme mantığını bir worker sınıfına kapsülleyip `InterruptMonitor`'ı kullanarak hem hız hem de sağlamlık elde edersiniz. Bu deseni klasörleri toplu işlemek, ilerleme raporları eklemek veya daha büyük bir görüntü‑işleme hattına entegre etmek için genişletmekten çekinmeyin.

---

**Last Updated:** 2025-12-25  
**Tested With:** Aspose.PSD for Java 24.10  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}