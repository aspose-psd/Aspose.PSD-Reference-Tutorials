---
title: Java के लिए Aspose.PSD के साथ एक छवि का गामा समायोजित करें
linktitle: किसी छवि का गामा समायोजित करें
second_title: Aspose.PSD जावा एपीआई
description: Aspose.PSD for Java का उपयोग करके आसानी से इमेज गामा को समायोजित करना सीखें। सर्वोत्तम परिणामों के लिए हमारे चरण-दर-चरण मार्गदर्शिका का पालन करें।
weight: 23
url: /hi/java/advanced-techniques/adjust-gamma/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java के लिए Aspose.PSD के साथ एक छवि का गामा समायोजित करें

## परिचय

छवि प्रसंस्करण के क्षेत्र में, छवि के गामा को समायोजित करना इसकी दृश्य अपील को बढ़ाने के लिए एक महत्वपूर्ण कदम है। जावा के लिए Aspose.PSD जावा डेवलपर्स के लिए छवि गामा को आसानी से हेरफेर करने के लिए एक शक्तिशाली समाधान प्रदान करता है। इस ट्यूटोरियल में, हम Aspose.PSD का उपयोग करके गामा को समायोजित करने का तरीका जानेंगे, एक सहज कार्यान्वयन सुनिश्चित करने के लिए प्रत्येक चरण को तोड़ेंगे।

## आवश्यक शर्तें

ट्यूटोरियल में आगे बढ़ने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित पूर्वापेक्षाएँ निर्धारित हैं:

1. जावा विकास वातावरण: सुनिश्चित करें कि आपके सिस्टम पर जावा विकास वातावरण स्थापित है।
2.  Aspose.PSD लाइब्रेरी: Aspose.PSD लाइब्रेरी को अपने Java प्रोजेक्ट में डाउनलोड और एकीकृत करें। आप आवश्यक संसाधन यहाँ पा सकते हैं[प्रलेखन](https://reference.aspose.com/psd/java/).
3. नमूना छवि: एक नमूना PSD छवि तैयार करें जिसका उपयोग आप गामा समायोजन लागू करने के लिए करेंगे।

## पैकेज आयात करें

प्रक्रिया शुरू करने के लिए, अपने जावा प्रोजेक्ट में आवश्यक पैकेज आयात करें। यह Aspose.PSD कार्यक्षमताओं का सहजता से उपयोग करने के लिए मंच तैयार करता है।

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## चरण 1: छवि लोड करें

 नमूना PSD छवि को एक उदाहरण में लोड करके प्रारंभ करें`RasterImage` यह बाद के गामा समायोजनों का आधार है।

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// RasterImage वर्ग के एक उदाहरण में एक मौजूदा छवि लोड करें
Image image = Image.load(sourceFile);

// छवि के ऑब्जेक्ट को RasterImage में कास्ट करें
RasterImage rasterImage = (RasterImage)image;

// बेहतर प्रदर्शन के लिए जाँच करें कि RasterImage कैश किया गया है या नहीं
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

## चरण 2: गामा समायोजित करें

 अब, लोड की गई छवि के गामा को समायोजित करें`adjustGamma` विधि। अपनी आवश्यकताओं के अनुसार गामा मानों को ठीक करें।

```java
// गामा समायोजित करें
rasterImage.adjustGamma(2.2f, 2.2f, 2.2f);
```

## चरण 3: TiffOptions बनाएँ

 इसका एक उदाहरण बनाएं`TiffOptions` परिणामी छवि के लिए। आउटपुट को अपने विनिर्देशों के अनुसार तैयार करने के लिए प्रति नमूना बिट्स और फोटोमेट्रिक विकल्प जैसे विभिन्न गुण सेट करें।

```java
// परिणामी छवि के लिए TiffOptions का एक उदाहरण बनाएँ
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

## चरण 4: परिणामी छवि को सहेजें

 पहले से परिभाषित विधि का उपयोग करके संशोधित छवि को TIFF प्रारूप में सहेजें`TiffOptions`.

```java
// परिणामी छवि को TIFF प्रारूप में सहेजें
String destName = dataDir + "AdjustGamma_out.tiff";
rasterImage.save(destName, tiffOptions);
```

## निष्कर्ष

बधाई हो! आपने Aspose.PSD for Java का उपयोग करके किसी छवि के गामा को सफलतापूर्वक समायोजित कर लिया है। यह प्रक्रिया डेवलपर्स को छवि की गुणवत्ता को सहजता से बढ़ाने में सक्षम बनाती है, जिससे उपयोगकर्ता अनुभव को आकर्षक बनाने में मदद मिलती है।

## अक्सर पूछे जाने वाले प्रश्न

### प्रश्न 1: मैं Aspose.PSD दस्तावेज़ कहां पा सकता हूं?

 A1: आप दस्तावेज़ों तक यहां से पहुंच सकते हैं[https://reference.aspose.com/psd/java/](https://reference.aspose.com/psd/java/).

### प्रश्न 2: मैं Java के लिए Aspose.PSD कैसे डाउनलोड करूं?

 A2: लाइब्रेरी को यहाँ से डाउनलोड करें[https://releases.aspose.com/psd/java/](https://releases.aspose.com/psd/java/).

### प्रश्न 3: मैं Aspose.PSD कहां से खरीद सकता हूं?

 A3: विजिट करें[https://purchase.aspose.com/buy](https://purchase.aspose.com/buy) Aspose.PSD खरीदने के लिए.

### प्रश्न 4: क्या कोई निःशुल्क परीक्षण उपलब्ध है?

 A4: हाँ, आप यहाँ निःशुल्क परीक्षण का लाभ उठा सकते हैं[https://releases.aspose.com/](https://releases.aspose.com/).

### प्रश्न 5: मैं Aspose.PSD के लिए समर्थन कहां से प्राप्त कर सकता हूं?

 A5: सहायता के लिए, Aspose.PSD फोरम पर जाएँ[https://forum.aspose.com/c/psd/34](https://forum.aspose.com/c/psd/34).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
