---
date: 2026-03-13
description: Lär dig hur du skapar PSD‑bildprojekt i Java samtidigt som du hanterar
  cache‑omfördelning med Aspose.PSD för Java. Optimera minne och diskutrymme effektivt.
linktitle: Create PSD Image Java – Control Cache Reallocation
second_title: Aspose.PSD Java API
title: Skapa PSD-bild i Java – Kontrollera cache‑omallokering
url: /sv/java/modifying-converting-psd-images/control-cache-reallocation-psd-files/
weight: 22
---

 remain as is.

Now craft final answer.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Kontrollera cache‑omallokering i PSD-filer

## Introduktion
Om du behöver **create PSD image java**‑projekt effektivt är kontroll av cache‑omallokering avgörande. När du arbetar med bilder och Photoshop‑filer programatiskt är effektivitet en nyckelfaktor. Aspose.PSD for Java erbjuder robusta funktioner för att hantera och manipulera PSD‑filer sömlöst. En av de grundläggande aspekterna för att optimera prestanda är att kontrollera cache‑omallokering. Cachhantering hjälper till att upprätthålla balansen mellan minne och diskutrymme, vilket säkerställer att din applikation körs smidigt utan oväntade krascher eller långsamhet.  

## Snabba svar
- **Vad gör cache‑omallokering?** Den balanserar minne och diskutrymme när stora PSD‑filer bearbetas.  
- **Vilken cache‑typ är bäst för stora bilder?** `CacheOnDiskOnly` håller minnet fritt genom att lagra cache på disk.  
- **Hur mycket diskutrymme kan jag allokera?** Upp till 1 GB (eller vilken storlek du än anger med `setMaxDiskSpaceForCache`).  
- **Behöver jag en licens för att använda dessa funktioner?** En licens tar bort begränsningarna i provversionen; se Aspose‑köpsidan.  
- **Kan jag övervaka cache‑användning vid körning?** Ja, använd `Cache.getAllocatedDiskBytesCount()` och `Cache.getAllocatedMemoryBytesCount()`.  

## Varför kontrollera cache‑omallokering?
Att hantera cache är avgörande när du **create PSD image java**‑applikationer som hanterar högupplösta eller flerskikts‑filer. Korrekt cache‑inställningar förhindrar out‑of‑memory‑fel, minskar GC‑pauser och ger dig förutsägbar prestanda på servrar eller skrivbordsprogram.  

## Förutsättningar
Innan vi hoppar in i koddelen finns det några saker du måste säkerställa så att allt fungerar smidigt:
1. Java Development Kit (JDK): Se till att du har JDK installerat på din maskin. Du kan ladda ner det från [Oracle's website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. Aspose.PSD for Java: Du behöver ladda ner Aspose.PSD‑biblioteket. Du kan hitta den senaste versionen [here](https://releases.aspose.com/psd/java/).  
3. IDE‑inställning: En integrerad utvecklingsmiljö (IDE) som IntelliJ IDEA eller Eclipse gör det enklare att hantera din kod.  
4. Grundläggande kunskap i Java: Bekantskap med Java‑programmering hjälper dig att bättre förstå koncepten och kodsnuttarna.  
5. Aspose‑licens (valfritt): Om du vill ta bort vattenstämplar och få full funktionalitet, överväg att köpa en licens [here](https://purchase.aspose.com/buy) eller prova den kostnadsfria provversionen [here](https://releases.aspose.com/).  

## Importera paket
Innan vi börjar skriva koden, låt oss säkerställa att vi har importerat de nödvändiga paketen. Nedan är en kort lista på vad som ska inkluderas i början av din Java‑fil:
```java
import com.aspose.psd.Cache;
import com.aspose.psd.CacheType;
import com.aspose.psd.Color;
import com.aspose.psd.ColorPalette;
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.imageoptions.GifOptions;
import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.sources.StreamSource;
import com.aspose.psd.system.io.MemoryStream;
```

## Hur man skapar PSD Image Java med cache‑kontroll
Nedan följer en steg‑för‑steg‑genomgång som kopplar cache‑konfiguration direkt till processen att skapa en PSD‑bild i Java.

### Steg 1: Ställa in din datakatalog
Först och främst måste du skapa en katalog där du vill lagra dina cache‑filer. Detta är nödvändigt för att hantera cachen effektivt.
```java
String dataDir = "Your Document Directory";
Cache.setCacheFolder(dataDir);
```

- `String dataDir`: Definiera katalogen för ditt dokument‑cache.  
- `Cache.setCacheFolder(dataDir)`: Denna metod sätter cache‑mappen till den angivna katalogen. All cache som skapas av Aspose kommer nu att lagras här istället för standard‑temporärkatalogen.  

### Steg 2: Konfigurera cache till disk
Därefter specificerar vi att vi vill att vår cache endast ska lagras på disk. Detta är särskilt användbart om din applikation använder stora filer och du vill säkerställa att minnet förblir fritt.
```java
Cache.setCacheType(CacheType.CacheOnDiskOnly);
```

- `Cache.setCacheType(CacheType.CacheOnDiskOnly)`: Detta alternativ säkerställer att cachen inte hålls i minnet, vilket är fördelaktigt för att hantera stora PSD‑filer utan att förbruka för mycket RAM.  

### Steg 3: Ställa in maximal disk‑ och minnes‑cachestorlek
Nu ska vi begränsa våra cachestorlekar. Detta är avgörande eftersom obegränsad cache kan leda till prestandaproblem.
```java
Cache.setMaxDiskSpaceForCache(1073741824); // 1 gigabyte
Cache.setMaxMemoryForCache(1073741824); // 1 gigabyte
```

- `Cache.setMaxDiskSpaceForCache(1073741824)`: Detta sätter en gräns på 1 GB för cachen på disk. Du kan justera denna storlek efter dina behov.  
- `Cache.setMaxMemoryForCache(1073741824)`: På samma sätt begränsar detta den in‑memory‑cachen, vilket säkerställer att din applikation inte använder för mycket minne.  

### Steg 4: Hantera cache‑omallokeringsstrategi
Att hantera hur cache omallokeras är viktigt för att upprätthålla prestanda. Så här kan du konfigurera det.
```java
Cache.setExactReallocateOnly(false);
```

- `Cache.setExactReallocateOnly(false)`: När den är satt till `false` tillåter den Aspose att hantera cache‑omallokering mer flexibelt, vilket kan leda till bättre prestanda.  

### Steg 5: Kontrollera allokerad cachestorlek
Detta steg handlar om att övervaka hur många byte som för närvarande är allokerade för cachen i minnet eller på disk. Låt oss implementera det:
```java
long l1 = Cache.getAllocatedDiskBytesCount();
long l2 = Cache.getAllocatedMemoryBytesCount();
```

- `long l1`: Lagrar antalet byte som är allokerade på disken.  
- `long l2`: Lagrar antalet byte som är allokerade i minnet.  
Du kan kontrollera dessa värden när som helst för att säkerställa att din applikation hanterar minne och diskutrymme som förväntat.  

### Steg 6: Skapa en PSD‑bild
Nu när vi har våra cache‑konfigurationer på plats, låt oss skapa en enkel PSD‑bild.
```java
PsdOptions options = new PsdOptions();
Color[] color = { Color.getRed(), Color.getBlue(), Color.getBlack(), Color.getWhite() };
options.setPalette(new ColorPalette(color));
options.setSource(new StreamSource(new ByteArrayInputStream(new byte[0])));
RasterImage image = (RasterImage) Image.create(options, 100, 100);
```

- `PsdOptions options`: Detta objekt låter dig specificera alternativ när du skapar en Photoshop‑bild.  
- `Color[] color`: En array som innehåller färgerna som kommer att användas i bildpaletten.  

### Steg 7: Spara pixeldatat till bilden
Nu ska vi fylla vår bild med pixeldata och spara den.
```java
Color[] pixels = new Color[10000];
for (int i = 0; i < pixels.length; i++) {
    pixels[i] = Color.getWhite();
}
image.savePixels(image.getBounds(), pixels);
```

- `Color[] pixels`: Detta är en array av färgobjekt. Här fyller vi den med vita pixlar.  
- `image.savePixels(image.getBounds(), pixels)`: Denna metod sparar pixeldatan till bilden. Den uppdaterar bilden med de färger vi har definierat.  

### Steg 8: Övervaka allokerad cache efter bildskapande
Efter att bilden har skapats är det en god praxis att kontrollera hur många byte som är allokerade för cachen igen.
```java
long diskBytes = Cache.getAllocatedDiskBytesCount();
long memoryBytes = Cache.getAllocatedMemoryBytesCount();
```

- `long diskBytes`: Fångar den aktuella allokeringen på disken efter bildskapandet.  
- `long memoryBytes`: Fångar den aktuella allokeringen i minnet.  
Detta steg hjälper dig att avgöra hur mycket cache som förbrukas efter dina operationer.  

### Steg 9: Kontrollera korrekt borttagning
Slutligen är det avgörande att säkerställa att alla Aspose.PSD‑objekt har frigjorts korrekt för att undvika minnesläckor.
```java
l1 = Cache.getAllocatedDiskBytesCount();
l2 = Cache.getAllocatedMemoryBytesCount();
```

- `l1` och `l2`: Dessa variabler hjälper dig att kontrollera den slutgiltiga allokeringen. Om de inte är noll indikerar det att vissa objekt inte har frigjorts korrekt.  

## Vanliga problem och lösningar
- **Cache‑mapp skapades inte** – Verifiera att applikationen har skrivbehörighet för sökvägen du skickade till `Cache.setCacheFolder`.  
- **Out‑of‑memory‑fel** – Dubbelkolla att `Cache.setCacheType(CacheType.CacheOnDiskOnly)` har använts innan du laddar stora PSD‑filer.  
- **Oväntad cache‑storlek** – Använd `Cache.getAllocated*BytesCount()`‑metoderna efter varje större operation för att spåra tillväxt.  

## Vanliga frågor
**Q: Vad är Aspose.PSD?**  
A: Aspose.PSD är ett bibliotek för .NET- och Java‑utvecklare för att programatiskt skapa, manipulera och konvertera Photoshop‑ (PSD)‑filer.  

**Q: Hur kontrollerar jag allokerad cachestorlek?**  
A: Använd metoder som `Cache.getAllocatedDiskBytesCount()` och `Cache.getAllocatedMemoryBytesCount()` för att övervaka aktuell cache‑användning.  

**Q: Kan jag ange en anpassad katalog för cache?**  
A: Ja, du kan specificera en annan katalog genom att använda `Cache.setCacheFolder("Your Directory Path")`.  

**Q: Är Aspose.PSD gratis att använda?**  
A: Aspose.PSD är ett betalt bibliotek, men du kan börja med en kostnadsfri provversion som finns på deras [website](https://releases.aspose.com/).  

**Q: Vad händer om jag inte frigör objekt?**  
A: Att inte frigöra objekt kan leda till minnesläckor, vilket får din applikation att använda mer resurser än nödvändigt.  

## Slutsats
Att kontrollera cache‑omallokering när du **create PSD image java**‑applikationer kan göra en betydande skillnad i prestanda. Genom att följa stegen ovan kommer du att hantera cachen effektivt, minimera minnesförbrukningen och generera högkvalitativa PSD‑filer med Aspose.PSD for Java. Använd dessa tekniker så kommer dina projekt att köra smidigare och skala bättre.

---

**Last Updated:** 2026-03-13  
**Testad med:** Aspose.PSD for Java (latest release)  
**Författare:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}