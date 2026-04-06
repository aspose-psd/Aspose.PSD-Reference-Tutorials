---
date: 2025-12-30
description: Aspose.PSD का उपयोग करके दो छवियों को मिलाकर जावा में PSD फ़ाइल बनाना
  सीखें। तेज़ी से छवियों को PSD फ़ाइल में मर्ज करने के लिए हमारी चरण‑दर‑चरण गाइड का
  पालन करें।
linktitle: Combine Images
second_title: Aspose.PSD Java API
title: Java में PSD फ़ाइल कैसे बनाएं – Aspose.PSD के साथ छवियों को संयोजित करें
url: /hi/java/image-editing/combine-images/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java में PSD फ़ाइल बनाएँ – Aspose.PSD का इस्तेमाल करके इमेज को मिलाएँ

## परिचय

यदि आपको **Java में PSD फ़ाइल बनानी है** कई इमेज को मिलाकर, तो Aspose.PSD इस काम को आसान बनाता है। इस ट्यूटोरियल में हम दो इमेज को एक ही PSD कैनवास में जोड़ने की प्रक्रिया को दिखाएंगे, यह समझाएंगे कि यह तरीका क्यों उपयोगी है, और तैयार करने वाला कोड देंगे। अंत में आप **Java स्टाइल में दो इमेज को मिलाकर** एक प्रोफ़ेशनल-लुकिंग लेयर्ड फ़ाइल बना पाएँगे।

## क्विक आंसर
- **क्या लाइब्रेरी इमेज को PSD में मिलाने के लिए सबसे अच्छी है?** Aspose.PSD for Java.
- **इम्प्लीमेंटेशन में कितना समय लगेगा?** बेसिक कॉम्बिनेशन के लिए लगभग 10‑15 मिनट।
- **क्या लाइसेंस चाहिए?** टेस्टिंग के लिए फ्री ट्रायल चलती है; प्रोडक्शन के लिए आउटपुट लाइसेंस ज़रूरी है।
- **क्या दो से ज़्यादा इमेज जोड़ सकते हैं?** हाँ – हर एक्स्ट्रा लेयर के लिए `drawImage` कॉल को डबल करेंगी.

- **कौन सा Java वर्जन सपोर्टेड है?** Java8 और उसके बाद के वर्जन.

## ज़रूरी शर्तें

शुरू करने से पहले पक्का करें कि आपके पास ये हैं:

1. **Aspose.PSD Library** – इसे [here](https://releases.aspose.com/psd/java/) से डाउनलोड करें।
2. **Java Development Kit (JDK)** – Java8+ की सलाह दी जाती है।
3. **Document Directory** – आपकी मशीन पर एक फोल्डर जहाँ सोर्स इमेज और आउटपुट PSD फाइलें होंगे.

## पैकेज इंपोर्ट करें

अपने प्रोजेक्ट में आवश्यक Aspose.PSD क्लासेज़ को इम्पोर्ट करें:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;

import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.sources.FileCreateSource;
```

## स्टेप-बाय-स्टेप गाइड

### स्टेप 1: PSD ऑप्शन बनाएं (फ़ाइल तैयार करें)

सबसे पहले हम एक `PsdOptions` इंस्टेंस बनाते हैं जो आउटपुट सेटिंग्स को रखेगा।

```java
PsdOptions imageOptions = new PsdOptions();
```

### स्टेप 2: FileCreateSource सेट करें (तय करें कि PSD कहाँ सेव होगा)

ऑप्शन्स में एक `FileCreateSource` असाइन करें, जो इच्छित परिणाम फ़ाइल की ओर इशारा करेगा।

```java
imageOptions.setSource(new FileCreateSource(dataDir + "Two_images_result_out.psd", false));
```

### स्टेप 3: इमेज इंस्टेंस बनाएँ (कैनवस साइज़ इनिशियलाइज़ करें)

`Image` ऑब्जेक्ट को ऑप्शन्स के साथ बनाएं और 600 × 600 पिक्सेल का कैनवास निर्धारित करें।

```java
Image image = Image.create(imageOptions, 600, 600);
```

### स्टेप 4: ग्राफ़िक्स इनिशियलाइज़ करें और पहली पिक्चर बनाएँ

एक `Graphics` ऑब्जेक्ट हमें कैनवास पर पेंट करने देता है। हम बैकग्राउंड को सफ़ेद साफ़ करते हैं और पहले स्रोत इमेज को बाएँ आधे हिस्से में ड्रॉ करते हैं।

```java
Graphics graphics = new Graphics(image);
graphics.clear(Color.getWhite());
graphics.drawImage(Image.load(dataDir + "example1.psd"), 0, 0, 300, 600);
```

### स्टेप 5: दूसरी पिक्चर बनाएँ (कम्बाइन पूरा करें)

अब हम उसी कैनवास के दाएँ आधे हिस्से में दूसरी इमेज रखेंगे।

```java
graphics.drawImage(Image.load(dataDir + "example2.psd"), 300, 0, 300, 600);
```

### स्टेप 6: रिज़ल्टिंग PSD फ़ाइल सेव करें

अंत में, संयुक्त कैनवास को डिस्क पर सेव करें।

```java
image.save();
```

बधाई हो! आपने सफलतापूर्वक **इमेज को PSD में मर्ज** किया और Java में एक PSD फ़ाइल बनाई।

## इमेज को Aspose.PSD के साथ क्यों मिलाएं?

- **Layer‑aware** – हर `drawImage` कॉल एक अलग लेयर जोड़ता है जिसे बाद में एडिट किया जा सकता है।
- **फॉर्मेट फ्लेक्सिबिलिटी** – PSD, PNG, JPEG, BMP, और कई दूसरे फॉर्मेट सपोर्ट करता है।
- **कोई नेटिव डिपेंडेंसी नहीं** – शुद्ध Java, किसी भी OS पर चलाने लायक जहाँ JDK उपलब्ध है।

## आम दिक्कतें और समाधान

| दिक्कत | कारण | ठीक करें |
|-------|-------|-----|
| सोर्स इमेज लोड करते समय `File not found` एरर | गलत `dataDir` पाथ | वेरिफाई करें `dataDir` उस फोल्डर की ओर इशारा करता है जिसमें `example1.psd` और `example2.psd` है। |
| आउटपुट PSD खाली है | ड्राइंग के बाद `graphics.clear` को कॉल किया गया | पक्का करें कि किसी भी `drawImage` कॉल से **पहले** `graphics.clear(Color.getWhite())` एग्जीक्यूट हो। |
| रनटाइम पर लाइसेंस एक्सेप्शन | Aspose.PSD लाइसेंस मिसिंग या एक्सपायर हो चुका है | किसी भी API कॉल से पहले `License license = new License(); license.setLicense("Aspose.PSD.lic");` का इस्तेमाल करके एक वैलिड लाइसेंस अप्लाई करें। |

## अक्सर पूछे जाने वाले सवाल

### Q1: क्या Aspose.PSD सभी इमेज फॉर्मेट के साथ कम्पैटिबल है?

A1: Aspose.PSD मुख्य रूप से PSD फाइल फॉर्मेट पर फोकस करता है। हालांकि, यह इनपुट और आउटपुट के लिए कई दूसरे फॉर्मेट को सपोर्ट करता है।

### Q2: क्या मैं कंबाइंड इमेज पर और मॉडिफिकेशन कर सकता हूं?

A2: बिल्कुल! इमेज को कंबाइंड करने के बाद, आप Aspose.PSD के बड़े फीचर्स का इस्तेमाल करके बनने वाले PSD को और मैनिपुलेट कर सकते हैं।

### Q3: क्या Aspose.PSD इस्तेमाल करने के लिए कोई लाइसेंसिंग रिक्वायरमेंट हैं?

A3: हां, कमर्शियल इस्तेमाल के लिए एक वैलिड लाइसेंस ज़रूरी है। इसे [यहां](https://purchase.aspose.com/buy) से पाएं।

### Q4: क्या Aspose.PSD के लिए कोई फ़्री ट्रायल उपलब्ध है?
A4: हां, आप [यहां](https://releases.aspose.com/) फ़्री ट्रायल के साथ Aspose.PSD को एक्सप्लोर कर सकते हैं।

### Q5: मुझे Aspose.PSD से जुड़े सवालों के लिए सपोर्ट कहां मिल सकता है?
A5: कम्युनिटी सपोर्ट और चर्चा के लिए [Aspose.PSD फ़ोरम](https://forum.aspose.com/c/psd/34) पर जाएं।

---

**पिछला अपडेट:** 2025-12-30
**इसके साथ टेस्ट किया गया:** Java के लिए Aspose.PSD 24.11
**लेखक:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}