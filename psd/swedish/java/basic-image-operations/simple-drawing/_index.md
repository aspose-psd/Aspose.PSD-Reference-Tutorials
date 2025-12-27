---
date: 2025-12-27
description: Lär dig hur du ritar en röd rektangel och andra former i PSD‑filer med
  Aspose.PSD för Java. Denna steg‑för‑steg‑guide täcker att skapa dokument, lägga
  till lager och rita med kodexempel.
linktitle: Perform Simple Drawing
second_title: Aspose.PSD Java API
title: Rita röd rektangel med Aspose.PSD för Java
url: /sv/java/basic-image-operations/simple-drawing/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Rita röd rektangel med Aspose.PSD för Java

## Introduktion

Välkommen till denna steg‑för‑steg‑guide om hur du **ritar en röd rektangel** med Aspose.PSD för Java! I den här handledningen går vi igenom hur du skapar ett nytt PSD‑dokument, lägger till ett lager och ritar former med anpassade färger. Oavsett om du automatiserar grafiska resurser eller bygger ett design‑verktygs‑backend, ger den här handledningen dig de grundläggande byggstenarna.

## Snabba svar
- **Vad är den primära klassen för att skapa en PSD‑fil?** `PsdImage`
- **Vilken metod rensar ett lagers bakgrundsfärg?** `Graphics.clear(Color)`
- **Hur ritar du en röd rektangel?** `graphic.drawRectangle(new Pen(Color.getRed()), new Rectangle(...))`
- **Behöver jag en licens för utveckling?** En gratis provversion fungerar för testning; en licens krävs för produktion.
- **Kan jag manipulera befintliga PSD‑filer med samma API?** Ja, Aspose.PSD stöder full PSD‑redigering.

## Vad innebär att rita en röd rektangel i en PSD‑fil?
Att rita en röd rektangel innebär att använda `Graphics`‑objektet för att rendera en rektangulär form fylld eller konturerad med färgen röd på ett specifikt lager i en PSD‑bild. Denna operation är vanlig för att markera områden, skapa platshållare eller lägga till enkla grafikprogrammerat.

## Varför använda Aspose.PSD för Java för att manipulera PSD‑filer?
Aspose.PSD erbjuder ett rent Java‑API som låter dig läsa, redigera och skriva Photoshop PSD‑filer utan att behöva ha Photoshop installerat. Det stöder lagermhantering, färgmanipulation och vektorritning, vilket gör det idealiskt för server‑sidig bildbehandling, automatiserade tillgångspipelines och anpassad grafikgenerering.

## Förutsättningar

- Java Development Kit (JDK) installerat på din maskin.  
- Aspose.PSD för Java‑biblioteket. Du kan ladda ner det från den [Aspose.PSD for Java Documentation](https://reference.aspose.com/psd/java/).

## Importera paket

För att börja, importera de nödvändiga klasserna i ditt Java‑projekt:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Pen;
import com.aspose.psd.Rectangle;
import com.aspose.psd.brushes.SolidBrush;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
```

## Steg 1: Skapa ett nytt dokument

Först, skapa ett nytt PSD‑dokument med önskad canvas‑storlek. Detta dokument kommer att hysa lagret som vi ska rita på.

```java
//ExStart:CreateDocument
String outputDir = "Your Document Directory";
String outPsdFilePath = outputDir + "output.psd";
int width = 100;
int height = 100;

PsdImage image = new PsdImage(width, height);
//ExEnd:CreateDocument
```

## Steg 2: Lägg till ett lager

Därefter, lägg till ett nytt tomt lager som täcker bildens fulla bredd och höjd. Lager är viktiga för att separera ritoperationer.

```java
//ExStart:AddLayer
Layer layer = new Layer();
layer.setBottom(height);
layer.setRight(width);
image.addLayer(layer);
//ExEnd:AddLayer
```

## Steg 3: Rita former

Vi kommer att använda `Graphics`‑klassen för att manipulera lagrets pixeldata. Nedan följer tre exempel som visar hur man rensar bakgrunden och ritar rektanglar med olika färger.

### Rensa lagrets färg (sätt bakgrund till gul)

```java
//ExStart:DrawRectangleYellow
Graphics graphic = new Graphics(layer);
graphic.clear(Color.getYellow());
//ExEnd:DrawRectangleYellow
```

### Rita en röd rektangel (huvudfokus)

```java
//ExStart:DrawRedRectangle
graphic.drawRectangle(new Pen(Color.getRed()), new Rectangle(30, 10, 40, 80));
//ExEnd:DrawRedRectangle
```

### Rita en blå rektangel (ytterligare exempel)

```java
//ExStart:DrawBlueRectangle
graphic.drawRectangle(new Pen(new SolidBrush(Color.getBlue())), new Rectangle(10, 30, 80, 40));
//ExEnd:DrawBlueRectangle
```

## Steg 4: Spara ändringarna

Slutligen, skriv den modifierade PSD‑bilden till disk. Filen kommer att innehålla det nya lagret och de ritade formerna.

```java
//ExStart:SaveChanges
image.save(outPsdFilePath);
//ExEnd:SaveChanges
```

## Vanliga problem och lösningar

- **Lagret syns inte efter ritning:** Se till att lagret läggs till i bilden **innan** du skapar `Graphics`‑objektet.
- **Färger visas felaktigt:** Verifiera att du använder `Color.getRed()` (eller andra statiska metoder) istället för anpassade RGB‑värden som kan ligga utanför intervallet.
- **Filen sparas inte:** Bekräfta att sökvägen `outputDir` finns och att applikationen har skrivbehörighet.

## Vanliga frågor

### Q1: Kan jag använda Aspose.PSD för Java för att manipulera befintliga PSD‑filer?

A1: Ja, Aspose.PSD för Java erbjuder omfattande funktionalitet för att redigera och manipulera befintliga PSD‑filer.

### Q2: Var kan jag hitta support för Aspose.PSD för Java?

A2: Du kan besöka [Aspose.PSD for Java Forum](https://forum.aspose.com/c/psd/34) för eventuella supportrelaterade frågor.

### Q3: Finns det en gratis provversion tillgänglig för Aspose.PSD för Java?

A3: Ja, du kan komma åt den gratis provversionen [här](https://releases.aspose.com/).

### Q4: Hur kan jag köpa en licens för Aspose.PSD för Java?

A4: Du kan köpa en licens från [Aspose.PSD Purchase Page](https://purchase.aspose.com/buy).

### Q5: Finns tillfälliga licenser tillgängliga för Aspose.PSD för Java?

A5: Ja, du kan skaffa en tillfällig licens [här](https://purchase.aspose.com/temporary-license/).

## Ytterligare vanliga frågor

**Q: Kan jag rita andra former än rektanglar?**  
A: Ja, `Graphics`‑klassen stödjer även att rita ellipser, linjer och anpassade banor.

**Q: Stöder Aspose.PSD transparens i ritade former?**  
A: Absolut; du kan använda `SolidBrush` med en ARGB‑färg för att inkludera alfa‑transparens.

**Q: Är det möjligt att redigera opaciteten för ett lager?**  
A: Ja, varje `Layer`‑objekt har en `setOpacity`‑metod som accepterar ett värde från 0 till 255.

**Q: Hur laddar jag en befintlig PSD‑fil istället för att skapa en ny?**  
A: Använd `PsdImage image = (PsdImage)Image.load("path/to/file.psd");` innan du manipulerar lager.

## Slutsats

Du har nu lärt dig hur du **ritar en röd rektangel** och andra grundläggande former i en PSD‑fil med Aspose.PSD för Java. Genom att skapa ett dokument, lägga till ett lager, rensa dess bakgrund och rita med `Graphics`‑API:t kan du automatisera många grafiska designuppgifter. Utforska vidare genom att experimentera med olika penslar, lagereffekter och filformat.

---

**Last Updated:** 2025-12-27  
**Tested With:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}