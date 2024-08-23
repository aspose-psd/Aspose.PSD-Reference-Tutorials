---
title: Java के लिए Aspose.PSD के साथ एक छवि की चमक समायोजित करें
linktitle: छवि की चमक समायोजित करें
second_title: Aspose.PSD जावा एपीआई
description: Aspose.PSD के साथ Java में छवि की चमक बढ़ाएँ। प्रोग्रामेटिक रूप से छवि की चमक समायोजित करने के लिए चरण-दर-चरण मार्गदर्शिका।
type: docs
weight: 21
url: /hi/java/advanced-techniques/adjust-brightness/
---
## परिचय

ग्राफिक डिज़ाइन और डिजिटल फ़ोटोग्राफ़ी में छवियों को बेहतर बनाना एक आम ज़रूरत है। Aspose.PSD for Java प्रोग्रामेटिक रूप से छवि की चमक को समायोजित करने के लिए एक शक्तिशाली समाधान प्रदान करता है। इस ट्यूटोरियल में, हम चरण दर चरण किसी छवि की चमक को समायोजित करने के लिए Aspose.PSD for Java लाइब्रेरी का उपयोग करने का तरीका जानेंगे।

## आवश्यक शर्तें

ट्यूटोरियल में शामिल होने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित पूर्वापेक्षाएँ हैं:

-  Aspose.PSD for Java लाइब्रेरी: लाइब्रेरी को डाउनलोड करें और इंस्टॉल करें[Aspose.PSD for Java दस्तावेज़ीकरण](https://reference.aspose.com/psd/java/).

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

// RasterImage वर्ग के एक उदाहरण में एक मौजूदा छवि लोड करें
Image image = Image.load(sourceFile);
// छवि के ऑब्जेक्ट को RasterImage में कास्ट करें
RasterImage rasterImage = (RasterImage) image;

// जाँच करें कि RasterImage कैश किया गया है या नहीं और बेहतर प्रदर्शन के लिए RasterImage को कैश करें
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

 इस चरण में, हम लक्ष्य छवि को लोड करते हैं और इसे एक में डालते हैं`RasterImage` आगे और भी परिवर्तन के लिए।

## चरण 2: चमक समायोजित करें

```java
// चमक समायोजित करें
rasterImage.adjustBrightness(-50);
```

 यहाँ, हम उपयोग करते हैं`adjustBrightness`छवि की चमक को संशोधित करने की विधि। इस उदाहरण में, हम चमक को 50 इकाइयों से कम करते हैं, लेकिन आप अपनी आवश्यकताओं के आधार पर इस मान को अनुकूलित कर सकते हैं।

## चरण 3: TiffOptions सेट करें

```java
int[] ushort = {8, 8, 8};
// परिणामी छवि के लिए TiffOptions का एक उदाहरण बनाएँ
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

 कॉन्फ़िगर करें`TiffOptions` समायोजित छवि को सहेजने के लिए।`bitsPerSample` और`photometric` आपकी विशिष्ट आवश्यकताओं के आधार पर गुण।

## चरण 4: परिणामी छवि को सहेजें

```java
// परिणामी छवि सहेजें
rasterImage.save(destName, tiffOptions);
```

 अंत में, निर्दिष्ट का उपयोग करके संशोधित छवि को सहेजें`TiffOptions`.

## निष्कर्ष

Aspose.PSD for Java के साथ प्रोग्रामेटिक रूप से छवि की चमक को समायोजित करना आसान हो गया है। इस ट्यूटोरियल ने आपके Java अनुप्रयोगों में इस कार्यक्षमता को लागू करने के बारे में एक व्यापक मार्गदर्शिका प्रदान की है।

## अक्सर पूछे जाने वाले प्रश्न

### प्रश्न 1: क्या मैं PSD के अलावा अन्य छवि प्रारूपों में चमक समायोजित कर सकता हूँ?

A1: हां, Java के लिए Aspose.PSD JPEG, PNG और TIFF जैसे विभिन्न छवि प्रारूपों का समर्थन करता है।

### प्रश्न 2: मैं छवि समायोजन प्रक्रिया के दौरान त्रुटियों को कैसे संभाल सकता हूँ?

A2: आप संभावित अपवादों को प्रबंधित करने के लिए try-catch ब्लॉक का उपयोग करके त्रुटि प्रबंधन को कार्यान्वित कर सकते हैं।

### प्रश्न 3: क्या चमक समायोजन की सीमा की कोई सीमा है?

A3: समायोजन की सीमा छवि सामग्री और प्रारूप पर निर्भर करती है, लेकिन Aspose.PSD अनुकूलन में लचीलापन प्रदान करता है।

### प्रश्न 4: क्या मैं व्यावसायिक परियोजनाओं में Java के लिए Aspose.PSD का उपयोग कर सकता हूँ?

 A4: हाँ, Aspose.PSD for Java एक वाणिज्यिक लाइब्रेरी है, और आप इससे लाइसेंस प्राप्त कर सकते हैं[यहाँ](https://purchase.aspose.com/buy).

### प्रश्न 5: क्या Java के लिए Aspose.PSD का निःशुल्क परीक्षण उपलब्ध है?

 A5: हाँ, आप निःशुल्क परीक्षण के साथ पुस्तकालय का भ्रमण कर सकते हैं[यहाँ](https://releases.aspose.com/).