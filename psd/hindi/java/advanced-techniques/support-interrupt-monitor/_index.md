---
date: 2025-12-25
description: Aspose.PSD for Java का उपयोग करके PSD को PNG में कैसे बदलें, इंटरप्ट
  मॉनिटर समर्थन के साथ, जिसमें जावा थ्रेड इंटरप्ट का उदाहरण और PSD को PNG के रूप में
  सहेजने के टिप्स शामिल हैं।
linktitle: Support for Interrupt Monitor
second_title: Aspose.PSD Java API
title: Aspose.PSD for Java में इंटरप्ट मॉनिटर समर्थन के साथ PSD को PNG में कैसे बदलें
url: /hi/java/advanced-techniques/support-interrupt-monitor/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java में Interrupt Monitor के साथ PSD को PNG में बदलें

## परिचय

यदि आपको **PSD को PNG में बदलना** है और साथ ही लंबी‑चलने वाली इमेज कन्वर्ज़न पर पूर्ण नियंत्रण रखना है, तो Aspose.PSD for Java का Interrupt Monitor वही टूल है जिसकी आपको तलाश थी। इस ट्यूटोरियल में हम एक वास्तविक **java thread interrupt example** के माध्यम से दिखाएंगे कि कैसे आप प्रक्रिया के मध्य में कन्वर्ज़न को रोक सकते हैं, जिससे आप संसाधनों का प्रबंधन, टाइम‑आउट लागू करना, या उपयोगकर्ता द्वारा रद्द करने पर प्रतिक्रिया दे सकें।

## त्वरित उत्तर
- **Interrupt Monitor क्या करता है?** यह चल रही इमेज कन्वर्ज़न को सुरक्षित रूप से रोकने का संकेत देता है।  
- **क्या मैं इसके साथ PSD को PNG में बदल सकता हूँ?** हाँ – मॉनिटर किसी भी सेव ऑपरेशन के साथ काम करता है, जिसमें PNG भी शामिल है।  
- **क्या अलग थ्रेड की आवश्यकता है?** आमतौर पर आप कन्वर्ज़न को एक अलग थ्रेड में चलाते हैं ताकि आप उसे इंटरप्ट कर सकें।  
- **कौन सा Aspose.PSD संस्करण आवश्यक है?** कोई भी नवीनतम संस्करण जो `com.aspose.psd.multithreading.InterruptMonitor` को शामिल करता है।  
- **उत्पादन के लिए लाइसेंस चाहिए?** हाँ, गैर‑ट्रायल उपयोग के लिए एक वैध Aspose.PSD लाइसेंस आवश्यक है।

## “Interrupt Monitor” के साथ “PSD को PNG में बदलना” क्या है?

बड़ी Photoshop डॉक्यूमेंट (PSD/PSB) को PNG इमेज में बदलना CPU‑गहन हो सकता है। कन्वर्ज़न वर्कर के साथ **Interrupt Monitor** जोड़ने से आप प्रोग्रामेटिक रूप से प्रक्रिया को रोक सकते हैं—वेब सर्विसेज, बैच जॉब्स, या UI एप्लिकेशन जहाँ उपयोगकर्ता ऑपरेशन रद्द कर सकते हैं, के लिए यह आदर्श है।

## Interrupt Monitor क्यों उपयोग करें?

- **रिस्पॉन्सिव UI:** बड़ी फ़ाइल प्रोसेस होते समय आपके एप्लिकेशन को फ्रीज़ होने से बचाता है।  
- **संसाधन प्रबंधन:** उन कन्वर्ज़न को रोकें जो समय या मेमोरी बजट से अधिक हो रहे हैं।  
- **त्रुटि संभालना:** इंटरप्शन होने पर आंशिक आउटपुट फ़ाइलों को सुगमता से साफ़ करें।

## पूर्वापेक्षाएँ

- जावा विकास पर्यावरण (JDK 8 या नया)।  
- Aspose.PSD for Java लाइब्रेरी – इसे **[here](https://releases.aspose.com/psd/java/)** से डाउनलोड करें।  
- एक फ़ोल्डर जिसमें वह PSD/PSB फ़ाइलें हों जिन्हें आप उपयोग करना चाहते हैं।

## पैकेज इम्पोर्ट करें

आवश्यक क्लासेस को इम्पोर्ट करके शुरू करें। इससे आपको इमेज विकल्प, इंटरप्ट मॉनिटर, और थ्रेडिंग यूटिलिटीज़ तक पहुँच मिलती है।

```java
import com.aspose.psd.ImageOptionsBase;

import static com.aspose.psd.examples.Utils.Utils.getDateTime;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.multithreading.InterruptMonitor;
import com.aspose.psd.system.Threading.ThreadStart;
import java.io.File;
```

## चरण‑दर‑चरण गाइड

### चरण 1: अपना डॉक्यूमेंट डायरेक्टरी सेट करें

```java
String dataDir = "Your Document Directory";
```

`"Your Document Directory"` को उस पूर्ण पथ से बदलें जहाँ आपके PSD फ़ाइलें स्थित हैं।

### चरण 2: इमेज विकल्प और आउटपुट पाथ निर्धारित करें

```java
ImageOptionsBase saveOptions = new PngOptions();
String source = dataDir + "big2.psb";
String output = dataDir + "big_out.png";
```

यहाँ हम `PngOptions` का उपयोग करके **PSD को PNG के रूप में सेव** करते हैं। फ़ाइल नाम आवश्यकतानुसार समायोजित करें।

### चरण 3: Interrupt Monitor और SaveImageWorker को इनिशियलाइज़ करें

```java
InterruptMonitor monitor = new InterruptMonitor();
SaveImageWorker worker = new SaveImageWorker(source, output, saveOptions, monitor);
```

`InterruptMonitor` इंस्टेंस बाद में कन्वर्ज़न को रोकने के लिए उपयोग किया जाएगा। `SaveImageWorker` मॉनिटर को कन्वर्ज़न टास्क से जोड़ता है।

### चरण 4: अलग थ्रेड में इमेज कन्वर्ज़न शुरू करें

```java
Thread thread = new Thread(worker.ThreadProc());
try {
    thread.start();
    // Add a timeout to allow for potential interruption
    Thread.sleep(3000);
```

हम बैकग्राउंड थ्रेड पर कन्वर्ज़न लॉन्च करते हैं ताकि मुख्य थ्रेड रिस्पॉन्सिव बना रहे। `Thread.sleep(3000)` कॉल एक टाइम‑आउट परिदृश्य का सिमुलेशन करता है।

### चरण 5: प्रक्रिया को इंटरप्ट करें (Java Thread Interrupt Example)

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

`monitor.interrupt()` को कॉल करने से **how to interrupt monitor** लॉजिक ट्रिगर होता है। इंटरप्शन के बाद हम किसी भी आंशिक रूप से लिखी गई PNG फ़ाइल को साफ़ कर देते हैं।

## सामान्य समस्याएँ और समाधान

| समस्या | कारण | समाधान |
|--------|------|--------|
| कन्वर्ज़न कभी नहीं रुकता | मॉनिटर वर्कर से जुड़ा नहीं है | सुनिश्चित करें कि `SaveImageWorker` को वही `InterruptMonitor` इंस्टेंस प्राप्त हो। |
| इंटरप्ट के बाद आउटपुट फ़ाइल बनी रहती है | क्लीन‑अप कोड नहीं चल रहा | जाँचें कि `finally` ब्लॉक निष्पादित हो रहा है और फ़ाइल पाथ सही है। |
| बड़े PSB फ़ाइलों पर `OutOfMemoryError` | स्ट्रीमिंग विकल्प नहीं उपयोग किए | `PsdImage` को `LoadOptions` के साथ उपयोग करें जो मेमोरी‑कुशल लोडिंग सक्षम करता है। |

## अक्सर पूछे जाने वाले प्रश्न

### Q1: Aspose.PSD for Java में Interrupt Monitor क्या है?

A1: Interrupt Monitor डेवलपर्स को **इमेज कन्वर्ज़न प्रक्रियाओं को प्रबंधित और इंटरप्ट** करने की सुविधा देता है, जिससे आप लंबी‑चलने वाले टास्क पर सूक्ष्म नियंत्रण प्राप्त कर सकते हैं।

### Q2: मैं Aspose.PSD लाइब्रेरी for Java कैसे प्राप्त करूँ?

A2: आप Aspose.PSD for Java लाइब्रेरी **[here](https://releases.aspose.com/psd/java/)** से डाउनलोड कर सकते हैं।

### Q3: क्या Aspose.PSD for Java के लिए कोई फ्री ट्रायल उपलब्ध है?

A3: हाँ, आप Aspose.PSD का फ्री ट्रायल **[here](https://releases.aspose.com/)** पर एक्सप्लोर कर सकते हैं।

### Q4: Aspose.PSD for Java के लिए सपोर्ट कहाँ मिल सकता है?

A4: Aspose.PSD for Java सपोर्ट फ़ोरम **[here](https://forum.aspose.com/c/psd/34)** पर देखें।

### Q5: Aspose.PSD for Java के लिए लाइसेंस कैसे खरीदें?

A5: आप Aspose.PSD for Java का लाइसेंस **[here](https://purchase.aspose.com/buy)** से खरीद सकते हैं।

---

**अंतिम अपडेट:** 2025-12-25  
**परीक्षित संस्करण:** Aspose.PSD 24.11 for Java  
**लेखक:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}