---
title: जावा के लिए Aspose.PSD के साथ रनटाइम पर प्रभाव जोड़ें
linktitle: रनटाइम पर प्रभाव जोड़ें
second_title: Aspose.PSD जावा एपीआई
description: छवियों में गतिशील रूप से मनमोहक प्रभाव जोड़ने के लिए जावा के लिए Aspose.PSD के सहज एकीकरण का अन्वेषण करें। इस सहज ट्यूटोरियल के साथ अपने जावा विकास को उन्नत करें।
type: docs
weight: 20
url: /hi/java/advanced-techniques/add-effects-runtime/
---
## परिचय

जावा विकास की दुनिया में, छवियों में गतिशील प्रभाव जोड़ना एक सामान्य आवश्यकता है। जावा के लिए Aspose.PSD, एक शक्तिशाली और बहुमुखी जावा लाइब्रेरी के साथ, आप अपनी छवियों को बेहतर बनाने के लिए रनटाइम पर आसानी से प्रभाव जोड़ सकते हैं। इस ट्यूटोरियल में, हम स्पष्ट उदाहरणों और पालन करने में आसान निर्देशों का उपयोग करके चरण दर चरण प्रभाव जोड़ने की प्रक्रिया में आपका मार्गदर्शन करेंगे।

## आवश्यक शर्तें

ट्यूटोरियल में जाने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित आवश्यक शर्तें हैं:

1.  जावा डेवलपमेंट किट (जेडीके): सुनिश्चित करें कि आपके सिस्टम पर जावा स्थापित है। आप नवीनतम JDK यहां से डाउनलोड कर सकते हैं[यहाँ](https://www.oracle.com/java/technologies/javase-downloads.html).

2.  जावा लाइब्रेरी के लिए Aspose.PSD: जावा लाइब्रेरी के लिए आपके पास Aspose.PSD होना चाहिए। यदि आपने पहले से नहीं किया है, तो इसे यहां से डाउनलोड करें[Aspose.PSD जावा दस्तावेज़ीकरण](https://reference.aspose.com/psd/java/).

3. दस्तावेज़ निर्देशिका: अपने दस्तावेज़ों के लिए एक निर्देशिका सेट करें, और पथ याद रखें। दिए गए उदाहरण में, निर्देशिका को कहा गया है`Your Document Directory`.

## पैकेज आयात करें

अपने जावा प्रोजेक्ट में, जावा के लिए Aspose.PSD की कार्यक्षमता का लाभ उठाने के लिए आवश्यक पैकेज आयात करें।

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.layereffects.ColorOverlayEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
```

## चरण 1: PSD छवि लोड करें

उस PSD छवि को लोड करके प्रारंभ करें जिस पर आप प्रभाव लागू करना चाहते हैं। उचित फ़ाइल पथ सेट करना सुनिश्चित करें.

```java
String sourceFileName = "Your Document Directory/ThreeRegularLayers.psd";
String exportPath = "Your Document Directory/ThreeRegularLayersChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

## चरण 2: रंग ओवरले प्रभाव जोड़ें

इस चरण में, हम PSD छवि की एक विशिष्ट परत पर एक रंग ओवरले प्रभाव जोड़ेंगे।

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

बधाई हो! आपने Java के लिए Aspose.PSD का उपयोग करके रनटाइम पर सफलतापूर्वक प्रभाव जोड़ दिए हैं।

## निष्कर्ष

जावा के लिए Aspose.PSD आपकी छवियों में गतिशील प्रभाव जोड़ने की प्रक्रिया को सरल बनाता है, आपको छवि हेरफेर के लिए एक शक्तिशाली टूलकिट प्रदान करता है। इस ट्यूटोरियल का अनुसरण करके, आपने रनटाइम पर रंग ओवरले प्रभाव लागू करने, अपनी छवियों की दृश्य अपील को बढ़ाने में अंतर्दृष्टि प्राप्त की है।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या मैं एक ही परत पर अनेक प्रभाव लागू कर सकता हूँ?

A1: हाँ, आप Java के लिए Aspose.PSD द्वारा प्रदान की गई संबंधित विधियों का उपयोग करके एक ही परत पर कई प्रभाव लागू कर सकते हैं।

### Q2: क्या Aspose.PSD विभिन्न छवि प्रारूपों के साथ संगत है?

A2: हां, Aspose.PSD PSD, BMP, JPEG, PNG और अन्य सहित छवि प्रारूपों की एक विस्तृत श्रृंखला का समर्थन करता है।

### Q3: मैं जावा के लिए Aspose.PSD के लिए अस्थायी लाइसेंस कैसे प्राप्त कर सकता हूं?

 A3: आप यहां से अस्थायी लाइसेंस प्राप्त कर सकते हैं[यहाँ](https://purchase.aspose.com/temporary-license/).

### Q4: Aspose.PSD से संबंधित किसी भी मुद्दे या प्रश्न के लिए मैं कहां सहायता मांग सकता हूं?

 A4: Aspose.PSD पर जाएँ[सहयता मंच](https://forum.aspose.com/c/psd/34) सहायता प्राप्त करने और समुदाय से जुड़ने के लिए।

### Q5: क्या Java के लिए Aspose.PSD का निःशुल्क परीक्षण उपलब्ध है?

 A5: हां, आप नि:शुल्क परीक्षण संस्करण का पता लगा सकते हैं।[यहाँ](https://releases.aspose.com/).