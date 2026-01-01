---
date: 2026-01-01
description: Aspose.PSD for Java के साथ इमेज को क्रॉप करना सीखकर जावा इमेज प्रोसेसिंग
  में महारत हासिल करें। सहज इमेज मैनिपुलेशन के लिए एक व्यापक ट्यूटोरियल।
linktitle: Crop Image by Shifts
second_title: Aspose.PSD Java API
title: जावा इमेज प्रोसेसिंग – शिफ्ट्स द्वारा इमेज क्रॉप करना Aspose.PSD के साथ
url: /hi/java/image-editing/crop-image-by-shifts/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java इमेज प्रोसेसिंग – शिफ्ट्स द्वारा इमेज क्रॉप करना Aspose.PSD के साथ

## परिचय

यदि आप **java image processing** पर काम कर रहे हैं, तो आप जल्दी ही पाएँगे कि सटीक क्रॉपिंग किसी भी ग्राफ़िक्स वर्कफ़्लो की बुनियादी इमारत है। चाहे आपको बॉर्डर ट्रिम करने हों, अनचाहे बैकग्राउंड को हटाना हो, या वेब डिलीवरी के लिए एसेट तैयार करने हों, प्रोग्रामेटिक रूप से **how to crop image** जानना अनगिनत मैन्युअल घंटों की बचत करता है। इस ट्यूटोरियल में हम प्रत्येक साइड के शिफ्ट वैल्यूज़ निर्दिष्ट करके रास्टर इमेज को क्रॉप करने की प्रक्रिया को **Aspose.PSD for Java** लाइब्रेरी की मदद से दिखाएँगे। अंत तक आप **use the crop method** को आत्मविश्वास से उपयोग कर पाएँगे और बेहतर प्रदर्शन के लिए **optimize image cropping** भी कर सकेंगे।

## त्वरित उत्तर
- **java इमेज प्रोसेसिंग को कौन सी लाइब्रेरी संभालती है?** Aspose.PSD for Java  
- **कौन सा मेथड रास्टर इमेज को क्रॉप करता है?** `RasterImage.crop(left, right, top, bottom)`  
- **क्या मुझे पहले डेटा कैश करना चाहिए?** हाँ – कैशिंग बड़े PSD फ़ाइलों के लिए गति बढ़ाती है  
- **क्या मैं कस्टम क्रॉपिंग मार्जिन सेट कर सकता हूँ?** बिल्कुल – बाएँ, दाएँ, ऊपर और नीचे के शिफ्ट निर्दिष्ट करें  
- **कौन से आउटपुट फ़ॉर्मेट समर्थित हैं?** JPEG, PNG, BMP, और `ImageOptions` के माध्यम से कई और फ़ॉर्मेट

## Java इमेज प्रोसेसिंग क्या है?
Java इमेज प्रोसेसिंग का अर्थ है जावा‑आधारित API का उपयोग करके बिटमैप और वेक्टर ग्राफ़िक्स को बदलना। कार्यों में री‑साइज़िंग, फ़िल्टरिंग, फ़ॉर्मेट कन्वर्ज़न, और **image cropping margins** समायोजन शामिल हैं—इन सभी को सर्वर‑साइड या डेस्कटॉप एप्लिकेशन में स्वचालित किया जा सकता है।

## Java इमेज प्रोसेसिंग के लिए Aspose.PSD क्यों उपयोग करें?
Aspose.PSD एक शुद्ध‑जावा समाधान प्रदान करता है जो Photoshop‑संगत PSD फ़ाइलें, लेयर्स, चैनल और मास्क को समझता है। यह नेटिव लाइब्रेरी की आवश्यकता को समाप्त करता है, क्रॉस‑प्लेटफ़ॉर्म काम करता है, और एक सहज **crop raster image** API देता है जो मौजूदा जावा प्रोजेक्ट्स में आसानी से एकीकृत हो जाता है।

## पूर्वापेक्षाएँ

- **Java Development Kit (JDK)** – नवीनतम संस्करण [यहाँ](https://www.oracle.com/java/technologies/javase-downloads.html) से डाउनलोड करें।  
- **Aspose.PSD for Java Library** – नवीनतम रिलीज़ [डाउनलोड पेज](https://releases.aspose.com/psd/java/) से प्राप्त करें।  
- **Integrated Development Environment (IDE)** – Eclipse, IntelliJ IDEA, या आपका पसंदीदा कोई भी एडिटर।

## पैकेज इम्पोर्ट करें

अपने जावा प्रोजेक्ट में आवश्यक क्लासेज़ को इम्पोर्ट करें ताकि क्रॉपिंग वर्कफ़्लो शुरू किया जा सके:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imageoptions.JpegOptions;
```

## चरण‑दर‑चरण गाइड

### चरण 1: इमेज लोड करें (how to crop image)

सबसे पहले, स्रोत PSD फ़ाइल को `RasterImage` इंस्टेंस में लोड करें। यह आपको पिक्सेल‑लेवल एक्सेस देता है।

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
RasterImage rasterImage = (RasterImage)Image.load(sourceFile);
```

### चरण 2: इमेज डेटा कैश करें (optimize image cropping)

इमेज डेटा को मेमोरी में कैश करने से कई ऑपरेशन्स (जैसे क्रॉपिंग) करते समय I/O ओवरहेड कम हो जाता है।

```java
if (!rasterImage.isCached()) {
  rasterImage.cacheData();
}
```

### चरण 3: क्रॉपिंग मार्जिन परिभाषित करें (image cropping margins)

प्रत्येक साइड से आप कितने पिक्सेल ट्रिम करना चाहते हैं, यह निर्दिष्ट करें। इन वैल्यूज़ को अपने इच्छित **image cropping margins** के अनुसार समायोजित करें।

```java
int leftShift = 10;
int rightShift = 10;
int topShift = 10;
int bottomShift = 10;
```

### चरण 4: क्रॉप लागू करें (use crop method)

अब शिफ्ट वैल्यूज़ के साथ `crop` मेथड को कॉल करें। यह **crop raster image** ऑपरेशन अंतर्निहित बिटमैप को संशोधित करता है।

```java
rasterImage.crop(leftShift, rightShift, topShift, bottomShift);
```

### चरण 5: परिणाम सहेजें (how to crop image to a new format)

अंत में, क्रॉप की गई इमेज को डिस्क पर लिखें। इस उदाहरण में हम JPEG चुनते हैं, लेकिन Aspose.PSD द्वारा समर्थित कोई भी फ़ॉर्मेट उपयोग किया जा सकता है।

```java
String destName = dataDir + "CroppingByShifts_out.jpg";
rasterImage.save(destName, new JpegOptions());
```

बधाई हो! आपने Aspose.PSD for Java का उपयोग करके **shifts द्वारा इमेज को क्रॉप** करने की प्रक्रिया सफलतापूर्वक पूरी कर ली है, जो किसी भी **java image processing** टूलकिट में एक मुख्य कौशल है।

## सामान्य समस्याएँ और समाधान

| समस्या | समाधान |
|-------|----------|
| **`OutOfMemoryError` on large PSD files** | सुनिश्चित करें कि आप `cacheData()` (चरण 2) कॉल कर रहे हैं और JVM हीप साइज (`-Xmx`) बढ़ाने पर विचार करें। |
| **Unexpected transparent borders** | जाँचें कि आपके शिफ्ट वैल्यूज़ इच्छित मार्जिन को सही ढंग से दर्शाते हैं; नकारात्मक वैल्यूज़ ट्रिम करने के बजाय विस्तार कर सकती हैं। |
| **Saving in the wrong format** | `save` कॉल करते समय उपयुक्त `ImageOptions` सबक्लास (जैसे `PngOptions`) का उपयोग करें। |

## अक्सर पूछे जाने वाले प्रश्न

**Q: क्या Aspose.PSD सभी इमेज फ़ॉर्मेट के साथ संगत है?**  
A: हाँ, Aspose.PSD रास्टर और वेक्टर दोनों प्रकार के कई फ़ॉर्मेट को सपोर्ट करता है, जिससे आपके प्रोजेक्ट्स में बहुमुखी प्रतिभा आती है।

**Q: क्या मैं एक ही इमेज पर कई क्रॉपिंग ऑपरेशन लागू कर सकता हूँ?**  
A: बिल्कुल। आप `crop` को बार‑बार कॉल कर सकते हैं; प्रत्येक कॉल वर्तमान इमेज स्थिति पर कार्य करती है।

**Q: क्या Aspose.PSD सपोर्ट के लिए कोई कम्युनिटी फ़ोरम है?**  
A: हाँ, आप [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34) पर सपोर्ट पा सकते हैं और समुदाय के साथ जुड़ सकते हैं।

**Q: मैं Aspose.PSD के लिए अस्थायी लाइसेंस कैसे प्राप्त करूँ?**  
A: अस्थायी लाइसेंस प्राप्त करने के लिए [यहाँ](https://purchase.aspose.com/temporary-license/) जाएँ।

**Q: क्या Aspose.PSD की कार्यक्षमताओं को दर्शाने वाले कोई सैंपल प्रोजेक्ट्स हैं?**  
A: दस्तावेज़ीकरण और उदाहरणों के लिए [Aspose.PSD Java Documentation](https://reference.aspose.com/psd/java/) देखें।

## निष्कर्ष

इस गाइड में हमने शिफ्ट वैल्यूज़ निर्दिष्ट करके **crop raster image** फ़ाइलों को क्रॉप करने की पूरी प्रक्रिया को कवर किया, जो सटीक **java image processing** के लिए आवश्यक तकनीक है। अब आपके पास बड़े वर्कफ़्लो में क्रॉपिंग को एकीकृत करने की ठोस नींव है, चाहे आप वेब के लिए एसेट तैयार कर रहे हों, थंबनेल बना रहे हों, या स्कैन किए हुए दस्तावेज़ों को साफ़ कर रहे हों।

---

**अंतिम अपडेट:** 2026-01-01  
**परीक्षण किया गया:** Aspose.PSD 24.11 for Java  
**लेखक:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}