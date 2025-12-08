---
date: 2025-12-08
description: Lär dig hur du konverterar PSD till PNG och ändrar storlek på bilder
  proportionellt i Java med Aspose.PSD. Denna steg‑för‑steg‑handledning täcker bildcachning,
  storleksändring och sparande som PNG.
language: sv
linktitle: Convert PSD to PNG & Resize Proportionally
second_title: Aspose.PSD Java API
title: Hur man konverterar PSD till PNG och ändrar storlek proportionellt med Aspose.PSD
  för Java
url: /java/advanced-image-manipulation/resize-image-proportionally/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hur man konverterar PSD till PNG och ändrar storlek proportionellt med Aspose.PSD för Java

## Introduction

Om du behöver **konvertera PSD till PNG** samtidigt som du behåller originalförhållandet, har du hamnat på rätt ställe. I den här handledningen går vi igenom en komplett **Aspose.PSD-handledning** som visar dig **hur man ändrar storlek på bild**‑filer proportionellt i Java, cachar bilden för optimal prestanda, och slutligen sparar resultatet som en PNG. I slutet kommer du kunna integrera detta arbetsflöde i någon Java‑baserad bildbehandlingspipeline.

## Quick Answers
- **Kan Aspose.PSD konvertera PSD till PNG?** Ja – ladda bara PSD-filen och spara den med `PngOptions`.
- **Stöder biblioteket proportionell storleksändring?** Absolut; använd `resizeWidthProportionally` och `resizeHeightProportionally`.
- **Behöver jag cacha bilden först?** Caching (`image.cacheData()`) förbättrar prestanda för stora PSD-filer.
- **Vilken Java-version krävs?** Java 8 eller senare stöds fullt ut.
- **Krävs en licens för produktion?** Ja, en kommersiell licens tar bort evalueringsvattenstämplar.

## What is “convert PSD to PNG” and why does it matter?

Att konvertera ett Photoshop-dokument (PSD) till en portable network graphics (PNG)-fil låter dig dela lagerdesign som ett lättviktigt, webbvänligt format. PNG behåller transparens och förlustfri kvalitet, vilket gör det idealiskt för UI‑tillgångar, miniatyrbilder eller någon situation där bildkvalitet är viktig.

## Why resize image proportionally in Java?

Att ändra storlek **hur man ändrar storlek på bild** utan att förvränga dess bildförhållande säkerställer att grafik ser naturlig ut på olika skärmar. `Aspose.PSD`‑API:et erbjuder dedikerade metoder för proportionell skalning, som automatiskt beräknar matchande höjd eller bredd, vilket sparar dig från manuella beräkningsfel.

## Prerequisites

Innan vi dyker ner i koden, se till att du har:

1. **Java Development Kit (JDK)** – Java 8 eller senare installerat.
2. **Aspose.PSD for Java** – ladda ner den senaste JAR‑filen från den officiella webbplatsen [here](https://releases.aspose.com/psd/java/).
3. En exempel‑PSD‑fil (`sample.psd`) placerad i en katalog som du kan referera till från ditt projekt.

## Import Packages

Lägg till nödvändiga imports i din Java‑klass. Dessa klasser ger dig åtkomst till bildladdning, caching, storleksändring och PNG‑utdataalternativ.

```java
import com.aspose.psd.Image;
import com.aspose.psd.imageoptions.PngOptions;
```

## Step 1: Load the PSD Image

Först, ladda käll‑PSD‑filen. Om filen är stor, minskar caching av bilddata minnesanvändningen när du utför efterföljande operationer.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

Image image = Image.load(sourceFile);

if (!image.isCached()) {
    // Image caching java – improves performance for large files
    image.cacheData();
}
```

## Step 2: Resize Image Proportionally (Java)

Bestäm nu de nya dimensionerna. I det här exemplet minskar vi bilden till **hälften** av dess originalstorlek samtidigt som vi bevarar bildförhållandet. Du kan justera målbredd eller mål‑höjd efter behov.

```java
int newWidth = image.getWidth() / 2;
image.resizeWidthProportionally(newWidth);

int newHeight = image.getHeight() / 2;
image.resizeHeightProportionally(newHeight);
```

> **Pro tip:** Använd antingen `resizeWidthProportionally` *eller* `resizeHeightProportionally`—biblioteket beräknar automatiskt den andra dimensionen för att hålla bilden proportionell.

## Step 3: Save the Resized Image as PNG

Slutligen, exportera den ändrade bilden till PNG‑format. Detta steg slutför **convert PSD to PNG**‑arbetsflödet.

```java
String destName = dataDir + "SimpleResizeImageProportionally_out.png";
image.save(destName, new PngOptions());
```

När koden körs kommer du att hitta en PNG‑fil som är hälften så stor som den ursprungliga PSD‑filen, med samma visuella kvalitet och utan förvrängning.

## Common Issues & Solutions

| Problem | Orsak | Lösning |
|---------|-------|---------|
| **OutOfMemoryError** | Stor PSD inte cachad | Anropa `image.cacheData()` innan storleksändring |
| **Blank PNG output** | Felaktig filsökväg | Verifiera `dataDir` och skrivbehörigheter |
| **Aspect ratio looks off** | Använder både bredd och höjd manuellt | Använd de proportionella metoderna som tillhandahålls av Aspose.PSD |

## Frequently Asked Questions

**Q: Är Aspose.PSD kompatibel med alla bildformat?**  
A: Aspose.PSD stöder PSD, PNG, JPEG, BMP, GIF och många fler. Se den fullständiga listan i [dokumentationen](https://reference.aspose.com/psd/java/).

**Q: Kan jag använda Aspose.PSD för kommersiella projekt?**  
A: Ja. Köp en kommersiell licens i [Aspose‑butiken](https://purchase.aspose.com/buy).

**Q: Finns tillfälliga licenser tillgängliga för testning?**  
A: Absolut – begär en tillfällig licens [här](https://purchase.aspose.com/temporary-license/) för utvärderingsändamål.

**Q: Var kan jag hitta community‑support?**  
A: [Aspose.PSD‑forumet](https://forum.aspose.com/c/psd/34) är en bra plats för att ställa frågor och dela lösningar.

**Q: Hur får jag åtkomst till den fullständiga API‑referensen?**  
A: Detaljerad API‑dokumentation finns tillgänglig [här](https://reference.aspose.com/psd/java/).

## Conclusion

Du vet nu hur du **konverterar PSD till PNG**, ändrar bildens storlek proportionellt och hanterar caching effektivt med Aspose.PSD för Java. Integrera dessa steg i dina egna applikationer för att leverera snabb, högkvalitativ bildbehandling utan att behöva Photoshop‑installationer.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2025-12-08  
**Tested With:** Aspose.PSD 24.12 for Java  
**Author:** Aspose