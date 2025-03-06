---
title: .NET के लिए Aspose.PSD में टाइमलाइन के साथ कार्य करना
linktitle: टाइमलाइन के साथ काम करना
second_title: Aspose.PSD .NET एपीआई
description: Aspose.PSD for .NET टाइमलाइन क्लास के साथ PSD इमेज मैनिपुलेशन को बेहतर बनाएँ। फ्रेम प्रॉपर्टीज, लेयर स्टेट्स को नियंत्रित करें और रचनात्मक संभावनाओं को सहजता से उजागर करें।
weight: 16
url: /hi/net/psd-file-manipulation/timeline/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# .NET के लिए Aspose.PSD में टाइमलाइन के साथ कार्य करना

## परिचय
ग्राफिक डिज़ाइन और छवि हेरफेर की गतिशील दुनिया में, छवियों की समयरेखा को नियंत्रित करने और उसमें हेरफेर करने की क्षमता महत्वपूर्ण है। .NET के लिए Aspose.PSD अपने टाइमलाइन वर्ग के साथ एक शक्तिशाली समाधान प्रदान करता है। यह उच्च-स्तरीय सुविधा उपयोगकर्ताओं को PsdImage की समयरेखा में परिवर्तन करने में सक्षम बनाती है, जैसे कि फ़्रेम विलंब को बदलना, विशिष्ट फ़्रेम पर लेयर स्टेट को संपादित करना, और बहुत कुछ।
## आवश्यक शर्तें
टाइमलाइन क्लास द्वारा प्रस्तुत रोमांचक संभावनाओं में गोता लगाने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित पूर्वापेक्षाएँ हैं:
-  Aspose.PSD for .NET लाइब्रेरी: सुनिश्चित करें कि आपके पास Aspose.PSD for .NET लाइब्रेरी स्थापित है। आप इसे यहाँ से डाउनलोड कर सकते हैं[.NET के लिए Aspose.PSD दस्तावेज़](https://reference.aspose.com/psd/net/).
-  दस्तावेज़ और आउटपुट निर्देशिकाएँ: कोड में अपने दस्तावेज़ और आउटपुट निर्देशिकाओं के लिए पथ परिभाषित करें।`baseDir` और`outputDir` अपनी परियोजना संरचना के अनुसार चर का चयन करें।
अब, आइए चरण दर चरण देखें कि टाइमलाइन क्लास का उपयोग कैसे करें।
## नामस्थान आयात करें
टाइमलाइन क्लास के साथ काम करना शुरू करने के लिए, अपने कोड में आवश्यक नेमस्पेस आयात करें:
```csharp
using System;
using System.Collections.Generic;
using System.IO;
using Aspose.PSD.FileFormats.Core.Blending;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers.Animation;
```
## चरण 1: PSD छवि लोड करें
निर्दिष्ट स्रोत फ़ाइल से PSD छवि लोड करके आरंभ करें। सुनिश्चित करें कि स्रोत फ़ाइल पथ सही ढंग से सेट किया गया है:
```csharp
string sourceFile = Path.Combine(baseDir, "image1219.psd");
using (PsdImage psdImage = (PsdImage)Image.Load(sourceFile))
{
    //आगे के कार्यों के लिए आपका कोड यहां दिया गया है
}
```
## चरण 2: टाइमलाइन तक पहुंचें
एक बार PSD छवि लोड हो जाने पर, निम्नलिखित कोड का उपयोग करके टाइमलाइन तक पहुंचें:
```csharp
Timeline timeline = psdImage.Timeline;
```
## चरण 3: डिस्पोज़ विधि बदलें
किसी विशिष्ट फ़्रेम के डिस्पोज़ विधि में बदलाव करें। इस उदाहरण में, हम फ़्रेम 1 के डिस्पोज़ विधि को बदलते हैं:
```csharp
timeline.Frames[0].DisposalMethod = FrameDisposalMethod.DoNotDispose;
```
## चरण 4: फ़्रेम विलंब समायोजित करें
किसी विशेष फ़्रेम की देरी को संशोधित करें। यहाँ, हम फ़्रेम 2 की देरी को 15 में बदलते हैं:
```csharp
timeline.Frames[1].Delay = 15;
```
## चरण 5: परत स्थिति संपादित करें
किसी विशिष्ट फ़्रेम पर 'लेयर 1' की अपारदर्शिता बदलें। इस उदाहरण में, हमने फ़्रेम 2 पर अपारदर्शिता को 50 पर सेट किया है:
```csharp
LayerState layerState11 = timeline.Frames[1].LayerStates[1];
layerState11.Opacity = 50;
```
## चरण 6: परत ले जाएँ
'लेयर 1' को किसी विशिष्ट फ्रेम (इस उदाहरण में फ्रेम 3) पर बाएँ-नीचे कोने में ले जाएँ:
```csharp
LayerState layerState21 = timeline.Frames[2].LayerStates[1];
layerState21.PositionOffset = new Point(-50, 230);
```
## चरण 7: नया फ़्रेम जोड़ें
टाइमलाइन में नया फ़्रेम जोड़ें:
```csharp
List<Frame> frames = new List<Frame>(timeline.Frames);
frames.Add(new Frame());
timeline.Frames = frames.ToArray();
```
## चरण 8: ब्लेंड मोड बदलें
किसी विशिष्ट फ्रेम (इस मामले में फ्रेम 4) पर 'लेयर 1' के ब्लेंड मोड को बदलें:
```csharp
LayerState layerState31 = timeline.Frames[3].LayerStates[1];
layerState31.BlendMode = BlendMode.Dissolve;
```
## चरण 9: परिवर्तन सहेजें
परिवर्तनों को PsdImage इंस्टैंस पर वापस लागू करें और संशोधित PSD छवि को सहेजें:
```csharp
psdImage.Save(outputPsd);
```
## चरण 10: सफ़ाई करें
अंत में, अस्थायी आउटपुट फ़ाइल को हटाकर सफाई करें:
```csharp
File.Delete(outputPsd);
```
## निष्कर्ष

निष्कर्ष में, .NET के लिए Aspose.PSD में टाइमलाइन क्लास डेवलपर्स को PSD छवियों की टाइमलाइन पर बारीक नियंत्रण रखने की शक्ति देता है। सरल चरणों की एक श्रृंखला के माध्यम से, आप फ़्रेम गुणों, परत की स्थिति और बहुत कुछ में हेरफेर कर सकते हैं, जिससे रचनात्मक संभावनाओं का एक क्षेत्र खुल जाता है।

## अक्सर पूछे जाने वाले प्रश्न

### प्रश्न 1: क्या Aspose.PSD for .NET शुरुआती लोगों के लिए उपयुक्त है?

A1: बिल्कुल! .NET के लिए Aspose.PSD एक उपयोगकर्ता के अनुकूल इंटरफ़ेस और व्यापक प्रलेखन प्रदान करता है, जो इसे शुरुआती और अनुभवी डेवलपर्स दोनों के लिए सुलभ बनाता है।

### प्रश्न 2: क्या मैं GIF छवियों पर समयरेखा परिवर्तन लागू कर सकता हूँ?

A2: टाइमलाइन क्लास विशेष रूप से PSD छवियों के लिए डिज़ाइन की गई है। GIF हेरफेर के लिए, .NET के लिए Aspose.GIF देखें।

### प्रश्न 3: मैं अतिरिक्त सहायता कहां पा सकता हूं या मुद्दों पर चर्चा कहां कर सकता हूं?

 A3: पर जाएँ[Aspose.PSD फ़ोरम](https://forum.aspose.com/c/psd/34) सामुदायिक समर्थन और मुद्दे पर चर्चा के लिए।

### प्रश्न 4: मैं .NET के लिए Aspose.PSD का अस्थायी लाइसेंस कैसे प्राप्त कर सकता हूं?

 A4: अस्थायी लाइसेंस प्राप्त करें[यहाँ](https://purchase.aspose.com/temporary-license/).

### प्रश्न 5: .NET के लिए Aspose.PSD का उपयोग करने के मुख्य लाभ क्या हैं?

A5: .NET के लिए Aspose.PSD उन्नत छवि प्रसंस्करण क्षमताओं, PSD फ़ाइल हेरफेर, और उच्च प्रदर्शन रेंडरिंग प्रदान करता है।
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
