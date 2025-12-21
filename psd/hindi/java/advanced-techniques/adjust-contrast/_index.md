---
date: 2025-12-21
description: Aspose.PSD for Java, एक प्रमुख जावा इमेज मैनिपुलेशन लाइब्रेरी का उपयोग
  करके छवियों का कंट्रास्ट कैसे समायोजित करें, और PSD को TIFF में कुशलतापूर्वक परिवर्तित
  करें, यह सीखें।
linktitle: Adjust Contrast of an Image
second_title: Aspose.PSD Java API
title: Aspose.PSD for Java के साथ एक छवि का कंट्रास्ट कैसे समायोजित करें
url: /hi/java/advanced-techniques/adjust-contrast/
weight: 22
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java के साथ छवि का कंट्रास्ट कैसे समायोजित करें

## परिचय

यदि आप अपने Java प्रोजेक्ट्स में **how to adjust contrast** खोज रहे हैं, तो आप सही जगह पर आए हैं। Aspose.PSD for Java एक शक्तिशाली **java image manipulation library** है जो आपको कंट्रास्ट, ब्राइटनेस और अन्य गुणों को बारीकी से समायोजित करने की सुविधा देती है। इस ट्यूटोरियल में हम PSD फ़ाइल का कंट्रास्ट बढ़ाने के सटीक चरणों को दिखाएंगे और फिर **convert PSD to TIFF** को डाउनस्ट्रीम वर्कफ़्लोज़ के लिए करेंगे।

## त्वरित उत्तर
- **What does “adjust contrast” mean?** यह सबसे गहरे और सबसे उज्ज्वल पिक्सेल के बीच के अंतर को बदलता है, जिससे विवरण उभर कर सामने आते हैं।
- **Which library handles this?** Aspose.PSD for Java – एक पूर्ण‑फ़ीचर वाला इमेज प्रोसेसिंग टूलकिट।
- **Do I need a license?** परीक्षण के लिए एक टेम्पररी लाइसेंस काम करता है; प्रोडक्शन के लिए पूर्ण लाइसेंस आवश्यक है।
- **Can I save the result as TIFF?** हाँ, हम प्रोसेस्ड इमेज को एक्सपोर्ट करने के लिए `TiffOptions` का उपयोग करेंगे।
- **How long does the code take to run?** सामान्य‑आकार की PSD फ़ाइलों के लिए आमतौर पर एक सेकंड से कम समय लेता है।

## कंट्रास्ट समायोजन क्या है?

कंट्रास्ट समायोजन एक छवि की टोनल रेंज को बदलता है, प्रकाश और अंधेरे क्षेत्रों के बीच अंतर को बढ़ाता है। यह विशेष रूप से तब उपयोगी होता है जब स्कैनिंग के बाद छवियां सपाट दिखती हैं या प्रिंट के लिए ग्राफिक्स तैयार करते समय।

## Aspose.PSD for Java क्यों उपयोग करें?

- **Rich format support** – PSD, TIFF, PNG, JPEG और कई अन्य फ़ॉर्मैट को खोलें, संपादित करें और सहेजें।
- **High performance** – कैशिंग और रास्टर‑इमेज ऑप्टिमाइज़ेशन मेमोरी ओवरहेड को कम करते हैं।
- **Straight‑forward API** – `adjustContrast` जैसी सिंगल‑मेथड कॉल्स कोड को पढ़ने योग्य बनाती हैं।

## पूर्वापेक्षाएँ

शुरू करने से पहले, सुनिश्चित करें कि आपके पास है:

- जावा प्रोग्रामिंग का बुनियादी ज्ञान।
- Aspose.PSD for Java लाइब्रेरी स्थापित है। आप इसे [यहाँ](https://releases.aspose.com/psd/java/) डाउनलोड कर सकते हैं।

## पैकेज इम्पोर्ट करें

अपने जावा क्लास में आवश्यक इम्पोर्ट जोड़ें:

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

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);
```

हम स्रोत PSD फ़ाइल (`sample.psd`) को एक `Image` ऑब्जेक्ट में लोड करते हैं, जो आगे की सभी प्रोसेसिंग के लिए एंट्री पॉइंट के रूप में कार्य करता है।

## चरण 2: RasterImage में कास्ट करें और डेटा कैश करें

```java
// Cast object of Image to RasterImage
RasterImage rasterImage = (RasterImage)image;

// Check if RasterImage is cached and Cache RasterImage for better performance
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

`RasterImage` में कास्ट करने से हमें पिक्सेल‑लेवल ऑपरेशन्स तक पहुंच मिलती है। कैशिंग प्रदर्शन को सुधारती है, विशेष रूप से बड़े फ़ाइलों के लिए।

## छवि का कंट्रास्ट कैसे समायोजित करें

```java
// Adjust the contrast
rasterImage.adjustContrast(50);
```

`adjustContrast` मेथड एक पूर्णांक लेता है जो प्रतिशत परिवर्तन को दर्शाता है। इस उदाहरण में हम कंट्रास्ट को **50 %** बढ़ाते हैं।

## Aspose.PSD का उपयोग करके PSD को TIFF में कनवर्ट करें

```java
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);

// Save the resultant image to TIFF format
String destName = dataDir + "AdjustContrast_out.tiff";
rasterImage.save(destName, tiffOptions);
```

यहाँ हम `TiffOptions` (बिट्स प्रति सैंपल, फोटोमेट्रिक इंटरप्रिटेशन) को कॉन्फ़िगर करते हैं और कंट्रास्ट‑बढ़ी हुई छवि को TIFF फ़ाइल में लिखते हैं।

## सामान्य समस्याएँ और समाधान
- **Image not cached:** बड़े PSDs के लिए हमेशा `cacheData()` कॉल करें ताकि `OutOfMemoryError` से बचा जा सके।
- **Unexpected color shift:** सुनिश्चित करें कि `setPhotometric` आपके लक्ष्य कलर स्पेस (RGB बनाम CMYK) से मेल खाता है।
- **File not found:** सुनिश्चित करें कि `dataDir` सही फ़ोल्डर की ओर इशारा कर रहा है और फ़ाइल नाम सही लिखा गया है।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या Aspose.PSD विभिन्न इमेज फ़ॉर्मैट्स के साथ संगत है?
A1: हाँ, Aspose.PSD विभिन्न इमेज फ़ॉर्मैट्स को सपोर्ट करता है, जिससे आपके प्रोजेक्ट्स में लचीलापन मिलता है।

### Q2: मैं Aspose.PSD के लिए टेम्पररी लाइसेंस कैसे प्राप्त कर सकता हूँ?
A2: आप टेम्पररी लाइसेंस [यहाँ](https://purchase.aspose.com/temporary-license/) प्राप्त कर सकते हैं।

### Q3: मैं Aspose.PSD दस्तावेज़ीकरण कहाँ पा सकता हूँ?
A3: दस्तावेज़ीकरण [यहाँ](https://reference.aspose.com/psd/java/) उपलब्ध है।

### Q4: Aspose.PSD के लिए कौन‑से सपोर्ट विकल्प उपलब्ध हैं?
A4: सपोर्ट के लिए, [Aspose.PSD फ़ोरम](https://forum.aspose.com/c/psd/34) पर जाएँ।

### Q5: क्या मैं Aspose.PSD खरीद सकता हूँ?
A5: हाँ, आप Aspose.PSD [यहाँ](https://purchase.aspose.com/buy) खरीद सकते हैं।

## निष्कर्ष

अब आप Aspose.PSD for Java का उपयोग करके PSD छवि का **how to adjust contrast** और आगे की प्रोसेसिंग के लिए **convert PSD to TIFF** करना जानते हैं। ये चरण आपको इमेज क्वालिटी पर सूक्ष्म नियंत्रण देते हैं जबकि कोड साफ़ और मेंटेनेबल रहता है। आप `adjustBrightness` या `adjustGamma` जैसे अन्य इमेज‑एडजस्टमेंट मेथड्स के साथ प्रयोग कर सकते हैं ताकि आपकी विशिष्ट आवश्यकताओं को पूरा किया जा सके।

---

**अंतिम अद्यतन:** 2025-12-21  
**परीक्षण किया गया:** Aspose.PSD for Java 24.12  
**लेखक:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}