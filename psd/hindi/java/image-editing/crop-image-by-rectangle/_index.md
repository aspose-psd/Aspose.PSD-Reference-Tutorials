---
title: Java के लिए Aspose.PSD में Rectangle द्वारा छवि क्रॉप करें
linktitle: आयत द्वारा छवि क्रॉप करें
second_title: Aspose.PSD जावा एपीआई
description: Aspose.PSD के साथ Java में सहज छवि क्रॉपिंग क्षमताओं का अन्वेषण करें। Java के लिए Aspose.PSD का उपयोग करके छवियों को आसानी से क्रॉप करने के लिए हमारे चरण-दर-चरण मार्गदर्शिका का पालन करें।
weight: 15
url: /hi/java/image-editing/crop-image-by-rectangle/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java के लिए Aspose.PSD में Rectangle द्वारा छवि क्रॉप करें

## परिचय

जावा डेवलपमेंट की दुनिया में, इमेज में हेरफेर करना एक आम काम है, और Aspose.PSD for Java इमेज प्रोसेसिंग के लिए एक शक्तिशाली समाधान प्रदान करता है। इस ट्यूटोरियल में, हम आपको Aspose.PSD for Java का उपयोग करके आयत द्वारा इमेज को क्रॉप करने की प्रक्रिया के बारे में बताएंगे। इसे आसानी से प्राप्त करने के लिए नीचे दिए गए चरणों का पालन करें।

## आवश्यक शर्तें

ट्यूटोरियल में आगे बढ़ने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित पूर्वापेक्षाएँ मौजूद हैं:

- आपकी मशीन पर जावा डेवलपमेंट किट (JDK) स्थापित है।
- Aspose.PSD for Java लाइब्रेरी। आप इसे यहाँ से डाउनलोड कर सकते हैं[वेबसाइट](https://releases.aspose.com/psd/java/).

## पैकेज आयात करें

Aspose.PSD for Java की क्षमताओं का लाभ उठाने के लिए अपने Java प्रोजेक्ट में आवश्यक पैकेज शामिल करना सुनिश्चित करें। अपनी Java फ़ाइल की शुरुआत में निम्नलिखित आयात कथन जोड़ें:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;

import com.aspose.psd.imageoptions.JpegOptions;
```

अब, आइए इस प्रक्रिया को कई चरणों में विभाजित करें ताकि आपको Java के लिए Aspose.PSD का उपयोग करके एक आयत द्वारा एक छवि को क्रॉप करने में मार्गदर्शन मिल सके।

## चरण 1: अपनी दस्तावेज़ निर्देशिका सेट करें

```java
String dataDir = "Your Document Directory";
```

 प्रतिस्थापित करें`"Your Document Directory"` वास्तविक पथ के साथ जहां आपकी PSD फ़ाइल स्थित है।

## चरण 2: स्रोत और गंतव्य फ़ाइलें निर्दिष्ट करें

```java
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "CroppingByRectangle_out.jpg";
```

अपनी स्रोत PSD फ़ाइल और गंतव्य JPEG फ़ाइल के लिए पथ परिभाषित करें।

## चरण 3: छवि लोड करें और कैश करें

```java
RasterImage rasterImage = (RasterImage)Image.load(sourceFile);

if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

 PSD छवि को एक में लोड करें`RasterImage` इंस्टेंस और उसके डेटा कैश करें.

## चरण 4: फसल आयत बनाएं और परिभाषित करें

```java
Rectangle rectangle = new Rectangle(20, 20, 20, 20);
```

 इसका एक उदाहरण बनाएं`Rectangle` फसल के लिए वांछित आकार के साथ वर्ग।

## चरण 5: छवि को क्रॉप करें और सेव करें

```java
rasterImage.crop(rectangle);
rasterImage.save(destName, new JpegOptions());
```

निर्दिष्ट आयत का उपयोग करके क्रॉप ऑपरेशन करें और परिणामों को JPEG फ़ाइल के रूप में सहेजें।

आवश्यकतानुसार इन चरणों को दोहराएं तथा अपनी विशिष्ट आवश्यकताओं के अनुसार मापदंडों को समायोजित करें।

## निष्कर्ष

इस ट्यूटोरियल में, हमने जावा के लिए Aspose.PSD का उपयोग करके एक आयत द्वारा एक छवि को क्रॉप करने की प्रक्रिया को देखा। इन चरणों का पालन करके, आप आसानी से अपने जावा अनुप्रयोगों में शक्तिशाली छवि हेरफेर क्षमताओं को एकीकृत कर सकते हैं।

## अक्सर पूछे जाने वाले प्रश्न

### प्रश्न 1: क्या मैं अन्य Java फ्रेमवर्क के साथ Java के लिए Aspose.PSD का उपयोग कर सकता हूं?

A1: हां, Aspose.PSD for Java को विभिन्न Java फ्रेमवर्क के साथ एकीकृत किया जा सकता है, जो आपकी विकास परियोजनाओं में लचीलापन प्रदान करता है।

### प्रश्न 2: क्या Java के लिए Aspose.PSD का निःशुल्क परीक्षण उपलब्ध है?

 A2: हां, आप निःशुल्क परीक्षण संस्करण का उपयोग कर सकते हैं[यहाँ](https://releases.aspose.com/).

### प्रश्न 3: मुझे अतिरिक्त समर्थन या सहायता कहां मिल सकती है?

 A3: पर जाएँ[Aspose.PSD फ़ोरम](https://forum.aspose.com/c/psd/34) सामुदायिक समर्थन और चर्चा के लिए।

### प्रश्न 4: मैं Java के लिए Aspose.PSD हेतु अस्थायी लाइसेंस कैसे प्राप्त करूं?

 A4: आप एक अस्थायी लाइसेंस प्राप्त कर सकते हैं[यहाँ](https://purchase.aspose.com/temporary-license/).

### प्रश्न 5: Aspose.PSD for Java में क्रॉपिंग के लिए समर्थित छवि प्रारूप क्या हैं?

A5: Java के लिए Aspose.PSD विभिन्न छवि प्रारूपों का समर्थन करता है, जिसमें PSD, PNG, JPEG, और अधिक शामिल हैं।
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
