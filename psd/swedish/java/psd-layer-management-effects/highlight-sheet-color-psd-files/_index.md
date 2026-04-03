---
date: 2026-04-03
description: Lär dig hur du markerar färger på lager i PSD-filer med Aspose.PSD för
  Java. Följ vår steg‑för‑steg‑guide för att förbättra dina bildmanipuleringskunskaper
  i Java.
keywords:
- highlight sheet color psd
- change psd layer color
- Aspose.PSD Java
linktitle: Markera arkfärg i PSD‑filer med Aspise.PSD Java
second_title: Aspose.PSD Java API
title: Markera färg på blad i PSD-filer med Aspise.PSD Java
url: /sv/java/psd-layer-management-effects/highlight-sheet-color-psd-files/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Markera bladfärg i PSD-filer med Aspose.PSD Java

## Introduktion

Om du behöver **highlight sheet color psd**-filer programatiskt, har du kommit till rätt ställe. I den här handledningen går vi igenom ett komplett, praktiskt exempel som visar hur du ändrar bladfärgen på enskilda lager med Aspose.PSD för Java. Oavsett om du bygger ett batch‑bearbetningsverktyg, en anpassad redigerare eller bara automatiserar repetitiva designuppgifter, ger dig behärskning av denna teknik fin kontroll över dina PSD‑tillgångar.

## Snabba svar
- **Vad betyder “highlight sheet color”?** Det är en visuell indikator som tilldelas ett lager och visas som ett färgat streck i Photoshop‑lagerpanelen.  
- **Vilket bibliotek hanterar detta i Java?** Aspose.PSD för Java tillhandahåller `SheetColorHighlightEnum` och relaterade API:er.  
- **Behöver jag en licens för att prova?** En gratis provversion finns tillgänglig; en licens krävs för produktionsbruk.  
- **Kan jag ändra flera lager samtidigt?** Ja—loopa igenom `Layer[]`‑samlingen och sätt varje lagers markering.  
- **Vilken Java‑version krävs?** JDK 8 eller högre.

## Vad är “highlight sheet color psd”?

En bladfärgsmarkering är ett metadata‑attribut som lagras i en PSD‑fil och talar om för Photoshop (och kompatibla verktyg) att rita ett färgat fält bredvid lagernamnet. Det är användbart för snabbt identifiera lagergrupper—tänk på det som en visuell tagg som kan sättas till färger som violett, orange, gul osv.

## Varför ändra PSD‑lagerfärg programatiskt?

- **Automation:** Bearbeta hundratals filer utan manuella klick.  
- **Konsistens:** Upprätthåll ett namn‑/färgschema över ett designsystem.  
- **Integration:** Kombinera PSD‑manipulering med andra Java‑baserade arbetsflöden (t.ex. generering av resurser för mobilappar).  

## Förutsättningar

Innan vi dyker in i koden, se till att du har följande:

- **Java Development Kit (JDK) 8+** – ladda ner från [Java website](https://www.oracle.com/java/technologies/javase-downloads.html).  
- **IDE** – IntelliJ IDEA, Eclipse eller NetBeans (valfritt).  
- **Aspose.PSD for Java library** – hämta den från [Aspose's website](https://releases.aspose.com/psd/java/).  
- **Sample PSD file** – `SheetColorHighlightExample.psd` (skapa din egen eller hämta ett exempel online).  
- **Basic Java knowledge** – du bör vara bekväm med klasser, metoder och enkel fil‑I/O.

## Importera paket

Först importerar vi de klasser vi behöver. Dessa importeringar ger oss tillgång till kärnbildhantering, lagermanipulering och uppräkningen för bladfärgsmarkeringar.

```java
import com.aspose.psd.Image;
import com.aspose.psd.examples.Utils.Assert;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.fileformats.psd.layers.layerresources.SheetColorHighlightEnum;
```

## Steg‑för‑steg‑guide

### Steg 1: Ladda PSD‑filen

#### 1.1 Definiera filsökvägarna

Ställ in käll‑ och destinationssökvägarna. Ersätt platshållaren med den faktiska mappen som innehåller din PSD‑fil.

```java
String dataDir = "YOUR DOCUMENT DIRECTORY";

String sourceFileName = dataDir + "SheetColorHighlightExample.psd";
String exportPath = dataDir + "SheetColorHighlightExampleChanged.psd";
```

#### 1.2 Ladda PSD‑filen

Använd `Image.load()` och kasta resultatet till `PsdImage` så att vi kan arbeta med PSD‑specifika funktioner.

```java
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

### Steg 2: Åtkomst och inspektion av lager

Lager innehåller det visuella innehållet i en PSD. Vi läser de aktuella bladfärgsmarkeringarna för att verifiera starttillståndet.

#### 2.1 Åtkomst till första lagret

```java
Layer layer1 = im.getLayers()[0];
Assert.areEqual(SheetColorHighlightEnum.Violet, layer1.getSheetColorHighlight());
```

#### 2.2 Åtkomst till andra lagret

```java
Layer layer2 = im.getLayers()[1];
Assert.areEqual(SheetColorHighlightEnum.Orange, layer2.getSheetColorHighlight());
```

### Steg 3: Ändra bladfärgsmarkeringen

Nu ändrar vi markeringen för det första lagret till Gul, vilket demonstrerar hur man **change psd layer color** programatiskt.

```java
layer1.setSheetColorHighlight(SheetColorHighlightEnum.Yellow);
```

### Steg 4: Spara den modifierade PSD‑filen

Spara förändringarna till en ny fil så att originalet förblir orört.

```java
im.save(exportPath);
```

## Vanliga problem och lösningar

| Problem | Varför det händer | Lösning |
|---------|-------------------|---------|
| `Assert` fails | Lagrets befintliga markering är inte vad koden förväntar sig (t.ex. annan PSD). | Öppna PSD‑filen i Photoshop för att verifiera färgerna, eller ta bort `Assert`‑kontrollerna för ett mer flexibelt skript. |
| `NullPointerException` on `im.getLayers()` | Filen laddades inte korrekt (fel sökväg eller korrupt fil). | Dubbelkolla `sourceFileName` och säkerställ att PSD‑filen är giltig. |
| Highlight doesn’t appear in Photoshop | Photoshop cachar lagerinformation; du kan behöva öppna filen igen. | Stäng och öppna PSD‑filen efter sparning, eller använd `im.flush()` före sparning. |

## Vanliga frågor

**Q: Vad är Aspose.PSD för Java?**  
A: Aspose.PSD för Java är ett bibliotek som låter utvecklare läsa, redigera och spara PSD‑filer utan att behöva ha Photoshop installerat.

**Q: Kan jag använda Aspose.PSD för Java med andra filformat?**  
A: Ja—BMP, PNG, JPEG, GIF, TIFF och fler stöds, vilket möjliggör konvertering till och från PSD.

**Q: Är det möjligt att ångra ändringar gjorda i en PSD‑fil med Aspose.PSD för Java?**  
A: När filen har sparats är ändringarna permanenta. Behåll en backup av originalfilen om du behöver återgå.

**Q: Hur får jag en licens för Aspose.PSD för Java?**  
A: Köp en licens från [Aspose website](https://purchase.aspose.com/buy). Om du utvärderar kan du begära en [temporary license](https://purchase.aspose.com/temporary-license/) för en begränsad period.

**Q: Kan jag markera flera lager samtidigt i en PSD‑fil?**  
A: Absolut. Loop igenom `im.getLayers()` och anropa `setSheetColorHighlight()` på varje lager efter behov.

---

**Senast uppdaterad:** 2026-04-03  
**Testad med:** Aspose.PSD 24.11 för Java  
**Författare:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}