---
date: 2026-03-31
description: Aspose.PSD for Java का उपयोग करके PSD को PNG के रूप में सहेजना सीखें।
  यह PSD चैनल मिक्सर ट्यूटोरियल दिखाता है कि PSD को PNG में कैसे बदलें, RGB और CMYK
  लेयर को कैसे संशोधित करें, और PSD फ़ाइलों को बैच में कैसे प्रोसेस करें।
linktitle: Export Channel Mixer Adjustment Layer in PSD - Java
second_title: Aspose.PSD Java API
title: Java में Channel Mixer Adjustment Layer के साथ PSD को PNG के रूप में कैसे सहेजें
url: /hi/java/psd-layer-management-effects/export-channel-mixer-adjustment-layer-psd/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java में Channel Mixer Adjustment Layer के साथ PSD को PNG के रूप में सहेजें

## परिचय

यदि आपको **save PSD as PNG** करना है और Channel Mixer लेयर द्वारा किए गए समायोजनों को बनाए रखना है, तो आप सही जगह पर आए हैं। इस चरण‑दर‑चरण **psd channel mixer tutorial** में, हम एक PSD फ़ाइल लोड करने, दोनों RGB और CMYK Channel Mixer Adjustment Layers को समायोजित करने, और अंत में परिणाम को PNG में निर्यात करने की प्रक्रिया देखेंगे। आप यह भी देखेंगे कि समान दृष्टिकोण को **batch process PSD files** के लिए बड़े‑पैमाने पर कैसे लागू किया जा सकता है।

## त्वरित उत्तर

- **What does “save PSD as PNG” mean?** यह एक Photoshop दस्तावेज़ को बिना हानि वाले PNG में परिवर्तित करता है जबकि पारदर्शिता को बनाए रखता है।  
- **Which library handles the conversion?** Aspose.PSD for Java समायोजन लेयरों के लिए पूर्ण समर्थन प्रदान करता है।  
- **Can I work with both RGB and CMYK files?** हाँ – API में `RgbChannelMixerLayer` और `CmykChannelMixerLayer` क्लासेस शामिल हैं।  
- **Do I need a license for production use?** उत्पादन उपयोग के लिए लाइसेंस आवश्यक है; परीक्षण के लिए एक अस्थायी लाइसेंस उपलब्ध है।  
- **Is batch processing possible?** बिल्कुल – आप एक फ़ोल्डर के माध्यम से लूप करके प्रत्येक PSD पर समान चरण लागू कर सकते हैं।

## Channel Mixer Adjustment Layer क्या है?

Channel Mixer Adjustment Layer आपको लाल, हरे, नीले (या सियान, मैजेंटा, येलो, ब्लैक) चैनलों के योगदान को पुनः मिश्रित करने की अनुमति देता है ताकि सटीक रंग संतुलन प्राप्त किया जा सके। एक सामान्य लेयर के विपरीत, यह गैर‑विनाशकारी है, जिसका अर्थ है कि मूल पिक्सेल डेटा अपरिवर्तित रहता है।

## Aspose.PSD का उपयोग क्यों करें **convert PSD to PNG** करने के लिए?

- **Full layer fidelity** – सभी समायोजन लेयरों को रूपांतरण के दौरान संरक्षित रखा जाता है।  
- **No Photoshop required** – कोड को किसी भी सर्वर या CI पाइपलाइन पर चलाया जा सकता है।  
- **Supports both RGB and CMYK** – प्रिंट‑तैयार वर्कफ़्लो के लिए आदर्श।

## पूर्वापेक्षाएँ

1. **Aspose.PSD for Java** – इसे [download page](https://releases.aspose.com/psd/java/) से डाउनलोड करें।  
2. **Java Development Kit (JDK) 8+** – सुनिश्चित करें कि `java` आपके PATH में है।  
3. **IDE** – IntelliJ IDEA, Eclipse, या कोई भी एडिटर जो आप पसंद करते हैं।  
4. **Sample PSD files** – ऐसी फ़ाइलें जिनमें Channel Mixer Adjustment Layers हों (RGB और CMYK दोनों प्रकार)।

## पैकेज आयात करें

सबसे पहले, उन क्लासेस को आयात करें जिनकी हमें आवश्यकता होगी। यह PSD फ़ाइलों और PNG निर्यात विकल्पों के साथ काम करने के लिए वातावरण स्थापित करता है।

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.CmykChannelMixerLayer;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.RgbChannelMixerLayer;
import com.aspose.psd.imageoptions.PngOptions;
```

## कैसे **save PSD as PNG** – RGB उदाहरण

### चरण 1: उस PSD फ़ाइल को लोड करें जिसमें RGB Channel Mixer लेयर हो

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "ChannelMixerAdjustmentLayerRgb.psd";

PsdImage im = (PsdImage) Image.load(sourceFileName);
```

हम अपने PSD वाले फ़ोल्डर (`dataDir`) की ओर इशारा करते हैं और फ़ाइल को `PsdImage` ऑब्जेक्ट में लोड करते हैं, जो हमें उसकी सभी लेयरों तक पूर्ण पहुँच प्रदान करता है।

### चरण 2: RGB Channel Mixer लेयर को संशोधित करें

```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof RgbChannelMixerLayer) {
        RgbChannelMixerLayer rgbLayer = (RgbChannelMixerLayer) im.getLayers()[i];
        rgbLayer.getRedChannel().setBlue((short) 100);
        rgbLayer.getBlueChannel().setGreen((short) -100);
        rgbLayer.getGreenChannel().setConstant((short) 50);
    }
}
```

हम प्रत्येक लेयर पर इटररेट करते हैं, `RgbChannelMixerLayer` को खोजते हैं, और उसके चैनल मानों को समायोजित करते हैं। यह उदाहरण लाल चैनल में नीले योगदान को बढ़ाता है, नीले चैनल में हरे को कम करता है, और हरे चैनल में एक स्थिर ऑफ़सेट जोड़ता है।

### चरण 3: संशोधित PSD को सहेजें (अभी भी PSD)

```java
String psdPathAfterChange = dataDir + "ChannelMixerAdjustmentLayerRgbChanged.psd";
im.save(psdPathAfterChange);
```

फ़ाइल को सहेजने से समायोजन लेयर संरक्षित रहता है ताकि आवश्यकता पड़ने पर आप इसे बाद में Photoshop में फिर से खोल सकें।

### चरण 4: छवि को PNG में निर्यात करें (the **save PSD as PNG** step)

```java
String pngExportPath = dataDir + "ChannelMixerAdjustmentLayerRgbChanged.png";
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
im.save(pngExportPath, saveOptions);
```

हम एक `PngOptions` इंस्टेंस बनाते हैं, रंग प्रकार को `TruecolorWithAlpha` सेट करते हैं ताकि पारदर्शिता बनी रहे, और फिर छवि को निर्यात करते हैं।

## कैसे **save PSD as PNG** – CMYK उदाहरण

### चरण 5: उस PSD फ़ाइल को लोड करें जिसमें CMYK Channel Mixer लेयर हो

```java
sourceFileName = dataDir + "ChannelMixerAdjustmentLayerCmyk.psd";
PsdImage img = (PsdImage) Image.load(sourceFileName);
```

लोडिंग प्रक्रिया समान है; हम केवल एक अलग फ़ाइल के साथ काम करते हैं जो CMYK रंग मॉडल का उपयोग करती है।

### चरण 6: CMYK Channel Mixer लेयर को संशोधित करें

```java
for (int i = 0; i < img.getLayers().length; i++) {
    if (img.getLayers()[i] instanceof CmykChannelMixerLayer) {
        CmykChannelMixerLayer cmykLayer = (CmykChannelMixerLayer) img.getLayers()[i];
        cmykLayer.getCyanChannel().setBlack((short) 20);
        cmykLayer.getMagentaChannel().setYellow((short) 50);
        cmykLayer.getYellowChannel().setCyan((short) -25);
        cmykLayer.getBlackChannel().setYellow((short) 25);
    }
}
```

यहाँ हम CMYK चैनलों को समायोजित करते हैं: सियान में काला जोड़ते हैं, मैजेंटा के येलो घटक को समायोजित करते हैं, आदि। यह प्रिंट‑उन्मुख फ़ाइलों के लिए API की लचीलापन दर्शाता है।

### चरण 7: संशोधित CMYK PSD को सहेजें

```java
psdPathAfterChange = dataDir + "ChannelMixerAdjustmentLayerCmykChanged.psd";
img.save(psdPathAfterChange);
```

फिर भी, हम नई समायोजन के साथ एक PSD संस्करण रखते हैं।

### चरण 8: CMYK छवि को PNG में निर्यात करें

```java
pngExportPath = dataDir + "ChannelMixerAdjustmentLayerCmykChanged.png";
PngOptions options = new PngOptions();
options.setColorType(PngColorType.TruecolorWithAlpha);
img.save(pngExportPath, options);
```

भले ही स्रोत CMYK है, PNG निर्यात स्वचालित रूप से इसे RGB‑आधारित PNG में परिवर्तित करता है जबकि पारदर्शिता को बनाए रखता है।

## सामान्य समस्याएँ और समाधान

| समस्या | क्यों होता है | समाधान |
|-------|----------------|-----|
| PNG में गलत रंग दिखाई देते हैं | उचित प्रोफ़ाइल के बिना CMYK → RGB रूपांतरण | सुनिश्चित करें कि स्रोत PSD में एम्बेडेड ICC प्रोफ़ाइल हो; निर्यात के दौरान Aspose.PSD इसका सम्मान करता है। |
| समायोजन लेयर नहीं मिला | लेयर प्रकार का मिलान नहीं (जैसे, “Color Balance” लेयर) | कास्ट करने से पहले लेयर क्लास (`RgbChannelMixerLayer` या `CmykChannelMixerLayer`) की पुष्टि करें। |
| रनटाइम पर लाइसेंस अपवाद | वैध लाइसेंस के बिना लाइब्रेरी का उपयोग करना | विकास के दौरान [temporary license](https://purchase.aspose.com/temporary-license/) पृष्ठ से एक अस्थायी लाइसेंस लागू करें। |

## अक्सर पूछे जाने वाले प्रश्न

**Q: क्या मैं Aspose.PSD for Java को अन्य इमेज फ़ॉर्मैट्स के साथ उपयोग कर सकता हूँ?**  
A: हाँ, लाइब्रेरी PNG, JPEG, BMP, TIFF, और PSD के अलावा कई अन्य फ़ॉर्मैट्स का समर्थन करती है।

**Q: मैं Curves या Levels जैसी अन्य समायोजन लेयरों को कैसे संभालूँ?**  
A: प्रत्येक समायोजन प्रकार की अपनी क्लास होती है (जैसे, `CurvesAdjustmentLayer`)। आप उन्हें चैनल मिक्सर उदाहरण की तरह ही हेरफेर कर सकते हैं।

**Q: क्या **batch process PSD files** को PNG में बदलने का कोई तरीका है?**  
A: बिल्कुल। ऊपर दिए गए चरणों को एक `for‑each` लूप में रखें जो डायरेक्टरी में फ़ाइलों पर इटररेट करता है, समान संशोधन और निर्यात लॉजिक लागू करता है।

**Q: रूपांतरण के समय अधिकतम इमेज क्वालिटी बनाए रखने की सर्वोत्तम प्रथा क्या है?**  
A: `PngOptions` को `TruecolorWithAlpha` के साथ उपयोग करें और डाउन‑सैंपलिंग से बचें। साथ ही, यदि बाद में लॉसलेस एडिट्स की आवश्यकता हो तो मूल PSD रखें।

**Q: क्या उत्पादन उपयोग के लिए मुझे पेड लाइसेंस चाहिए?**  
A: हाँ। मूल्यांकन के लिए एक अस्थायी लाइसेंस ठीक है, लेकिन व्यावसायिक तैनाती के लिए पूर्ण लाइसेंस आवश्यक है।

---

**अंतिम अपडेट:** 2026-03-31  
**परीक्षण किया गया:** Aspose.PSD for Java 24.12  
**लेखक:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}