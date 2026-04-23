---
date: 2026-03-07
description: Aspose.PSD for Java का उपयोग करके PSD फ़ाइलों में लेवल एडजस्टमेंट लेयर
  जोड़कर लेवल कैसे समायोजित करें, सीखें। टोनल ट्यूनिंग को जल्दी से मास्टर करें।
linktitle: Add Level Adjustment Layer in PSD
second_title: Aspose.PSD Java API
title: लेवल को कैसे समायोजित करें – PSD में लेवल एडजस्टमेंट लेयर जोड़ें
url: /hi/java/modifying-converting-psd-images/add-level-adjustment-layer-psd/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD में लेवल एडजस्टमेंट लेयर जोड़ें

## Introduction
यदि आप अपने Photoshop दस्तावेज़ों में **लेवल कैसे समायोजित करें** ढूँढ रहे हैं, तो Level Adjustment Layer एक आदर्श टूल है। यह आपको शैडोज़, मिड‑टोन और हाइलाइट्स को मूल पिक्सेल को स्थायी रूप से बदले बिना बारीकी से ट्यून करने देता है। इस ट्यूटोरियल में हम Aspose.PSD for Java का उपयोग करके PSD फ़ाइल में Level Adjustment Layer जोड़ने की प्रक्रिया दिखाएंगे, जिससे आप कुछ ही चरणों में प्रोफ़ेशनल‑ग्रेड टोनल कंट्रोल प्राप्त कर सकते हैं।

## Quick Answers
- **Level Adjustment Layer क्या करता है?** यह एक छवि की टोनल रेंज को नॉन‑डिस्ट्रक्टिवली संशोधित करता है।  
- **कौनसी लाइब्रेरी उपयोग की जाती है?** Aspose.PSD for Java.  
- **क्या मुझे लाइसेंस चाहिए?** विकास के लिए एक फ्री ट्रायल काम करता है; प्रोडक्शन के लिए लाइसेंस आवश्यक है।  
- **इम्प्लीमेंटेशन में कितना समय लगता है?** बेसिक एडजस्टमेंट के लिए लगभग 10‑15 मिनट।  
- **क्या मैं कई चैनलों को समायोजित कर सकता हूँ?** हाँ, आप प्रत्येक कलर चैनल के लिए इनपुट/आउटपुट लेवल अलग‑अलग सेट कर सकते हैं।

## What is a Level Adjustment Layer?
Level Adjustment Layer आपको एक छवि की टोनल बैलेंस को इनपुट शैडोज़, मिड‑टोन और हाइलाइट्स के साथ-साथ आउटपुट लेवल को समायोजित करके सुधारने देता है। क्योंकि यह अपनी स्वयं की लेयर पर रहता है, आप इसकी विजिबिलिटी टॉगल कर सकते हैं या इसे डिलीट कर सकते हैं बिना नीचे की आर्टवर्क को प्रभावित किए।

## Why add a Level Adjustment Layer with Aspose.PSD?
- **ऑटोमेशन:** लेवल ट्यून को बैच प्रोसेसिंग पाइपलाइन में इंटीग्रेट करें।  
- **क्रॉस‑प्लेटफ़ॉर्म:** किसी भी OS पर काम करता है जो Java को सपोर्ट करता है।  
- **प्रिसीजन:** प्रत्येक चैनल की सेटिंग्स को प्रोग्रामेटिकली एक्सेस करके सटीक परिणाम प्राप्त करें।  

## Prerequisites
1. Java Development Kit (JDK)। यदि आपके पास नहीं है, तो इसे [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) से डाउनलोड करें या OpenJDK उपयोग करें।  
2. Aspose.PSD for Java लाइब्रेरी – नवीनतम JAR इस [download link](https://releases.aspose.com/psd/java/) से प्राप्त करें।  
3. Java प्रोग्रामिंग का बुनियादी ज्ञान।  
4. IntelliJ IDEA, Eclipse, या NetBeans जैसे IDE जिसमें Aspose.PSD JAR प्रोजेक्ट के क्लासपाथ में जोड़ा गया हो।  

## Import Packages
कोड लिखना शुरू करने से पहले, हमें Aspose.PSD लाइब्रेरी से आवश्यक पैकेज इम्पोर्ट करने की जरूरत है। इसे आप इस प्रकार कर सकते हैं:
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.LevelsLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.LevelChannel;
```
These imports give us access to classes for loading PSD files, working with level adjustment layers, and manipulating individual channel settings.

## How to Adjust Levels in a PSD File
नीचे एक चरण‑दर‑चरण गाइड है जो आपको प्रोग्रामेटिकली **लेवल कैसे समायोजित करें** दिखाता है।

### Step 1: Set Up Your File Paths
परिभाषित करें कि स्रोत PSD कहाँ स्थित है और संपादित फ़ाइल कहाँ सहेजी जाएगी।
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "LevelsAdjustmentLayer.psd";
String psdPathAfterChange = dataDir + "LevelsAdjustmentLayerChanged.psd";
```
`"Your Document Directory"` को अपने मशीन पर वास्तविक फ़ोल्डर से बदलें।

### Step 2: Load the PSD File
स्रोत फ़ाइल से एक `PsdImage` इंस्टेंस बनाएं।
```java
PsdImage im = (PsdImage) Image.load(sourceFileName);
```
अब आपके पास PSD के भीतर सभी लेयर्स तक पूरी पहुँच है।

### Step 3: Iterate Through the Layers
उस Level Adjustment Layer को खोजें जिसे आप संशोधित करना चाहते हैं।
```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof LevelsLayer) {
        LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
        // Further manipulation will go here...
    }
}
```
`instanceof LevelsLayer` जांच यह सुनिश्चित करती है कि हम केवल लेवल एडजस्टमेंट लेयर्स के साथ काम करें।

### Step 4: Adjust the Level Channel Settings
चयनित चैनल के इनपुट और आउटपुट मानों को ट्यून करें।
```java
LevelChannel channel = levelsLayer.getChannel(0);
channel.setInputMidtoneLevel(2.0f);
channel.setInputShadowLevel((short) 10);
channel.setInputHighlightLevel((short) 230);
channel.setOutputShadowLevel((short) 20);
channel.setOutputHighlightLevel((short) 200);
```
- **Input Midtone Level:** मिड‑टोन रेंज को शिफ्ट करता है।  
- **Input Shadow Level:** शैडोज़ को डार्क या लाइट करता है।  
- **Input Highlight Level:** सबसे उज्ज्वल भागों को नियंत्रित करता है।  
- **Output Shadow/Highlight Levels:** अंतिम आउटपुट रेंज को परिभाषित करता है।

विभिन्न मानों के साथ प्रयोग करने में संकोच न करें ताकि आप देख सकें कि वे छवि को कैसे प्रभावित करते हैं।

### Step 5: Save the Modified PSD File
अपने बदलावों को एक नई फ़ाइल में सहेजें।
```java
im.save(psdPathAfterChange);
```
आपको अपडेटेड PSD उस स्थान पर मिलेगा जो आपने `psdPathAfterChange` में निर्दिष्ट किया था।

## Common Issues and Solutions
- **File not found:** सुनिश्चित करें कि `dataDir` सही फ़ोल्डर की ओर इशारा कर रहा है और स्रोत PSD मौजूद है।  
- **ClassCastException:** सुनिश्चित करें कि आप जो फ़ाइल लोड कर रहे हैं वह वास्तव में PSD है; अन्य फॉर्मेट्स के लिए अलग क्लासेज़ की आवश्यकता होती है।  
- **License errors:** प्रोडक्शन बिल्ड्स के लिए वैध Aspose.PSD लाइसेंस उपयोग करें; विकास के लिए ट्रायल काम करता है।

## Conclusion
अब आप जानते हैं **लेवल कैसे समायोजित करें** Aspose.PSD for Java के साथ PSD फ़ाइल में Level Adjustment Layer जोड़कर और कॉन्फ़िगर करके। यह तकनीक आपको टोनल बैलेंस पर सटीक नियंत्रण देती है जबकि आपका वर्कफ़्लो पूरी तरह ऑटोमेटेड रहता है। विभिन्न चैनल मानों के साथ प्रयोग करते रहें और बैच प्रोसेसिंग का अन्वेषण करें ताकि समान एडजस्टमेंट कई छवियों पर लागू कर सकें।

## Frequently Asked Questions

**Q: Level Adjustment Layer क्या है?**  
A: यह एक नॉन‑डिस्ट्रक्टिव लेयर है जो आपको छवि की टोनल रेंज (शैडोज़, मिड‑टोन, हाइलाइट्स) को संशोधित करने देता है।

**Q: क्या मैं Aspose.PSD को लाइसेंस खरीदे बिना उपयोग कर सकता हूँ?**  
A: हाँ, आप लाइब्रेरी को फ्री ट्रायल के साथ इवैल्यूएट कर सकते हैं, लेकिन व्यावसायिक डिप्लॉयमेंट के लिए लाइसेंस आवश्यक है।

**Q: Aspose.PSD की डॉक्यूमेंटेशन कहाँ मिल सकती है?**  
A: आप डॉक्यूमेंटेशन [here](https://reference.aspose.com/psd/java/) पर पा सकते हैं।

**Q: क्या Aspose उत्पादों के लिए कम्युनिटी सपोर्ट है?**  
A: बिल्कुल! आप प्रश्न पूछ सकते हैं और मदद प्राप्त कर सकते हैं [Aspose forum](https://forum.aspose.com/c/psd/34) में।

**Q: Aspose.PSD के लिए टेम्पररी लाइसेंस कैसे प्राप्त करूँ?**  
A: आप टेम्पररी लाइसेंस के लिए [here](https://purchase.aspose.com/temporary-license/) पर आवेदन कर सकते हैं।

---

**अंतिम अपडेट:** 2026-03-07  
**परीक्षण किया गया:** Aspose.PSD नवीनतम संस्करण (Java)  
**लेखक:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}