---
title: Styr cacheomfördelning i PSD-filer
linktitle: Styr cacheomfördelning i PSD-filer
second_title: Aspose.PSD Java API
description: Hantera omfördelning av cache i PSD-filer med Aspose.PSD för Java. Lär dig hur du optimerar minne och filhantering effektivt – perfekt för utvecklare.
weight: 22
url: /sv/java/modifying-converting-psd-images/control-cache-reallocation-psd-files/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Styr cacheomfördelning i PSD-filer

## Introduktion
När du arbetar med bilder och Photoshop-filer programmatiskt är effektivitet en nyckelfaktor. Aspose.PSD för Java erbjuder robusta funktioner för att hantera och manipulera PSD-filer sömlöst. En av de grundläggande aspekterna av att optimera prestanda är att kontrollera cacheomfördelning. Cachehantering hjälper till att upprätthålla balansen mellan minne och diskanvändning, vilket säkerställer att din applikation körs smidigt, utan oväntade krascher eller nedgångar. 
## Förutsättningar
Innan vi hoppar in i kodningsdelen finns det några saker du måste se till så att allt går smidigt:
1. Java Development Kit (JDK): Se till att du har JDK installerat på din maskin. Du kan ladda ner den från[Oracles hemsida](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
2. Aspose.PSD för Java: Du måste ladda ner Aspose.PSD-biblioteket. Du kan hitta den senaste versionen[här](https://releases.aspose.com/psd/java/).
3. IDE-installation: En integrerad utvecklingsmiljö (IDE) som IntelliJ IDEA eller Eclipse gör det lättare för dig att hantera din kod.
4. Grundläggande förståelse för Java: Bekantskap med Java-programmering hjälper dig att förstå begreppen och kodavsnitten bättre.
5.  Aspose-licens (valfritt): Om du vill ta bort vattenstämplar och få full funktionalitet, överväg att köpa en licens[här](https://purchase.aspose.com/buy) eller prova den kostnadsfria provperioden[här](https://releases.aspose.com/).
## Importera paket
Innan vi börjar skriva koden, låt oss se till att vi har de nödvändiga paketen importerade. Nedan är en kort lista över vad som ska inkluderas i början av din Java-fil:
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
## Steg 1: Konfigurera din datakatalog
Först och främst måste du skapa en katalog där du vill att dina cachefiler ska lagras. Detta är viktigt för att hantera cachen effektivt.
```java
String dataDir = "Your Document Directory";
Cache.setCacheFolder(dataDir);
```

- String dataDir: Definiera katalogen för din dokumentcache.
- Cache.setCacheFolder(dataDir): Denna metod ställer in cachemappen till den angivna katalogen. Varje cache som skapas av Aspose kommer nu att lagras här istället för den tillfälliga standardkatalogen.
## Steg 2: Konfigurera cache till disk
Därefter specificerar vi att vi vill att vår cache endast ska lagras på disken. Detta är särskilt användbart om ditt program använder stora filer och du vill säkerställa att minnet förblir ledigt.
```java
Cache.setCacheType(CacheType.CacheOnDiskOnly);
```

- Cache.setCacheType(CacheType.CacheOnDiskOnly): Detta alternativ säkerställer att cachen inte hålls i minnet, vilket är fördelaktigt för att hantera stora PSD-filer utan att förbruka för mycket RAM.
## Steg 3: Ställ in maximal disk- och minnescachestorlek
Låt oss nu begränsa våra cachestorlekar. Detta är avgörande eftersom obegränsad cache kan leda till prestandaproblem.
```java
Cache.setMaxDiskSpaceForCache(1073741824); // 1 gigabyte
Cache.setMaxMemoryForCache(1073741824); // 1 gigabyte
```

- Cache.setMaxDiskSpaceForCache(1073741824): Detta sätter en gräns på 1 GB för cachen på disken. Du kan justera denna storlek beroende på dina behov.
- Cache.setMaxMemoryForCache(1073741824): På liknande sätt begränsar detta cacheminnet i minnet, vilket säkerställer att ditt program inte använder för mycket minne.
## Steg 4: Hantera strategi för cacheomfördelning
Att hantera hur cacheminnet omfördelas är viktigt för att upprätthålla prestanda. Så här kan du ställa in det.
```java
Cache.setExactReallocateOnly(false);
```

- Cache.setExactReallocateOnly(false): När den är inställd på false tillåter detta Aspose att hantera cacheomfördelning mer flexibelt, vilket kan leda till bättre prestanda.
## Steg 5: Kontrollera allokerad cachestorlek
Det här steget handlar om att övervaka hur många byte som för närvarande allokeras för cachen i minnet eller på disken. Låt oss implementera det:
```java
long l1 = Cache.getAllocatedDiskBytesCount();
long l2 = Cache.getAllocatedMemoryBytesCount();
```

- long l1: Lagrar antalet byte som tilldelats på disken.
- long l2: Lagrar antalet byte som tilldelats i minnet. 
Du kan kontrollera dessa värden när som helst för att säkerställa att din applikation hanterar minne och diskanvändning som förväntat.
## Steg 6: Skapa en PSD-bild
Nu när vi har konfigurerat våra cache-konfigurationer, låt oss skapa en enkel PSD-bild.
```java
PsdOptions options = new PsdOptions();
Color[] color = { Color.getRed(), Color.getBlue(), Color.getBlack(), Color.getWhite() };
options.setPalette(new ColorPalette(color));
options.setSource(new StreamSource(new ByteArrayInputStream(new byte[0])));
RasterImage image = (RasterImage) Image.create(options, 100, 100);
```

- Alternativ för PsdOptions: Detta objekt låter dig ange alternativ när du skapar en Photoshop-bild.
- Färg[] färg: En array som innehåller färgerna som kommer att användas i bildpaletten.
## Steg 7: Spara pixeldata till bilden
Låt oss nu fylla på vår bild med pixeldata och spara den.
```java
Color[] pixels = new Color[10000];
for (int i = 0; i < pixels.length; i++) {
    pixels[i] = Color.getWhite();
}
image.savePixels(image.getBounds(), pixels);
```

- Färg[] pixlar: Detta är en uppsättning färgobjekt. Här fyller vi den med vita pixlar.
- image.savePixels(image.getBounds(), pixlar): Denna metod sparar pixeldata i bilden. Den uppdaterar bilden med de färger vi har definierat.
## Steg 8: Övervakning av allokerad cache efter bildskapande
Efter att ha skapat bilden är det en bra praxis att kontrollera hur många byte som tilldelats cachen igen.
```java
long diskBytes = Cache.getAllocatedDiskBytesCount();
long memoryBytes = Cache.getAllocatedMemoryBytesCount();
```

- long diskBytes: Fångar den aktuella allokeringen på disken efter bildskapandet.
- long memoryBytes: Fångar den aktuella allokeringen i minnet. 
Detta steg hjälper dig att avgöra hur mycket cache som förbrukas efter dina operationer.
## Steg 9: Kontrollera att de kasseras på rätt sätt
Slutligen är det avgörande att se till att alla Aspose.PSD-objekt kasserades på rätt sätt för att undvika minnesläckor.
```java
l1 = Cache.getAllocatedDiskBytesCount();
l2 = Cache.getAllocatedMemoryBytesCount();
```

- l1 och l2: Dessa variabler hjälper dig att kontrollera den slutliga allokeringen. Om de inte är noll indikerar det att vissa föremål inte har kasserats på rätt sätt.
## Slutsats
Att kontrollera omfördelning av cache i Aspose.PSD för Java kan göra en betydande skillnad i din applikations prestanda. Genom att följa stegen som beskrivs ovan kan du effektivt hantera cachen, minimera minnesanvändningen och skapa vackra PSD-filer effektivt. Omfamna dessa tekniker och se dina applikationer frodas med optimal prestanda!
## FAQ's
### Vad är Aspose.PSD?
Aspose.PSD är ett bibliotek för .NET- och Java-utvecklare för att skapa, manipulera och konvertera Photoshop-filer (PSD) programmatiskt.
### Hur kontrollerar jag tilldelad cachestorlek?
 Använd metoder som`Cache.getAllocatedDiskBytesCount()` och`Cache.getAllocatedMemoryBytesCount()` för att övervaka aktuell cacheanvändning.
### Kan jag ställa in en anpassad katalog för cache?
 Ja, du kan ange en annan katalog genom att använda`Cache.setCacheFolder("Your Directory Path")`.
### Är Aspose.PSD gratis att använda?
Aspose.PSD är ett betalbibliotek, men du kan börja med en gratis testversion tillgänglig på deras[webbplats](https://releases.aspose.com/).
### Vad händer om jag inte gör mig av med föremål?
Att inte kassera föremål kan leda till minnesläckor, vilket gör att din applikation använder mer resurser än nödvändigt.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
