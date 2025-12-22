---
date: 2025-12-21
description: Aspose.PSD के साथ इमेज गामा को समायोजित करके जावा इमेज प्रोसेसिंग कैसे
  करें, सीखें। PSD को TIFF में बदलने और गामा सुधार लागू करने के लिए चरण‑दर‑चरण गाइड।
linktitle: Adjust Gamma of an Image
second_title: Aspose.PSD Java API
title: जावा इमेज प्रोसेसिंग – Aspose.PSD के साथ गामा समायोजित करें
url: /hi/java/advanced-techniques/adjust-gamma/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java इमेज प्रोसेसिंग – Aspose.PSD के साथ गामा एडजस्ट करें

## परिचय

यदि आप **java image processing** पर काम कर रहे हैं, तो किसी चित्र का गामा समायोजित करना एक बुनियादी तकनीक है जिससे आप विवरण खोए बिना चमक और कंट्रास्ट को सुधार सकते हैं। इस ट्यूटोरियल में हम देखेंगे कि **Aspose.PSD for Java** का उपयोग करके PSD फ़ाइल पर गामा करेक्शन कैसे लागू किया जाए और फिर परिणाम को TIFF इमेज के रूप में एक्सपोर्ट किया जाए। आप समझेंगे कि यह तरीका तेज़, भरोसेमंद और सर्वर‑साइड इमेज पाइपलाइन के लिए परफ़ेक्ट क्यों है।

## क्विक आंसर
- **What does gamma correction do?** यह ल्यूमिनेंस वैल्यूज़ को रीमैप करता है ताकि डार्क एरिया उज्ज्वल हों या ब्राइट एरिया डार्क हों, जबकि कुल मिलाकर विवरण बरकरार रहे।  
- **Which library handles the processing?** Aspose.PSD for Java रास्टर इमेजेज़ के लिए एक समर्पित `adjustGamma` मेथड प्रदान करता है।  
- **Can I convert PSD to TIFF in the same flow?** हाँ – गामा समायोजन के बाद आप सीधे `TiffOptions` का उपयोग करके इमेज को TIFF में सेव कर सकते हैं।  
- **Do I need a license for development?** परीक्षण के लिए एक फ्री ट्रायल काम करता है; प्रोडक्शन उपयोग के लिए एक कमर्शियल लाइसेंस आवश्यक है।  
- **What Java version is supported?** Aspose.PSD Java 8 और उसके बाद के संस्करणों को सपोर्ट करता है।

## जावा इमेज प्रोसेसिंग क्या है?

Java image processing का अर्थ है जावा लाइब्रेरीज़ का उपयोग करके विज़ुअल डेटा का हेरफेर, विश्लेषण और रूपांतरण। कार्यों में री-साइज़िंग, फ़िल्टरिंग, कलर करेक्शन और फ़ॉर्मेट कन्वर्ज़न शामिल हैं—इन सभी को डेस्कटॉप या वेब एप्लिकेशन में ऑटोमेट किया जा सकता है।

## गामा करेक्शन के लिए Aspose.PSD का इस्तेमाल क्यों करें?

Aspose.PSD एक हाई‑लेवल API प्रदान करता है जो PSD फ़ॉर्मेट की जटिलता को एब्स्ट्रैक्ट कर देता है, जिससे आप वास्तविक इमेज समायोजन पर ध्यान केंद्रित कर सकते हैं। यह कैशिंग, कलर प्रोफ़ाइल्स को संभालता है और एक सरल `adjustGamma` कॉल प्रदान करता है, जिससे **image gamma correction** और **convert psd to tiff** वर्कफ़्लो के लिए यह आदर्श बनता है।

## ज़रूरी शर्तें

ट्यूटोरियल शुरू करने से पहले सुनिश्चित करें कि आपके पास निम्नलिखित प्री‑रिक्विज़िट्स सेट हैं:

1. **Java Development Environment** – सुनिश्चित करें कि आपके सिस्टम पर जावा डेवलपमेंट एनवायरनमेंट इंस्टॉल है।  
2. **Aspose.PSD Library** – Aspose.PSD लाइब्रेरी को डाउनलोड करके अपने जावा प्रोजेक्ट में इंटीग्रेट करें। आवश्यक संसाधन आप [documentation](https://reference.aspose.com/psd/java/) में पा सकते हैं।  
3. **Sample Image** – एक सैंपल PSD इमेज तैयार रखें जिसे आप गामा एडजस्टमेंट के लिए उपयोग करेंगे।

## पैकेज आयात करें

प्रक्रिया शुरू करने के लिए, अपने जावा प्रोजेक्ट में आवश्यक पैकेज इम्पोर्ट करें। यह Aspose.PSD फ़ंक्शनैलिटी को सहजता से उपयोग करने के लिए मंच तैयार करता है।

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## स्टेप 1: इमेज लोड करें

सैंपल PSD इमेज को `RasterImage` क्लास की एक इंस्टेंस में लोड करें। यह आगे के गामा समायोजन का आधार होगा।

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);

// Cast object of Image to RasterImage
RasterImage rasterImage = (RasterImage)image;

// Check if RasterImage is cached for better performance
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

## स्टेप 2: गामा एडजस्ट करें

अब, लोड की गई इमेज पर `adjustGamma` मेथड का उपयोग करके गामा समायोजित करें। अपनी आवश्यकताओं के अनुसार गामा वैल्यूज़ को फाइन‑ट्यून करें।

```java
// Adjust the gamma
rasterImage.adjustGamma(2.2f, 2.2f, 2.2f);
```

## स्टेप 3: TiffOptions बनाएं

परिणामी इमेज के लिए `TiffOptions` की एक इंस्टेंस बनाएं। विभिन्न प्रॉपर्टीज़ सेट करें, जैसे बिट्स पर सैंपल और फोटोमेट्रिक ऑप्शन, ताकि आउटपुट को अपनी विशिष्टताओं के अनुसार कस्टमाइज़ किया जा सके।

```java
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

## स्टेप 4: रिज़ल्टेंट इमेज सेव करें

पहले परिभाषित `TiffOptions` का उपयोग करके मैनिपुलेटेड इमेज को TIFF फ़ॉर्मेट में सेव करें।

```java
// Save the resultant image to TIFF format
String destName = dataDir + "AdjustGamma_out.tiff";
rasterImage.save(destName, tiffOptions);
```

## आम मुद्दे और समाधान

| समस्या | ऐसा क्यों होता है | कैसे ठीक करें |
|-------|----------------|-------|
| **इमेज धुंधली दिखती है** | गामा वैल्यू बहुत ज़्यादा है (जैसे, > 2.5) | गामा फैक्टर को 1.8 और 2.2 के बीच की वैल्यू पर कम करें। |
| **`rasterImage.isCached()` गलत रिटर्न करता है** | इमेज अभी मेमोरी में लोड नहीं हुई है | गामा एडजस्ट करने से पहले `rasterImage.cacheData()` को कॉल करें। |
| **TIFF फ़ाइल का साइज़ बड़ा है** | हर सैंपल के बिट्स 16‑bit पर सेट हैं | उदाहरण में दिखाए गए अनुसार 8‑bit सैंपल (`{8,8,8}`) का इस्तेमाल करें। |

## अक्सर पूछे जाने वाले सवाल

**सवाल: क्या मैं हर कलर चैनल पर अलग-अलग गामा वैल्यू लगा सकता हूँ?**
जवाब: हाँ – `adjustGamma` मेथड रेड, ग्रीन और ब्लू चैनल के लिए अलग-अलग फ्लोट वैल्यू लेता है।

**सवाल: क्या सेव करने से पहले कई इमेज एडजस्टमेंट को चेन करना मुमकिन है?**
जवाब: बिल्कुल। आप एक ही `RasterImage` इंस्टेंस पर एक के बाद एक साइज़ बदलना, क्रॉप करना या कलर करेक्शन कर सकते हैं।

**सवाल: क्या Aspose.PSD मल्टी-पेज PSD फ़ाइलों को सपोर्ट करता है?**
जवाब: हाँ, हर लेयर को अलग-अलग एक्सेस और प्रोसेस किया जा सकता है।

**सवाल: TIFF के अलावा मैं किस फ़ॉर्मेट में एक्सपोर्ट कर सकता हूँ?**
जवाब: Aspose.PSD PNG, JPEG, BMP, और कई दूसरे फ़ॉर्मेट को उनके अपने ऑप्शन क्लास के ज़रिए सपोर्ट करता है।

## नतीजा

बधाई हो! आपने **java image processing** को सफलतापूर्वक किया है, PSD फ़ाइल का गामा समायोजित करके और Aspose.PSD for Java का उपयोग करके इसे TIFF इमेज के रूप में एक्सपोर्ट किया है। यह वर्कफ़्लो आपको इमेज की ब्राइटनेस और कंट्रास्ट पर सूक्ष्म नियंत्रण देता है, जिससे यह ऑटोमेटेड ग्राफ़िक्स पाइपलाइन, वेब सर्विसेज़ या डेस्कटॉप यूटिलिटीज़ के लिए आदर्श बनता है।

---
**पिछला अपडेट:** 2025-12-21
**इसके साथ टेस्ट किया गया:** Java के लिए Aspose.PSD 24.11
**लेखक:** Aspose

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
