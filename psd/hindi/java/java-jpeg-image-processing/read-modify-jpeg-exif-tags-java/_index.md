---
date: 2026-01-25
description: इस चरण-दर-चरण गाइड में सीखें कि Aspose.PSD for Java का उपयोग करके EXIF
  डेटा कैसे निकाला जाए और JPEG EXIF टैग्स को कैसे संशोधित किया जाए। इमेज मेटाडेटा
  संभालने वाले डेवलपर्स के लिए एकदम उपयुक्त।
linktitle: Read and Modify JPEG EXIF Tags in Java
second_title: Aspose.PSD Java API
title: जावा में EXIF डेटा निकालने और JPEG टैग्स को संशोधित करने का तरीका
url: /hi/java/java-jpeg-image-processing/read-modify-jpeg-exif-tags-java/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java में EXIF डेटा निकालें और JPEG टैग संशोधित करें

## Introduction
नमस्ते! क्या आपने कभी सोचा है कि आप **EXIF डेटा** कैसे निकाल सकते हैं और Java का उपयोग करके JPEG EXIF टैग को कैसे संशोधित कर सकते हैं? यदि हाँ, तो आप सही जगह पर हैं! यह ट्यूटोरियल आपको Aspose.PSD for Java का उपयोग करके प्रक्रिया को चरण‑दर‑चरण समझाएगा। चाहे आप एक अनुभवी डेवलपर हों या अभी शुरुआत कर रहे हों, इस गाइड के अंत तक आप EXIF जानकारी को पढ़ना, बदलना और सहेजना प्रो की तरह कर पाएँगे। चलिए शुरू करते हैं!

## Quick Answers
- **Java में EXIF को संभालने वाली लाइब्रेरी कौन सी है?** Aspose.PSD for Java  
- **क्या मैं कैमरा मालिक का नाम बदल सकता हूँ?** हाँ, `setCameraOwnerName` का उपयोग करके  
- **क्या थंबनेल EXIF उपलब्ध है?** हाँ, थंबनेल रिसोर्स के माध्यम से  
- **क्या उत्पादन के लिए लाइसेंस चाहिए?** एक वैध Aspose लाइसेंस आवश्यक है  
- **इम्प्लीमेंटेशन में कितना समय लगता है?** बेसिक टास्क के लिए आमतौर पर 15 मिनट से कम  

## Prerequisites
Before we start, make sure you have the following:
1. Java Development Kit (JDK): सुनिश्चित करें कि आपके सिस्टम पर JDK स्थापित है। आप इसे [Oracle वेबसाइट](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) से डाउनलोड कर सकते हैं।
2. Aspose.PSD for Java Library: आपको Aspose.PSD for Java लाइब्रेरी डाउनलोड करनी होगी। इसे आप [Aspose रिलीज़ पेज](https://releases.aspose.com/psd/java/) से प्राप्त कर सकते हैं।
3. Integrated Development Environment (IDE): IntelliJ IDEA या Eclipse जैसे IDE से आपका कोडिंग अनुभव सुगम होगा।
4. Basic Java Knowledge: इस ट्यूटोरियल को समझने के लिए Java की बुनियादी समझ आवश्यक है।

## What is EXIF Data?
EXIF (Exchangeable Image File Format) डेटा JPEG छवियों में एम्बेडेड मेटाडेटा है जो कैमरा सेटिंग्स, ओरिएंटेशन और टाइमस्टैम्प जैसी जानकारी संग्रहीत करता है। EXIF डेटा निकालने से आप प्रोग्रामेटिक रूप से इन विवरणों का विश्लेषण या संशोधन कर सकते हैं।

## Why Extract EXIF Data in Java?
- Aspose.PSD के साथ **Java इमेज मेटाडेटा** हैंडलिंग आसान हो जाती है।  
- आप **एपर्चर वैल्यू** बदल सकते हैं, **EXIF ओरिएंटेशन** अपडेट कर सकते हैं, या **थंबनेल EXIF** को बदल सकते हैं बिना इमेज पिक्सल को छुए।  
- मेटाडेटा समायोजन को ऑटोमेट करना फोटो‑मैनेजमेंट ऐप्स, डिजिटल एसेट पाइपलाइन और कंप्लायंस वर्कफ़्लो के लिए आवश्यक है।

## Import Packages
सबसे पहले, आवश्यक पैकेज इम्पोर्ट करें। अपना Java IDE खोलें और एक नया Java प्रोजेक्ट बनाएं। फिर, अपने प्रोजेक्ट की डिपेंडेंसीज़ में Aspose.PSD for Java लाइब्रेरी शामिल करें।

```java
import com.aspose.psd.Image;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```

## Step 1: Load the PSD Image
### चरण 1: PSD इमेज लोड करें
इस चरण में, हम वह PSD इमेज लोड करेंगे जिससे हम EXIF डेटा पढ़ना चाहते हैं। सुनिश्चित करें कि आपकी इमेज सही डायरेक्टरी में है।

```java
String dataDir = "Your Document Directory";
PsdImage image = null;
try {
    image = (PsdImage) Image.load(dataDir + "1280px-Zebras_Serengeti.psd");
} catch (IOException e) {
    e.printStackTrace();
}
```

## Step 2: Iterate Over Image Resources
### चरण 2: इमेज रिसोर्सेज़ पर इटरेट करें
इमेज लोड हो जाने के बाद, अगला चरण इसका रिसोर्सेज़ पर इटरेट करना है ताकि थंबनेल रिसोर्स पाया जा सके, जिसमें आमतौर पर EXIF डेटा होता है।

```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource) {
        ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
        // Proceed to next step
    }
}
```

## Step 3: Extract EXIF Data
### चरण 3: EXIF डेटा निकालें
अब जब हमारे पास थंबनेल रिसोर्स है, हम उससे EXIF डेटा निकाल सकते हैं। EXIF डेटा में कैमरा मालिक का नाम, एपर्चर वैल्यू, ओरिएंटेशन आदि जैसी मूल्यवान जानकारी शामिल होती है।

```java
JpegExifData exifData = thumbnail.getJpegOptions().getExifData();
if (exifData != null) {
    System.out.println("Camera Owner Name: " + exifData.getCameraOwnerName());
    System.out.println("Aperture Value: " + exifData.getApertureValue());
    System.out.println("Orientation: " + exifData.getOrientation());
    System.out.println("Focal Length: " + exifData.getFocalLength());
    System.out.println("Compression: " + exifData.getCompression());
}
```

## Step 4: Modify EXIF Data
### चरण 4: EXIF डेटा संशोधित करें
EXIF डेटा पढ़ने के बाद, आप **एपर्चर वैल्यू** बदलना या अन्य फ़ील्ड्स अपडेट करना चाह सकते हैं। इसे करने का तरीका यहाँ दिया गया है:

```java
if (exifData != null) {
    exifData.setCameraOwnerName("New Camera Owner");
    exifData.setApertureValue(3.5);
    exifData.setOrientation(1);
    exifData.setFocalLength(35.0);
    exifData.setCompression(6);
    thumbnail.getJpegOptions().setExifData(exifData);
}
```

## Step 5: Save the Changes
### चरण 5: बदलाव सहेजें
अंत में, EXIF डेटा संशोधित करने के बाद, बदलावों को एक नई PSD फ़ाइल में सहेजें।

```java
try {
    image.save(dataDir + "Modified_Zebras_Serengeti.psd");
} catch (IOException e) {
    e.printStackTrace();
}
```

## Common Issues and Solutions
| Issue | Solution |
|-------|----------|
| `thumbnail` is `null` | सुनिश्चित करें कि PSD वास्तव में थंबनेल रिसोर्स रखता है; कुछ इमेजेज़ EXIF को सीधे मुख्य इमेज में स्टोर करती हैं। |
| `ExifData` returns `null` | जाँचें कि थंबनेल पर JPEG विकल्प मौजूद हैं; सभी थंबनेल में EXIF नहीं होता। |
| Permission errors on `save` | जाँचें कि लक्ष्य डायरेक्टरी लिखने योग्य है और आपके पास पर्याप्त फ़ाइल सिस्टम परमिशन हैं। |

## Frequently Asked Questions

**Q: EXIF डेटा क्या है?**  
A: EXIF (Exchangeable Image File Format) डेटा इमेज के बारे में मेटाडेटा रखता है, जैसे कैमरा सेटिंग्स और ओरिएंटेशन।

**Q: क्या मैं Aspose.PSD for Java को मुफ्त में उपयोग कर सकता हूँ?**  
A: आप [Aspose रिलीज़ पेज](https://releases.aspose.com/) से एक फ्री ट्रायल प्राप्त कर सकते हैं।

**Q: क्या Aspose.PSD for Java सभी Java संस्करणों के साथ संगत है?**  
A: Aspose.PSD for Java Java SE 7 और उसके ऊपर के संस्करणों को सपोर्ट करता है।

**Q: Aspose.PSD for Java पर [डॉक्यूमेंटेशन](https://reference.aspose.com/psd/java/) देखें।

**Q: Aspose.PSD for Java के लिए सपोर्ट कैसे प्राप्त करें?**  
A: आप [Aspose PSD सपोर्ट फ़ोरम](https://forum.aspose.com/c/psd/34) से सपोर्ट ले सकते हैं।

**Q: क्या मैं पूरी इमेज लोड किए बिना थंबनेल EXIF निकाल सकता हूँ?**  
A: हाँ, केवल थंबनेल रिसोर्सेज़ पर इटरेट करके आप पूरे PSD पिक्सल डेटा को प्रोसेस किए बिना EXIF डेटा तक पहुँच सकते हैं।

**Q: Java में EXIF ओरिएंटेशन कैसे बदलें?**  
A: `exifData.setOrientation(value)` का उपयोग करें जहाँ `value` EXIF ओरिएंटेशन स्टैंडर्ड (1‑8) के अनुसार हो।

## Conclusion
और लीजिए! इन चरणों का पालन करके आप आसानी से **EXIF डेटा निकाल सकते हैं**, JPEG EXIF टैग संशोधित कर सकते हैं, और Aspose.PSD for Java का उपयोग करके अपडेटेड इमेज को सहेज सकते हैं। यह शक्तिशाली लाइब्रेरी इमेज मेटाडेटा को संभालना बहुत आसान बनाती है, चाहे आप फोटो‑मैनेजमेंट टूल बना रहे हों या बैच अपडेट को ऑटोमेट कर रहे हों। इसे अपने अगले प्रोजेक्ट में आज़माएँ और देखें कि आप कितना समय बचाते हैं।

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**अंतिम अपडेट:** 2026-01-25  
**परीक्षण किया गया:** Aspose.PSD for Java 24.12 (latest)  
**लेखक:** Aspose  

---