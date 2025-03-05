---
title: Java के लिए Aspose.PSD के साथ एक छवि का कंट्रास्ट समायोजित करें
linktitle: किसी छवि का कंट्रास्ट समायोजित करें
second_title: Aspose.PSD जावा एपीआई
description: Aspose.PSD के साथ जावा में इमेज कंट्रास्ट एडजस्टमेंट की दुनिया का अन्वेषण करें। सहज इमेज हेरफेर के लिए हमारे चरण-दर-चरण गाइड का पालन करें।
type: docs
weight: 22
url: /hi/java/advanced-techniques/adjust-contrast/
---
## परिचय

जावा के साथ इमेज प्रोसेसिंग के क्षेत्र में, Aspose.PSD एक शक्तिशाली उपकरण के रूप में सामने आता है। इसकी असंख्य विशेषताओं में से, इमेज कंट्रास्ट को समायोजित करना एक सामान्य आवश्यकता है। यह ट्यूटोरियल आपको जावा के लिए Aspose.PSD का उपयोग करके इमेज कंट्रास्ट को समायोजित करने की प्रक्रिया से परिचित कराएगा। चाहे आप एक अनुभवी डेवलपर हों या अभी शुरुआत कर रहे हों, यह गाइड आपको इमेज हेरफेर के इस आवश्यक पहलू में महारत हासिल करने में मदद करेगा।

## आवश्यक शर्तें

ट्यूटोरियल में आगे बढ़ने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित पूर्वापेक्षाएँ मौजूद हैं:

- जावा प्रोग्रामिंग की बुनियादी समझ.
-  Aspose.PSD for Java लाइब्रेरी स्थापित है। आप इसे डाउनलोड कर सकते हैं[यहाँ](https://releases.aspose.com/psd/java/).

## पैकेज आयात करें

आरंभ करने के लिए, आपको अपने जावा प्रोजेक्ट में आवश्यक पैकेज आयात करने होंगे। अपने कोड में निम्न पंक्तियाँ जोड़ें:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## चरण 1: छवि लोड करें

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// RasterImage वर्ग के एक उदाहरण में एक मौजूदा छवि लोड करें
Image image = Image.load(sourceFile);
```

 इस चरण में, हम नमूना छवि ("sample.psd") को लोड करते हैं`Image.load` तरीका।

## चरण 2: RasterImage और कैश डेटा पर कास्ट करें

```java
// छवि के ऑब्जेक्ट को RasterImage में कास्ट करें
RasterImage rasterImage = (RasterImage)image;

// जाँच करें कि RasterImage कैश किया गया है या नहीं और बेहतर प्रदर्शन के लिए RasterImage को कैश करें
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

 यहाँ, हम जेनेरिक कास्ट करते हैं`Image` किसी बात पर आपत्ति जताना`RasterImage` विशिष्ट प्रसंस्करण के लिए। छवि डेटा को कैश करने से प्रदर्शन में सुधार होता है।

## चरण 3: कंट्रास्ट समायोजित करें

```java
// कंट्रास्ट समायोजित करें
rasterImage.adjustContrast(50);
```

`adjustContrast`छवि के कंट्रास्ट को संशोधित करने के लिए विधि का उपयोग किया जाता है। इस उदाहरण में, कंट्रास्ट 50% तक बढ़ जाता है।

## चरण 4: TiffOptions बनाएं और सहेजें

```java
// परिणामी छवि के लिए TiffOptions का एक उदाहरण बनाएँ
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);

// परिणामी छवि को TIFF प्रारूप में सहेजें
String destName = dataDir + "AdjustContrast_out.tiff";
rasterImage.save(destName, tiffOptions);
```

 यहाँ, हमने स्थापित किया`TiffOptions` आउटपुट छवि के लिए, प्रारूप और अन्य गुण निर्दिष्ट करना। फिर अंतिम छवि को TIFF फ़ाइल में सहेजा जाता है।

## निष्कर्ष

बधाई हो! आपने Aspose.PSD for Java का उपयोग करके किसी छवि के कंट्रास्ट को सफलतापूर्वक समायोजित कर लिया है। इस ट्यूटोरियल में पैकेज आयात करने से लेकर संसाधित छवि को सहेजने तक के आवश्यक चरणों को शामिल किया गया है।

## अक्सर पूछे जाने वाले प्रश्न

### प्रश्न 1: क्या Aspose.PSD विभिन्न छवि प्रारूपों के साथ संगत है?

A1: हां, Aspose.PSD विभिन्न छवि प्रारूपों का समर्थन करता है, जो आपकी परियोजनाओं में लचीलापन प्रदान करता है।

### प्रश्न 2: मैं Aspose.PSD के लिए अस्थायी लाइसेंस कैसे प्राप्त कर सकता हूं?

 A2: आप अस्थायी लाइसेंस प्राप्त कर सकते हैं[यहाँ](https://purchase.aspose.com/temporary-license/).

### प्रश्न 3: मैं Aspose.PSD दस्तावेज़ कहां पा सकता हूं?

A3: दस्तावेज़ उपलब्ध है[यहाँ](https://reference.aspose.com/psd/java/).

### प्रश्न 4: Aspose.PSD के लिए कौन से समर्थन विकल्प उपलब्ध हैं?

 A4: सहायता के लिए, यहां जाएं[Aspose.PSD फ़ोरम](https://forum.aspose.com/c/psd/34).

### प्रश्न 5: क्या मैं Aspose.PSD खरीद सकता हूँ?

 A5: हाँ, आप Aspose.PSD खरीद सकते हैं[यहाँ](https://purchase.aspose.com/buy).