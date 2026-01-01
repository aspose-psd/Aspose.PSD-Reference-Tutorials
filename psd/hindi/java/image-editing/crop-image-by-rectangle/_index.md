---
date: 2026-01-01
description: Aspose.PSD for Java का उपयोग करके जावा में इमेज को कैसे क्रॉप करें, जानें।
  हमारे चरण‑दर‑चरण गाइड का पालन करके PSD फ़ाइल लोड करें, इमेज रेक्टेंगल को क्रॉप करें,
  और PSD को JPEG में बदलें।
linktitle: Crop Image by Rectangle
second_title: Aspose.PSD Java API
title: 'क्रॉप इमेज जावा: Aspose.PSD के साथ आयत द्वारा इमेज क्रॉप करें'
url: /hi/java/image-editing/crop-image-by-rectangle/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Crop Image Java: Crop Image by Rectangle with Aspose.PSD

## Introduction

ग्राफ़िक्स को मैनीपुलेट करना **java image processing** का एक नियमित हिस्सा है, और Aspose.PSD for Java आपको PSD फ़ाइलों के साथ काम करने के लिए एक साफ़, हाई‑परफ़ॉर्मेंस API प्रदान करता है। इस ट्यूटोरियल में आप सीखेंगे **कैसे इमेज को एक रेक्टैंगल से क्रॉप करें**, एक PSD फ़ाइल लोड करें, और अंत में परिणाम को JPEG में कनवर्ट करें—सिर्फ कुछ ही लाइनों के Java कोड के साथ।

## Quick Answers
- **“crop image java” का क्या मतलब है?** यह Java कोड का उपयोग करके एक परिभाषित रेक्टैंगल में इमेज को ट्रिम करने को दर्शाता है।  
- **कौन सी लाइब्रेरी यह ऑपरेशन संभालती है?** Aspose.PSD for Java आवश्यक क्लासेज़ प्रदान करती है।  
- **क्या परीक्षण के लिए लाइसेंस चाहिए?** एक फ्री ट्रायल उपलब्ध है; प्रोडक्शन के लिए लाइसेंस आवश्यक है।  
- **क्या मैं क्रॉप किए गए PSD को JPEG में कनवर्ट कर सकता हूँ?** हाँ—सेव करते समय `JpegOptions` का उपयोग करें।  
- **इम्प्लीमेंटेशन में कितना समय लगेगा?** आमतौर पर बेसिक सीनारियो के लिए 10 मिनट से कम।

## What is cropping an image rectangle in Java?

इमेज रेक्टैंगल को क्रॉप करना मतलब है एक विशिष्ट एरिया (X, Y, width, और height द्वारा परिभाषित) को चुनना और उस एरिया के बाहर की सभी सामग्री को हटा देना। यह ऑपरेशन तब सामान्य होता है जब आपको बड़े PSD डॉक्यूमेंट के किसी विशेष हिस्से पर फोकस करना हो।

## Why use Aspose.PSD for this task?

- **कोई बाहरी डिपेंडेंसी नहीं** – शुद्ध Java के साथ काम करता है।  
- **PSD, PNG, JPEG, और कई अन्य फॉर्मैट्स को सपोर्ट करता है** – आप **PSD को तुरंत JPEG में कनवर्ट** कर सकते हैं।  
- **हाई‑फिडेलिटी रेंडरिंग** – क्रॉप के दौरान लेयर जानकारी और कलर प्रोफ़ाइल को बरकरार रखता है।  

## Prerequisites

- Java Development Kit (JDK) इंस्टॉल हो।  
- Aspose.PSD for Java लाइब्रेरी – इसे [website](https://releases.aspose.com/psd/java/) से डाउनलोड करें।  

## Import Packages

अपने Java प्रोजेक्ट में Aspose.PSD for Java की क्षमताओं को उपयोग करने के लिए आवश्यक पैकेजेज़ को शामिल करना सुनिश्चित करें। अपने Java फ़ाइल की शुरुआत में नीचे दिए गए इम्पोर्ट स्टेटमेंट्स जोड़ें:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;

import com.aspose.psd.imageoptions.JpegOptions;
```

अब, हम प्रक्रिया को कई चरणों में विभाजित करेंगे ताकि आप Aspose.PSD for Java का उपयोग करके रेक्टैंगल द्वारा इमेज को क्रॉप करने के बारे में मार्गदर्शन पा सकें।

## Step 1: Set up Your Document Directory

```java
String dataDir = "Your Document Directory";
```

`"Your Document Directory"` को उस वास्तविक पाथ से बदलें जहाँ आपकी PSD फ़ाइल स्थित है।

## Step 2: Specify Source and Destination Files

```java
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "CroppingByRectangle_out.jpg";
```

अपने स्रोत PSD फ़ाइल और गंतव्य JPEG फ़ाइल के पाथ को परिभाषित करें।

## Step 3: Load and Cache the Image

```java
RasterImage rasterImage = (RasterImage)Image.load(sourceFile);

if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

यहाँ हम **PSD फ़ाइल को** `RasterImage` इंस्टेंस में लोड करते हैं और प्रदर्शन सुधारने के लिए उसकी डेटा को कैश करते हैं।

## Step 4: Create and Define the Crop Rectangle

```java
Rectangle rectangle = new Rectangle(20, 20, 20, 20);
```

`Rectangle` क्लास का एक इंस्टेंस बनाएँ जिसमें आप क्रॉप के लिए इच्छित आकार दें। पैरामीटर्स क्रमशः **X**, **Y**, **width**, और **height** दर्शाते हैं।

## Step 5: Crop and Save the Image

```java
rasterImage.crop(rectangle);
rasterImage.save(destName, new JpegOptions());
```

निर्दिष्ट रेक्टैंगल का उपयोग करके क्रॉप ऑपरेशन करें और `JpegOptions` के साथ परिणाम को सेव करके **PSD को JPEG में कनवर्ट** करें।

इन चरणों को आवश्यकता अनुसार दोहराएँ, अपने विशिष्ट आवश्यकताओं के अनुसार पैरामीटर्स को समायोजित करें।

## Common Issues & Tips

- **Rectangle outside image bounds** – रेक्टैंगल के कोऑर्डिनेट्स को स्रोत इमेज के डायमेंशन के भीतर रखें।  
- **Memory consumption** – काम समाप्त होने पर `rasterImage.dispose()` कॉल करके नेटिव रिसोर्सेज़ को फ्री करें।  
- **Quality control** – आउटपुट JPEG की कम्प्रेशन लेवल को नियंत्रित करने के लिए `JpegOptions.setQuality(int)` सेट कर सकते हैं।

## Conclusion

इस ट्यूटोरियल में हमने **crop image java** को रेक्टैंगल द्वारा Aspose.PSD for Java का उपयोग करके कैसे किया, यह दिखाया। इन चरणों का पालन करके आप किसी भी Java एप्लिकेशन में शक्तिशाली इमेज मैनीपुलेशन क्षमताएँ—PSD फ़ाइल लोड करना, एक विशिष्ट क्षेत्र को क्रॉप करना, और परिणाम को JPEG में कनवर्ट करना—आसानी से इंटीग्रेट कर सकते हैं।

## FAQ's

### Q1: Can I use Aspose.PSD for Java with other Java frameworks?

A1: Yes, Aspose.PSD for Java can be integrated with various Java frameworks, providing flexibility in your development projects.

### Q2: Is there a free trial available for Aspose.PSD for Java?

A2: Yes, you can access the free trial version [here](https://releases.aspose.com/).

### Q3: Where can I find additional support or assistance?

A3: Visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) for community support and discussions.

### Q4: How do I obtain a temporary license for Aspose.PSD for Java?

A4: You can acquire a temporary license [here](https://purchase.aspose.com/temporary-license/).

### Q5: What are the supported image formats for cropping in Aspose.PSD for Java?

A5: Aspose.PSD for Java supports various image formats, including PSD, PNG, JPEG, and more.

---

**Last Updated:** 2026-01-01  
**Tested With:** Aspose.PSD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}