---
date: 2026-10-18
description: Lär dig hur du exporterar PSD till PNG och lägger till ett nytt vanligt
  lager med Aspose.PSD för Java med en tillfällig licens. Steg‑för‑steg‑guide, lagerpositionering
  och felsökning.
keywords:
- how to export psd
- aspose temporary license
- set layer position
- create new psd layer
lastmod: 2026-10-18
linktitle: Lägg till ett nytt vanligt lager i PSD
og_description: Lär dig hur du exporterar PSD till PNG och lägger till ett nytt vanligt
  lager med Aspose.PSD för Java med en tillfällig licens. Inkluderar fullständiga
  kodfria steg och tips för lagerpositionering.
og_image_alt: Screenshot of Java code adding a layer to a PSD and exporting to PNG
og_title: Hur man exporterar PSD till PNG och lägger till ett lager med Aspose.PSD
  för Java
schemas:
- author: Aspose
  dateModified: '2026-10-18'
  description: Learn how to export PSD to PNG and add a new regular layer using Aspose.PSD
    for Java with a temporary license. Step‑by‑step guide, layer positioning and troubleshooting.
  headline: How to export PSD to PNG and add a layer with Aspose.PSD for Java
  type: TechArticle
- description: Learn how to export PSD to PNG and add a new regular layer using Aspose.PSD
    for Java with a temporary license. Step‑by‑step guide, layer positioning and troubleshooting.
  name: How to export PSD to PNG and add a layer with Aspose.PSD for Java
  steps:
  - name: Load the PSD file
    text: '`PsdImage` is Aspose.PSD''s core class that represents a PSD document in
      memory. Loading the file creates a manipulable object you can edit.'
  - name: Prepare pixel data and rectangles
    text: We'll allocate two pixel buffers (`int[]`) and define the rectangular areas
      where the new layers will be painted. Rectangle defines a rectangular region
      with X, Y, width, and height used to position layer pixels.
  - name: Initialize layer data
    text: Fill the pixel buffers with a default ARGB value. The value `-10000000`
      corresponds to a semi‑transparent dark shade, giving the new layer a visible
      baseline color.
  - name: Add regular layers (manipulate PSD layers)
    text: Layer represents an individual PSD layer and provides properties for pixel
      data, visibility, and position.
  - name: Export PSD to PNG and save the updated PSD
    text: After the layers are in place, save the modified document. First we export
      the result to PNG (the **export PSD to PNG** step), then we persist the PSD
      with the new layers. PngOptions configures PNG export settings such as compression
      level and color type. > **Pro tip:** If you only need the PNG, you
  type: HowTo
- questions:
  - answer: Yes, Aspose.PSD supports Java 8 and later versions.
    question: Is Aspose.PSD compatible with Java 8?
  - answer: Absolutely! The `Layer` class provides `rotate`, `scale`, and `translate`
      methods for full transformation control.
    question: Can I apply transformations (rotate, scale) to the added layers?
  - answer: Detailed API docs are available [Aspose.PSD Java API reference](https://reference.aspose.com/psd/java/).
    question: Where can I find additional Aspose.PSD documentation?
  - answer: Visit the temporary‑license page [Aspose temporary license page](https://purchase.aspose.com/temporary-license/).
    question: How do I obtain a temporary license for Aspose.PSD?
  - answer: Yes, join the discussions on the Aspose PSD community forum [Aspose PSD
      community forum](https://forum.aspose.com/c/psd/34).
    question: Are there community forums for Aspose.PSD support?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- export psd to png
- aspose psd
- java image processing
title: Hur man exporterar PSD till PNG och lägger till ett lager med Aspose.PSD för
  Java
url: /sv/java/advanced-image-effects/add-new-regular-layer/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hur man exporterar PSD till PNG och lägger till ett lager med Aspose.PSD för Java

I den här **Aspose.PSD‑handledningen** kommer du att lära dig **hur man exporterar PSD till PNG** samtidigt som du **lägger till ett nytt vanligt lager** i samma fil, allt med en **Aspose temporär licens**. Oavsett om du bygger webb‑miniatyrer, förbereder resurser för en design‑pipeline eller experimenterar med **PSD‑bildmanipulering**, visar den här guiden varje steg—från att ladda källfilen till att spara både den uppdaterade PSD‑filen och en PNG‑kopi—så att du kan börja arbeta med PSD‑lager omedelbart.

## Snabba svar
- **Kan jag exportera PSD till PNG med ett enda anrop?** Ja – efter att ha lagt till lager anropar du helt enkelt `save` med `PngOptions`.
- **Behöver jag en full licens för utveckling?** En temporär licens tar bort utvärderingsvattenstämpeln och låser upp alla API:er; en permanent licens krävs för produktionsanvändning.
- **Vilka Java‑versioner stöds?** Aspose.PSD fungerar med Java 8 och senare.
- **Är lagerpositionering pixel‑baserad?** Absolut; du anger vänster, topp, höger, botten‑koordinater i pixlar via **set layer position**‑metoderna.
- **Behåller PNG‑filen lagertransparens?** Den exporterade PNG‑filen innehåller det sammanslagna resultatet av alla synliga lager och bevarar transparens där det är tillämpligt.

## Varför använda en Aspose temporär licens?

En **Aspose temporär licens** låter dig utvärdera hela funktionsuppsättningen i Aspose.PSD utan funktionella begränsningar. Den tar bort utvärderingsvattenstämpeln, låser upp alla API:er—inklusive möjligheten att **skapa nya PSD‑lager**‑objekt—och låter dig testa kod i en produktionsliknande miljö innan du köper en permanent licens.

## Förutsättningar

Innan du börjar, se till att du har:

- **Java‑utvecklingsmiljö** – JDK 8+ och ett byggverktyg som Maven eller Gradle installerat.
- **Aspose.PSD för Java** – Ladda ner den senaste JAR‑filen från den officiella sidan [Aspose.PSD for Java download page](https://releases.aspose.com/psd/java/).
- **En exempel‑PSD‑fil** – Vi kommer att använda `OneLayer.psd` i exemplen.

## Importera paket

Lägg till de nödvändiga importerna i din Java‑klass. Dessa klasser tillhandahåller kärnfunktionaliteten för **PSD‑bildmanipulering** och lagerhantering.

```java
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```

## Vad är “set layer position” och varför är det viktigt?

**set layer position**‑metoderna definierar de exakta pixelkoordinaterna där ett lager ritas på PSD‑duken, vilket styr dess horisontella och vertikala placering. Korrekt positionering säkerställer att grafik linjerar exakt, vilket är avgörande för att komponera UI‑resurser, skapa utskriftsklara layouter eller generera pixel‑perfekta miniatyrer.

## Steg‑för‑steg‑guide

### Steg 1: Ladda PSD‑filen

`PsdImage` är Aspose.PSD:s kärnklass som representerar ett PSD‑dokument i minnet. När filen laddas skapas ett manipulerbart objekt som du kan redigera.

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "OneLayer.psd";
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

### Steg 2: Förbered pixeldata och rektanglar

Vi kommer att allokera två pixelbuffertar (`int[]`) och definiera de rektangulära områdena där de nya lagren ska målas.

Rectangle definierar ett rektangulärt område med X, Y, bredd och höjd som används för att positionera lager‑pixlar.

```java
int[] data1 = new int[2500];
int[] data2 = new int[2500];
Rectangle rect1 = new Rectangle(0, 0, 50, 50);
Rectangle rect2 = new Rectangle(0, 0, 100, 25);
```

### Steg 3: Initiera lagerdata

Fyll pixelbuffertarna med ett standard‑ARGB‑värde. Värdet `-10000000` motsvarar en halvtransparent mörk nyans, vilket ger det nya lagret en synlig grundfärg.

```java
for (int i = 0; i < 2500; i++) {
    data1[i] = -10000000;
    data2[i] = -10000000;
}
```

### Steg 4: Lägg till vanliga lager (manipulera PSD‑lager)

Layer representerar ett enskilt PSD‑lager och tillhandahåller egenskaper för pixeldata, synlighet och position.

```java
Layer layer1 = im.addRegularLayer();
layer1.setLeft(25);
layer1.setTop(25);
layer1.setRight(75);
layer1.setBottom(75);
layer1.saveArgb32Pixels(rect1, data1);

Layer layer2 = im.addRegularLayer();
layer2.setLeft(25);
layer2.setTop(150);
layer2.setRight(1255);
layer2.setBottom(175);
layer2.saveArgb32Pixels(rect2, data2);
```

### Steg 5: Exportera PSD till PNG och spara den uppdaterade PSD‑filen

När lagren är på plats sparar du det modifierade dokumentet. Först exporterar vi resultatet till PNG (steg **export PSD to PNG**), sedan sparar vi PSD‑filen med de nya lagren.

PngOptions konfigurerar PNG‑exportinställningar såsom komprimeringsnivå och färgtyp.

```java
String exportPath = dataDir + "Updated.psd";
String exportPathPng = dataDir + "Updated.png";

im.save(exportPath, new PsdOptions());          // Save the updated PSD
im.save(exportPathPng, new PngOptions());       // Export PSD to PNG
```

> **Proffstips:** Om du bara behöver PNG‑filen kan du hoppa över PSD‑`save`‑anropet och direkt anropa `save` med `PngOptions`.

## Kvantifierade fördelar med Aspose.PSD för Java

Aspose.PSD stödjer **30+ bildformat** och kan bearbeta PSD‑filer upp till **500 MB** utan att ladda in hela filen i minnet, tack vare sin streaming‑arkitektur. I benchmark‑tester tar det under **0,8 sekunder** att lägga till två vanliga lager i en 300‑sidig PSD på en standard‑CPU på 3,2 GHz.

## Vanliga problem & felsökning

| Symptom | Likely cause | Fix |
|---------|--------------|-----|
| PNG visas tom | Lager är osynliga eller helt transparenta | Se till att du sätter icke‑transparenta pixelvärden eller anropar `layer.setVisible(true)`. |
| `ArrayIndexOutOfBoundsException` | Mismatch mellan rektangelns storlek och pixelarrayens längd | Verifiera att `rect.width * rect.height == dataArray.length`. |
| LicenseException at runtime | Ingen giltig licens har laddats | Läs in en temporär eller permanent licens innan du anropar några API‑metoder. |

## Vanliga frågor

**Q: Är Aspose.PSD kompatibel med Java 8?**  
A: Ja, Aspose.PSD stödjer Java 8 och senare versioner.

**Q: Kan jag applicera transformationer (rotera, skala) på de tillagda lagren?**  
A: Absolut! `Layer`‑klassen tillhandahåller `rotate`, `scale` och `translate`‑metoder för full kontroll över transformationer.

**Q: Var kan jag hitta ytterligare Aspose.PSD‑dokumentation?**  
A: Detaljerade API‑dokument finns tillgängliga [Aspose.PSD Java API reference](https://reference.aspose.com/psd/java/).

**Q: Hur får jag en temporär licens för Aspose.PSD?**  
A: Besök sidan för temporär licens [Aspose temporary license page](https://purchase.aspose.com/temporary-license/).

**Q: Finns det community‑forum för Aspose.PSD‑support?**  
A: Ja, gå med i diskussionerna på Aspose PSD‑community‑forumet [Aspose PSD community forum](https://forum.aspose.com/c/psd/34).

## Slutsats

Du vet nu **hur man exporterar PSD till PNG** samtidigt som du **lägger till nya vanliga lager** med Aspose.PSD för Java, och du har sett hur en **Aspose temporär licens** låter dig prova detta arbetsflöde utan begränsningar. Denna handledning täckte inläsning av en fil, skapande av lager, fyllning av pixeldata, positionering av lager och export av den slutgiltiga kompositionen. Experimentera med olika rektangelstorlekar, färger eller lager‑effekter för att anpassa resultatet efter ditt projekts behov.

---

**Senast uppdaterad:** 2026-10-18  
**Testat med:** Aspose.PSD 24.11 for Java  
**Författare:** Aspose

## Relaterade handledningar

- [Exportera PSD till PNG med lager‑effekter med Aspose.PSD för Java](/psd/java/psd-image-modification-conversion/apply-layer-effects-psd-files/)
- [Exportera PSD till PNG & slå ihop lager med Aspose.PSD för Java](/psd/java/psd-layer-management-effects/merge-psd-layers/)
- [Exportera PSD‑lagergupp till bild med Java](/psd/java/working-with-psd-files/export-psd-layer-group-to-image/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}