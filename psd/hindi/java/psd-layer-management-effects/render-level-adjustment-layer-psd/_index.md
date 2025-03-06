---
title: PSD फ़ाइलों में रेंडर लेवल समायोजन परत - जावा
linktitle: PSD फ़ाइलों में रेंडर लेवल समायोजन परत - जावा
second_title: Aspose.PSD जावा एपीआई
description: Aspose.PSD for Java का उपयोग करके आसानी से छवि कंट्रास्ट और जीवंतता को बढ़ाने का तरीका जानें। इस चरण-दर-चरण मार्गदर्शिका के साथ लेवल एडजस्टमेंट लेयर्स में महारत हासिल करें।
weight: 17
url: /hi/java/psd-layer-management-effects/render-level-adjustment-layer-psd/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD फ़ाइलों में रेंडर लेवल समायोजन परत - जावा

## परिचय

क्या आपने कभी PSD फ़ाइल खोली है और पाया है कि छवि में कंट्रास्ट या जीवंतता की कमी है? डरो मत, छवि संपादन योद्धा! Aspose.PSD for Java अपनी शक्तिशाली Levels समायोजन परत हेरफेर क्षमताओं के साथ बचाव के लिए आता है। यह मार्गदर्शिका आपको Levels का उपयोग करके अपनी छवियों को आसानी से ठीक करने के ज्ञान से लैस करेगी। 

## आवश्यक शर्तें

- जावा डेवलपमेंट किट (JDK): सुनिश्चित करें कि आपके सिस्टम पर JDK का नवीनतम संस्करण स्थापित है। आप इसे Oracle वेबसाइट से डाउनलोड कर सकते हैं ([https://www.oracle.com/java/technologies/javase-downloads.html](https://www.oracle.com/java/technologies/javase-downloads.html)).
- Aspose.PSD for Java लाइब्रेरी: डाउनलोड पृष्ठ से Aspose.PSD for Java लाइब्रेरी डाउनलोड करें ([https://releases.aspose.com/psd/java/](https://releases.aspose.com/psd/java/)) आपको पूर्ण सुविधाओं का उपयोग करने के लिए एक वैध लाइसेंस की आवश्यकता होगी, लेकिन आरंभ करने के लिए एक निःशुल्क परीक्षण उपलब्ध है ([https://releases.aspose.com/](https://releases.aspose.com/)).

## पैकेज आयात करें

कोड में गोता लगाने से पहले, हमें PSD फ़ाइलों के साथ इंटरैक्ट करने के लिए आवश्यक Aspose.PSD क्लासेस को आयात करना होगा। यहाँ आपको क्या चाहिए:

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.LevelsLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.LevelChannel;
import com.aspose.psd.imageoptions.PngOptions;
```

`com.aspose.psd` पैकेज PSD हेरफेर कार्यक्षमताओं तक पहुंच प्रदान करता है, जबकि`com.aspose.psd.imaging.PngOptions` हमें छवि को PNG के रूप में सहेजते समय विकल्प परिभाषित करने की अनुमति देता है।

अब, आइए हम अपने स्तर समायोजन साहसिक कार्य पर चलें:

## चरण 1: फ़ाइल पथ सेट करना:

- अपने दस्तावेज़ निर्देशिका के लिए चर परिभाषित करें (`dataDir`), स्रोत PSD फ़ाइल नाम (`sourceFileName`), संशोधन के बाद लक्ष्य PSD फ़ाइल नाम (`psdPathAfterChange`), और अंतिम PNG निर्यात पथ (`pngExportPath`) कोड की पठनीयता में सुधार के लिए वर्णनात्मक नामों का उपयोग करने पर विचार करें।

```java
String dataDir = "Your Document Directory";

String sourceFileName = dataDir + "LevelsAdjustmentLayer.psd";
String psdPathAfterChange = dataDir + "LevelsAdjustmentLayerChanged.psd";
String pngExportPath = dataDir + "LevelsAdjustmentLayerChanged.png";
```

## चरण 2: PSD छवि लोड करना:

-  उपयोग`Image.load` स्रोत PSD फ़ाइल को खोलने और इसे संग्रहीत करने की विधि`PsdImage`वस्तु (`im`) Aspose.PSD स्वचालित रूप से फ़ाइल स्वरूप का पता लगाता है।

```java
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

## चरण 3: परतों के माध्यम से पुनरावृत्ति:

- हमें आपके PSD में लेवल एडजस्टमेंट लेयर ढूँढ़ने की ज़रूरत है। Aspose लूप का उपयोग करके सभी लेयर्स के माध्यम से पुनरावृति करने का एक सुविधाजनक तरीका प्रदान करता है।

```java
for (int i = 0; i < im.getLayers().length; i++) {
   // ... (लेवल लेयर की जांच करने के लिए कोड यहां जोड़ा जाएगा)
}
```

## चरण 4: स्तर परत की पहचान करना:

- लूप के अंदर, जाँच करें कि क्या वर्तमान परत (`im.getLayers()[i]` ) इसका एक उदाहरण है`LevelsLayer` कक्षा का उपयोग कर`instanceof` ऑपरेटर. 
-  यदि ऐसा है, तो परत को एक पर डालें`LevelsLayer` आगे हेरफेर के लिए वस्तु।

```java
for (int i = 0; i < im.getLayers().length; i++) {
   if (im.getLayers()[i] instanceof LevelsLayer) {
	   LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
	   // ... (स्तर समायोजित करने के लिए कोड यहां जोड़ा जाएगा)
   }
}
```
## चरण 5: स्तरों को ठीक करना (जारी):

-  आउटपुट स्तर को समायोजित करने के लिए निम्न का उपयोग करें:`setOutputShadowLevel` और`setOutputHighlightLevel` परिणामी छवि के अंधेरे और हल्केपन को नियंत्रित करने के लिए। ये मान इनपुट स्तरों की सीमा निर्धारित करते हैं जिन्हें आउटपुट रेंज में मैप किया जाएगा।

```java
for (int i = 0; i < im.getLayers().length; i++) {
   if (im.getLayers()[i] instanceof LevelsLayer) {
	   LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
	   LevelChannel channel = levelsLayer.getChannel(0);

	   // इनपुट स्तर समायोजित करें (0-255):
	   channel.setInputShadowLevel((short) 10); // छाया को थोड़ा गहरा करें
	   channel.setInputMidtoneLevel(2.0f);     // मिडटोन बढ़ाएँ
	   channel.setInputHighlightLevel((short) 230); // हाइलाइट्स कम करें

	   // आउटपुट स्तर समायोजित करें (0-255):
	   channel.setOutputShadowLevel((short) 20); // छाया को और अधिक गहरा करें
	   channel.setOutputHighlightLevel((short) 200); //हाइलाइट्स को उज्ज्वल करें
   }
}
```

## चरण 6: संशोधित PSD को सहेजना:

-  उपयोग`save` की विधि`PsdImage` संशोधित छवि को निर्दिष्ट पथ पर सहेजने के लिए ऑब्जेक्ट (`psdPathAfterChange`).

```java
im.save(psdPathAfterChange);
```

## चरण 7: PNG के रूप में निर्यात करना (वैकल्पिक):

-  यदि आपको समायोजित छवि का PNG संस्करण चाहिए, तो बनाएं`PngOptions` ऑब्जेक्ट और रंग प्रकार सेट करें`TruecolorWithAlpha` . फिर, का उपयोग करें`save` पीएनजी निर्यात पथ और विकल्पों के साथ फिर से विधि का उपयोग करें।

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
im.save(pngExportPath, saveOptions);
```

और अब यह हो गया! आपने Aspose.PSD for Java का उपयोग करके अपनी PSD फ़ाइल में Levels Adjustment Layer को सफलतापूर्वक समायोजित कर लिया है। इन चरणों को समझकर और विभिन्न मानों के साथ प्रयोग करके, आप अपनी छवियों के कंट्रास्ट और समग्र स्वरूप को बेहतर बना सकते हैं।

## निष्कर्ष

Aspose.PSD for Java आपको अपनी छवि संपादन प्रक्रिया पर नियंत्रण रखने की शक्ति देता है। लेवल एडजस्टमेंट लेयर में महारत हासिल करके, आप अपनी तस्वीरों और डिज़ाइन में नई जान डाल सकते हैं। याद रखें, अभ्यास से ही पूर्णता आती है, इसलिए इस शक्तिशाली टूल की पूरी क्षमता का प्रयोग करने और उसका पता लगाने में संकोच न करें।
 
## अक्सर पूछे जाने वाले प्रश्न

### क्या मैं अलग-अलग रंग चैनल (RGB) को अलग-अलग समायोजित कर सकता हूँ? 
हां, आप प्रत्येक रंग चैनल तक पहुंच सकते हैं`getChannel` की विधि`LevelsLayer` ऑब्जेक्ट और उसके स्तरों को स्वतंत्र रूप से संशोधित करें।

### मैं PSD में एकाधिक स्तर समायोजन परतों को कैसे संभालूँ?
कोड सभी परतों के माध्यम से पुनरावृत्त होता है, इसलिए यह छवि में पाई जाने वाली किसी भी अतिरिक्त स्तर परत को स्वचालित रूप से संसाधित करेगा।

### क्या लेवल के अलावा छवि कंट्रास्ट को समायोजित करने के अन्य तरीके भी हैं?
बिल्कुल! Aspose.PSD विभिन्न छवि समायोजन उपकरण जैसे कर्व्स, ब्राइटनेस/कंट्रास्ट, और बहुत कुछ प्रदान करता है।

### क्या मैं एकाधिक छवियों के लिए इस प्रक्रिया को स्वचालित कर सकता हूँ? 
हां, आप एकाधिक PSD फ़ाइलों को कुशलतापूर्वक संसाधित करने के लिए इस कोड को लूप या बैच प्रोसेसिंग स्क्रिप्ट में शामिल कर सकते हैं।

### मुझे अधिक जानकारी और सहायता कहां मिल सकती है?
Aspose व्यापक दस्तावेज उपलब्ध कराता है ([https://reference.aspose.com/psd/java/](https://reference.aspose.com/psd/java/)) और एक सहायता मंच ([https://forum.aspose.com/c/psd/34](https://forum.aspose.com/c/psd/34)) पर किसी भी प्रश्न या समस्या के लिए संपर्क करें।
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
