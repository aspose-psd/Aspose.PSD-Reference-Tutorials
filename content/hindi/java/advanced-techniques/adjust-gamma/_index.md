---
title: जावा के लिए Aspose.PSD के साथ एक छवि का गामा समायोजित करें
linktitle: किसी छवि का गामा समायोजित करें
second_title: Aspose.PSD जावा एपीआई
description: जावा के लिए Aspose.PSD का उपयोग करके छवि गामा को आसानी से समायोजित करना सीखें। सर्वोत्तम परिणामों के लिए हमारे चरण-दर-चरण मार्गदर्शिका का पालन करें।
type: docs
weight: 23
url: /hi/java/advanced-techniques/adjust-gamma/
---
## परिचय

छवि प्रसंस्करण के क्षेत्र में, किसी छवि के गामा को समायोजित करना उसकी दृश्य अपील को बढ़ाने के लिए एक महत्वपूर्ण कदम है। जावा के लिए Aspose.PSD जावा डेवलपर्स के लिए छवि गामा में आसानी से हेरफेर करने के लिए एक शक्तिशाली समाधान प्रदान करता है। इस ट्यूटोरियल में, हम यह पता लगाएंगे कि Aspose.PSD का उपयोग करके गामा को कैसे समायोजित किया जाए, एक निर्बाध कार्यान्वयन सुनिश्चित करने के लिए प्रत्येक चरण को तोड़ दिया जाए।

## आवश्यक शर्तें

ट्यूटोरियल में जाने से पहले, सुनिश्चित करें कि आपने निम्नलिखित आवश्यक शर्तें स्थापित कर ली हैं:

1. जावा विकास वातावरण: सुनिश्चित करें कि आपके सिस्टम पर जावा विकास वातावरण स्थापित है।
2.  Aspose.PSD लाइब्रेरी: Aspose.PSD लाइब्रेरी को डाउनलोड करें और अपने जावा प्रोजेक्ट में एकीकृत करें। आप इसमें आवश्यक संसाधन पा सकते हैं[प्रलेखन](https://reference.aspose.com/psd/java/).
3. नमूना छवि: एक नमूना PSD छवि तैयार करें जिसका उपयोग आप गामा समायोजन लागू करने के लिए करेंगे।

## पैकेज आयात करें

प्रक्रिया शुरू करने के लिए, अपने जावा प्रोजेक्ट में आवश्यक पैकेज आयात करें। यह Aspose.PSD कार्यक्षमताओं का निर्बाध रूप से उपयोग करने के लिए मंच तैयार करता है।

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## चरण 1: छवि लोड करें

 नमूना PSD छवि को एक उदाहरण में लोड करके प्रारंभ करें`RasterImage` कक्षा। यह बाद के गामा समायोजनों का आधार है।

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// किसी मौजूदा छवि को RasterImage वर्ग के उदाहरण में लोड करें
Image image = Image.load(sourceFile);

// छवि के ऑब्जेक्ट को RasterImage पर कास्ट करें
RasterImage rasterImage = (RasterImage)image;

// बेहतर प्रदर्शन के लिए जांचें कि RasterImage कैश्ड है या नहीं
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

## चरण 2: गामा समायोजित करें

 अब, का उपयोग करके लोड की गई छवि के गामा को समायोजित करें`adjustGamma` तरीका। अपनी आवश्यकताओं के अनुसार गामा मूल्यों को ठीक करें।

```java
// गामा समायोजित करें
rasterImage.adjustGamma(2.2f, 2.2f, 2.2f);
```

## चरण 3: टिफऑप्शंस बनाएं

 का एक उदाहरण बनाएं`TiffOptions` परिणामी छवि के लिए. आउटपुट को अपने विनिर्देशों के अनुरूप बनाने के लिए विभिन्न गुण सेट करें, जैसे प्रति नमूना बिट्स और फोटोमेट्रिक विकल्प।

```java
// परिणामी छवि के लिए TiffOptions का एक उदाहरण बनाएं
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

## चरण 4: परिणामी छवि सहेजें

 पहले से परिभाषित का उपयोग करके हेरफेर की गई छवि को टीआईएफएफ प्रारूप में सहेजें`TiffOptions`.

```java
// परिणामी छवि को TIFF प्रारूप में सहेजें
String destName = dataDir + "AdjustGamma_out.tiff";
rasterImage.save(destName, tiffOptions);
```

## निष्कर्ष

बधाई हो! आपने Java के लिए Aspose.PSD का उपयोग करके किसी छवि के गामा को सफलतापूर्वक समायोजित कर लिया है। यह प्रक्रिया डेवलपर्स को छवि गुणवत्ता को सहजता से बढ़ाने और एक आकर्षक उपयोगकर्ता अनुभव में योगदान करने के लिए सशक्त बनाती है।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: मुझे Aspose.PSD दस्तावेज़ कहां मिल सकता है?

 A1: आप यहां दस्तावेज़ तक पहुंच सकते हैं[https://reference.aspose.com/psd/java/](https://reference.aspose.com/psd/java/).

### Q2: मैं जावा के लिए Aspose.PSD कैसे डाउनलोड करूं?

 ए2: यहां से लाइब्रेरी डाउनलोड करें[https://releases.aspose.com/psd/java/](https://releases.aspose.com/psd/java/).

### Q3: मैं Aspose.PSD कहां से खरीद सकता हूं?

 ए3: विजिट करें[https://purchase.aspose.com/buy](https://purchase.aspose.com/buy) Aspose.PSD खरीदने के लिए।

### Q4: क्या कोई निःशुल्क परीक्षण उपलब्ध है?

 उ4: हां, आप यहां नि:शुल्क परीक्षण का पता लगा सकते हैं[https://releases.aspose.com/](https://releases.aspose.com/).

### Q5: मैं Aspose.PSD के लिए समर्थन कहाँ से प्राप्त कर सकता हूँ?

 A5: समर्थन के लिए, Aspose.PSD फोरम पर जाएँ[https://forum.aspose.com/c/psd/34](https://forum.aspose.com/c/psd/34).