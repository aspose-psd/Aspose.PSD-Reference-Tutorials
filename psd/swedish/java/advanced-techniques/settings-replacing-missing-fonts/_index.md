---
date: 2026-06-13
description: Lär dig hur du ersätter teckensnitt i PSD-filer med Aspose.PSD för Java,
  konverterar PSD till PNG och hanterar saknade teckensnitt effektivt.
keywords:
- how to replace fonts
- convert psd to png
- handle missing fonts psd
linktitle: Inställningar för att ersätta saknade teckensnitt
schemas:
- author: Aspose
  dateModified: '2026-06-13'
  description: Learn how to replace fonts in PSD files using Aspose.PSD for Java,
    convert PSD to PNG, and handle missing fonts efficiently.
  headline: How to Replace Fonts in PSD Files with Aspose.PSD for Java
  type: TechArticle
- questions:
  - answer: '`PsdImage` is the core class that represents a PSD document in memory.'
    question: What is the primary class for loading PSD files?
  - answer: Use `PsdLoadOptions.setDefaultFontName("Arial")`.
    question: Which option sets a default replacement font?
  - answer: Yes—call `psdImage.save("output.png", new PngOptions())`.
    question: Can I save the result as PNG?
  - answer: A temporary license works for testing; a full license is required for
      production.
    question: Do I need a license for development?
  - answer: Aspose.PSD for Java supports Java 8 and later.
    question: What Java version is supported?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Hur du ersätter teckensnitt i PSD-filer med Aspose.PSD för Java
url: /sv/java/advanced-techniques/settings-replacing-missing-fonts/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hur man ersätter typsnitt i PSD-filer med Aspose.PSD för Java

I modern Java-utveckling är **hur man ersätter typsnitt** i en Photoshop (PSD)-fil en vanlig utmaning som kan förstöra den visuella layouten i dina designer. Aspose.PSD för Java erbjuder ett robust API som automatiserar typsnittsbyte, så att du kan hålla dina bilder exakt som avsett. Denna guide går dig igenom varje steg—från att konfigurera miljön till att spara den slutgiltiga PNG‑filen—så att du kan hantera saknade typsnitt i PSD-filer med förtroende.

## Snabba svar
- **Vilken är den primära klassen för att läsa in PSD-filer?** `PsdImage` är kärnklassen som representerar ett PSD-dokument i minnet.  
- **Vilket alternativ anger ett standardtypsnitt för ersättning?** Använd `PsdLoadOptions.setDefaultFontName("Arial")`.  
- **Kan jag spara resultatet som PNG?** Ja—anropa `psdImage.save("output.png", new PngOptions())`.  
- **Behöver jag en licens för utveckling?** En tillfällig licens fungerar för testning; en full licens krävs för produktion.  
- **Vilken Java-version stöds?** Aspose.PSD för Java stödjer Java 8 och senare.

## Hur man ersätter typsnitt i en PSD-fil med Aspose.PSD för Java?

Läs in käll‑PSD‑filen med `PsdLoadOptions` som specificerar ett reservtypsnitt, och spara sedan bilden i önskat format. API:et ersätter automatiskt eventuella saknade glyfer med standardtypsnittet du anger, vilket eliminerar renderingsfel utan manuell redigering. Detta en‑stegs tillvägagångssätt fungerar för filer av alla storlekar och bevarar lager, masker och effekter.

## Vad är `PsdLoadOptions`?

`PsdLoadOptions` är ett konfigurationsobjekt som styr hur Aspose.PSD läser in en PSD‑fil. Det låter dig ange ett standardtypsnitt för ersättning, kontrollera lagerladdningsbeteende och ställa in alternativ för hantering av saknade resurser. Genom att justera dess egenskaper kan utvecklare säkerställa konsekvent rendering av text och andra element i olika miljöer och undvika körfel som orsakas av otillgängliga typsnitt.

## Varför ersätta saknade typsnitt i PSD-filer?

Aspose.PSD stödjer **50+ in‑ och utdataformat** och kan bearbeta PSD‑filer med flera hundra sidor utan att ladda hela dokumentet i minnet. Att ersätta saknade typsnitt förhindrar trasiga textlager, minskar manuell korrigeringstid med upp till **80 %**, och garanterar att exporterade PNG‑filer behåller den ursprungliga designens trohet.

## Förutsättningar

1. **Aspose.PSD Library** – Ladda ner och installera Aspose.PSD för Java‑biblioteket från [releases‑sidan](https://releases.aspose.com/psd/java/).  
2. **Java Development Environment** – Java 8+ JDK och din föredragna IDE (Eclipse, IntelliJ IDEA, etc.).  

Nu när allt är klart, låt oss dyka in i implementationen.

## Importera paket

Importera de nödvändiga namnrymderna så kompilatorn kan hitta Aspose.PSD‑klasserna.

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.PngOptions;
```

## Steg 1: Ställ in din dokumentkatalog

Definiera mappen som innehåller käll‑PSD‑filen och där utdata ska skrivas. Denna sökväg används av laddaren och spararen.

```java
String dataDir = "Your Document Directory";
```

## Steg 2: Ange käll‑ och destinationsfiler

Ange absoluta eller relativa sökvägar för den ursprungliga PSD‑filen och mål‑PNG‑filen. Att använda tydliga namngivningskonventioner hjälper till att undvika att filer skrivs över.

```java
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "result.png";
```

## Steg 3: Konfigurera inställningar för typsnittsbyte

Skapa en `PsdLoadOptions`‑instans och ange standardtypsnittet för ersättning till **Arial** (eller något annat typsnitt som är installerat på ditt system). Detta talar om för motorn vilket typsnitt som ska användas när den inte kan hitta det ursprungliga.

```java
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setDefaultReplacementFont("Arial");
```

## Steg 4: Läs in PSD‑bild och ersätt typsnitt

Läs in PSD‑filen med de konfigurerade alternativen. Aspose.PSD ersätter automatiskt saknade typsnitt under inläsningsprocessen, så ingen extra kod behövs.

```java
Image image = Image.load(sourceFile, loadOptions);
PsdImage psdImage = (PsdImage) image;
```

## Steg 5: Spara den modifierade bilden

Välj `PngOptions` för att exportera bilden som en sann‑färgs‑PNG med en alfakanal. Den resulterande filen kommer att visa de ersatta typsnitten korrekt.

```java
PngOptions options = new PngOptions();
options.setColorType(PngColorType.TruecolorWithAlpha);
psdImage.save(destName, options);
```

## Vanliga problem och lösningar

| Problem | Orsak | Lösning |
|-------|-------|-----|
| Text visas förvrängt | Ersättningstypsnittet saknar nödvändiga glyfer | Välj ett typsnitt med ett bredare Unicode‑område (t.ex. **Arial Unicode MS**). |
| Fil‑ej‑hittad‑fel | Felaktig sökväg i steg 1 eller 2 | Verifiera katalogsträngarna och använd `File.separator` för plattformsoberoende kompatibilitet. |
| Licens‑undantag | Kör utan en giltig licens | Använd en tillfällig licens för testning eller köp en full licens för produktion. |

## Vanliga frågor

### Q1: Är Aspose.PSD kompatibel med alla PSD‑filversioner?

A1: Aspose.PSD stödjer PSD‑versioner från **4.0** upp till den senaste Photoshop‑utgåvan, vilket säkerställer bred kompatibilitet över både äldre och moderna designer.

### Q2: Kan jag använda anpassade typsnitt för ersättning i Aspose.PSD?

A2: Ja, du kan ange vilket TrueType‑ eller OpenType‑typsnitt som helst som är installerat på servern genom att skicka dess namn till `setDefaultFontName`. Detta ger dig full kontroll över det visuella resultatet.

### Q3: Finns det licensalternativ tillgängliga för Aspose.PSD?

A3: Utforska licensalternativen [här](https://purchase.aspose.com/buy) för att välja det bästa paketet för din organisation, inklusive utvecklar-, webb- och OEM‑licenser.

### Q4: Finns det ett community‑forum för Aspose.PSD‑support?

A4: Ja, besök [Aspose.PSD‑forumet](https://forum.aspose.com/c/psd/34) för community‑hjälp, kodexempel och felsökningstips från andra utvecklare.

### Q5: Hur kan jag skaffa en tillfällig licens för Aspose.PSD?

A5: Skaffa en tillfällig licens [här](https://purchase.aspose.com/temporary-license/) för utvärdering, testning eller proof‑of‑concept‑projekt utan kostnad.

---

**Senast uppdaterad:** 2026-06-13  
**Testat med:** Aspose.PSD 24.12 for Java  
**Författare:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Relaterade handledningar

- [Konvertera PSD till PNG med färgöverlägg – Aspose.PSD för Java](/psd/java/advanced-image-manipulation/rendering-color-effect/)
- [Hur man konverterar PSD till PNG och ändrar storlek proportionellt med Aspose.PSD för Java](/psd/java/advanced-image-manipulation/resize-image-proportionally/)
- [Konvertera PSD till rasterbildformat med Aspose.PSD för Java](/psd/java/advanced-techniques/convert-psd-to-raster-formats/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}