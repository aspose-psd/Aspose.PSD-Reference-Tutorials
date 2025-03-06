---
title: Java के लिए Aspose.PSD के साथ रनटाइम पर प्रभाव जोड़ें
linktitle: रनटाइम पर प्रभाव जोड़ें
second_title: Aspose.PSD जावा एपीआई
description: छवियों में गतिशील रूप से आकर्षक प्रभाव जोड़ने के लिए Aspose.PSD for Java के सहज एकीकरण का अन्वेषण करें। इस सहज ट्यूटोरियल के साथ अपने Java विकास को आगे बढ़ाएँ।
weight: 20
url: /hi/java/advanced-techniques/add-effects-runtime/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java के लिए Aspose.PSD के साथ रनटाइम पर प्रभाव जोड़ें

## परिचय

जावा विकास की दुनिया में, छवियों में गतिशील प्रभाव जोड़ना एक सामान्य आवश्यकता है। Aspose.PSD for Java, एक शक्तिशाली और बहुमुखी जावा लाइब्रेरी के साथ, आप अपनी छवियों को बेहतर बनाने के लिए रनटाइम पर आसानी से प्रभाव जोड़ सकते हैं। इस ट्यूटोरियल में, हम आपको स्पष्ट उदाहरणों और आसान-से-अनुसरण निर्देशों का उपयोग करके, चरण दर चरण प्रभाव जोड़ने की प्रक्रिया के माध्यम से मार्गदर्शन करेंगे।

## आवश्यक शर्तें

ट्यूटोरियल में शामिल होने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित पूर्वापेक्षाएँ मौजूद हैं:

1.  जावा डेवलपमेंट किट (JDK): सुनिश्चित करें कि आपके सिस्टम पर जावा इंस्टॉल है। आप नवीनतम JDK को यहाँ से डाउनलोड कर सकते हैं[यहाँ](https://www.oracle.com/java/technologies/javase-downloads.html).

2.  Aspose.PSD for Java लाइब्रेरी: आपके पास Aspose.PSD for Java लाइब्रेरी होनी चाहिए। अगर आपके पास पहले से नहीं है, तो इसे यहाँ से डाउनलोड करें।[Aspose.PSD जावा दस्तावेज़](https://reference.aspose.com/psd/java/).

3.  दस्तावेज़ निर्देशिका: अपने दस्तावेज़ों के लिए एक निर्देशिका सेट करें, और पथ याद रखें। दिए गए उदाहरण में, निर्देशिका को इस प्रकार संदर्भित किया जाता है`Your Document Directory`.

## पैकेज आयात करें

अपने जावा प्रोजेक्ट में, Aspose.PSD for Java की कार्यक्षमताओं का लाभ उठाने के लिए आवश्यक पैकेज आयात करें।

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.layereffects.ColorOverlayEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
```

## चरण 1: PSD छवि लोड करें

सबसे पहले उस PSD इमेज को लोड करें जिस पर आप इफ़ेक्ट लागू करना चाहते हैं। उचित फ़ाइल पथ सेट करना सुनिश्चित करें।

```java
String sourceFileName = "Your Document Directory/ThreeRegularLayers.psd";
String exportPath = "Your Document Directory/ThreeRegularLayersChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

## चरण 2: रंग ओवरले प्रभाव जोड़ें

इस चरण में, हम PSD छवि की एक विशिष्ट परत पर रंग ओवरले प्रभाव जोड़ेंगे।

```java
ColorOverlayEffect effect = im.getLayers()[1].getBlendingOptions().addColorOverlay();
effect.setColor(Color.getGreen());
effect.setOpacity((byte)128);
effect.setBlendMode(BlendMode.Normal);
```

## चरण 3: संशोधित छवि सहेजें

अंत में, संशोधित छवि को लागू प्रभावों के साथ एक नई फ़ाइल में सहेजें।

```java
im.save(exportPath);
```

बधाई हो! आपने Java के लिए Aspose.PSD का उपयोग करके रनटाइम पर सफलतापूर्वक प्रभाव जोड़ दिया है।

## निष्कर्ष

Aspose.PSD for Java आपकी छवियों में गतिशील प्रभाव जोड़ने की प्रक्रिया को सरल बनाता है, जिससे आपको छवि हेरफेर के लिए एक शक्तिशाली टूलकिट मिलता है। इस ट्यूटोरियल का अनुसरण करके, आपने रनटाइम पर रंग ओवरले प्रभाव लागू करने में अंतर्दृष्टि प्राप्त की है, जिससे आपकी छवियों की दृश्य अपील बढ़ गई है।

## अक्सर पूछे जाने वाले प्रश्न

### प्रश्न 1: क्या मैं एक ही परत पर एकाधिक प्रभाव लागू कर सकता हूँ?

A1: हाँ, आप Java के लिए Aspose.PSD द्वारा प्रदान की गई संबंधित विधियों का उपयोग करके एकल परत पर एकाधिक प्रभाव लागू कर सकते हैं।

### प्रश्न 2: क्या Aspose.PSD विभिन्न छवि प्रारूपों के साथ संगत है?

A2: हां, Aspose.PSD PSD, BMP, JPEG, PNG, और अधिक सहित छवि प्रारूपों की एक विस्तृत श्रृंखला का समर्थन करता है।

### प्रश्न 3: मैं Java के लिए Aspose.PSD का अस्थायी लाइसेंस कैसे प्राप्त कर सकता हूं?

 A3: आप यहाँ से अस्थायी लाइसेंस प्राप्त कर सकते हैं[यहाँ](https://purchase.aspose.com/temporary-license/).

### प्रश्न 4: मैं Aspose.PSD से संबंधित किसी भी समस्या या प्रश्न के लिए सहायता कहां से प्राप्त कर सकता हूं?

 A4: Aspose.PSD पर जाएँ[सहयता मंच](https://forum.aspose.com/c/psd/34) सहायता प्राप्त करने और समुदाय से जुड़ने के लिए।

### प्रश्न 5: क्या Java के लिए Aspose.PSD का निःशुल्क परीक्षण उपलब्ध है?

 A5: हाँ, आप निःशुल्क परीक्षण संस्करण का उपयोग कर सकते हैं[यहाँ](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
