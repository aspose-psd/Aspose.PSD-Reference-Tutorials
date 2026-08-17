---
date: 2026-03-13
description: Aspose.PSD for Java का उपयोग करके PSD फ़ाइलों में ह्यू सैचुरेशन लेयर
  कैसे जोड़ें, सीखें। यह गाइड यह भी दिखाता है कि कैसे PSD फ़ाइलों को बैच में प्रोसेस
  करें और प्रोग्रामेटिकली ह्यू एडजस्टमेंट लेयर बनाएं।
linktitle: Add Hue Saturation Layer to PSD
second_title: Aspose.PSD Java API
title: Add Hue Saturation Layer to PSD with Aspose.PSD for Java
url: /hi/java/modifying-converting-psd-images/add-hue-saturation-adjustment-layer-psd/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD में ह्यू सैचुरेशन लेयर जोड़ें

## परिचय
ग्राफिक डिज़ाइन में रंग संशोधन एक महत्वपूर्ण भूमिका निभाता है—विशेष रूप से, ह्यू, सैचुरेशन और लाइटनेस को समायोजित करने से किसी भी छवि का मूड और गुणवत्ता काफी बदल सकती है। इसे प्राप्त करने का एक प्रभावी तरीका फ़ोटोशॉप (PSD फ़ाइलें) में एडजस्टमेंट लेयर्स का उपयोग है। यदि आप जावा का उपयोग करके प्रोग्रामेटिक रूप से **add hue saturation layer** जोड़ना चाहते हैं, तो Aspose.PSD लाइब्रेरी मदद के लिए तैयार है! यह ट्यूटोरियल आपको आपके PSD फ़ाइलों में Hue Saturation Adjustment Layer जोड़ने के चरणों के माध्यम से ले जाएगा, जिससे आपका कार्यप्रवाह अधिक उत्पादक और कुशल बन जाएगा।

## त्वरित उत्तर
- **जावा में hue saturation layer जोड़ने वाली लाइब्रेरी कौन सी है?** Aspose.PSD for Java.  
- **क्या मुझे Photoshop स्थापित करना आवश्यक है?** No, the library works independently of Photoshop.  
- **क्या मैं इस विधि से PSD फ़ाइलों को बैच प्रोसेस कर सकता हूँ?** Yes—once you automate the steps you can apply them to many files.  
- **कौन सा जावा संस्करण आवश्यक है?** JDK 8 or later.  
- **क्या उत्पादन उपयोग के लिए लाइसेंस आवश्यक है?** Yes, a commercial license is required after the trial period.  

## “add hue saturation layer” ऑपरेशन क्या है?
एक **add hue saturation layer** ऑपरेशन एक non‑destructive एडजस्टमेंट लेयर बनाता है जो आपको मूल पिक्सेल डेटा को बदले बिना ह्यू, सैचुरेशन और लाइटनेस मानों को संशोधित करने देता है। यह पूरी कंपोज़िशन या विशिष्ट रंग रेंज में रंगों को फाइन‑ट्यून करने के लिए आदर्श है।

## Aspose.PSD for Java का उपयोग क्यों करें?
- **Photoshop निर्भरता नहीं** – works on any platform that runs Java.  
- **पूर्ण PSD सटीकता** – preserves all layer information, masks, and effects.  
- **बैच‑तैयार** – you can loop through folders and apply the same adjustment to dozens of files.  
- **प्रदर्शन‑उन्मुख** – optimized for large documents and server‑side automation.  

## पूर्वापेक्षाएँ
कोड में कूदने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित मौजूद हैं:

1. **Java Development Kit (JDK):** Ensure you have JDK 8 or above installed on your machine. You can download it from the [Java SE Development Kit Downloads](https://www.oracle.com/java/technologies/javase-downloads.html).  
2. **Aspose.PSD for Java Library:** You’ll need to have the Aspose.PSD library, which you can [download here](https://releases.aspose.com/psd/java/).  
3. **IDE:** A suitable Integrated Development Environment (IDE) like IntelliJ IDEA or Eclipse for Java development.  
4. **Basic Java Knowledge:** Familiarity with Java programming is a plus, but don’t worry—we’ll walk you through each line.

अब जब हमारी पूर्वापेक्षाएँ तैयार हैं, चलिए मज़ेदार भाग—कोडिंग—की ओर बढ़ते हैं!

## पैकेज इम्पोर्ट करें
Aspose.PSD लाइब्रेरी के साथ काम शुरू करने के लिए, पहला कदम आवश्यक क्लासेज़ को इम्पोर्ट करना है। यहाँ आप इसे अपने जावा फ़ाइल में कैसे कर सकते हैं:

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.HueSaturationLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.ColorRangeHsl;
```

सुनिश्चित करें कि आपके प्रोजेक्ट में उपयुक्त लाइब्रेरीज़ जोड़ी गई हैं ताकि ये इम्पोर्ट्स सहजता से काम करें।

## चरण 1: अपने डॉक्यूमेंट डायरेक्टरी सेट करें
हर प्रोजेक्ट को एक प्रारंभिक बिंदु चाहिए, और हमारा भी अपवाद नहीं है। आपको वह डायरेक्टरी निर्दिष्ट करनी होगी जहाँ आपके PSD फ़ाइलें संग्रहीत हैं। यह इमेज़ लोड करने और सेव करने के लिए महत्वपूर्ण है।

```java
String dataDir = "Your Document Directory"; // Update this path to your actual directory
```

## चरण 2: मौजूदा PSD फ़ाइल लोड करें
मौजूदा PSD फ़ाइल को संशोधित करने के लिए, हमें पहले इसे अपने प्रोग्राम में लोड करना होगा। यहाँ आप यह कैसे कर सकते हैं:

```java
String sourceFileName = dataDir + "HueSaturationAdjustmentLayer.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

इस कोड में, `"HueSaturationAdjustmentLayer.psd"` को अपनी मौजूदा PSD फ़ाइल के नाम से अपडेट करें जिसे आप संपादित करना चाहते हैं।

## चरण 3: Hue/Saturation लेयर संपादित करें
अगले चरण में, हम लोड किए गए PSD इमेज की लेयर्स के माध्यम से लूप करेंगे ताकि किसी भी मौजूदा Hue/Saturation लेयर को खोजकर संपादित कर सकें। इस चरण में ह्यू, सैचुरेशन और लाइटनेस मानों को संशोधित करना शामिल है।

```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof HueSaturationLayer) {
        HueSaturationLayer hueLayer = (HueSaturationLayer) im.getLayers()[i];
        hueLayer.setHue((short) -25);
        hueLayer.setSaturation((short) -12);
        hueLayer.setLightness((short) 67);
        ColorRangeHsl colorRange = hueLayer.getRange(2);
        colorRange.setHue((short) -40);
        colorRange.setSaturation((short) 50);
        colorRange.setLightness((short) -20);
        colorRange.setMostLeftBorder((short) 300);
    }
}
```

इस उदाहरण में:  
- हम ह्यू को **-25**, सैचुरेशन को **-12**, और लाइटनेस को **+67** पर सेट कर रहे हैं।  
- `getRange(2)` मेथड हमें इच्छानुसार विशिष्ट रंग रेंज को ट्यून करने देता है।

## चरण 4: संशोधित PSD फ़ाइल सहेजें
समायोजन करने के बाद, अगला चरण फ़ाइल को सहेजना है। यह हमारी प्रक्रिया का एक महत्वपूर्ण भाग है, जिससे किए गए बदलाव खो न जाएँ।

```java
String psdPathAfterChange = dataDir + "HueSaturationAdjustmentLayerChanged.psd";
im.save(psdPathAfterChange);
```

## चरण 5: नया Hue/Saturation लेयर जोड़ें
यदि आपको शून्य से **create hue adjustment layer** बनाने की आवश्यकता है, तो आप किसी अन्य PSD फ़ाइल में एक नया Hue/Saturation एडजस्टमेंट लेयर जोड़ सकते हैं। वही लोडिंग पैटर्न अपनाएँ लेकिन `addHueSaturationAdjustmentLayer()` मेथड का उपयोग करें।

```java
sourceFileName = dataDir + "PhotoExample.psd";
PsdImage img = (PsdImage) Image.load(sourceFileName);
HueSaturationLayer hueLayerNew = img.addHueSaturationAdjustmentLayer();
```

## चरण 6: नए लेयर के लिए नए Hue/Saturation मान सेट करें
अब जब आपने यह नया लेयर बना लिया है, तो पहले की तरह इच्छित ह्यू, सैचुरेशन और लाइटनेस सेटिंग्स लागू करें।

```java
hueLayerNew.setHue((short) -25);
hueLayerNew.setSaturation((short) -12);
hueLayerNew.setLightness((short) 67);
ColorRangeHsl newColorRange = hueLayerNew.getRange(2);
newColorRange.setHue((short) -160);
newColorRange.setSaturation((short) 100);
newColorRange.setLightness((short) 20);
newColorRange.setMostLeftBorder((short) 300);
```

## चरण 7: अपडेटेड PSD फ़ाइल सहेजें
अंत में, जोड़ा गया Hue/Saturation लेयर के साथ PSD फ़ाइल को सहेजें ताकि आप अपने बदलाव देख सकें।

```java
String psdPathAfterNewLayerChange = dataDir + "PhotoExampleAddedHueSaturation.psd";
img.save(psdPathAfterNewLayerChange);
```

बधाई हो! आपने Aspose.PSD for Java का उपयोग करके सफलतापूर्वक PSD फ़ाइलों को संशोधित किया है। अब आप विभिन्न इमेज़ और गहरी बदलावों के साथ प्रयोग कर सकते हैं, जिससे आपके ग्राफिक डिज़ाइन प्रोजेक्ट जीवंत हो जाएंगे।

## ह्यू समायोजन के साथ PSD फ़ाइलों को बैच प्रोसेस कैसे करें
क्योंकि ऊपर दिया गया कोड पूरी तरह स्क्रिप्टेबल है, आप पूरे क्रम को एक लूप में रख सकते हैं जो किसी फ़ोल्डर में प्रत्येक `.psd` फ़ाइल पर इटररेट करता है। इससे आप **batch process psd files** कर सकते हैं और एक ही रन में समान ह्यू, सैचुरेशन और लाइटनेस समायोजन लागू कर सकते हैं—बड़े‑पैमाने पर ब्रांडिंग अपडेट के लिए उपयुक्त।

## सामान्य समस्याएँ और समाधान
- **फ़ाइल लोड करते समय NullPointerException:** Verify that `dataDir` ends with the appropriate file‑separator (`/` or `\`) and that the file name is correct.  
- **Adjustment values out of range:** Hue, saturation, and lightness accept values from -255 to 255. Keep your numbers within this range.  
- **Layer not found:** If the PSD has no Hue/Saturation layer, the `instanceof` check will skip the block. Use `addHueSaturationAdjustmentLayer()` to create one first.  

## अक्सर पूछे जाने वाले प्रश्न

**Q: Hue Saturation Adjustment Layer क्या है?**  
A: यह आपको किसी छवि के रंग गुणों को मूल पिक्सेल को स्थायी रूप से बदले बिना संशोधित करने की अनुमति देता है।

**Q: Aspose.PSD उपयोग करने के लिए क्या मुझे Photoshop स्थापित करना आवश्यक है?**  
A: No, Aspose.PSD is a standalone library that works independently of Photoshop.

**Q: क्या मैं Aspose.PSD का उपयोग बैच प्रोसेसिंग के लिए कर सकता हूँ?**  
A: Yes, you can automate and batch process multiple PSD files with Aspose.PSD.

**Q: क्या Aspose.PSD मुफ्त है?**  
A: Aspose.PSD एक मुफ्त ट्रायल प्रदान करता है, लेकिन दीर्घकालिक उपयोग के लिए लाइसेंस आवश्यक है। आप मूल्य निर्धारण यहाँ देख सकते हैं: [here](https://purchase.aspose.com/buy).

## निष्कर्ष
ग्राफिक्स को प्रोग्रामेटिक रूप से संभालना संभावनाओं की एक नई दुनिया खोलता है। Aspose.PSD for Java का उपयोग करके **add hue saturation layer** और **create hue adjustment layer** करने से लचीलापन और दक्षता मिलती है जो आपके डिज़ाइन वर्कफ़्लो को सुव्यवस्थित कर सकती है। चाहे आप किसी प्रोजेक्ट के लिए फ़ोटो को बेहतर बना रहे हों या शानदार विज़ुअल कंटेंट बना रहे हों, इन टूल्स में निपुणता आपके आउटपुट को काफी सुधार सकती है।

Aspose.PSD की अधिक कार्यक्षमताओं का अन्वेषण करने के लिए [documentation](https://reference.aspose.com/psd/java/) में डुबकी लगाएँ या लाइब्रेरी की पूरी शक्ति को परीक्षण करने के लिए एक [temporary license](https://purchase.aspose.com/temporary-license/) प्राप्त करने पर विचार करें।

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**अंतिम अपडेट:** 2026-03-13  
**परीक्षित संस्करण:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**लेखक:** Aspose  

---