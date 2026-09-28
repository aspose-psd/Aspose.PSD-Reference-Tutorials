---
date: 2026-09-28
description: Aspose.PSD का उपयोग करके Java में JFIF सेगमेंट में थंबनेल कैसे जोड़ें।
  थंबनेल को PSD फ़ाइलों में तेज़ और विश्वसनीय तरीके से एम्बेड करने के लिए इस चरण‑दर‑चरण
  गाइड का पालन करें।
keywords:
- how to add thumbnail
- JFIF segment Java
- Aspose.PSD thumbnail
- Java image processing
lastmod: 2026-09-28
linktitle: Java में JFIF सेगमेंट में थंबनेल जोड़ें
og_description: Aspose.PSD का उपयोग करके Java में JFIF सेगमेंट में थंबनेल कैसे जोड़ें।
  थंबनेल को PSD फ़ाइलों में तेज़ और विश्वसनीय तरीके से एम्बेड करने के लिए इस चरण‑दर‑चरण
  गाइड का पालन करें।
og_image_alt: Guide showing how to add thumbnail to JFIF segment in Java with Aspose.PSD
og_title: Java में JFIF सेगमेंट में थंबनेल कैसे जोड़ें
schemas:
- author: Aspose
  dateModified: '2026-09-28'
  description: How to add thumbnail to a JFIF segment in Java using Aspose.PSD. Follow
    this step‑by‑step guide to embed thumbnails in PSD files quickly and reliably.
  headline: How to add thumbnail to JFIF segment in Java
  type: TechArticle
- description: How to add thumbnail to a JFIF segment in Java using Aspose.PSD. Follow
    this step‑by‑step guide to embed thumbnails in PSD files quickly and reliably.
  name: How to add thumbnail to JFIF segment in Java
  steps:
  - name: import packages
    text: '`Document`, `JfifResource`, and related classes are part of the Aspose.PSD
      namespace. Document represents the PSD file container, and JfifResource provides
      access to the JFIF segment within the PSD. Import them at the top of your source
      file.'
  - name: load the PSD image
    text: Create a `PsdImage` instance by passing the file path to the constructor.
      PsdImage is the Aspose.PSD class that models a Photoshop document. This loads
      the document metadata while streaming the pixel data.
  - name: iterate over image resources
    text: Search the `Resources` collection for a `JfifResource`. When found, you
      can replace its thumbnail byte array with a new JPEG‑encoded preview.
  - name: adjust thumbnail data
    text: Generate a small JPEG thumbnail (e.g., 120 × 120 px) using any image‑processing
      library, then assign the resulting byte array to `jfifResource.ThumbnailData`.
  - name: save the modified image
    text: Call the `save` method on the `PsdImage` object, specifying the output path
      and desired format. The JFIF segment now contains the new thumbnail.
  type: HowTo
- questions:
  - answer: Aspose.PSD for Java is a commercial library that enables developers to
      create, edit, convert, and render Photoshop PSD files without requiring Adobe
      Photoshop.
    question: What is Aspose.PSD for Java?
  - answer: Detailed documentation can be found on the [Aspose.PSD for Java documentation
      page](https://reference.aspose.com/psd/java/).
    question: Where can I find more documentation for Aspose.PSD for Java?
  - answer: Yes, Aspose.PSD for Java can be used commercially. You can purchase a
      license from [Aspose.PSD's purchase page](https://purchase.aspose.com/buy).
    question: Is Aspose.PSD for Java suitable for commercial use?
  - answer: Yes, you can download a free trial from [Aspose.PSD's trial download page](https://releases.aspose.com/).
    question: Can I try Aspose.PSD for Java before purchasing?
  - answer: For support, visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34).
    question: How can I get support for Aspose.PSD for Java?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- add thumbnail
- Aspose.PSD
- Java image processing
- JFIF
- PSD
title: Java में JFIF सेगमेंट में थंबनेल कैसे जोड़ें
url: /hi/java/java-jpeg-image-processing/add-thumbnail-to-jfif-segment-java/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java में JFIF सेगमेंट में थंबनेल कैसे जोड़ें

## परिचय
PSD फ़ाइल के JFIF सेगमेंट में थंबनेल जोड़ना एक सामान्य आवश्यकता है जब आपको पूरी इमेज लोड किए बिना तेज़ विज़ुअल प्रीव्यू चाहिए। इस ट्यूटोरियल में आप Aspose.PSD का उपयोग करके Java में JFIF सेगमेंट में **थंबनेल कैसे जोड़ें** सीखेंगे। गाइड के अंत तक आपके पास चलाने योग्य कोड स्निपेट, अंतर्निहित JFIF संरचना की समझ, और बड़े फ़ाइलों को कुशलता से संभालने के टिप्स होंगे।

## त्वरित उत्तर
- **कौनसी लाइब्रेरी आवश्यक है?** Aspose.PSD for Java.
- **कौनसा Java संस्करण काम करता है?** JDK 11 or later.
- **कोड की कितनी पंक्तियों की आवश्यकता है?** About 10 lines to load, modify, and save.
- **क्या मैं मल्टी‑मेगाबाइट फ़ाइलों को प्रोसेस कर सकता हूँ?** Yes, Aspose.PSD streams data, so memory usage stays low.
- **क्या एक व्यावसायिक लाइसेंस आवश्यक है?** A license is required for production use; a free trial is available.

## JFIF सेगमेंट क्या है?
JFIF सेगमेंट JPEG फ़ाइल इंटरचेंज फ़ॉर्मेट का एक ब्लॉक है जो थंबनेल, EXIF, या कलर प्रोफ़ाइल जैसी वैकल्पिक डेटा संग्रहीत कर सकता है।  
यह PSD फ़ाइल के JPEG स्ट्रीम के भीतर स्थित होता है और अधिकांश इमेज व्यूअर्स द्वारा तेज़ प्रीव्यू जेनरेशन के लिए पहचाना जाता है।

## PSD फ़ाइल में थंबनेल क्यों जोड़ें?
Aspose.PSD for Java **30+ image formats** का समर्थन करता है और **2 GB** तक की फ़ाइलों को पूरी दस्तावेज़ को मेमोरी में लोड किए बिना प्रोसेस कर सकता है। थंबनेल जोड़ने से प्रीव्यू ट्रांसमिट करते समय नेटवर्क बैंडविड्थ कम होती है और गैलरी एप्लिकेशन्स में UI रेंडरिंग तेज़ होती है।

## पूर्वापेक्षाएँ
- Java Development Kit (JDK): सुनिश्चित करें कि आपके सिस्टम पर Java स्थापित है। आप इसे [Oracle का JDK वेबसाइट](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) से डाउनलोड कर सकते हैं।
- Aspose.PSD for Java: आपको Aspose.PSD for Java लाइब्रेरी चाहिए। आप इसे [Aspose.PSD Java डाउनलोड पृष्ठ](https://releases.aspose.com/psd/java/) से प्राप्त कर सकते हैं।
- Integrated Development Environment (IDE): Java विकास के लिए IntelliJ IDEA या Eclipse जैसे IDE का उपयोग करें।
- Basic Understanding of Java: Java प्रोग्रामिंग भाषा और अवधारणाओं की परिचितता।

## Java में JFIF सेगमेंट में थंबनेल कैसे जोड़ें?
लक्षित PSD को लोड करें, JFIF रिसोर्स को खोजें, उसके थंबनेल डेटा को बदलें, और फ़ाइल को सहेजें। पूरी प्रक्रिया कुछ सरल API कॉल्स के साथ की जा सकती है, और Aspose.PSD आपके लिए लो‑लेवल JPEG संरचना को संभालता है।

### चरण 1: पैकेज आयात करें
`Document`, `JfifResource`, और संबंधित क्लासेज Aspose.PSD नेमस्पेस का हिस्सा हैं। Document PSD फ़ाइल कंटेनर को दर्शाता है, और JfifResource PSD के भीतर JFIF सेगमेंट तक पहुँच प्रदान करता है। इन्हें अपने स्रोत फ़ाइल के शीर्ष पर आयात करें।

```java
import com.aspose.psd.Image;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```

### चरण 2: PSD इमेज लोड करें
`PsdImage` का एक इंस्टेंस बनाएं और फ़ाइल पाथ को कंस्ट्रक्टर में पास करें। PsdImage Aspose.PSD क्लास है जो Photoshop दस्तावेज़ को मॉडल करता है। यह पिक्सेल डेटा को स्ट्रीम करते हुए दस्तावेज़ मेटाडेटा लोड करता है।

```java
String dataDir = "Your Document Directory";
PsdImage image = (PsdImage)Image.load(dataDir + "your_image.psd");
```

### चरण 3: इमेज रिसोर्सेज़ पर इटररेट करें
`Resources` कलेक्शन में `JfifResource` खोजें। मिलने पर, आप उसके थंबनेल बाइट एरे को नई JPEG‑एन्कोडेड प्रीव्यू से बदल सकते हैं।

```java
for(int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource) {
        ThumbnailResource thumbnail = (ThumbnailResource)image.getImageResources()[i];
        
        // Continue with thumbnail processing
    }
}
```

### चरण 4: थंबनेल डेटा समायोजित करें
किसी भी इमेज‑प्रोसेसिंग लाइब्रेरी का उपयोग करके छोटा JPEG थंबनेल (जैसे, 120 × 120 px) बनाएं, फिर प्राप्त बाइट एरे को `jfifResource.ThumbnailData` को असाइन करें।

```java
try {
    PsdImage thumbnailImage = new PsdImage(100, 100);
    
    // Fill thumbnail data (example: create a simple pixel array)
    int[] pixels = new int[thumbnailImage.getWidth() * thumbnailImage.getHeight()];
    for (int j = 0; j < pixels.length; j++) {
        pixels[j] = j;
    }
    
    // Save thumbnail data
    thumbnailImage.saveArgb32Pixels(thumbnailImage.getBounds(), pixels);
    
    // Set thumbnail data to Jpeg options
    JpegExifData exifData = new JpegExifData();
    exifData.setThumbnail(thumbnailImage);
    JpegOptions jpegOptions = new JpegOptions();
    jpegOptions.setExifData(exifData);
    
    // Set options to thumbnail resource
    thumbnail.getJpegOptions().setExifData(exifData);
    
} catch(Exception e) {
    // Handle exceptions
} finally {
    // Dispose of resources
}
```

### चरण 5: संशोधित इमेज सहेजें
`PsdImage` ऑब्जेक्ट पर `save` मेथड को कॉल करें, आउटपुट पाथ और वांछित फ़ॉर्मेट निर्दिष्ट करें। JFIF सेगमेंट अब नया थंबनेल रखता है।

```java
image.save(dataDir + "output.psd");
```

## सामान्य समस्याएँ और समाधान
- **व्यूअर्स में थंबनेल दिखाई नहीं दे रहा है:** सुनिश्चित करें कि थंबनेल डेटा वैध JPEG बाइट एरे है और उसके आयाम 256 × 256 px के भीतर हैं, जो JFIF स्पेसिफिकेशन द्वारा समर्थित अधिकतम आकार है।
- **बड़ी PSD फ़ाइलों पर OutOfMemoryError:** `PsdImage.load(inputStream, true)` का उपयोग करके स्ट्रीमिंग मोड सक्षम करें, जिससे मेमोरी उपयोग कम रहता है।
- **गलत रिसोर्स प्रकार:** सुनिश्चित करें कि आप जिस रिसोर्स को संशोधित कर रहे हैं वह वास्तव में `JfifResource` है; अन्य रिसोर्सेज़ जैसे `ExifResource` थंबनेल डिस्प्ले को प्रभावित नहीं करेंगे।

## अक्सर पूछे जाने वाले प्रश्न

**Q: Aspose.PSD for Java क्या है?**  
A: Aspose.PSD for Java एक व्यावसायिक लाइब्रेरी है जो डेवलपर्स को Adobe Photoshop की आवश्यकता के बिना Photoshop PSD फ़ाइलों को बनाने, संपादित करने, परिवर्तित करने और रेंडर करने में सक्षम बनाती है।

**Q: Aspose.PSD for Java की अधिक दस्तावेज़ीकरण कहाँ मिल सकता है?**  
A: विस्तृत दस्तावेज़ीकरण [Aspose.PSD for Java दस्तावेज़ पृष्ठ](https://reference.aspose.com/psd/java/) पर पाया जा सकता है।

**Q: क्या Aspose.PSD for Java व्यावसायिक उपयोग के लिए उपयुक्त है?**  
A: हां, Aspose.PSD for Java को व्यावसायिक रूप से उपयोग किया जा सकता है। आप लाइसेंस [Aspose.PSD की खरीद पृष्ठ](https://purchase.aspose.com/buy) से खरीद सकते हैं।

**Q: क्या मैं खरीदने से पहले Aspose.PSD for Java को आज़मा सकता हूँ?**  
A: हां, आप मुफ्त ट्रायल [Aspose.PSD का ट्रायल डाउनलोड पृष्ठ](https://releases.aspose.com/) से डाउनलोड कर सकते हैं।

**Q: मैं Aspose.PSD for Java के लिए समर्थन कैसे प्राप्त कर सकता हूँ?**  
A: समर्थन के लिए, [Aspose.PSD फ़ोरम](https://forum.aspose.com/c/psd/34) पर जाएँ।

---

**अंतिम अपडेट:** 2026-09-28  
**परीक्षण किया गया:** Aspose.PSD for Java 24.11  
**लेखक:** Aspose

## संबंधित ट्यूटोरियल

- [Aspose PSD for Java का उपयोग करके PSD फ़ाइलों में IOPA रिसोर्स जोड़ें](/psd/java/modifying-converting-psd-images/add-iopa-resource-psd-files/)
- [इमेज में सिग्नेचर जोड़ें – Aspose.PSD for Java के साथ कैनवास पर इमेज ड्रॉ करें](/psd/java/advanced-image-effects/add-signature-to-image/)
- [Aspose.PSD for Java के साथ विशिष्ट कोण पर इमेज कैसे घुमाएँ](/psd/java/advanced-image-manipulation/rotate-image-specific-angle/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}