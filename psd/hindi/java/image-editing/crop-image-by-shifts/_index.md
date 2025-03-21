---
title: Java के लिए Aspose.PSD में Shifts द्वारा छवि क्रॉप करें
linktitle: Shifts द्वारा छवि क्रॉप करें
second_title: Aspose.PSD जावा एपीआई
description: Java के लिए Aspose.PSD के साथ इमेज क्रॉपिंग में महारत हासिल करें। सहज इमेज हेरफेर के लिए एक व्यापक ट्यूटोरियल।
weight: 16
url: /hi/java/image-editing/crop-image-by-shifts/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java के लिए Aspose.PSD में Shifts द्वारा छवि क्रॉप करें

## परिचय

जावा-आधारित इमेज प्रोसेसिंग के क्षेत्र में, Aspose.PSD अत्यंत सटीकता के साथ छवियों में हेरफेर करने और उन्हें बेहतर बनाने के लिए एक शक्तिशाली उपकरण के रूप में सामने आता है। Aspose.PSD को अलग करने वाली प्रमुख विशेषताओं में से एक है इसकी छवि को सहजता से क्रॉप करने की क्षमता। इस ट्यूटोरियल में, हम जावा के लिए Aspose.PSD का उपयोग करके छवि क्रॉपिंग की कला में तल्लीन होंगे। अंत तक, आप अपनी विशिष्टताओं के अनुसार छवियों को आसानी से क्रॉप करने के कौशल से लैस हो जाएँगे।

## आवश्यक शर्तें

इससे पहले कि हम इस रोमांचक यात्रा पर निकलें, आइए सुनिश्चित करें कि आपके पास आवश्यक पूर्वापेक्षाएँ मौजूद हैं:

### जावा डेवलपमेंट किट (JDK)

 सुनिश्चित करें कि आपके सिस्टम पर JDK का नवीनतम संस्करण स्थापित है। आप इसे यहाँ से डाउनलोड कर सकते हैं[यहाँ](https://www.oracle.com/java/technologies/javase-downloads.html).

### Aspose.PSD for Java लाइब्रेरी

 आरंभ करने के लिए, आपको Aspose.PSD for Java लाइब्रेरी प्राप्त करनी होगी।[डाउनलोड पृष्ठ](https://releases.aspose.com/psd/java/) और नवीनतम संस्करण प्राप्त करें.

### एकीकृत विकास वातावरण (आईडीई)

सहज कोडिंग अनुभव के लिए अपना पसंदीदा जावा आईडीई, जैसे इक्लिप्स या इंटेलीज, चुनें।

## पैकेज आयात करें

अपने जावा प्रोजेक्ट में, छवि क्रॉपिंग प्रक्रिया को प्रारंभ करने के लिए आवश्यक पैकेज आयात करें:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imageoptions.JpegOptions;
```

अब, आइए Aspose.PSD for Java का उपयोग करके किसी छवि को क्रॉप करने की प्रक्रिया को सरल चरणों की एक श्रृंखला में विभाजित करें:

## चरण 1: छवि लोड करें

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// RasterImage वर्ग के एक उदाहरण में एक मौजूदा छवि लोड करें
RasterImage rasterImage = (RasterImage)Image.load(sourceFile);
```

## चरण 2: छवि डेटा कैश करें

बेहतर प्रदर्शन के लिए क्रॉपिंग से पहले छवि डेटा को कैश करना उचित है:

```java
if (!rasterImage.isCached()) {
  rasterImage.cacheData();
}
```

## चरण 3: शिफ्ट मान परिभाषित करें

छवि के सभी चार पक्षों के लिए शिफ्ट मान निर्दिष्ट करें:

```java
int leftShift = 10;
int rightShift = 10;
int topShift = 10;
int bottomShift = 10;
```

## चरण 4: क्रॉपिंग लागू करें

 निर्धारित शिफ्ट मानों के आधार पर, छवि पर क्रॉपिंग लागू करें`crop` तरीका:

```java
rasterImage.crop(leftShift, rightShift, topShift, bottomShift);
```

## चरण 5: परिणाम सहेजें

क्रॉप की गई छवि को वांछित प्रारूप में डिस्क पर सहेजें, इस मामले में, JPEG:

```java
String destName = dataDir + "CroppingByShifts_out.jpg";
rasterImage.save(destName, new JpegOptions());
```

बधाई हो! आपने Java के लिए Aspose.PSD का उपयोग करके सफलतापूर्वक एक छवि क्रॉप की है।

## निष्कर्ष

इस ट्यूटोरियल में, हमने Aspose.PSD for Java के साथ इमेज क्रॉपिंग की पेचीदगियों का पता लगाया। इस ज्ञान से लैस होकर, अब आप अपनी Java परियोजनाओं में इमेज क्रॉपिंग को सहजता से एकीकृत कर सकते हैं, जिससे आपकी इमेज प्रोसेसिंग क्षमताओं में और भी निखार आएगा।

## अक्सर पूछे जाने वाले प्रश्न

### प्रश्न 1: क्या Aspose.PSD सभी छवि प्रारूपों के साथ संगत है?

A1: हां, Aspose.PSD छवि प्रारूपों की एक विस्तृत श्रृंखला का समर्थन करता है, जो आपकी परियोजनाओं में बहुमुखी प्रतिभा सुनिश्चित करता है।

### प्रश्न 2: क्या मैं एक ही छवि पर एकाधिक क्रॉपिंग ऑपरेशन लागू कर सकता हूँ?

उत्तर2: बिल्कुल, आप एक ही छवि पर क्रमिक रूप से कई क्रॉपिंग ऑपरेशन कर सकते हैं।

### प्रश्न 3: क्या Aspose.PSD समर्थन के लिए कोई सामुदायिक मंच है?

 A3: हाँ, आप यहाँ समर्थन पा सकते हैं और समुदाय के साथ जुड़ सकते हैं[Aspose.PSD फ़ोरम](https://forum.aspose.com/c/psd/34).

### प्रश्न 4: मैं Aspose.PSD के लिए अस्थायी लाइसेंस कैसे प्राप्त कर सकता हूं?

 A4: विजिट करें[यहाँ](https://purchase.aspose.com/temporary-license/) अस्थायी लाइसेंस प्राप्त करने के लिए।

### प्रश्न 5: क्या Aspose.PSD कार्यक्षमताओं को प्रदर्शित करने वाली कोई नमूना परियोजनाएं हैं?

 A5: दस्तावेज़ और उदाहरण देखें[Aspose.PSD जावा दस्तावेज़ीकरण](https://reference.aspose.com/psd/java/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
