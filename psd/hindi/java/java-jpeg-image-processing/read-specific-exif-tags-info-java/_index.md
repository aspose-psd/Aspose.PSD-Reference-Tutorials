---
date: 2026-10-08
description: हमारे चरण‑दर‑चरण ट्यूटोरियल के साथ Aspose.PSD for Java (asp) का उपयोग
  करके जावा में EXIF टैग पढ़ना सीखें, और अपनी इमेज प्रोसेसिंग क्षमताओं को बढ़ाएँ।
keywords:
- read exif tags java
- java exif tag extraction
- java image metadata extraction
lastmod: 2026-10-08
linktitle: जावा में विशिष्ट EXIF टैग जानकारी पढ़ें
og_description: Aspose.PSD का उपयोग करके जावा डेवलपर्स जल्दी से इमेज मेटाडेटा निकाल
  सकते हैं। यह गाइड आपको PSD लोड करने, थंबनेल रिसोर्सेज़ खोजने, और WhiteBalance तथा
  ISO speed जैसे प्रमुख EXIF फ़ील्ड प्रिंट करने की प्रक्रिया दिखाता है।
og_image_alt: Guide showing how to read EXIF tags from PSD files in Java using Aspose.PSD
og_title: Aspose.PSD के साथ जावा में EXIF टैग कैसे पढ़ें
schemas:
- author: Aspose
  dateModified: '2026-10-08'
  description: Learn how to read EXIF tags in Java using Aspose.PSD for Java (asp)
    with our step‑by‑step tutorial, and boost your image processing capabilities.
  headline: How to read EXIF tags in Java with Aspose.PSD
  type: TechArticle
- description: Learn how to read EXIF tags in Java using Aspose.PSD for Java (asp)
    with our step‑by‑step tutorial, and boost your image processing capabilities.
  name: How to read EXIF tags in Java with Aspose.PSD
  steps:
  - name: 'Java Development Kit (JDK): Ensure you have JDK installed on your machine.
      You can download it from the [Oracle JDK website](https://www.oracle.com/java/technologies/javase-downloads.html).'
    text: 'Java Development Kit (JDK): Ensure you have JDK installed on your machine.
      You can download it from the [Oracle JDK website](https://www.oracle.com/java/technologies/javase-downloads.html).'
  - name: 'Aspose.PSD for Java: Download the library from the [Aspose.PSD for Java
      download page](https://releases.aspose.com/psd/java/).'
    text: 'Aspose.PSD for Java: Download the library from the [Aspose.PSD for Java
      download page](https://releases.aspose.com/psd/java/).'
  - name: 'Integrated Development Environment (IDE): An IDE like IntelliJ IDEA, Eclipse,
      or NetBeans will make coding more convenient.'
    text: 'Integrated Development Environment (IDE): An IDE like IntelliJ IDEA, Eclipse,
      or NetBeans will make coding more convenient.'
  - name: 'PSD file: A PSD file with EXIF data. You can use the sample provided in
      this tutorial or any other PSD file with EXIF tags.'
    text: 'PSD file: A PSD file with EXIF data. You can use the sample provided in
      this tutorial or any other PSD file with EXIF tags.'
  type: HowTo
- questions:
  - answer: Aspose.PSD (asp)
    question: What library reads EXIF data from PSD in Java?
  - answer: WhiteBalance, PixelXDimension, PixelYDimension, ISOSpeed, FocalLength,
      and more.
    question: Which tags can be extracted?
  - answer: Yes, a commercial license is required; a free trial is available.
    question: Do I need a license for production?
  - answer: The same API supports PNG, JPEG, TIFF via Java image metadata extraction.
    question: Can I use this with other image formats?
  - answer: About 10‑15 minutes for a basic read‑only scenario.
    question: How long does implementation take?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- read exif tags java
- Aspose.PSD
- java image metadata extraction
- EXIF extraction
- PSD processing
title: Aspose.PSD के साथ जावा में EXIF टैग कैसे पढ़ें
url: /hi/java/java-jpeg-image-processing/read-specific-exif-tags-info-java/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# जावा में Aspose (asp) के साथ विशिष्ट EXIF टैग जानकारी पढ़ें

## परिचय
यदि आपको **read EXIF tags in Java** की आवश्यकता है, तो Aspose.PSD (asp) एक साफ़, शुद्ध‑Java API प्रदान करता है जो Photoshop के बिना काम करता है। इस ट्यूटोरियल में आप सीखेंगे कि PSD इमेज से EXIF डेटा कैसे निकालें, केवल उन टैग्स को चुनें जिनकी आपको ज़रूरत है, और उन्हें कंसोल में प्रिंट करें। हम आपके विकास पर्यावरण को सेटअप करने से लेकर WhiteBalance, ISO speed, और focal length जैसे मेटाडेटा निकालने तक सब कुछ कवर करेंगे। चलिए शुरू करते हैं!

## त्वरित उत्तर
- **जावा में PSD से EXIF डेटा पढ़ने वाली लाइब्रेरी कौन सी है?** Aspose.PSD (asp)  
- **कौन से टैग निकाले जा सकते हैं?** WhiteBalance, PixelXDimension, PixelYDimension, ISOSpeed, FocalLength, and more.  
- **उत्पादन के लिए मुझे लाइसेंस चाहिए?** Yes, a commercial license is required; a free trial is available.  
- **क्या मैं इसे अन्य इमेज फ़ॉर्मैट्स के साथ उपयोग कर सकता हूँ?** The same API supports PNG, JPEG, TIFF via Java image metadata extraction.  
- **इम्प्लीमेंटेशन में कितना समय लगेगा?** About 10‑15 minutes for a basic read‑only scenario.

## asp (Aspose.PSD for Java) क्या है?
Aspose.PSD for Java एक शुद्ध‑Java लाइब्रेरी है जो डेवलपर्स को Adobe Photoshop फ़ाइलों (PSD, PSB) के साथ बिना Photoshop इंस्टॉल किए काम करने की सुविधा देती है। यह लेयर्स, रिसोर्सेज, और मेटाडेटा—जिसमें EXIF टैग्स शामिल हैं—तक प्रोग्रामेटिक एक्सेस प्रदान करती है, जिससे यह **java image metadata extraction** कार्यों के लिए आदर्श बनती है।

## EXIF निष्कर्षण के लिए Aspose.PSD (asp) का उपयोग क्यों करें?
आप जावा में केवल दो मेथड कॉल्स से EXIF टैग्स निकाल सकते हैं, और लाइब्रेरी 2 GB तक की फ़ाइलों को पूरी डॉक्यूमेंट को मेमोरी में लोड किए बिना प्रोसेस करती है। यह **30+ image formats** का समर्थन करती है और सटीक कैमरा सेटिंग्स को संरक्षित रखती है, जिससे आपको Windows, Linux, और macOS पर्यावरण में निर्धारक परिणाम मिलते हैं।

## पूर्वापेक्षाएँ
कोड में डुबकी लगाने से पहले, कुछ चीज़ें हैं जो आपके पास होनी चाहिए:

1. Java Development Kit (JDK): सुनिश्चित करें कि आपके मशीन पर JDK स्थापित है। आप इसे [Oracle JDK website](https://www.oracle.com/java/technologies/javase-downloads.html) से डाउनलोड कर सकते हैं।  
2. Aspose.PSD for Java: लाइब्रेरी को [Aspose.PSD for Java download page](https://releases.aspose.com/psd/java/) से डाउनलोड करें।  
3. Integrated Development Environment (IDE): IntelliJ IDEA, Eclipse, या NetBeans जैसे IDE कोडिंग को अधिक सुविधाजनक बनाते हैं।  
4. PSD file: EXIF डेटा वाला एक PSD फ़ाइल। आप इस ट्यूटोरियल में प्रदान किया गया नमूना या कोई भी अन्य EXIF टैग्स वाला PSD फ़ाइल उपयोग कर सकते हैं।

## पैकेज आयात करें
PSD फ़ाइलों के साथ काम करने के लिए आवश्यक Aspose.PSD क्लासेज जैसे Image, PsdImage, ThumbnailResource, और JpegExifData को आयात करें।  
```java
import com.aspose.psd.Image;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```

## चरण 1: PSD इमेज लोड करें
`Image.load()` एक फ़ाइल लोड करता है और इमेज डेटा का प्रतिनिधित्व करने वाला Image ऑब्जेक्ट लौटाता है।  
`PsdImage` Aspose.PSD क्लास है जो PSD‑विशिष्ट कार्यक्षमता प्रदान करती है।  
`Image.load()` मेथड किसी भी समर्थित इमेज फ़ाइल को मेमोरी में लोड करता है, एक सामान्य `Image` ऑब्जेक्ट लौटाता है जिसे आप PSD‑विशिष्ट प्रकार में कास्ट कर सकते हैं।  
```java
String dataDir = "Your Document Directory";
PsdImage image = (PsdImage) Image.load(dataDir + "1280px-Zebras_Serengeti.psd");
```

इस चरण में, हम `Image.load()` मेथड का उपयोग करके PSD फ़ाइल लोड करते हैं। `PsdImage` क्लास का उपयोग PSD इमेज को दर्शाने के लिए किया जाता है, और हम लोड की गई इमेज को इस क्लास में कास्ट करके PSD‑विशिष्ट कार्यक्षमताओं तक पहुंचते हैं।

## चरण 2: इमेज रिसोर्सेज पर इटरेट करें
`PsdImage.getResources()` थंबनेल और EXIF डेटा जैसे एम्बेडेड रिसोर्सेज का संग्रह लौटाता है।  
`PsdImage.getResources()` कॉल सभी एम्बेडेड रिसोर्सेज का संग्रह देता है। इस संग्रह पर इटरेट करके आप थंबनेल रिसोर्सेज को ढूंढ सकते हैं जिनमें EXIF मेटाडेटा होता है।  
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource || 
        image.getImageResources()[i] instanceof Thumbnail4Resource) {
        // Further processing will be done here
    }
}
```

हम `for` लूप का उपयोग करके इमेज रिसोर्सेज के माध्यम से लूप करते हैं। लक्ष्य यह पहचानना है कि कौन से रिसोर्सेज `ThumbnailResource` या `Thumbnail4Resource` के इंस्टेंस हैं, क्योंकि ये ही प्रकार EXIF डेटा रखते हैं।

## चरण 3: EXIF डेटा निकालें
`ThumbnailResource.getJpegOptions()` JPEG विकल्पों तक पहुँच प्रदान करता है जिसमें EXIF मेटाडेटा शामिल है।  
`JpegExifData` व्यक्तिगत EXIF टैग मानों को रखता है।  
`ThumbnailResource.getJpegOptions()` मेथड एक `JpegExifData` ऑब्जेक्ट तक पहुँच देता है, जो WhiteBalance, ISOSpeed, और FocalLength जैसे व्यक्तिगत EXIF टैग्स को रखता है।  
```java
if (image.getImageResources()[i] instanceof ThumbnailResource) {
    JpegExifData exif = ((ThumbnailResource) image.getImageResources()[i]).getJpegOptions().getExifData();
    if (exif != null) {
        System.out.println("Exif WhiteBalance: " + exif.getWhiteBalance());
        System.out.println("Exif PixelXDimension: " + exif.getPixelXDimension());
        System.out.println("Exif PixelYDimension: " + exif.getPixelYDimension());
        System.out.println("Exif ISOSpeed: " + exif.getISOSpeed());
        System.out.println("Exif FocalLength: " + exif.getFocalLength());
    }
}
```

हम `if` स्टेटमेंट का उपयोग करके जांचते हैं कि रिसोर्स `ThumbnailResource` का इंस्टेंस है या नहीं। यदि है, तो हम इसे कास्ट करके उसका `JpegOptions` प्राप्त करते हैं ताकि `ExifData` तक पहुँच सकें। अंत में, हम विभिन्न EXIF टैग्स जैसे WhiteBalance, Pixel Dimensions, ISOSpeed, और FocalLength को प्रिंट करते हैं।

## सामान्य समस्याएँ और सुझाव
- **Null EXIF data:** कुछ PSD फ़ाइलों में EXIF जानकारी वाला थंबनेल रिसोर्स नहीं हो सकता। टैग मानों तक पहुँचने से पहले हमेशा `null` की जाँच करें।  
- **File path errors:** पूर्ण पथ का उपयोग करें या सुनिश्चित करें कि कार्य निर्देशिका आपके PSD फ़ाइल वाले फ़ोल्डर की ओर इशारा कर रही है।  
- **License restrictions:** फ्री ट्रायल प्रोसेस की जा सकने वाली पेजों की संख्या सीमित करता है; अनलिमिटेड उपयोग के लिए पूर्ण लाइसेंस में अपग्रेड करें।

## अक्सर पूछे जाने वाले प्रश्न
### EXIF डेटा क्या है?
EXIF (Exchangeable Image File Format) डेटा इमेज फ़ाइलों में एम्बेडेड मेटाडेटा है, जिसमें कैमरा सेटिंग्स, तिथि और समय, तथा इमेज आयाम जैसी जानकारी शामिल होती है।

### क्या मैं Aspose.PSD का उपयोग करके EXIF डेटा संपादित कर सकता हूँ?
हाँ, Aspose.PSD आपको EXIF डेटा पढ़ने और संशोधित करने की अनुमति देता है। आप टैग्स को अपडेट कर सकते हैं और बदलावों को इमेज फ़ाइल में वापस सहेज सकते हैं।

### क्या Aspose.PSD for Java मुफ्त है?
Aspose.PSD एक फ्री ट्रायल संस्करण प्रदान करता है जिसे आप [Aspose.PSD official releases page](https://releases.aspose.com/) से डाउनलोड कर सकते हैं। पूर्ण सुविधाओं के लिए, आपको लाइसेंस खरीदना होगा।

### Aspose.PSD कौन से अन्य फ़ॉर्मैट्स का समर्थन करता है?
Aspose.PSD विभिन्न Adobe Photoshop फ़ॉर्मैट्स का समर्थन करता है, जिसमें PSD, PSB, और अन्य शामिल हैं। यह इन फ़ॉर्मैट्स को PNG, JPEG, TIFF आदि में बदलने के विकल्प भी प्रदान करता है।

### मैं Aspose.PSD के लिए समर्थन कैसे प्राप्त करूँ?
आप Aspose.PSD [forum](https://forum.aspose.com/c/psd/34) के माध्यम से समर्थन प्राप्त कर सकते हैं।

### यह **java image metadata extraction** में कैसे मदद करता है?
`JpegExifData` ऑब्जेक्ट का उपयोग करके, आप प्रोग्रामेटिक रूप से किसी भी आवश्यक EXIF टैग को निकाल सकते हैं, जिससे यह विभिन्न इमेज फ़ॉर्मैट्स में व्यापक मेटाडेटा निष्कर्षण कार्यों के लिए एक ठोस आधार बन जाता है।

---

**अंतिम अद्यतन:** 2026-10-08  
**परीक्षित संस्करण:** Aspose.PSD for Java 24.11 (latest at time of writing)  
**लेखक:** Aspose

## संबंधित ट्यूटोरियल

- [जावा में JPEG EXIF टैग पढ़ें और संशोधित करें](/psd/java/java-jpeg-image-processing/read-modify-jpeg-exif-tags-java/)
- [जावा JPEG इमेज प्रोसेसिंग](/psd/java/java-jpeg-image-processing/)
- [Aspose.PSD for Java के साथ विशिष्ट कोण पर इमेज घुमाने का तरीका](/psd/java/advanced-image-manipulation/rotate-image-specific-angle/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}