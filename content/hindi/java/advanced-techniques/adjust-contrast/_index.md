---
title: जावा के लिए Aspose.PSD के साथ एक छवि का कंट्रास्ट समायोजित करें
linktitle: किसी छवि का कंट्रास्ट समायोजित करें
second_title: Aspose.PSD जावा एपीआई
description: Aspose.PSD के साथ जावा में छवि कंट्रास्ट समायोजन की दुनिया का अन्वेषण करें। निर्बाध छवि हेरफेर के लिए हमारी चरण-दर-चरण मार्गदर्शिका का पालन करें।
type: docs
weight: 22
url: /hi/java/advanced-techniques/adjust-contrast/
---
## परिचय

जावा के साथ इमेज प्रोसेसिंग के क्षेत्र में, Aspose.PSD एक शक्तिशाली उपकरण के रूप में सामने आता है। इसकी असंख्य विशेषताओं में से, छवि कंट्रास्ट को समायोजित करना एक सामान्य आवश्यकता है। यह ट्यूटोरियल आपको जावा के लिए Aspose.PSD का उपयोग करके छवि कंट्रास्ट को समायोजित करने की प्रक्रिया के बारे में बताएगा। चाहे आप एक अनुभवी डेवलपर हों या अभी शुरुआत कर रहे हों, यह मार्गदर्शिका आपको छवि हेरफेर के इस आवश्यक पहलू में महारत हासिल करने में मदद करेगी।

## आवश्यक शर्तें

ट्यूटोरियल में जाने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित आवश्यक शर्तें हैं:

- जावा प्रोग्रामिंग की बुनियादी समझ.
-  जावा लाइब्रेरी के लिए Aspose.PSD स्थापित किया गया। आप इसे डाउनलोड कर सकते हैं[यहाँ](https://releases.aspose.com/psd/java/).

## पैकेज आयात करें

आरंभ करने के लिए, आपको अपने जावा प्रोजेक्ट में आवश्यक पैकेज आयात करने होंगे। अपने कोड में निम्नलिखित पंक्तियाँ जोड़ें:

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

// किसी मौजूदा छवि को RasterImage वर्ग के उदाहरण में लोड करें
Image image = Image.load(sourceFile);
```

 इस चरण में, हम नमूना छवि ("sample.psd") का उपयोग करके लोड करते हैं`Image.load` तरीका।

## चरण 2: RasterImage और Cache डेटा पर कास्ट करें

```java
// छवि के ऑब्जेक्ट को RasterImage पर कास्ट करें
RasterImage rasterImage = (RasterImage)image;

// जांचें कि क्या RasterImage कैश्ड है और बेहतर प्रदर्शन के लिए RasterImage को कैश करें
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

 यहां, हमने जेनेरिक डाला`Image` ए पर आपत्ति`RasterImage` विशिष्ट प्रसंस्करण के लिए. छवि डेटा को कैश करने से प्रदर्शन में सुधार होता है।

## चरण 3: कंट्रास्ट समायोजित करें

```java
// कंट्रास्ट को समायोजित करें
rasterImage.adjustContrast(50);
```

`adjustContrast`छवि के कंट्रास्ट को संशोधित करने के लिए विधि का उपयोग किया जाता है। इस उदाहरण में, कंट्रास्ट 50% बढ़ गया है।

## चरण 4: टिफ़ऑप्शंस बनाएं और सहेजें

```java
// परिणामी छवि के लिए TiffOptions का एक उदाहरण बनाएं
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);

// परिणामी छवि को TIFF प्रारूप में सहेजें
String destName = dataDir + "AdjustContrast_out.tiff";
rasterImage.save(destName, tiffOptions);
```

 यहाँ, हमने स्थापित किया`TiffOptions` आउटपुट छवि के लिए, प्रारूप और अन्य गुणों को निर्दिष्ट करना। फिर अंतिम छवि को TIFF फ़ाइल में सहेजा जाता है।

## निष्कर्ष

बधाई हो! आपने जावा के लिए Aspose.PSD का उपयोग करके एक छवि के कंट्रास्ट को सफलतापूर्वक समायोजित कर लिया है। इस ट्यूटोरियल में पैकेज आयात करने से लेकर संसाधित छवि को सहेजने तक के आवश्यक चरण शामिल हैं।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या Aspose.PSD विभिन्न छवि प्रारूपों के साथ संगत है?

A1: हां, Aspose.PSD आपके प्रोजेक्ट में लचीलापन प्रदान करते हुए विभिन्न छवि प्रारूपों का समर्थन करता है।

### Q2: मैं Aspose.PSD के लिए अस्थायी लाइसेंस कैसे प्राप्त कर सकता हूं?

 A2: आप अस्थायी लाइसेंस प्राप्त कर सकते हैं[यहाँ](https://purchase.aspose.com/temporary-license/).

### Q3: मुझे Aspose.PSD दस्तावेज़ कहां मिल सकता है?

A3: दस्तावेज़ उपलब्ध है[यहाँ](https://reference.aspose.com/psd/java/).

### Q4: Aspose.PSD के लिए कौन से समर्थन विकल्प उपलब्ध हैं?

 A4: सहायता के लिए, पर जाएँ[Aspose.PSD फोरम](https://forum.aspose.com/c/psd/34).

### Q5: क्या मैं Aspose.PSD खरीद सकता हूँ?

 A5: हाँ, आप Aspose.PSD खरीद सकते हैं[यहाँ](https://purchase.aspose.com/buy).