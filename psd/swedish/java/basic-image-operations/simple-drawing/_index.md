---
date: 2026-06-13
description: Lär dig hur du ritar en rektangel i PSD‑filer med Aspose.PSD för Java.
  Denna guide visar steg‑för‑steg‑kod, lägger till lager, server‑sidig bildbehandling
  och formritning.
keywords:
- how to draw rectangle
- how to create psd
- java graphics draw rectangle
- server side image processing
- add layer to psd
linktitle: Utför enkel ritning
schemas:
- author: Aspose
  dateModified: '2026-06-13'
  description: Learn how to draw rectangle in PSD files using Aspose.PSD for Java.
    This guide shows step‑by‑step code, adding layers, server‑side image processing
    and shape drawing.
  headline: How to Draw Rectangle in PSD with Aspose.PSD for Java
  type: TechArticle
- questions:
  - answer: Yes, the `Graphics` class also supports drawing ellipses, lines, and custom
      paths via the `drawPath` method.
    question: Can I draw other shapes besides rectangles?
  - answer: Absolutely; you can use `SolidBrush` with an ARGB color to include alpha
      transparency, enabling semi‑transparent overlays.
    question: Does Aspose.PSD support transparency in drawn shapes?
  - answer: Yes, each `Layer` object has a `setOpacity` method that accepts a value
      from 0 to 255, allowing fine‑grained control over layer transparency.
    question: Is it possible to edit the opacity of a layer?
  - answer: Use `PsdImage image = (PsdImage)Image.load("path/to/file.psd");` before
      manipulating layers. The loaded image retains all original layers and masks.
    question: How do I load an existing PSD file instead of creating a new one?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Hur man ritar en rektangel i PSD med Aspose.PSD för Java
url: /sv/java/basic-image-operations/simple-drawing/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Så ritar du en rektangel i PSD med Aspose.PSD för Java

## Introduktion

I den här handledningen kommer du att upptäcka **hur man ritar rektangel**-former i en Photoshop PSD‑fil med det rena Java‑biblioteket Aspose.PSD. Oavsett om du bygger en server‑sidig asset‑pipeline, automatiserar skapandet av miniatyrbilder eller lägger till dynamisk grafik i befintliga designer, ger stegen nedan en komplett, produktionsklar lösning. Vi går igenom hur man skapar ett nytt PSD‑dokument, lägger till ett lager, rensar bakgrunden och slutligen ritar både röda och blå rektanglar – utan att någonsin starta Photoshop.

## Snabba svar
- **Vilken är den primära klassen för att skapa en PSD‑fil?** `PsdImage`
- **Vilken metod rensar ett lagers bakgrundsfärg?** `Graphics.clear(Color)`
- **Hur ritar du en röd rektangel?** `graphic.drawRectangle(new Pen(Color.getRed()), new Rectangle(...))`
- **Behöver jag en licens för utveckling?** En gratis provversion fungerar för testning; en licens krävs för produktion.
- **Kan jag manipulera befintliga PSD‑filer med samma API?** Ja, Aspose.PSD stödjer fullständig PSD‑redigering.

## Vad är att rita en röd rektangel i en PSD‑fil?

Att rita en röd rektangel innebär att använda `Graphics`‑objektet för att rendera en rektangulär form fylld eller konturerad med färgen röd på ett specifikt lager i en PSD‑bild. Denna operation är vanlig för att markera områden, skapa platshållare eller lägga till enkel grafik programmässigt.

## Varför använda Aspose.PSD för Java för att manipulera PSD‑filer?

Aspose.PSD för Java stödjer **50+ in‑ och utdataformat**, kan bearbeta hundratals‑sidiga PSD‑filer utan att ladda hela filen i minnet, och körs på alla plattformar som stödjer Java 8 eller högre. Dess server‑sidiga bildbehandlingsmotor eliminerar behovet av Photoshop, minskar licenskostnader och möjliggör automatiserade arbetsflöden som hanterar upp till **10 GB** bilddata per timme på en modest VM.

## Förutsättningar

- Java Development Kit (JDK) 8 eller senare installerat på din maskin.  
- Aspose.PSD för Java‑biblioteket. Du kan ladda ner det från [Aspose.PSD for Java Documentation](https://reference.aspose.com/psd/java/).

## Importera paket

`import`‑satserna importerar de nödvändiga klasserna så att du kan arbeta med PSD‑bilder, lager, färger och grafik.

`PsdImage`‑klassen är Aspose.PSD:s översta objekt som representerar en enskild PSD‑fil i minnet.  
`Graphics` tillhandahåller ritprimitive som linjer, rektanglar och ellipser.  
`Color` och `Pen` låter dig ange linjefärger och tjocklek.  
`Layer`‑klassen representerar ett enskilt bildlager i ett PSD‑dokument.  
`Rectangle`‑klassen definierar position och storlek på ett rektangulärt område som används för ritoperationer.  
`SolidBrush`‑klassen fyller former med en solid färg.

## Vad är det första steget för att skapa ett PSD‑dokument?

Du instansierar `PsdImage` genom att ange canvasens bredd och höjd i pixlar, vilket skapar en tom PSD‑filstruktur. Efter att ha konfigurerat eventuella initiala lager eller bakgrund anropar du `save`‑metoden med en filsökväg för att skriva dokumentet till disk. Detta förbereder bilden för efterföljande redigeringsoperationer.

## Steg 1: Skapa ett nytt dokument

Skapa först ett nytt PSD‑dokument med önskad canvas‑storlek. Detta dokument kommer att hysa det lager på vilket vi ska rita.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Pen;
import com.aspose.psd.Rectangle;
import com.aspose.psd.brushes.SolidBrush;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
```

## Hur lägger du till ett nytt tomt lager i en PSD‑bild?

Skapa först en ny `Layer`‑instans med samma bredd och höjd som den överordnade `PsdImage`. Lägg sedan till detta lager i bildens `Layers`‑samling med `add`‑metoden. När lagret är en del av bilden hämtar du dess `Graphics`‑objekt för att utföra ritoperationer; utan detta steg visas inte teckningarna.

## Steg 2: Lägg till ett lager

Lägg sedan till ett nytt tomt lager som sträcker sig över bildens fulla bredd och höjd. Lager är väsentliga för att separera ritoperationer.

```java
//ExStart:CreateDocument
String outputDir = "Your Document Directory";
String outPsdFilePath = outputDir + "output.psd";
int width = 100;
int height = 100;

PsdImage image = new PsdImage(width, height);
//ExEnd:CreateDocument
```

## Vad är syftet med att rensa ett lagers bakgrundsfärg?

Att anropa `Graphics.clear` med en specifik `Color` fyller hela lagret med den färgen, vilket effektivt återställer all pixeldata. Detta säkerställer att tidigare innehåll tas bort och att lagret startar från en känd bakgrund, vilket undviker oväntad transparens eller färgblandning när PSD‑filen senare öppnas eller redigeras i Photoshop.

## Steg 3: Rita former

Vi använder `Graphics`‑klassen för att manipulera lagrets pixeldata. Nedan följer tre exempel som visar hur man rensar bakgrunden och ritar rektanglar med olika färger.

### Rensa lagrets färg (sätt bakgrund till gult)

```java
//ExStart:AddLayer
Layer layer = new Layer();
layer.setBottom(height);
layer.setRight(width);
image.addLayer(layer);
//ExEnd:AddLayer
```

### Rita en röd rektangel (primärt fokus)

```java
//ExStart:DrawRectangleYellow
Graphics graphic = new Graphics(layer);
graphic.clear(Color.getYellow());
//ExEnd:DrawRectangleYellow
```

### Rita en blå rektangel (ytterligare exempel)

```java
//ExStart:DrawRedRectangle
graphic.drawRectangle(new Pen(Color.getRed()), new Rectangle(30, 10, 40, 80));
//ExEnd:DrawRedRectangle
```

## Hur sparar du den redigerade PSD‑filen till disk?

Använd `save`‑metoden på `PsdImage`‑objektet, ange den fullständiga filsökvägen och specificera eventuellt önskat bildformat (PSD som standard). Detta skriver alla lager, masker och ritkommandon till en enda PSD‑fil som följer Photoshop‑specifikationen, så att den kan öppnas utan varningar.

## Steg 4: Spara ändringarna

Skriv slutligen den modifierade PSD‑bilden till disk. Filen kommer att innehålla det nya lagret och de ritade formerna.

```java
//ExStart:DrawBlueRectangle
graphic.drawRectangle(new Pen(new SolidBrush(Color.getBlue())), new Rectangle(10, 30, 80, 40));
//ExEnd:DrawBlueRectangle
```

## Vanliga problem och lösningar

- **Lagret syns inte efter ritning:** Se till att lagret har lagts till i bilden **innan** du skapar `Graphics`‑objektet. Ritytan måste vara kopplad till ett giltigt lager.
- **Färger visas felaktigt:** Verifiera att du använder `Color.getRed()` (eller `Color.getBlue()`) istället för att konstruera ett eget RGB‑värde som överstiger intervallet 0‑255.
- **Filen sparas inte:** Bekräfta att sökvägen `outputDir` existerar och att applikationen har skrivbehörighet. På Linux kan du behöva justera mappägarskap eller använda `Files.createDirectories`.
- **Prestandan saktar ner på stora filer:** Använd `PsdImage`‑metoden `setLoadOptions` för att endast ladda de kanaler som behövs, vilket minskar minnesförbrukningen för PSD‑filer större än 200 MB.

## Vanliga frågor

**Q1: Kan jag använda Aspose.PSD för Java för att manipulera befintliga PSD‑filer?**  
A1: Ja, Aspose.PSD för Java erbjuder omfattande funktionalitet för att redigera och manipulera befintliga PSD‑filer, inklusive lageromordning, maskjusteringar och vektorritning.

**Q2: Var kan jag hitta support för Aspose.PSD för Java?**  
A2: Du kan besöka [Aspose.PSD for Java Forum](https://forum.aspose.com/c/psd/34) för community‑driven hjälp och officiella svar från Aspose.

**Q3: Finns det en gratis provversion av Aspose.PSD för Java?**  
A3: Ja, du kan komma åt den kostnadsfria provversionen [här](https://releases.aspose.com/). Provversionen innehåller alla funktioner men lägger ett vattenmärke på sparade filer.

**Q4: Hur kan jag köpa en licens för Aspose.PSD för Java?**  
A4: Du kan köpa en licens via [Aspose.PSD Purchase Page](https://purchase.aspose.com/buy). Licensalternativen inkluderar evig licens, prenumeration och site‑licenser.

**Q5: Finns tillfälliga licenser för Aspose.PSD för Java?**  
A5: Ja, du kan skaffa en tillfällig licens [här](https://purchase.aspose.com/temporary-license/).

## Ytterligare vanliga frågor

**Q: Kan jag rita andra former än rektanglar?**  
A: Ja, `Graphics`‑klassen stödjer även ritning av ellipser, linjer och anpassade banor via `drawPath`‑metoden.

**Q: Stöder Aspose.PSD transparens i ritade former?**  
A: Absolut; du kan använda `SolidBrush` med en ARGB‑färg för att inkludera alfa‑transparens, vilket möjliggör halvtransparenta överlägg.

**Q: Är det möjligt att redigera opaciteten för ett lager?**  
A: Ja, varje `Layer`‑objekt har en `setOpacity`‑metod som accepterar ett värde mellan 0 och 255, vilket ger finjusterad kontroll över lagrets transparens.

**Q: Hur laddar jag en befintlig PSD‑fil istället för att skapa en ny?**  
A: Använd `PsdImage image = (PsdImage)Image.load("path/to/file.psd");` innan du manipulerar lager. Den laddade bilden behåller alla ursprungliga lager och masker.

## Slutsats

Du har nu lärt dig **hur man ritar rektangel**‑former och manipulerar lager i en PSD‑fil med Aspose.PSD för Java. Genom att skapa ett dokument, lägga till ett lager, rensa dess bakgrund och rita med `Graphics`‑API:t kan du automatisera otaliga grafiska designuppgifter på server‑sidan. Experimentera med olika pennor, borstar och lagereffekter för att bygga vidare på detta fundament till fullständiga bildgenereringspipeline.

```java
//ExStart:SaveChanges
image.save(outPsdFilePath);
//ExEnd:SaveChanges
```

{{< blocks/products/products-backtop-button >}}

## Relaterade handledningar

- [How to Draw Shapes Java – Basic Image Operations](/psd/java/basic-image-operations/)
- [Simple Resizing with Aspose.PSD – Java Image Manipulation Library](/psd/java/basic-image-operations/simple-resizing/)
- [Crop Image by Rectangle in Aspose.PSD for Java](/psd/java/image-editing/crop-image-by-rectangle/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

---

**Senast uppdaterad:** 2026-06-13  
**Testat med:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**Författare:** Aspose