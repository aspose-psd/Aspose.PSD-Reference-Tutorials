---
title: जावा के लिए Aspose.PSD के साथ एक छवि की चमक समायोजित करें
linktitle: किसी छवि की चमक समायोजित करें
second_title: Aspose.PSD जावा एपीआई
description: Aspose.PSD के साथ जावा में छवि चमक बढ़ाएँ। छवि चमक को प्रोग्रामेटिक रूप से समायोजित करने के लिए चरण-दर-चरण मार्गदर्शिका।
type: docs
weight: 21
url: /hi/java/advanced-techniques/adjust-brightness/
---
## परिचय

ग्राफ़िक डिज़ाइन और डिजिटल फ़ोटोग्राफ़ी में छवियों को बेहतर बनाना एक सामान्य आवश्यकता है। जावा के लिए Aspose.PSD प्रोग्रामेटिक रूप से छवि चमक को समायोजित करने के लिए एक शक्तिशाली समाधान प्रदान करता है। इस ट्यूटोरियल में, हम चरण दर चरण किसी छवि की चमक को समायोजित करने के लिए जावा लाइब्रेरी के लिए Aspose.PSD का उपयोग कैसे करें, इसका पता लगाएंगे।

## आवश्यक शर्तें

ट्यूटोरियल में जाने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित शर्तें हैं:

-  जावा लाइब्रेरी के लिए Aspose.PSD: लाइब्रेरी को डाउनलोड और इंस्टॉल करें[जावा दस्तावेज़ीकरण के लिए Aspose.PSD](https://reference.aspose.com/psd/java/).

## पैकेज आयात करें

आरंभ करने के लिए, अपने जावा प्रोजेक्ट में आवश्यक पैकेज आयात करें। इस उदाहरण में, हम निम्नलिखित का उपयोग करेंगे:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

अब, आइए किसी छवि की चमक को समायोजित करने की प्रक्रिया को सरल चरणों में विभाजित करें:

## चरण 1: छवि लोड करें

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "AdjustBrightness_out.tiff";

// किसी मौजूदा छवि को RasterImage वर्ग के उदाहरण में लोड करें
Image image = Image.load(sourceFile);
// छवि के ऑब्जेक्ट को RasterImage पर कास्ट करें
RasterImage rasterImage = (RasterImage) image;

// जांचें कि क्या RasterImage कैश्ड है और बेहतर प्रदर्शन के लिए RasterImage को कैश करें
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

 इस चरण में, हम लक्ष्य छवि को लोड करते हैं और उसे a पर डालते हैं`RasterImage` आगे और भी परिवर्तन के लिए।

## चरण 2: चमक समायोजित करें

```java
// चमक समायोजित करें
rasterImage.adjustBrightness(-50);
```

 यहां, हम इसका उपयोग करते हैं`adjustBrightness`छवि की चमक को संशोधित करने की विधि। इस उदाहरण में, हम चमक को 50 इकाइयों तक कम कर देते हैं, लेकिन आप अपनी आवश्यकताओं के आधार पर इस मान को अनुकूलित कर सकते हैं।

## चरण 3: टिफ़ऑप्शंस सेट करें

```java
int[] ushort = {8, 8, 8};
// परिणामी छवि के लिए TiffOptions का एक उदाहरण बनाएं
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

 कॉन्फ़िगर करें`TiffOptions` समायोजित छवि को सहेजने के लिए. समायोजित`bitsPerSample` और`photometric` आपकी विशिष्ट आवश्यकताओं के आधार पर गुण।

## चरण 4: परिणामी छवि सहेजें

```java
// परिणामी छवि सहेजें
rasterImage.save(destName, tiffOptions);
```

 अंत में, निर्दिष्ट का उपयोग करके संशोधित छवि को सहेजें`TiffOptions`.

## निष्कर्ष

जावा के लिए Aspose.PSD के साथ किसी छवि की चमक को प्रोग्रामेटिक रूप से समायोजित करना आसान बना दिया गया है। इस ट्यूटोरियल ने आपके जावा अनुप्रयोगों में इस कार्यक्षमता को लागू करने पर एक व्यापक मार्गदर्शिका प्रदान की है।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या मैं PSD के अलावा अन्य छवि प्रारूपों में चमक समायोजित कर सकता हूँ?

A1: हाँ, Java के लिए Aspose.PSD JPEG, PNG और TIFF जैसे विभिन्न छवि प्रारूपों का समर्थन करता है।

### Q2: मैं छवि समायोजन प्रक्रिया के दौरान त्रुटियों को कैसे संभाल सकता हूँ?

A2: आप होने वाले अपवादों को प्रबंधित करने के लिए ट्राई-कैच ब्लॉक का उपयोग करके त्रुटि प्रबंधन को कार्यान्वित कर सकते हैं।

### Q3: क्या चमक समायोजन की सीमा की कोई सीमा है?

A3: समायोजन की सीमा छवि सामग्री और प्रारूप पर निर्भर करती है, लेकिन Aspose.PSD अनुकूलन में लचीलापन प्रदान करता है।

### Q4: क्या मैं व्यावसायिक परियोजनाओं में जावा के लिए Aspose.PSD का उपयोग कर सकता हूँ?

 A4: हाँ, Java के लिए Aspose.PSD एक व्यावसायिक लाइब्रेरी है, और आप इससे लाइसेंस प्राप्त कर सकते हैं[यहाँ](https://purchase.aspose.com/buy).

### Q5: क्या Java के लिए Aspose.PSD का निःशुल्क परीक्षण उपलब्ध है?

 A5: हां, आप नि:शुल्क परीक्षण के साथ लाइब्रेरी का पता लगा सकते हैं[यहाँ](https://releases.aspose.com/).