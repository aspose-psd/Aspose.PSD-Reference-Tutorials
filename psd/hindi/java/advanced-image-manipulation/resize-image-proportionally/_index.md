---
title: Java के लिए Aspose.PSD के साथ आनुपातिक रूप से छवि का आकार बदलें
linktitle: छवि का आकार आनुपातिक रूप से बदलें
second_title: Aspose.PSD जावा एपीआई
description: Aspose.PSD के साथ अपने जावा एप्लिकेशन को बेहतर बनाएँ। छवियों को आनुपातिक रूप से आसानी से आकार देने के लिए हमारे गाइड का पालन करें। आज ही अपनी छवि प्रबंधन क्षमताओं को बढ़ाएँ।
weight: 17
url: /hi/java/advanced-image-manipulation/resize-image-proportionally/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java के लिए Aspose.PSD के साथ आनुपातिक रूप से छवि का आकार बदलें

## परिचय

Aspose.PSD for Java का उपयोग करके छवियों का आनुपातिक रूप से आकार बदलने के बारे में हमारी चरण-दर-चरण मार्गदर्शिका में आपका स्वागत है। यदि आप अपने Java अनुप्रयोगों को कुशल छवि आकार बदलने की क्षमताओं के साथ बढ़ाना चाहते हैं, तो आप सही जगह पर आए हैं। इस ट्यूटोरियल में, हम आपको स्पष्ट और संक्षिप्त चरणों का उपयोग करके प्रक्रिया के माध्यम से चलेंगे।

## आवश्यक शर्तें

ट्यूटोरियल में आगे बढ़ने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित पूर्वापेक्षाएँ मौजूद हैं:

1. जावा वातावरण: सुनिश्चित करें कि आपके सिस्टम पर जावा स्थापित है।
2.  Aspose.PSD लाइब्रेरी: Aspose.PSD लाइब्रेरी डाउनलोड करें और इंस्टॉल करें। आप आवश्यक संसाधन पा सकते हैं[यहाँ](https://releases.aspose.com/psd/java/).

## पैकेज आयात करें

एक बार जब आप अपनी पूर्व-आवश्यकताओं को हल कर लें, तो अपने जावा प्रोजेक्ट में आवश्यक पैकेज आयात करें। सुनिश्चित करें कि Aspose.PSD लाइब्रेरी आपके प्रोजेक्ट में सही ढंग से संदर्भित है।

```java
import com.aspose.psd.Image;

import com.aspose.psd.imageoptions.PngOptions;
```

## चरण 1: छवि लोड करें

सबसे पहले उस छवि को अपने जावा अनुप्रयोग में लोड करें जिसका आकार आप बदलना चाहते हैं।

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

Image image = Image.load(sourceFile);

if (!image.isCached()) {
    image.cacheData();
}
```

## चरण 2: चौड़ाई और ऊंचाई निर्दिष्ट करें

अपनी आकार बदली गई छवि के लिए नई चौड़ाई और ऊँचाई निर्धारित करें। इस उदाहरण में, हम छवि का आकार उसके मूल आयामों के आधे तक बदल देंगे।

```java
int newWidth = image.getWidth() / 2;
image.resizeWidthProportionally(newWidth);

int newHeight = image.getHeight() / 2;
image.resizeHeightProportionally(newHeight);
```

## चरण 3: पुनःआकारित छवि को सहेजें

प्रारूप विकल्प (इस मामले में PNG) निर्दिष्ट करते हुए, पुनःआकारित छवि को अपने इच्छित स्थान पर सहेजें।

```java
String destName = dataDir + "SimpleResizeImageProportionally_out.png";
image.save(destName, new PngOptions());
```

और बस, अब आपने Aspose.PSD for Java का उपयोग करके छवि का आनुपातिक आकार सफलतापूर्वक बदल दिया है।

## निष्कर्ष

इस ट्यूटोरियल में, हमने जावा के लिए Aspose.PSD लाइब्रेरी का उपयोग करके छवियों का आनुपातिक रूप से आकार बदलने के लिए आवश्यक चरणों को कवर किया है। अब, आप बेहतर छवि प्रबंधन के लिए इस कार्यक्षमता को अपने जावा अनुप्रयोगों में आसानी से एकीकृत कर सकते हैं।

## अक्सर पूछे जाने वाले प्रश्न

### प्रश्न 1: क्या Aspose.PSD सभी छवि प्रारूपों के साथ संगत है?

 A1: Aspose.PSD विभिन्न छवि प्रारूपों का समर्थन करता है, जिसमें PSD, PNG, JPEG, और बहुत कुछ शामिल है।[प्रलेखन](https://reference.aspose.com/psd/java/) विस्तृत सूची के लिए कृपया देखें.

### प्रश्न 2: क्या मैं व्यावसायिक परियोजनाओं के लिए Aspose.PSD का उपयोग कर सकता हूँ?

 A2: हाँ, आप जा सकते हैं।[खरीद पृष्ठ](https://purchase.aspose.com/buy) लाइसेंसिंग विवरण के लिए कृपया देखें.

### प्रश्न 3: क्या परीक्षण प्रयोजनों के लिए अस्थायी लाइसेंस उपलब्ध हैं?

 A3: हां, आप एक अस्थायी लाइसेंस प्राप्त कर सकते हैं[यहाँ](https://purchase.aspose.com/temporary-license/) मूल्यांकन हेतु.

### प्रश्न 4: मैं Aspose.PSD के लिए समर्थन कहां पा सकता हूं?

 A4: पर जाएँ[Aspose.PSD फ़ोरम](https://forum.aspose.com/c/psd/34) सामुदायिक समर्थन और सहायता के लिए।

### प्रश्न 5: मैं Aspose.PSD दस्तावेज़ तक कैसे पहुंच सकता हूं?

 A5: विस्तृत दस्तावेज़ देखें[यहाँ](https://reference.aspose.com/psd/java/).
`
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
