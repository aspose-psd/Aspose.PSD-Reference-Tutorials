---
date: 2026-02-09
description: Lär dig hur du konverterar PSD till PNG och ändrar storlek på bilder
  proportionellt i Java med Aspose.PSD. Denna steg‑för‑steg‑handledning täcker bildcachning,
  storleksändring och sparande som PNG.
linktitle: Convert PSD to PNG & Resize Proportionally
second_title: Aspose.PSD Java API
title: Hur man konverterar PSD till PNG och ändrar storlek proportionellt med Aspose.PSD
  för Java
url: /sv/java/advanced-image-manipulation/resize-image-proportionally/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hur man konverterar PSD till PNG och ändrar storlek proportionellt med Aspose.PSD för Java

## Introduktion

Om du behöver **konvertera PSD till PNG** samtidigt som du behåller det ursprungliga bildförhållandet, har du hamnat på rätt ställe. I den här **Aspose.PSD Java**‑handledningen går vi igenom en komplett **java image processing tutorial** som visar hur du **ändrar storlek på bild**‑filer proportionellt, cachar bilden för optimal prestanda och slutligen sparar resultatet som en PNG. När du är klar kan du integrera detta arbetsflöde i vilken Java‑baserad bildbehandlingspipeline som helst.

## Snabba svar
- **Kan Aspose.PSD konvertera PSD till PNG?** Ja – ladda bara PSD‑filen och spara den med `PngOptions`.
- **Stöder biblioteket proportionell storleksändring?** Absolut; använd `resizeWidthProportionally` och `resizeHeightProportionally`.
- **Behöver jag cacha bilden först?** Caching (`image.cacheData()`) förbättrar prestandan för stora PSD‑filer.
- **Vilken Java‑version krävs?** Java 8 eller nyare stöds fullt ut.
- **Behövs en licens för produktion?** Ja, en kommersiell licens tar bort utvärderingsvattenstämplar.

## Vad betyder “konvertera PSD till PNG” och varför är det viktigt?

Att konvertera ett Photoshop‑dokument (PSD) till en Portable Network Graphics (PNG)‑fil låter dig dela lagerbaserade designer som ett lättviktigt, webbvänligt format. PNG behåller transparens och förlustfri kvalitet, vilket gör det idealiskt för UI‑tillgångar, miniatyrbilder eller alla situationer där bildkvalitet är viktig.

## Varför ändra bildstorlek proportionellt i Java?

Att ändra **hur man ändrar storlek på bild** utan att förvränga bildförhållandet säkerställer att grafik ser naturlig ut på olika skärmar. `Aspose.PSD`‑API:et erbjuder dedikerade metoder för **resize image proportionally**, som automatiskt beräknar motsvarande höjd eller bredd och sparar dig från manuella beräkningsfel.

## Varför detta är viktigt för utvecklare

- **Minskad PSD‑filstorlek** – Genom att skala ner stora PSD‑filer innan konvertering minskar du minnesanvändningen och påskyndar efterföljande bearbetning.  
- **Konsekvent UI‑rendering** – Proportionell storleksändring garanterar att ikoner och grafik behåller sin visuella balans på alla enheter.  
- **Ingen Photoshop‑beroende** – Du kan utföra dessa operationer på en server eller i en CI‑pipeline utan att installera Photoshop.

## Förutsättningar

Innan vi dyker ner i koden, se till att du har:

1. **Java Development Kit (JDK)** – Java 8 eller senare installerat.  
2. **Aspose.PSD för Java** – ladda ner den senaste JAR‑filen från den officiella sidan [here](https://releases.aspose.com/psd/java/).  
3. En exempel‑PSD‑fil (`sample.psd`) placerad i en katalog som du kan referera till från ditt projekt.

## Importera paket

Lägg till nödvändiga import‑satser i din Java‑klass. Dessa klasser ger dig åtkomst till bildladdning, caching, storleksändring och PNG‑utdataalternativ.

```java
import com.aspose.psd.Image;
import com.aspose.psd.imageoptions.PngOptions;
```

## Steg 1: Ladda PSD‑bilden

Först laddar du käll‑PSD‑filen. Om filen är stor minskar caching av bilddata minnesbelastningen när du utför efterföljande operationer.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

Image image = Image.load(sourceFile);

if (!image.isCached()) {
    // Image caching java – improves performance for large files
    image.cacheData();
}
```

## Steg 2: Ändra bildstorlek proportionellt (Java)

Bestäm nu de nya dimensionerna. I detta exempel minskar vi bilden till **hälften** av dess ursprungliga storlek samtidigt som vi bevarar bildförhållandet. Du kan justera målbredd eller mål‑höjd efter behov.

```java
int newWidth = image.getWidth() / 2;
image.resizeWidthProportionally(newWidth);

int newHeight = image.getHeight() / 2;
image.resizeHeightProportionally(newHeight);
```

> **Proffstips:** Använd antingen `resizeWidthProportionally` *eller* `resizeHeightProportionally` — biblioteket beräknar automatiskt den andra dimensionen för att hålla bilden proportionell.

## Steg 3: Spara den ändrade bilden som PNG

Till sist exporterar du den ändrade bilden till PNG‑format. Detta steg slutför **konvertera PSD till PNG**‑arbetsflödet.

```java
String destName = dataDir + "SimpleResizeImageProportionally_out.png";
image.save(destName, new PngOptions());
```

När koden körs hittar du en PNG‑fil som är hälften så stor som den ursprungliga PSD‑filen, med samma visuella kvalitet och utan förvrängning.

## Vanliga problem & lösningar

| Problem | Orsak | Åtgärd |
|-------|-------|-----|
| **OutOfMemoryError** | Stor PSD ej cachad | Anropa `image.cacheData()` innan storleksändring |
| **Blank PNG‑utdata** | Felaktig filsökväg | Kontrollera `dataDir` och skrivbehörigheter |
| **Bildförhållandet ser felaktigt ut** | Manuell angivelse av både bredd och höjd | Använd de proportionella metoderna som tillhandahålls av Aspose.PSD |

## Tips för att minska PSD‑filstorlek

- **Beskär onödiga lager** innan du laddar filen.  
- **Ändra storlek proportionellt** som visat ovan för att tidigt minska dimensionerna.  
- **Spara som PNG med lämplig bitdjup** för att undvika onödig data.

## Vanliga frågor

**Q: Är Aspose.PSD kompatibel med alla bildformat?**  
A: Aspose.PSD stödjer PSD, PNG, JPEG, BMP, GIF och många fler. Se hela listan i [dokumentationen](https://reference.aspose.com/psd/java/).

**Q: Kan jag använda Aspose.PSD i kommersiella projekt?**  
A: Ja. Köp en kommersiell licens i [Aspose‑butiken](https://purchase.aspose.com/buy).

**Q: Finns tillfälliga licenser för testning?**  
A: Absolut – begär en tillfällig licens [here](https://purchase.aspose.com/temporary-license/) för utvärderingsändamål.

**Q: Var kan jag hitta community‑stöd?**  
A: [Aspose.PSD‑forumet](https://forum.aspose.com/c/psd/34) är en bra plats för frågor och lösningar.

**Q: Hur får jag åtkomst till hela API‑referensen?**  
A: Detaljerad API‑dokumentation finns [here](https://reference.aspose.com/psd/java/).

## Slutsats

Du vet nu hur du **konverterar PSD till PNG**, **ändrar bildstorlek proportionellt** och hanterar caching effektivt med Aspose.PSD för Java. Inkludera dessa steg i dina egna applikationer för att leverera snabb, högkvalitativ bildbehandling utan att förlita dig på lokala Photoshop‑installationer. Detta **aspose psd java**‑tillvägagångssätt är en pålitlig del av varje **java image processing tutorial** och hjälper dig hålla PSD‑filstorlekar under kontroll samtidigt som du bevarar visuell kvalitet.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Senast uppdaterad:** 2026-02-09  
**Testad med:** Aspose.PSD 24.12 för Java  
**Författare:** Aspose