---
title: चैनल मिक्सर समायोजन परत को PSD में निर्यात करें - जावा
linktitle: चैनल मिक्सर समायोजन परत को PSD में निर्यात करें - जावा
second_title: Aspose.PSD जावा एपीआई
description: Java के लिए Aspose.PSD का उपयोग करके PSD में चैनल मिक्सर एडजस्टमेंट लेयर्स को निर्यात करना सीखें। RGB और CMYK लेयर्स को संशोधित करने, परिवर्तनों को सहेजने और PNG में निर्यात करने के लिए चरण-दर-चरण मार्गदर्शिका।
type: docs
weight: 14
url: /hi/java/psd-layer-management-effects/export-channel-mixer-adjustment-layer-psd/
---
## परिचय

जब छवि संपादन की बात आती है, खासकर एडोब फोटोशॉप फ़ाइलों (PSD) के साथ, परतों को कुशलतापूर्वक प्रबंधित करना महत्वपूर्ण है। इन परतों में से, चैनल मिक्सर एडजस्टमेंट लेयर एक छवि के रंग संतुलन को बदलने में महत्वपूर्ण भूमिका निभाता है। यदि आप एक जावा डेवलपर हैं जो इन परतों को प्रोग्रामेटिक रूप से हेरफेर करना चाहते हैं, तो आप भाग्यशाली हैं! इस लेख में, हम आपको जावा के लिए Aspose.PSD का उपयोग करके चैनल मिक्सर एडजस्टमेंट लेयर्स को निर्यात करने की प्रक्रिया के बारे में बताएंगे। इस गाइड के अंत तक, आप RGB और CMYK चैनल मिक्सर एडजस्टमेंट लेयर्स को संभालने, अपने परिवर्तनों को सहेजने और अपनी अंतिम छवि को PSD और PNG दोनों प्रारूपों में निर्यात करने के लिए अच्छी तरह से सुसज्जित होंगे।

## आवश्यक शर्तें

इससे पहले कि हम कोड में उतरें, आइए सुनिश्चित करें कि आपके पास वह सब कुछ है जो आपको चाहिए:

1. Aspose.PSD for Java लाइब्रेरी: आपके पास Aspose.PSD for Java लाइब्रेरी इंस्टॉल होनी चाहिए। आप इसे यहाँ से डाउनलोड कर सकते हैं[डाउनलोड पृष्ठ](https://releases.aspose.com/psd/java/).
2. जावा डेवलपमेंट किट (JDK): सुनिश्चित करें कि आपके सिस्टम पर JDK 8 या उससे ऊपर का संस्करण स्थापित है।
3. एकीकृत विकास वातावरण (आईडीई): अपने जावा कोड को लिखने और निष्पादित करने के लिए इंटेलीज आईडीईए या एक्लिप्स जैसे आईडीई का उपयोग करें।
4. PSD फ़ाइलें: अपनी PSD फ़ाइलें तैयार रखें, विशेष रूप से वे जिनमें चैनल मिक्सर समायोजन परतें हों, जिन्हें आप संशोधित करना चाहते हैं।

## पैकेज आयात करें

सबसे पहले, आइए आवश्यक पैकेज आयात करें। यह चरण आवश्यक है क्योंकि यह आपके वातावरण को Aspose.PSD for Java के साथ काम करने के लिए सेट करता है।

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.CmykChannelMixerLayer;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.RgbChannelMixerLayer;
import com.aspose.psd.imageoptions.PngOptions;
```

## चरण 1: RGB चैनल मिक्सर लेयर के साथ PSD फ़ाइल लोड करना

आइए ट्यूटोरियल की शुरुआत एक PSD फ़ाइल लोड करके करें जिसमें RGB चैनल मिक्सर एडजस्टमेंट लेयर शामिल है।

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "ChannelMixerAdjustmentLayerRgb.psd";

PsdImage im = (PsdImage) Image.load(sourceFileName);
```

इस चरण में, हम उस निर्देशिका को परिभाषित करते हैं जहाँ हमारी PSD फ़ाइलें संग्रहीत हैं (`dataDir` ) फिर हम PSD फ़ाइल को लोड करते हैं`Image.load()` विधि और इसे एक में डालें`PsdImage` ऑब्जेक्ट, जो हमें इसकी परतों में हेरफेर करने की अनुमति देगा।

## चरण 2: RGB चैनल मिक्सर परत को संशोधित करना

एक बार फ़ाइल लोड हो जाने के बाद, हम RGB चैनल मिक्सर लेयर तक पहुंच सकते हैं और उसे संशोधित कर सकते हैं।

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

इस चरण में क्या हो रहा है, यहां बताया गया है:
- हम PSD फ़ाइल की सभी परतों से होकर गुजरते हैं।
-  हम जाँचते हैं कि क्या परत इसका उदाहरण है?`RgbChannelMixerLayer`.
- यदि ऐसा है, तो हम रंग चैनलों को समायोजित करने के लिए आगे बढ़ते हैं। उदाहरण के लिए, हम लाल चैनल के नीले घटक को 100 पर सेट करते हैं, नीले चैनल के हरे घटक को 100 से घटाते हैं, और हरे चैनल के लिए एक स्थिर मान सेट करते हैं।

## चरण 3: संशोधित PSD फ़ाइल को सहेजना

RGB चैनल मिक्सर लेयर को संशोधित करने के बाद, परिवर्तनों को सहेजने का समय आ गया है।

```java
String psdPathAfterChange = dataDir + "ChannelMixerAdjustmentLayerRgbChanged.psd";
im.save(psdPathAfterChange);
```

 इस चरण में, हम वह पथ निर्दिष्ट करते हैं जहाँ संशोधित PSD फ़ाइल सहेजी जाएगी और फिर इसका उपयोग करेंगे`save()` परिवर्तनों को संग्रहीत करने की विधि.

## चरण 4: छवि को PNG में निर्यात करना

अब जब PSD फ़ाइल सहेज ली गई है, तो आइए छवि को अल्फा पारदर्शिता के साथ PNG प्रारूप में निर्यात करें।

```java
String pngExportPath = dataDir + "ChannelMixerAdjustmentLayerRgbChanged.png";
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
im.save(pngExportPath, saveOptions);
```

इस चरण में:
- हम PNG फ़ाइल के लिए निर्यात पथ परिभाषित करते हैं।
-  हम एक बनाते हैं`PngOptions` ऑब्जेक्ट और उसका रंग प्रकार सेट करें`TruecolorWithAlpha`यह सुनिश्चित करते हुए कि छवि अपनी पारदर्शिता बरकरार रखे।
- अंत में, हम छवि को PNG फ़ाइल के रूप में सेव करते हैं।

## चरण 5: CMYK चैनल मिक्सर लेयर के साथ PSD फ़ाइल लोड करना

आगे, आइए जानें कि CMYK चैनल मिक्सर समायोजन परतों को कैसे संभालना है।

```java
sourceFileName = dataDir + "ChannelMixerAdjustmentLayerCmyk.psd";
PsdImage img = (PsdImage) Image.load(sourceFileName);
```

पिछले चरणों की तरह, हम CMYK चैनल मिक्सर लेयर युक्त PSD फ़ाइल लोड करते हैं।

## चरण 6: CMYK चैनल मिक्सर परत को संशोधित करना

फ़ाइल लोड होने के बाद, आइए CMYK चैनल मिक्सर लेयर को संशोधित करें।

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

इस चरण में, हम:
- CMYK चैनल मिक्सर परत की पहचान करने के लिए परतों के माध्यम से लूप करें।
- CMYK स्पेक्ट्रम के भीतर विभिन्न रंग चैनलों को संशोधित करें, जैसे कि सियान चैनल के काले घटक को 20 पर सेट करना और अन्य चैनलों को तदनुसार समायोजित करना।

## चरण 7: संशोधित PSD फ़ाइल को सहेजना

एक बार संशोधन हो जाने के बाद, हम अद्यतन PSD फ़ाइल को सहेज लेते हैं।

```java
psdPathAfterChange = dataDir + "ChannelMixerAdjustmentLayerCmykChanged.psd";
img.save(psdPathAfterChange);
```

 हम संशोधित CMYK PSD फ़ाइल को निर्दिष्ट पथ पर सहेजते हैं`save()` तरीका।

## चरण 8: CMYK छवि को PNG में निर्यात करना

अंत में, आइए संशोधित CMYK छवि को PNG फ़ाइल में निर्यात करें।

```java
pngExportPath = dataDir + "ChannelMixerAdjustmentLayerCmykChanged.png";
PngOptions options = new PngOptions();
options.setColorType(PngColorType.TruecolorWithAlpha);
img.save(pngExportPath, options);
```

RGB छवि की तरह ही, हम निर्यात पथ को परिभाषित करते हैं और CMYK छवि को अल्फा पारदर्शिता के साथ PNG प्रारूप में सहेजते हैं।

## निष्कर्ष

इस गाइड में, हमने Java के लिए Aspose.PSD का उपयोग करके PSD फ़ाइलों में चैनल मिक्सर एडजस्टमेंट लेयर्स को निर्यात करने की पूरी प्रक्रिया को बताया है। हमने PSD फ़ाइलों को लोड करने, RGB और CMYK चैनल मिक्सर लेयर्स को संशोधित करने से लेकर PSD और PNG दोनों प्रारूपों में आपकी छवियों को सहेजने और निर्यात करने तक सब कुछ कवर किया है। इन चरणों का पालन करके, अब आप अपने Java प्रोजेक्ट में चैनल मिक्सर लेयर्स को कुशलतापूर्वक प्रबंधित और हेरफेर कर सकते हैं।

## अक्सर पूछे जाने वाले प्रश्न

### क्या मैं अन्य छवि प्रारूपों के साथ Java के लिए Aspose.PSD का उपयोग कर सकता हूँ?  
हां, Java के लिए Aspose.PSD विभिन्न प्रारूपों का समर्थन करता है, जिनमें PNG, JPEG, BMP और TIFF आदि शामिल हैं।

### मैं कर्व्स या लेवल्स जैसी अन्य समायोजन परतों को कैसे संभालूँ?  
चैनल मिक्सर परतों के समान, आप Java के लिए Aspose.PSD द्वारा प्रदान की गई उपयुक्त कक्षाओं का उपयोग करके अन्य समायोजन परतों में हेरफेर कर सकते हैं।

### क्या एकाधिक PSD फ़ाइलों को बैच प्रोसेस करने का कोई तरीका है?  
हां, आप PSD फ़ाइलों की एक निर्देशिका के माध्यम से लूप कर सकते हैं और Java के लिए Aspose.PSD का उपयोग करके प्रत्येक फ़ाइल पर समान समायोजन लागू कर सकते हैं।

### PNG में निर्यात करते समय छवि गुणवत्ता बनाए रखने का सबसे अच्छा तरीका क्या है?  
 का उपयोग करते हुए`PngOptions` साथ`TruecolorWithAlpha` पारदर्शिता बनाए रखते हुए उच्च गुणवत्ता वाले निर्यात को सुनिश्चित करता है।

### क्या मुझे Java के लिए Aspose.PSD का उपयोग करने के लिए लाइसेंस की आवश्यकता है?  
 हां, Aspose.PSD for Java एक लाइसेंस प्राप्त उत्पाद है। आप एक प्राप्त कर सकते हैं[अस्थायी लाइसेंस](https://purchase.aspose.com/temporary-license/) परीक्षण के लिए या पूर्ण लाइसेंस खरीदने के लिए।