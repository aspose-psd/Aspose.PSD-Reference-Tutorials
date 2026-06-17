---
date: 2026-03-28
description: Aspose.PSD for Java का उपयोग करके फोटो फ़िल्टर लेयर बनाना और एडजस्टमेंट
  लेयर PSD फ़ाइलें जोड़ना सीखें। सहजता से फ़िल्टर संपादित करने और जोड़ने के लिए इस
  गाइड का पालन करें।
linktitle: How to Create Photo Filter Layer in PSD Using Java
second_title: Aspose.PSD Java API
title: जावा का उपयोग करके PSD में फोटो फ़िल्टर लेयर कैसे बनाएं
url: /hi/java/psd-image-modification-conversion/manage-photo-filter-adjustment-layer-psd/
weight: 24
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD में फोटो फ़िल्टर एडजस्टमेंट लेयर प्रबंधित करें - जावा

## परिचय
यदि आप एक जावा डेवलपर हैं जो PSD फ़ाइलों के भीतर **create photo filter layer** ऑब्जेक्ट बनाना चाहते हैं, तो आप सही जगह पर आए हैं। इस ट्यूटोरियल में हम Aspose.PSD for Java का उपयोग करके मौजूदा Photo Filter Adjustment Layers को संपादित करने और नए जोड़ने की प्रक्रिया देखेंगे। अंत तक, आप बिल्कुल जान जाएंगे कि कैसे **create photo filter layer** बनाएं, उसकी प्रॉपर्टीज़ को समायोजित करें, और यहाँ तक कि **add adjustment layer PSD** फ़ाइलों को प्रोग्रामेटिकली जोड़ें—जिससे आपका ग्राफ़िक‑डिज़ाइन वर्कफ़्लो तेज़ हो जाएगा।

## त्वरित उत्तर
- **जावा में PSD लेयर्स को संभालने वाली लाइब्रेरी कौन सी है?** Aspose.PSD for Java  
- **क्या मैं मौजूदा Photo Filter लेयर को संपादित कर सकता हूँ?** हाँ – PSD लोड करें, `PhotoFilterLayer` को खोजें, फिर उसकी प्रॉपर्टीज़ को संशोधित करें।  
- **मैं नया फ़िल्टर लेयर कैसे जोड़ूँ?** उपयोग करें `addPhotoFilterLayer(Color)` को `PsdImage` इंस्टेंस पर।  
- **क्या उत्पादन के लिए मुझे लाइसेंस चाहिए?** एक व्यावसायिक लाइसेंस आवश्यक है; एक मुफ्त ट्रायल उपलब्ध है।  
- **कौन सा जावा संस्करण समर्थित है?** JDK 8 या उससे ऊपर (JDK 11 की सिफ़ारिश की जाती है)।

## Photo Filter Adjustment Layer क्या है?
Photo Filter Adjustment Layer एक नॉन‑डिस्ट्रक्टिव इफ़ेक्ट है जो चुने हुए रंग से पूरी इमेज को टिंट करता है, जैसे फ़ोटोग्राफ़िक फ़िल्टर लागू करना। यह अपनी स्वयं की लेयर पर रहता है, जिससे आप रंग, घनत्व, और चमक को मूल पिक्सेल को बदले बिना समायोजित कर सकते हैं।

## फ़ोटो फ़िल्टर लेयर बनाने के लिए Aspose.PSD का उपयोग क्यों करें?
- **Full control** Adobe Photoshop के बिना PSD संरचना पर पूर्ण नियंत्रण।  
- **Cross‑platform** Java API Windows, Linux, और macOS पर काम करता है।  
- **No COM interop** – शुद्ध जावा, सर्वर‑साइड प्रोसेसिंग के लिए आदर्श।  
- **Supports PSD version 1‑8**, लेयर इफ़ेक्ट्स और मास्क को संरक्षित रखता है।

## पूर्वापेक्षाएँ
### आवश्यक सॉफ़्टवेयर
1. Java Development Kit (JDK): सुनिश्चित करें कि आपके मशीन पर संगत संस्करण का JDK स्थापित है। आप इसे [Oracle's website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) से डाउनलोड कर सकते हैं।  
2. Aspose.PSD for Java: PSD फ़ाइलों को हेरफेर करने के लिए आपको Aspose.PSD लाइब्रेरी की आवश्यकता होगी। आप इसे [Aspose releases page](https://releases.aspose.com/psd/java/) से डाउनलोड कर सकते हैं। अधिक विवरण के लिए [Aspose documentation](https://reference.aspose.com/psd/java/) देखना न भूलें।  
3. IDE (Integrated Development Environment): IntelliJ IDEA या Eclipse जैसे अच्छे IDE से आपका कोडिंग अनुभव सुगम होगा।

### बुनियादी समझ
Java प्रोग्रामिंग की परिचितता और PSD फ़ाइलों के काम करने के तरीके की बुनियादी समझ उपयोगी होगी। यदि आप जावा में लाइब्रेरीज़ का उपयोग करने में नए हैं, तो फ्रेमवर्क्स को इम्पोर्ट और उपयोग करने की आदत डालना अच्छा रहेगा।

## पैकेज इम्पोर्ट करें
शुरू करने के लिए, हमें Aspose.PSD लाइब्रेरी से आवश्यक क्लासेज़ इम्पोर्ट करने की जरूरत है। यहाँ एक सरल इम्पोर्ट स्टेटमेंट है जिसे आपको अपनी जावा फ़ाइल की शुरुआत में जोड़ना होगा:
```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.PhotoFilterLayer;
```
इसे अपनी जावा फ़ाइल के शीर्ष पर पेस्ट करें, और आप PSD इमेज़ के साथ काम करने के लिए तैयार हैं!

## मौजूदा Photo Filter लेयर संपादित करना
### चरण 1: डेटा डायरेक्टरी सेट करें
सबसे पहले, आपको वह डायरेक्टरी परिभाषित करनी होगी जहाँ आपके PSD फ़ाइलें संग्रहीत हैं। `"Your Document Directory"` को वास्तविक पाथ से बदलें। इस प्रकार आप सब कुछ व्यवस्थित कर सकते हैं:
```java
String dataDir = "Your Document Directory";
```

### चरण 2: अपनी PSD फ़ाइल लोड करें
अब, चलिए उस PSD फ़ाइल को लोड करते हैं जिसे आप संपादित करना चाहते हैं। सुनिश्चित करें कि `PhotoFilterAdjustmentLayer.psd` आपके निर्दिष्ट डायरेक्टरी में मौजूद है।
```java
String sourceFileName = dataDir + "PhotoFilterAdjustmentLayer.psd";
```

### चरण 3: इमेज ऑब्जेक्ट को इनिशियलाइज़ करें
Aspose की बिल्ट‑इन फ़ंक्शनैलिटी का उपयोग करके, हम इमेज को अपने प्रोजेक्ट में लोड करते हैं:
```java
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

### चरण 4: लेयर्स के माध्यम से इटरेट करें
अब हम PSD फ़ाइल के भीतर लेयर्स की जाँच करेंगे। हमारा लक्ष्य `PhotoFilterLayer` को ढूँढना है:
```java
for(int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof PhotoFilterLayer) {
        PhotoFilterLayer photoLayer = (PhotoFilterLayer) im.getLayers()[i];
        // Make changes to the layer
    }
}
```

### चरण 5: Photo Filter लेयर को कस्टमाइज़ करें
यहीं पर जादू होता है! आप `Color` और `Density` को संशोधित कर सकते हैं। उदाहरण के लिए, हम रंग को एक चमकीले लाल में सेट कर सकते हैं और घनत्व को समायोजित कर सकते हैं:
```java
photoLayer.setColor(Color.fromArgb(255, 60, 60));
photoLayer.setDensity(78);
photoLayer.setPreserveLuminosity(false);
```

### चरण 6: संपादित PSD फ़ाइल को सहेजें
अंत में, अपने बदलावों को सहेजें ताकि एक नई PSD फ़ाइल आपके एडजस्टमेंट्स के साथ बन सके:
```java
String psdPathAfterChange = dataDir + "PhotoFilterAdjustmentLayerChanged.psd";
im.save(psdPathAfterChange);
```
आपने अभी एक PSD फ़ाइल में Photo Filter Adjustment Layer को संपादित किया है।

## नया Photo Filter लेयर जोड़ना
### चरण 1: डायरेक्टरी पाथ सेट करें
पहले की तरह, हम अपने डेटा डायरेक्टरी को परिभाषित करके शुरू करते हैं:
```java
String dataDir = "Your Document Directory";
```

### चरण 2: स्रोत फ़ाइल लोड करें
इस उदाहरण के लिए, चलिए एक अलग PSD फ़ाइल लोड करते हैं जहाँ हम **add adjustment layer PSD** जोड़ना चाहते हैं:
```java
String sourceFileName = dataDir + "PhotoExample.psd";
```

### चरण 3: इमेज ऑब्जेक्ट को फिर से इनिशियलाइज़ करें
हमें एक नया `PsdImage` इंस्टेंस बनाना होगा, इसलिए हम फ़ाइल को लोड करते हैं:
```java
PsdImage img = (PsdImage) Image.load(sourceFileName);
```

### चरण 4: Photo Filter लेयर जोड़ें
अब, हम एक कस्टम रंग के साथ नया Photo Filter लेयर जोड़ सकते हैं। यह इस प्रकार किया जाता है:
```java
PhotoFilterLayer layer = img.addPhotoFilterLayer(Color.fromArgb(25, 255, 35));
```

### चरण 5: नई PSD फ़ाइल सहेजें
फिर से, हमारे बदलावों को सहेजने का समय है। यहाँ वह लाइन है जो यह करती है:
```java
String psdPathAfterChange = dataDir + "PhotoExampleAddedPhotoFilter.psd";
img.save(psdPathAfterChange);
```
आपने सफलतापूर्वक अपने PSD फ़ाइल में नया फोटो फ़िल्टर लेयर जोड़ दिया है।

## सामान्य समस्याएँ और समाधान
- **`ClassCastException` when loading the image** – सुनिश्चित करें कि आप जो फ़ाइल लोड कर रहे हैं वह PSD है; अन्य फ़ॉर्मेट्स के लिए अलग क्लासेज़ की आवश्यकता होती है।  
- **Color values appear incorrect** – `Color.fromArgb(alpha, red, green, blue)` का उपयोग करें जहाँ प्रत्येक घटक 0‑255 हो।  
- **Layer not found** – पुष्टि करें कि स्रोत PSD वास्तव में `PhotoFilterLayer` रखता है। डिबग करने के लिए `im.getLayers().length` का उपयोग करें।

## अक्सर पूछे जाने वाले प्रश्न
### Aspose.PSD क्या है?
Aspose.PSD एक .NET और जावा लाइब्रेरी है जो PSD फ़ाइलों को बनाने, संपादित करने और कनवर्ट करने के लिए उपयोग होती है।

### क्या मैं Aspose.PSD को मुफ्त में आज़मा सकता हूँ?
हाँ, Aspose एक मुफ्त ट्रायल संस्करण प्रदान करता है। इसे यहाँ देखें [here](https://releases.aspose.com/)।

### दस्तावेज़ीकरण कहाँ मिल सकता है?
आप पूरी दस्तावेज़ीकरण [Aspose's reference page](https://reference.aspose.com/psd/java/) पर पा सकते हैं।

### मैं Aspose.PSD कैसे खरीद सकता हूँ?
आप सॉफ़्टवेयर को [this link](https://purchase.aspose.com/buy) से खरीद सकते हैं।

### क्या Aspose.PSD के लिए समर्थन उपलब्ध है?
बिल्कुल! आप Aspose समर्थन फ़ोरम के माध्यम से समर्थन प्राप्त कर सकते हैं [here](https://forum.aspose.com/c/psd/34)।

---

**अंतिम अपडेट:** 2026-03-28  
**परीक्षित संस्करण:** Aspose.PSD for Java 24.11 (2026 तक नवीनतम)  
**लेखक:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}