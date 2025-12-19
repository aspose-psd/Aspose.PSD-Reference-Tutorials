---
date: 2025-12-19
description: Aspose.PSD for Java का उपयोग करके छवि की चमक को कैसे समायोजित करें, सीखें।
  यह जावा इमेज मैनिपुलेशन ट्यूटोरियल चरण‑दर‑चरण मार्गदर्शन प्रदान करता है।
linktitle: Adjust Brightness of an Image
second_title: Aspose.PSD Java API
title: Aspose.PSD for Java के साथ छवि की चमक को कैसे समायोजित करें
url: /hi/java/advanced-techniques/adjust-brightness/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java के साथ छवि की चमक समायोजित करें

## परिचय

यदि आपको **जावा कोड से सीधे छवि की चमक समायोजित करना** सीखना है, तो आप सही जगह पर हैं। चमक समायोजन ग्राफिक डिज़ाइनरों, फ़ोटोग्राफ़रों और इमेज‑प्रोसेसिंग पाइपलाइन बनाने वाले सभी के लिए एक सामान्य कार्य है। इस **java image manipulation tutorial** में हम पूरी प्रक्रिया—PSD/TIFF लोड करना, चमक ऑफ़सेट लागू करना, और परिणाम सहेजना—को Aspose.PSD for Java लाइब्रेरी का उपयोग करके दिखाएंगे।

## त्वरित उत्तर
- **कौन सी लाइब्रेरी चमक संभालती है?** Aspose.PSD for Java  
- **कौन सा मेथड चमक बदलता है?** `RasterImage.adjustBrightness()`  
- **क्या मैं PSD और TIFF फ़ाइलों के साथ काम कर सकता हूँ?** हाँ, API दोनों फ़ॉर्मेट को सपोर्ट करता है।  
- **उत्पादन के लिए लाइसेंस चाहिए?** गैर‑मूल्यांकन उपयोग के लिए एक व्यावसायिक लाइसेंस आवश्यक है।  
- **इम्प्लीमेंटेशन में कितना समय लगेगा?** बेसिक समायोजन के लिए आमतौर पर 10 मिनट से कम।

## इमेज ब्राइटनेस एडजस्टमेंट क्या है?

इमेज ब्राइटनेस एडजस्टमेंट एक छवि के प्रत्येक पिक्सेल की समग्र प्रकाशता को बदलता है। चमक बढ़ाने से अंधेरे क्षेत्रों को हल्का किया जाता है, जबकि घटाने से पूरी तस्वीर डार्क हो जाती है। यह ऑपरेशन अंडरएक्सपोज़्ड फ़ोटो को सुधारने, प्रिंट के लिए एसेट तैयार करने, या एप्लिकेशन में विज़ुअल इफ़ेक्ट बनाने में उपयोगी है।

## Aspose.PSD for Java क्यों उपयोग करें?

- **पूर्ण फ़ॉर्मेट सपोर्ट** – PSD, TIFF, JPEG, PNG, और अधिक।  
- **कोई बाहरी नेटिव डिपेंडेंसी नहीं** – शुद्ध जावा, आसान इंटीग्रेशन।  
- **हाई‑परफ़ॉर्मेंस कैशिंग** – रास्टर डेटा को तेज़ पुनरावृत्ति के लिए कैश किया जा सकता है।  
- **रिच API** – कलर करेक्शन, लेयर्स, मास्क और अन्य एडवांस्ड एडिट्स के लिए मेथड्स।

## पूर्वापेक्षाएँ

ट्यूटोरियल शुरू करने से पहले सुनिश्चित करें कि आपके पास निम्नलिखित पूर्वापेक्षाएँ हैं:

- Aspose.PSD for Java लाइब्रेरी: लाइब्रेरी को [Aspose.PSD for Java documentation](https://reference.aspose.com/psd/java/) से डाउनलोड और इंस्टॉल करें।

## पैकेज इम्पोर्ट करें

शुरू करने के लिए, आवश्यक पैकेजों को अपने जावा प्रोजेक्ट में इम्पोर्ट करें। इस उदाहरण में हम निम्नलिखित का उपयोग करेंगे:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

अब, छवि की चमक समायोजित करने की प्रक्रिया को सरल चरणों में विभाजित करते हैं:

## Aspose.PSD का उपयोग करके चमक कैसे समायोजित करें

### चरण 1: छवि लोड करें

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "AdjustBrightness_out.tiff";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);
// Cast object of Image to RasterImage
RasterImage rasterImage = (RasterImage) image;

// Check if RasterImage is cached and Cache RasterImage for better performance
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

इस चरण में हम लक्ष्य छवि को लोड करते हैं और आगे की प्रोसेसिंग के लिए इसे `RasterImage` में कास्ट करते हैं।

### चरण 2: चमक समायोजित करें

```java
// Adjust the brightness
rasterImage.adjustBrightness(-50);
```

यहाँ हम `adjustBrightness` मेथड का उपयोग करके छवि की चमक बदलते हैं। इस उदाहरण में हम चमक को 50 यूनिट घटाते हैं, लेकिन आप अपनी आवश्यकता के अनुसार इस मान को कस्टमाइज़ कर सकते हैं।

### चरण 3: TiffOptions सेट करें

```java
int[] ushort = {8, 8, 8};
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

समायोजित छवि को सहेजने के लिए `TiffOptions` को कॉन्फ़िगर करें। अपनी विशिष्ट जरूरतों के अनुसार `bitsPerSample` और `photometric` प्रॉपर्टीज़ को एडजस्ट करें।

### चरण 4: परिणामस्वरूप छवि सहेजें

```java
// Save the resultant image
rasterImage.save(destName, tiffOptions);
```

अंत में, निर्दिष्ट `TiffOptions` का उपयोग करके संशोधित छवि को सहेजें।

## सामान्य समस्याएँ और समाधान

| समस्या | कारण | समाधान |
|-------|--------|----------|
| **`ClassCastException` जब Image को कास्ट किया जाता है** | फ़ाइल रास्टर इमेज नहीं है (जैसे, वेक्टर PSD)। | स्रोत फ़ाइल फ़ॉर्मेट की जाँच करें या कास्ट करने से पहले `image instanceof RasterImage` का उपयोग करें। |
| **चमक परिवर्तन का कोई असर नहीं** | समायोजन से पहले इमेज कैश नहीं हुई थी। | चरण 1 में दिखाए अनुसार `rasterImage.cacheData()` कॉल करें। |
| **सहेजी गई फ़ाइल भ्रष्ट दिखती है** | `TiffOptions` कॉन्फ़िगरेशन गलत है। | सुनिश्चित करें कि `bitsPerSample` स्रोत इमेज की डेप्थ (आमतौर पर प्रति चैनल 8‑bit) से मेल खाता है। |

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या मैं PSD के अलावा अन्य इमेज फ़ॉर्मेट में भी चमक समायोजित कर सकता हूँ?

A1: हाँ, Aspose.PSD for Java JPEG, PNG, और TIFF सहित विभिन्न इमेज फ़ॉर्मेट को सपोर्ट करता है।

### Q2: इमेज एडजस्टमेंट प्रक्रिया के दौरान त्रुटियों को कैसे संभालूँ?

A2: आप `try‑catch` ब्लॉक्स का उपयोग करके उत्पन्न होने वाले एक्सेप्शन को मैनेज कर सकते हैं।

### Q3: चमक समायोजन की रेंज पर कोई सीमा है?

A3: रेंज इमेज कंटेंट और फ़ॉर्मेट पर निर्भर करती है, लेकिन Aspose.PSD कस्टमाइज़ेशन में लचीलापन प्रदान करता है।

### Q4: क्या मैं Aspose.PSD for Java को व्यावसायिक प्रोजेक्ट्स में उपयोग कर सकता हूँ?

A4: हाँ, Aspose.PSD for Java एक व्यावसायिक लाइब्रेरी है, और आप इसे [यहाँ](https://purchase.aspose.com/buy) से लाइसेंस प्राप्त कर सकते हैं।

### Q5: क्या Aspose.PSD for Java के लिए मुफ्त ट्रायल उपलब्ध है?

A5: हाँ, आप [यहाँ](https://releases.aspose.com/) से मुफ्त ट्रायल के साथ लाइब्रेरी का अन्वेषण कर सकते हैं।

### Q6: क्या `adjustBrightness` मेथड लेयर विज़िबिलिटी को प्रभावित करता है?

A6: यह मेथड रास्टराइज़्ड कॉम्पोजिट इमेज पर काम करता है, इसलिए लेयर विज़िबिलिटी रास्टराइज़ेशन के दौरान सम्मानित रहती है।

### Q7: क्या मैं कई एडजस्टमेंट (जैसे, कॉन्ट्रास्ट, सैचुरेशन) को एक साथ चेन कर सकता हूँ?

A7: बिल्कुल। चमक समायोजित करने के बाद आप उसी `RasterImage` इंस्टेंस पर `adjustContrast`, `adjustSaturation` आदि को कॉल कर सकते हैं।

---

**अंतिम अपडेट:** 2025-12-19  
**टेस्टेड विथ:** Aspose.PSD for Java 24.12 (लेखन समय पर नवीनतम)  
**लेखक:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}