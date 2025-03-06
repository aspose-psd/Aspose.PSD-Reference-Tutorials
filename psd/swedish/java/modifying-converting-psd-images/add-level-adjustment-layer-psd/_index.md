---
title: Lägg till nivåjusteringslager i PSD
linktitle: Lägg till nivåjusteringslager i PSD
second_title: Aspose.PSD Java API
description: Lär dig hur du effektivt lägger till ett nivåjusteringslager i dina PSD-filer med Aspose.PSD för Java. Öka dina färdigheter i bildredigering.
weight: 16
url: /sv/java/modifying-converting-psd-images/add-level-adjustment-layer-psd/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Lägg till nivåjusteringslager i PSD

## Introduktion
När det kommer till bildredigering kan hantering av nivåer göra en värld av skillnad när det gäller livlighet och klarhet i dina foton. Ett praktiskt verktyg i Photoshop-arsenalen är "Level Adjustment Layer", som låter dig justera tonomfånget och färgbalansen för dina bilder. I den här guiden går vi igenom hur du implementerar ett nivåjusteringslager i en PSD-fil med Aspose.PSD för Java. Så, ta din Java IDE.
## Förutsättningar
Innan du hoppar in i en värld av nivåjusteringar måste du ställa in några saker för att säkerställa en smidig körning:
1.  Java Development Kit (JDK): Se till att du har JDK installerat på din maskin. Om du inte har det kan du hämta det från[Oracle hemsida](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) eller använd OpenJDK.
2.  Aspose.PSD för Java Library: För att manipulera PSD-filer måste du ladda ner Aspose.PSD-biblioteket. Du kan hämta den senaste versionen från denna[nedladdningslänk](https://releases.aspose.com/psd/java/) och se till att du har inkluderat JAR i ditt projekts bibliotek.
3. Grundläggande kunskaper om Java: Att ha en grundläggande förståelse för Java-programmering kommer att hjälpa, eftersom vi kommer att dyka in i kodsnuttar genom hela den här handledningen.
4. IDE-installation: Du kan använda vilken Java IDE du föredrar – som IntelliJ IDEA, Eclipse eller NetBeans – för att skriva och köra din kod. Se bara till att du har ställt in ditt Java-projekt och lagt till Aspose.PSD-biblioteket.

## Importera paket
Innan vi börjar skriva vår kod måste vi importera de nödvändiga paketen från Aspose.PSD-biblioteket. Så här kan du göra det:
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.LevelsLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.LevelChannel;
```
Genom att importera dessa paket får vi tillgång till de klasser som krävs för att ladda, ändra och spara våra PSD-filer.

Låt oss nu dela upp processen i smältbara steg. Följ med när vi går igenom att ladda en PSD-fil, justera nivåerna och sedan spara dina ändringar. 
## Steg 1: Ställ in dina filsökvägar
Det första steget är att definiera var vår PSD-fil finns och var vi vill spara den modifierade utdatan. Du kan anpassa katalogsökvägen så att den passar dina behov.
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "LevelsAdjustmentLayer.psd";
String psdPathAfterChange = dataDir + "LevelsAdjustmentLayerChanged.psd";
```
 Här, byt ut`"Your Document Directory"`med den faktiska sökvägen på ditt system där din PSD-fil är lagrad. Detta sätter scenen för allt vi kommer att göra härnäst.
## Steg 2: Ladda PSD-filen
 Låt oss nu ladda PSD-filen med hjälp av`PsdImage` klass. Detta steg är viktigt eftersom det tillåter oss att komma åt och manipulera lagren.
```java
PsdImage im = (PsdImage) Image.load(sourceFileName);
```
 När du ringer`Image.load()` , kommer den att läsa PSD-filen och skapa en instans av`PsdImage` som du kan arbeta med.
## Steg 3: Iterera genom lagren
Eftersom vi vill justera ett nivåjusteringslager, måste vi gå igenom varje lager i vår PSD-fil. Detta hjälper oss att hitta det specifika lager vi vill modifiera.
```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof LevelsLayer) {
        LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
        // Ytterligare manipulation kommer att gå här...
    }
}
```
 I denna loop,`instanceof LevelsLayer` kontrollerar om det aktuella lagret är ett nivåjusteringslager. Om det är det, kan vi fortsätta att justera dess egenskaper.
## Steg 4: Justera nivåkanalinställningarna
När vi väl har identifierat rätt lager kan vi ändra dess ingångs- och utdatanivåer. Det är här magin händer! Justera olika parametrar för att se hur de påverkar bilden.
```java
LevelChannel channel = levelsLayer.getChannel(0);
channel.setInputMidtoneLevel(2.0f);
channel.setInputShadowLevel((short) 10);
channel.setInputHighlightLevel((short) 230);
channel.setOutputShadowLevel((short) 20);
channel.setOutputHighlightLevel((short) 200);
```
Så här gör varje parameter:
- Ingång mellan tonnivå: Justerar mellantonerna.
- Inmatningsskuggnivå: Justerar de mörkare områdena i bilden.
- Input Highlight Level: Ändrar de ljusa områdena i bilden.
- Output Shadow Level: Anger hur mörka skuggor ska visas.
- Output Highlight Level: Ställer in hur ljusa högdagrar ska visas.
Experimentera gärna med olika värderingar!
## Steg 5: Spara den modifierade PSD-filen
Nu när vi har gjort våra justeringar är det dags att spara den modifierade PSD-filen. Detta steg är avgörande för att säkerställa att dina ändringar tillämpas och lagras.
```java
im.save(psdPathAfterChange);
```
 Du kan nu hitta din justerade PSD-fil på den angivna`psdPathAfterChange`. 
## Slutsats
Du har precis lärt dig hur du lägger till ett nivåjusteringslager till en PSD-fil med Aspose.PSD för Java! Genom att följa den här guiden kan du enkelt justera tonkvaliteten på dina bilder, vilket banar väg för en mer levande och visuellt tilltalande utskrift. Kom ihåg att övning ger färdighet, så justera gärna justeringarna och utforska olika PSD-filer för att se effekterna av dina ändringar.
## FAQ's
### Vad är ett nivåjusteringslager?
Ett nivåjusteringslager låter dig korrigera tonomfånget i dina bilder, balansera skuggor, mellantoner och högdagrar.
### Kan jag använda Aspose.PSD utan köp?
Ja! Aspose erbjuder en gratis provperiod för att testa biblioteket innan du köper.
### Var kan jag hitta dokumentation för Aspose.PSD?
 Du hittar dokumentationen[här](https://reference.aspose.com/psd/java/).
### Finns det något communitystöd för Aspose-produkter?
 Absolut! Du kan ställa frågor och få stöd i[Aspose forum](https://forum.aspose.com/c/psd/34).
### Hur kan jag få en tillfällig licens för Aspose.PSD?
 Du kan ansöka om en tillfällig licens[här](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
