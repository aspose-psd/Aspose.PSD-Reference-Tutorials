---
title: Java के लिए Aspose.PSD में एक छवि घुमाएँ
linktitle: छवि घुमाएँ
second_title: Aspose.PSD जावा एपीआई
description: Aspose.PSD के साथ Java में इमेज रोटेशन को आसानी से एक्सप्लोर करें। PSD फ़ाइलों को आसानी से घुमाएँ, फ़्लिप करें और सेव करें।
weight: 19
url: /hi/java/advanced-image-manipulation/rotate-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java के लिए Aspose.PSD में एक छवि घुमाएँ

## परिचय

Aspose.PSD for Java छवियों के साथ काम करने के लिए सुविधाओं का एक शक्तिशाली सेट प्रदान करता है, जिससे डेवलपर्स PSD फ़ाइलों को कुशलतापूर्वक हेरफेर और संसाधित कर सकते हैं। इस ट्यूटोरियल में, हम एक विशिष्ट कार्य पर ध्यान केंद्रित करेंगे: एक छवि को घुमाना। चाहे आप एक फोटो संपादन एप्लिकेशन बना रहे हों या बस किसी छवि के अभिविन्यास को समायोजित करने की आवश्यकता हो, Aspose.PSD प्रक्रिया को सरल बनाता है।

## आवश्यक शर्तें

ट्यूटोरियल में शामिल होने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित पूर्वापेक्षाएँ मौजूद हैं:

-  Aspose.PSD for Java लाइब्रेरी: सुनिश्चित करें कि आपने Aspose.PSD for Java लाइब्रेरी डाउनलोड और इंस्टॉल कर ली है। आप लाइब्रेरी और विस्तृत दस्तावेज़ पा सकते हैं[यहाँ](https://reference.aspose.com/psd/java/).

- जावा विकास वातावरण: सुनिश्चित करें कि आपके मशीन पर जावा विकास वातावरण स्थापित है।

-  नमूना PSD फ़ाइल: एक नमूना PSD फ़ाइल तैयार करें जिसे आप घुमाना चाहते हैं।`sourceFile` उदाहरण कोड में अपने PSD फ़ाइल के पथ के साथ चर जोड़ें।

## पैकेज आयात करें

Aspose.PSD की क्षमताओं का लाभ उठाने के लिए आवश्यक पैकेजों को आयात करके प्रारंभ करें:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RotateFlipType;

import com.aspose.psd.imageoptions.JpegOptions;
```

## चरण 1: छवि लोड करें

 मौजूदा छवि को एक उदाहरण में लोड करें`Image` कक्षा:

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
Image image = Image.load(sourceFile);
```

## चरण 2: छवि को घुमाएँ

 छवि को घुमाएँ`rotateFlip` विधि। इस उदाहरण में, हम छवि को 270 डिग्री घुमाते हैं:

```java
image.rotateFlip(RotateFlipType.Rotate270FlipNone);
```

## चरण 3: घुमाई गई छवि को सहेजें

 घुमाई गई छवि को सहेजें`save` विधि और आउटपुट प्रारूप निर्दिष्ट करना (इस मामले में JPEG):

```java
String destName = dataDir + "RotatedImage_out.jpg";
image.save(destName, new JpegOptions());
```

## निष्कर्ष

बधाई हो! आपने Java के लिए Aspose.PSD का उपयोग करके सफलतापूर्वक एक छवि को घुमाया है। यह सरल लेकिन शक्तिशाली लाइब्रेरी आपके Java अनुप्रयोगों में छवि हेरफेर के लिए संभावनाओं की एक दुनिया खोलती है।

## अक्सर पूछे जाने वाले प्रश्न

### प्रश्न 1: क्या Aspose.PSD विभिन्न छवि प्रारूपों के साथ संगत है?

A1: हां, Aspose.PSD विभिन्न छवि प्रारूपों का समर्थन करता है, जिसमें PSD, JPEG, PNG, और अधिक शामिल हैं।

### प्रश्न 2: क्या मैं सिर्फ पूर्वनिर्धारित फ़्लिप ही नहीं, बल्कि कस्टम रोटेशन भी लागू कर सकता हूँ?

A2: बिल्कुल! Aspose.PSD आपकी विशिष्ट आवश्यकताओं को पूरा करने के लिए कस्टम रोटेशन लागू करने के लिए लचीलापन प्रदान करता है।

### प्रश्न 3: मुझे अतिरिक्त समर्थन या सहायता कहां मिल सकती है?

 A3: किसी भी प्रश्न या समस्या के लिए, पर जाएँ[Aspose.PSD फ़ोरम](https://forum.aspose.com/c/psd/34) सामुदायिक समर्थन के लिए.

### प्रश्न 4: क्या कोई निःशुल्क परीक्षण उपलब्ध है?

 A4: हाँ, आप Aspose.PSD का पता लगा सकते हैं[मुफ्त परीक्षण](https://releases.aspose.com/).

### प्रश्न 5: मैं अस्थायी लाइसेंस कैसे प्राप्त कर सकता हूँ?

 A5: यदि आपको अस्थायी लाइसेंस की आवश्यकता है, तो आप इसे प्राप्त कर सकते हैं[यहाँ](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
