---
title: जावा के लिए Aspose.PSD के साथ एक छवि को एक विशिष्ट कोण पर घुमाएँ
linktitle: किसी छवि को एक विशिष्ट कोण पर घुमाएँ
second_title: Aspose.PSD जावा एपीआई
description: जावा के लिए Aspose.PSD के साथ जावा में छवि रोटेशन का अन्वेषण करें। छवियों को विशिष्ट कोणों पर सहजता से घुमाएँ।
type: docs
weight: 20
url: /hi/java/advanced-image-manipulation/rotate-image-specific-angle/
---
## परिचय

जावा विकास की गतिशील दुनिया में, विभिन्न अनुप्रयोगों के लिए छवियों में हेरफेर करना एक सामान्य आवश्यकता है। जावा के लिए Aspose.PSD एक मजबूत समाधान के रूप में उभरता है, जो छवि रोटेशन को सहजता से संभालने के लिए शक्तिशाली सुविधाएँ प्रदान करता है। इस ट्यूटोरियल में, हम जावा के लिए Aspose.PSD का उपयोग करके एक छवि को एक विशिष्ट कोण पर घुमाने की प्रक्रिया में आपका मार्गदर्शन करेंगे। विवरण में जाने से पहले, आइए कुछ पूर्वापेक्षाओं के साथ मंच तैयार करें।

## आवश्यक शर्तें

इससे पहले कि आप इस छवि रोटेशन यात्रा को शुरू करें, सुनिश्चित करें कि आपके पास निम्नलिखित शर्तें हैं:

### 1. जावा विकास पर्यावरण
सुनिश्चित करें कि आपके सिस्टम पर जावा डेवलपमेंट वातावरण स्थापित है।

### 2. जावा लाइब्रेरी के लिए Aspose.PSD
 जावा लाइब्रेरी के लिए Aspose.PSD डाउनलोड और इंस्टॉल करें। आप आवश्यक पुस्तकालय और दस्तावेज़ पा सकते हैं[यहाँ](https://reference.aspose.com/psd/java/).

### 3. नमूना छवि
एक नमूना छवि तैयार करें (उदाहरण के लिए, "sample.psd") जिसे आप घुमाना चाहते हैं। इसे अपनी दस्तावेज़ निर्देशिका में रखें.

## पैकेज आयात करें

अब, आइए छवि रोटेशन प्रक्रिया शुरू करने के लिए आवश्यक पैकेज आयात करें:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imageoptions.JpegOptions;
```

अब, आइए किसी छवि को एक विशिष्ट कोण पर घुमाने की प्रक्रिया को पालन करने में आसान चरणों की एक श्रृंखला में विभाजित करें।

## चरण 1: अपनी दस्तावेज़ निर्देशिका परिभाषित करें

```java
String dataDir = "Your Document Directory";
```

"आपकी दस्तावेज़ निर्देशिका" को अपनी दस्तावेज़ निर्देशिका के वास्तविक पथ से बदलना सुनिश्चित करें।

## चरण 2: स्रोत और गंतव्य फ़ाइल पथ निर्दिष्ट करें

```java
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "RotatingImageOnSpecificAngle_out.jpg";
```

स्रोत फ़ाइल पथ को अपनी नमूना छवि के स्थान पर सेट करें और घुमाई गई छवि के लिए गंतव्य फ़ाइल पथ निर्दिष्ट करें।

## चरण 3: छवि लोड करें

```java
RasterImage image = (RasterImage)Image.load(sourceFile);
```

Aspose.PSD का उपयोग करके नमूना छवि लोड करें।

## चरण 4: छवि डेटा कैश करें

```java
if (!image.isCached())
{
    image.cacheData();
}
```

रोटेशन के दौरान बेहतर प्रदर्शन के लिए छवि डेटा को कैश करें।

## चरण 5: छवि को घुमाएँ

```java
image.rotate(20f, true, Color.getRed());
```

आनुपातिक आकार बनाए रखते हुए और लाल पृष्ठभूमि रंग का उपयोग करते हुए 20 डिग्री के कोण पर घुमाएँ।

## चरण 6: परिणाम सहेजें

```java
image.save(destName, new JpegOptions());
```

घुमाई गई छवि को निर्दिष्ट विकल्पों के साथ एक नई फ़ाइल में सहेजें (इस मामले में, JpegOptions का उपयोग करके)।

बधाई हो! आपने जावा के लिए Aspose.PSD का उपयोग करके एक छवि को एक विशिष्ट कोण पर सफलतापूर्वक घुमाया है।

## निष्कर्ष

इस ट्यूटोरियल में, हमने जावा के लिए Aspose.PSD के साथ छवियों को घुमाने की निर्बाध प्रक्रिया का पता लगाया। लाइब्रेरी की मजबूत विशेषताएं जावा डेवलपर्स को छवियों में सहजता से हेरफेर करने में सक्षम बनाती हैं, जिससे असंख्य रचनात्मक संभावनाओं के द्वार खुलते हैं।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या मैं जावा के लिए Aspose.PSD का उपयोग करके छवियों को पारदर्शिता के साथ घुमा सकता हूँ?

हां, जावा के लिए Aspose.PSD पारदर्शिता के साथ छवियों के रोटेशन का समर्थन करता है। अपने कोड के अनुसार पारदर्शिता-संबंधित विकल्पों को संभालना सुनिश्चित करें।

### Q2: क्या रोटेशन के लिए समर्थित छवि फ़ाइल स्वरूपों पर कोई सीमाएँ हैं?

नहीं, Java के लिए Aspose.PSD PSD, JPEG, PNG, TIFF, GIF, BMP, JPEG2000, WMF, EMF और अन्य सहित छवि फ़ाइल स्वरूपों की एक विस्तृत श्रृंखला का समर्थन करता है।

### Q3: क्या मैं छवियों को ऋणात्मक कोण से घुमा सकता हूँ?

 निश्चित रूप से! आप इसमें एक नकारात्मक कोण निर्दिष्ट कर सकते हैं`image.rotate()` छवियों को विपरीत दिशा में घुमाने की विधि।

### Q4: क्या जावा के लिए Aspose.PSD रोटेशन के दौरान वास्तविक समय छवि पूर्वावलोकन प्रदान करता है?

जावा के लिए Aspose.PSD मुख्य रूप से बैकएंड इमेज प्रोसेसिंग पर केंद्रित है। वास्तविक समय छवि पूर्वावलोकन के लिए, आपको अन्य तकनीकों का उपयोग करके फ्रंटएंड समाधान लागू करने की आवश्यकता हो सकती है।

### Q5: क्या Aspose.PSD के लिए कोई सामुदायिक मंच है जहां मैं मदद मांग सकता हूं?

 हां, आप यहां जा सकते हैं[Aspose.PSD फोरम](https://forum.aspose.com/c/psd/34) समुदाय के साथ जुड़ने, प्रश्न पूछने और सहायता मांगने के लिए।