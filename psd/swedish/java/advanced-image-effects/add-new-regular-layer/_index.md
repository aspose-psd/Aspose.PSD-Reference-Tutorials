---
date: 2026-04-08
description: Lär dig hur du exporterar PSD till PNG och skapar ett nytt PSD‑lager
  med Aspose.PSD för Java med en tillfällig Aspose‑licens. Denna steg‑för‑steg‑handledning
  täcker PSD‑bildmanipulation och att ställa in lagrets position.
keywords:
- aspose temporary license
- set layer position
- psd image manipulation
- create new psd layer
linktitle: Lägg till ett nytt vanligt lager i PSD
second_title: Aspose.PSD Java API
title: Exportera PSD till PNG och lägg till ett nytt vanligt lager med Aspose.PSD
  för Java – tillfällig Aspose‑licens
url: /sv/java/advanced-image-effects/add-new-regular-layer/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exportera PSD till PNG och lägg till ett nytt vanligt lager med Aspose.PSD för Java

## Introduktion

I den här **aspose psd tutorial** kommer du att upptäcka hur du **exporterar PSD till PNG** samtidigt som du **skapar ett nytt vanligt lager** i samma fil, **med en aspose temporär licens** för utveckling. Oavsett om du behöver generera webbklarar miniatyrer, förbereda resurser för en designpipeline, eller helt enkelt experimentera med **psd image manipulation**, så ger Aspose.PSD för Java dig full programmatisk kontroll. Vi går igenom varje steg—från att ladda källfilen till att spara både den uppdaterade PSD:n och en PNG-kopia—så att du kan börja manipulera PSD‑lager direkt.

## Snabba svar
- **Kan jag exportera PSD till PNG med ett anrop?** Ja, efter att ha lagt till lager kan du anropa `save` med `PngOptions`.
- **Behöver jag en licens för utveckling?** En temporär licens fungerar för testning; en full licens krävs för produktion.
- **Vilken Java‑version stöds?** Aspose.PSD fungerar med Java 8 och nyare.
- **Är lagerpositionering pixel‑baserad?** Ja, du anger vänster, topp, höger, botten‑koordinater i pixlar med hjälp av **set layer position**‑metoderna.
- **Behåller PNG‑filen lagertransparens?** PNG‑filen kommer att innehålla det sammanslagna resultatet av alla synliga lager.

## Varför använda en aspose temporär licens?

En **aspose temporary license** låter dig utvärdera hela funktionsuppsättningen i Aspose.PSD utan några funktionella begränsningar. Den tar bort utvärderingsvattenstämpeln, låser upp alla API:er—inklusive möjligheten att **create new psd layer**‑objekt—och låter dig testa din kod i en produktionsliknande miljö innan du köper en permanent licens.

## Förutsättningar

Innan du börjar, se till att du har:

- **Java Development Environment** – JDK 8+ och ett byggverktyg (Maven/Gradle) installerat.
- **Aspose.PSD for Java** – Ladda ner den senaste JAR‑filen från den officiella sidan [here](https://releases.aspose.com/psd/java/).
- **A sample PSD file** – Vi kommer att använda `OneLayer.psd` i exemplen.

## Importera paket

Lägg till de nödvändiga importerna i din Java‑klass. Dessa klasser tillhandahåller kärnfunktionaliteten för **psd image manipulation** och lagerhantering.

```java
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```

## Vad är “set layer position” och varför är det viktigt?

När du lägger till ett nytt lager måste du definiera var det visas på duken. Metoderna `setLeft`, `setTop`, `setRight` och `setBottom` **set layer position** i pixelkoordinater. Korrekt positionering säkerställer att dina grafikobjekt ligger exakt där du förväntar dig, vilket är avgörande för uppgifter som sammansättning av UI‑resurser eller förberedelse av utskriftsklara filer.

## Steg‑för‑steg‑guide

### Steg 1: Ladda PSD‑filen

Först, ladda den befintliga PSD‑filen du vill ändra. Detta ger dig ett `PsdImage`‑objekt som du kan arbeta med.

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "OneLayer.psd";
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

### Steg 2: Förbered pixeldata och rektanglar

Vi kommer att skapa två pixelbuffertar (`int[]`) och definiera de rektangulära områdena där de nya lagren ska målas. Detta är grunden för **creating a new psd layer**.

```java
int[] data1 = new int[2500];
int[] data2 = new int[2500];
Rectangle rect1 = new Rectangle(0, 0, 50, 50);
Rectangle rect2 = new Rectangle(0, 0, 100, 25);
```

### Steg 3: Initiera lagerdata

Fyll pixelbuffertarna med ett standard‑ARGB‑värde. Värdet `-10000000` motsvarar en halvtransparent mörk nyans.

```java
for (int i = 0; i < 2500; i++) {
    data1[i] = -10000000;
    data2[i] = -10000000;
}
```

### Steg 4: Lägg till vanliga lager (Manipulera PSD‑lager)

Nu **add regular layers** till PSD‑bilden och **set layer position** med hjälp av vänster, topp, höger och botten‑egenskaperna. Detta demonstrerar hur du **manipulate PSD layers** programatiskt.

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

När lagren är på plats, spara det modifierade dokumentet. Först exporterar vi resultatet till PNG (steg **export psd to png**), sedan sparar vi PSD‑filen med de nya lagren.

```java
String exportPath = dataDir + "Updated.psd";
String exportPathPng = dataDir + "Updated.png";

im.save(exportPath, new PsdOptions());          // Save the updated PSD
im.save(exportPathPng, new PngOptions());       // Export PSD to PNG
```

> **Pro tip:** Om du bara behöver PNG‑filen kan du hoppa över PSD‑`save`‑anropet och direkt anropa `save` med `PngOptions`.

## Vanliga problem & felsökning

| Symptom | Likely Cause | Fix |
|---------|--------------|-----|
| PNG visas tom | Lager är osynliga eller helt transparenta | Se till att du sätter icke‑transparenta pixelvärden eller anropar `layer.setVisible(true)`. |
| `ArrayIndexOutOfBoundsException` | Mismatch mellan rektangelns storlek och pixelarrayens längd | Verifiera att `rect.width * rect.height == dataArray.length`. |
| LicenseException at runtime | Ingen giltig licens laddad | Läs in en temporär eller permanent licens innan du anropar några API‑metoder. |

## Vanliga frågor

**Q: Är Aspose.PSD kompatibel med Java 8?**  
A: Ja, Aspose.PSD stödjer Java 8 och senare versioner.

**Q: Kan jag applicera transformationer (rotera, skala) på de tillagda lagren?**  
A: Absolut! `Layer`‑klassen tillhandahåller metoder som `rotate`, `scale` och `translate` för full kontroll över transformationer.

**Q: Var kan jag hitta ytterligare Aspose.PSD‑dokumentation?**  
A: Detaljerade API‑dokument finns tillgängliga [here](https://reference.aspose.com/psd/java/).

**Q: Hur får jag en temporär licens för Aspose.PSD?**  
A: Besök sidan för temporär licens [here](https://purchase.aspose.com/temporary-license/).

**Q: Finns det community‑forum för Aspose.PSD‑support?**  
A: Ja, gå med i diskussionerna på Aspose‑forumet [here](https://forum.aspose.com/c/psd/34).

## Slutsats

Du har nu lärt dig hur du **exporterar PSD till PNG** samtidigt som du **lägger till nya vanliga lager** med Aspose.PSD för Java, och du har sett hur en **aspose temporary license** gör det möjligt att prova detta arbetsflöde utan begränsningar. Denna handledning visar de grundläggande **psd image manipulation**‑funktionerna: ladda en fil, skapa lager, fylla pixeldata och exportera den färdiga kompositionen. Känn dig fri att experimentera med olika rektangelstorlekar, pixelfärger eller lager‑effekter för att anpassa resultatet efter ditt projekts behov.

---

**Senast uppdaterad:** 2026-04-08  
**Testat med:** Aspose.PSD 24.11 for Java  
**Författare:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}