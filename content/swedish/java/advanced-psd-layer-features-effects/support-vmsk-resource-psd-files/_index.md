---
title: Stöd Vmsk Resource i PSD-filer med Java
linktitle: Stöd Vmsk Resource i PSD-filer med Java
second_title: Aspose.PSD Java API
description: Hantera Vmsk-resurser enkelt i PSD-filer med Aspose.PSD för Java. En omfattande, steg-för-steg handledning idealisk för både utvecklare och designers.
type: docs
weight: 23
url: /sv/java/advanced-psd-layer-features-effects/support-vmsk-resource-psd-files/
---
## Introduktion
När det gäller att arbeta med PSD-filer (Photoshop Document) är hantering av resurser avgörande, särskilt när man integrerar specialfunktioner som Vmsk-resursen (Vector Mask). Vmsk-resurser kan stärka designers genom att lägga till komplexa vektorformer, vilket gör det möjligt för dem att skapa fantastisk grafik utan ansträngning. I den här guiden kommer vi att ta ett praktiskt tillvägagångssätt för att visa dig hur du stödjer Vmsk-resurser i PSD-filer med Aspose.PSD för Java. Oavsett om du är en utvecklare som vill förbättra din applikation eller en designer som söker automatisering, kommer den här handledningen att leda dig genom processen steg för steg, vilket gör det enkelt att följa och implementera.
## Förutsättningar
Innan vi dyker in i de saftiga detaljerna i hanteringen av Vmsk-resurser, låt oss se till att du har allt redo för en sömlös upplevelse.
### Vad du behöver
-  Java Development Kit (JDK): Se till att du har JDK installerat på din maskin. Om inte kan du ladda ner den från[Oracle hemsida](https://www.oracle.com/java/technologies/javase-downloads.html).
- Aspose.PSD för Java Library: Detta är ett kraftfullt bibliotek för att hantera PSD-filer. Du kan ladda ner den från[Aspose release sida](https://releases.aspose.com/psd/java/) . För de som vill prova innan de köper kan du också börja med[gratis provperiod](https://releases.aspose.com/).
- En IDE: Alla IDE för Java (som IntelliJ IDEA, Eclipse, etc.) kommer att fungera för detta projekt.
### Konfigurera din arbetsyta
1. Skapa ett nytt Java-projekt: Starta din föredragna IDE och skapa ett nytt Java-projekt. Det här är din lekplats för att arbeta med koden.
2. Lägg till Aspose-biblioteket: När du har laddat ner Aspose-biblioteket lägger du till jar-filen i ditt projekts bibliotek. Detta steg är avgörande eftersom det tillåter oss att använda alla dessa söta funktioner i Aspose.PSD.
Med dessa förutsättningar på plats är du redo att börja skapa, ändra och hantera PSD-filer med Vmsk-resurser. Låt oss gå direkt in i programmeringen!
## Importera paket
Innan vi kan arbeta med PSD-filer måste vi importera de nödvändiga paketen. Detta är ryggraden i vår kod, vilket ger oss tillgång till olika klasser och metoder som Aspose.PSD-biblioteket erbjuder.
```java
import com.aspose.psd.Image;
import com.aspose.psd.Point;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.fileformats.psd.layers.LayerResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.VmskResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.BezierKnotRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.InitialFillRuleRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.LengthRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.PathFillRuleRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathType;
```
Nu när vi har satt scenen är det dags för action! I det här avsnittet delar vi upp koden i hanterbara steg. Dessa steg guidar dig genom att läsa en PSD-fil, hantera Vmsk-resursen och till och med redigera den.
## Steg 1: Ladda din PSD-fil
Det första du vill göra är att ladda din PSD-fil. Det är här all magi börjar.
```java
String dataDir = "Your Document Directory"; // Uppdatera den här sökvägen
String sourceFileName = dataDir + "Rectangle.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

-  Vi ställer in`dataDir` till katalogen för din PSD-fil. 
-  Vi skapar en sträng för`sourceFileName`, kombinerar katalogen med PSD-filens namn.
-  Slutligen laddar vi PSD-filen i en`PsdImage` objekt använder`Image.load()`.
## Steg 2: Hämta Vmsk-resursen
Nu när vi har vår PSD-bild laddad, låt oss hämta Vmsk-resursen.
```java
VmskResource resource = getVmskResource(im);
```

-  Vi kallar`getVmskResource()` metod som hanterar sökning och hämtning av Vmsk-resursen från bilden.
## Steg 3: Validera Vmsk-resursegenskaper
Innan du fortsätter med ändringar är det viktigt att verifiera att vår Vmsk-resurs är i det förväntade tillståndet.
```java
if (resource.isDisabled() != false ||
	resource.isInverted() != false ||
	resource.isNotLinked() != false ||
	resource.getPaths().length != 7) {
	throw new RuntimeException("VmskResource was read wrong");
}
```

- Här kontrollerar vi olika egenskaper hos Vmsk-resursen. Vi vill säkerställa att den inte är inaktiverad, inverterad eller inte länkad, och att den har rätt antal sökvägar.
## Steg 4: Gå till varje sökväg och validera
Låt oss gräva lite djupare och inspektera vägarna inom Vmsk-resursen.
```java
PathFillRuleRecord pathFillRule = (PathFillRuleRecord) resource.getPaths()[0];
InitialFillRuleRecord initialFillRule = (InitialFillRuleRecord) resource.getPaths()[1];
LengthRecord subpathLength = (LengthRecord) resource.getPaths()[2];
if (pathFillRule.getType() != VectorPathType.PathFillRuleRecord ||
	initialFillRule.getType() != VectorPathType.InitialFillRuleRecord ||
	initialFillRule.isFillStartsWithAllPixels() != false ||
	subpathLength.getType() != VectorPathType.ClosedSubpathLengthRecord ||
	subpathLength.isClosed() != true) {
	throw new RuntimeException("VmskResource paths were read wrong");
}
```

- Vi extraherar tre specifika sökvägsposter och validerar deras typer och egenskaper för att säkerställa att de uppfyller våra kriterier.
## Steg 5: Redigera Vmsk-resursen
Nu går vi in på modifieringsdelen! Du kan justera egenskaperna för Vmsk-resursen efter behov.
```java
resource.setDisabled(true);
resource.setInverted(true);
resource.setNotLinked(true);
```

- I det här blocket växlar vi olika egenskaper för Vmsk-resursen. Genom att ställa in dem på sanna kan vi styra hur masken beter sig i PSD-filen.
## Steg 6: Ändra Bezier Knot Points
Bezier-knutar är avgörande för vektorbanor. Låt oss ändra några värden här.
```java
BezierKnotRecord bezierKnot = (BezierKnotRecord) resource.getPaths()[3];
bezierKnot.getPoints()[0] = new Point(0, 0);
bezierKnot = (BezierKnotRecord) resource.getPaths()[4];
bezierKnot.getPoints()[0] = new Point(8039797, 10905190);
```

-  Vi kommer åt specifika`BezierKnotRecord` banor och ändra deras punkter för att potentiellt omforma vektormasken.
## Steg 7: Spara den modifierade PSD-filen
När alla redigeringar är klara är det dags att spara den modifierade PSD-filen. 
```java
String exportPath = dataDir + "Rectangle_changed.psd";
im.save(exportPath);
```

-  Vi ställer in sökvägen för den exporterade PSD-filen och ringer sedan`im.save()` för att skriva ändringarna i den här nya filen.
## Steg 8: Rensa upp resurser
Slutligen måste vi se till att vi gör oss av med bilden på rätt sätt för att frigöra resurser.
```java
im.dispose();
```

- Det är alltid bra att göra sig av med alla resurser när du är klar. Detta hjälper till att undvika minnesläckor i dina applikationer.
## Slutsats
Grattis! Du har precis gått igenom en detaljerad process för att stödja Vmsk-resurser i PSD-filer med Aspose.PSD för Java. Från att ladda bilden, hämta och validera Vmsk-resursen, redigera dess egenskaper och sedan spara din modifierade PSD, har du täckt det väsentliga. Med dessa färdigheter kan du effektivt hantera och använda olika resurser inom PSD-filer, förbättra dina grafiska designprojekt eller automatiseringsskript.
## FAQ's
### Vad är en Vmsk-resurs?
En Vmsk-resurs är en vektormask i en PSD-fil som möjliggör komplexa vektorformer och redigeringsfunktioner.
### Kan jag använda Aspose.PSD i ett Maven-projekt?
Ja, du kan inkludera Aspose.PSD som ett beroende i ditt Maven-projekt med hjälp av dess koordinater från förvaret.
### Vilket format kan jag spara mina modifierade PSD-filer i?
Du kan spara tillbaka dem som PSD-filer eller exportera dem till andra format som PNG, JPEG, etc.
### Finns det en gratis testversion tillgänglig för Aspose.PSD?
 Ja, du kan få tillgång till en gratis testversion av Aspose.PSD för att testa dess funktioner. Besök[gratis testlänk](https://releases.aspose.com/).
### Hur kan jag få support för Aspose.PSD?
 Du kan gå med i[Aspose forum](https://forum.aspose.com/c/psd/34)för support och felsökningshjälp.