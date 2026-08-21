---
date: 2026-06-08
description: Aspose.PSD for Java का उपयोग करके PSD को PNG के रूप में कैसे सहेजें और
  आवश्यक होने पर रूपांतरण को रोकें, सीखें। इमेज वर्कफ़्लो को प्रभावी ढंग से प्रबंधित
  करें।
keywords:
- save psd as png
- how to interrupt conversion
- psd to png conversion
- manage image workflow
linktitle: Interrupt Monitor के लिए समर्थन
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
title: Aspose.PSD for Java में Interrupt Monitor के साथ PSD को PNG के रूप में कैसे
  सहेजें
url: /hi/java/advanced-techniques/support-interrupt-monitor/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java में Interrupt Monitor के साथ PSD को PNG के रूप में सहेजें

## परिचय

यदि आपको **save PSD as PNG** करते समय लंबी‑चलने वाली रूपांतरणों पर पूर्ण नियंत्रण रखना है, तो Aspose.PSD for Java का Interrupt Monitor बिल्कुल वही प्रदान करता है। इस ट्यूटोरियल में हम मॉनिटर सेटअप करने, PSD फ़ाइल को PNG में बदलने, और आवश्यकता पड़ने पर ऑपरेशन को सुरक्षित रूप से रोकने की प्रक्रिया को देखेंगे। आप यह भी समझेंगे कि यह सामान्य इमेज‑प्रोसेसिंग वर्कफ़्लो में कैसे फिट बैठता है और मजबूत अनुप्रयोगों के लिए यह क्यों आवश्यक है।

## त्वरित उत्तर
- **क्या मैं PSD‑to‑PNG रूपांतरण को बाधित कर सकता हूँ?** हाँ, प्रक्रिया को आवश्यकता अनुसार रोकने के लिए `InterruptMonitor` का उपयोग करें।  
- **कौन सा मेथड PSD को PNG के रूप में सहेजता है?** `save(outputPath, new PngOptions())` को कॉल करें।  
- **क्या उत्पादन के लिए लाइसेंस चाहिए?** एक व्यावसायिक लाइसेंस आवश्यक है; एक मुफ्त ट्रायल उपलब्ध है।  
- **कौन सा Java संस्करण समर्थित है?** Java 8 और उसके बाद के संस्करण पूरी तरह समर्थित हैं।  
- **क्या लाइब्रेरी थ्रेड‑सेफ़ है?** रूपांतरण अलग-अलग थ्रेड्स में चल सकते हैं; मॉनिटर बाधाओं को सुरक्षित रूप से संभालता है।

## पूर्वापेक्षाएँ

Interrupt Monitor के उपयोग की जटिलताओं में जाने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित पूर्वापेक्षाएँ मौजूद हैं:

- **Java Development Environment:** अपने सिस्टम पर Java विकास वातावरण सेट करें।  
- **Aspose.PSD Library:** Aspose.PSD for Java लाइब्रेरी प्राप्त करें। आप इसे [here](https://releases.aspose.com/psd/java/) से डाउनलोड कर सकते हैं। आप मुख्य Aspose साइट भी [here](https://releases.aspose.com/) पर देख सकते हैं।  
- **Document Directory:** अपने PSD दस्तावेज़ों के लिए एक निर्दिष्ट डायरेक्टरी रखें।

## पैकेज आयात करें

अपने Java प्रोजेक्ट में आवश्यक पैकेज आयात करके शुरू करें। यह सुनिश्चित करता है कि आपको Aspose.PSD कार्यक्षमताओं तक पहुंच प्राप्त हो।

```java
import com.aspose.psd.ImageOptionsBase;

import static com.aspose.psd.examples.Utils.Utils.getDateTime;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.multithreading.InterruptMonitor;
import com.aspose.psd.system.Threading.ThreadStart;
import java.io.File;
```

अब, हम उदाहरण कोड को चरण‑दर‑चरण गाइड में विभाजित करेंगे ताकि आप अपने Aspose.PSD for Java प्रोजेक्ट में Interrupt Monitor को सम्मिलित कर सकें।

## Interrupt Monitor का उपयोग करके PSD को PNG के रूप में कैसे सहेजें?

`PsdImage` मेमोरी में लोड की गई PSD दस्तावेज़ को दर्शाता है।  
`SaveImageWorker` अलग थ्रेड में इमेज रूपांतरण करता है।  

`new PsdImage("source.psd")` से अपनी PSD फ़ाइल लोड करें, `SaveImageWorker` को एक `InterruptMonitor` संलग्न करें, और `save("output.png", new PngOptions())` को कॉल करें। मॉनिटर रद्द करने के अनुरोध को देखता है और रूपांतरण को साफ़-सुथरे ढंग से रोक देता है, जिससे मिलिसेकंड में आपके एप्लिकेशन को नियंत्रण वापस मिल जाता है।

### चरण 1: अपनी Document Directory सेट करें

```java
String dataDir = "Your Document Directory";
```

सुनिश्चित करें कि “Your Document Directory” को उस वास्तविक पथ से बदलें जहाँ आपके PSD दस्तावेज़ संग्रहीत हैं।

### चरण 2: इमेज विकल्प और आउटपुट पाथ निर्धारित करें

```java
ImageOptionsBase saveOptions = new PngOptions();
String source = dataDir + "big2.psb";
String output = dataDir + "big_out.png";
```

इमेज विकल्प, स्रोत PSD फ़ाइल, और परिवर्तित इमेज के इच्छित आउटपुट पाथ को निर्दिष्ट करें।

### चरण 3: Interrupt Monitor और SaveImageWorker को इनिशियलाइज़ करें

`InterruptMonitor` क्लास चल रहे रूपांतरण को देखती है और जब `requestInterrupt()` कॉल किया जाता है तो उसे बाधित कर सकती है।  

```java
InterruptMonitor monitor = new InterruptMonitor();
SaveImageWorker worker = new SaveImageWorker(source, output, saveOptions, monitor);
```

`InterruptMonitor` और `SaveImageWorker` के इंस्टेंस बनाएं, मॉनिटर को इमेज रूपांतरण वर्कर से लिंक करें।

### चरण 4: इमेज रूपांतरण थ्रेड शुरू करें

```java
Thread thread = new Thread(worker.ThreadProc());
try {
    thread.start();
    // Add a timeout to allow for potential interruption
    Thread.sleep(3000);
```

इमेज रूपांतरण प्रक्रिया के लिए एक नया थ्रेड शुरू करें और बाधा की संभावना को ध्यान में रखते हुए एक टाइमआउट अवधि निर्धारित करें।

### चरण 5: प्रक्रिया को बाधित करें

`monitor.requestInterrupt()` को कॉल करने से मॉनिटर को चल रहे रूपांतरण को रोकने का संकेत मिलता है।  

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

`InterruptMonitor` का उपयोग करके इमेज रूपांतरण प्रक्रिया को बाधित करें और बाधा के पूर्ण होने की प्रतीक्षा करें। अंत में, आउटपुट फ़ाइल को हटाकर साफ़-सफ़ाई करें।

## PSD‑to‑PNG रूपांतरण के लिए Interrupt Monitor का उपयोग क्यों करें?

Aspose.PSD **30+ आउटपुट फ़ॉर्मैट** को सपोर्ट करता है, जिसमें PNG, JPEG, BMP, और TIFF शामिल हैं, और **500 MB** तक की फ़ाइलों को पूरी दस्तावेज़ को मेमोरी में लोड किए बिना प्रोसेस कर सकता है। एक Interrupt Monitor जोड़ने से आप CPU की बर्बादी कम करते हैं और बैच‑प्रोसेसिंग पाइपलाइन में प्रतिक्रिया क्षमता बढ़ाते हैं, विशेष रूप से जब रूपांतरण अपेक्षित समय सीमा से अधिक हो जाता है।

## सामान्य समस्याएँ और समाधान

- **Conversion hangs indefinitely:** सुनिश्चित करें कि मॉनिटर `save` को कॉल करने **से पहले** संलग्न हो।  
- **Output file is corrupted after interruption:** मॉनिटर साफ़-सुथरे ढंग से रोकता है; फिर भी, उपयोग करने से पहले हमेशा जाँचें कि फ़ाइल मौजूद है या नहीं।  
- **Thread‑safety concerns:** प्रत्येक रूपांतरण को अपने अलग थ्रेड में चलाएँ; मॉनिटर केवल अपने संबंधित वर्कर को प्रभावित करता है।

## अक्सर पूछे जाने वाले प्रश्न

**Q1: Aspose.PSD for Java में Interrupt Monitor क्या है?**  
A: Interrupt Monitor डेवलपर्स को लंबी‑चलने वाली इमेज रूपांतरणों को रोकने या रद्द करने की सुविधा देता है, जिससे संसाधन उपयोग पर वास्तविक‑समय नियंत्रण मिलता है।

**Q2: मैं Aspose.PSD लाइब्रेरी for Java कैसे प्राप्त कर सकता हूँ?**  
A: आप Aspose.PSD for Java लाइब्रेरी को [here](https://releases.aspose.com/psd/java/) से डाउनलोड कर सकते हैं।

**Q3: क्या Aspose.PSD for Java के लिए मुफ्त ट्रायल उपलब्ध है?**  
A: हाँ, आप Aspose.PSD का मुफ्त ट्रायल [here](https://releases.aspose.com/) पर देख सकते हैं।

**Q4: मैं Aspose.PSD for Java के लिए समर्थन कहाँ पा सकता हूँ?**  
A: Aspose.PSD for Java समर्थन फ़ोरम को [here](https://forum.aspose.com/c/psd/34) पर देखें।

**Q5: मैं Aspose.PSD for Java के लिए लाइसेंस कैसे खरीद सकता हूँ?**  
A: आप Aspose.PSD for Java का लाइसेंस [here](https://purchase.aspose.com/buy) से खरीद सकते हैं।

**Q6: क्या मैं कई PSD फ़ाइलों को समानांतर में PNG में बदल सकता हूँ?**  
A: हाँ, प्रत्येक फ़ाइल के लिए एक अलग थ्रेड बनाएं और प्रत्येक रूपांतरण वर्कर को एक व्यक्तिगत `InterruptMonitor` संलग्न करें।

**Q7: क्या लाइब्रेरी PSD‑to‑PNG रूपांतरण के दौरान कलर प्रोफ़ाइल को संभालती है?**  
A: बिल्कुल; Aspose.PSD एम्बेडेड ICC प्रोफ़ाइल को संरक्षित रखता है और उन्हें आउटपुट PNG पर स्वचालित रूप से लागू करता है।

---

**अंतिम अपडेट:** 2026-06-08  
**परीक्षित संस्करण:** Aspose.PSD 23.12 for Java  
**लेखक:** Aspose  

{{< blocks/products/products-backtop-button >}}

## संबंधित ट्यूटोरियल

- [Aspose.PSD for Java में PSD को PNG के रूप में सहेजें और रेंडरिंग ड्रॉप शैडो लागू करें](/psd/java/advanced-image-manipulation/rendering-drop-shadow/)
- [Aspose.PSD for Java का उपयोग करके PSD को PNG में निर्यात करें और एक नया नियमित लेयर जोड़ें](/psd/java/advanced-image-effects/add-new-regular-layer/)
- [PSD फ़ाइलों में Interrupt Monitor का समर्थन - Java](/psd/java/psd-layer-management-effects/support-interrupt-monitor-psd-files/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}