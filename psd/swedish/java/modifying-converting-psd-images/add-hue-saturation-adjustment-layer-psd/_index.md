---
title: Lägg till Hue Saturation Adjustment Layer till PSD
linktitle: Lägg till Hue Saturation Adjustment Layer till PSD
second_title: Aspose.PSD Java API
description: Lär dig hur du lägger till lager för nyansmättnadsjustering till PSD med Aspose.PSD för Java i denna omfattande, steg-för-steg handledning. Förbättra ditt arbetsflöde för grafisk design.
weight: 14
url: /sv/java/modifying-converting-psd-images/add-hue-saturation-adjustment-layer-psd/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Lägg till Hue Saturation Adjustment Layer till PSD

## Introduktion
När det kommer till grafisk design spelar färgmanipulation en avgörande roll – specifikt kan justering av nyans, mättnad och ljushet drastiskt förändra stämningen och kvaliteten på alla bilder. Ett effektivt sätt att uppnå detta är att använda justeringslager i Photoshop (PSD-filer). Om du vill förbättra dina PSD-filer programmatiskt med Java, är Aspose.PSD-biblioteket här för att hjälpa dig! Denna handledning tar dig igenom stegen för att lägga till ett nyansmättnadsjusteringslager till dina PSD-filer, vilket gör dina arbetsflöden mer produktiva och effektiva.
den här guiden kommer vi att täcka allt från att importera nödvändiga paket till de små detaljerna i kodexemplen.
## Förutsättningar
Innan vi hoppar in i koden, se till att du har följande på plats:
1.  Java Development Kit (JDK): Se till att du har JDK 8 eller högre installerat på din maskin. Du kan ladda ner den från[Nedladdning av Java SE Development Kit](https://www.oracle.com/java/technologies/javase-downloads.html).
2.  Aspose.PSD för Java Library: Du måste ha Aspose.PSD-biblioteket, vilket du kan[ladda ner här](https://releases.aspose.com/psd/java/). 
3. IDE: En lämplig Integrated Development Environment (IDE) som IntelliJ IDEA eller Eclipse för Java-utveckling.
4. Grundläggande Java-kunskaper: Bekantskap med Java-programmering är ett plus, men oroa dig inte; vi leder dig genom koden steg för steg.
Nu när vi har sorterat våra förutsättningar, låt oss gå vidare till den roliga delen – kodning!
## Importera paket
För att börja arbeta med Aspose.PSD-biblioteket är det första steget att importera de nödvändiga klasserna. Så här kan du göra det i din Java-fil:
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.HueSaturationLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.ColorRangeHsl;
```
Se till att du har lagt till lämpliga bibliotek i ditt projekt så att dessa importer fungerar sömlöst.
## Steg 1: Konfigurera din dokumentkatalog
Varje projekt behöver en utgångspunkt, och vårt är inget undantag. Du måste ange en katalog där dina PSD-filer lagras. Detta är avgörande för att ladda och spara bilder korrekt.
```java
String dataDir = "Your Document Directory"; // Uppdatera den här sökvägen till din faktiska katalog
```
## Steg 2: Ladda en befintlig PSD-fil
För att manipulera en befintlig PSD-fil måste vi först ladda den i vårt program. Så här kan du göra det:
```java
String sourceFileName = dataDir + "HueSaturationAdjustmentLayer.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```
 Uppdatera i den här koden`"HueSaturationAdjustmentLayer.psd"` till namnet på din befintliga PSD-fil som du vill redigera.
## Steg 3: Redigera färgton/mättnadslager
Därefter går vi igenom lagren i vår laddade PSD-bild för att hitta och redigera befintliga Hue/Saturation-lager. Detta steg innebär att ändra värdena för nyans, mättnad och ljushet.
```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof HueSaturationLayer) {
        HueSaturationLayer hueLayer = (HueSaturationLayer) im.getLayers()[i];
        hueLayer.setHue((short) -25);
        hueLayer.setSaturation((short) -12);
        hueLayer.setLightness((short) 67);
        ColorRangeHsl colorRange = hueLayer.getRange(2);
        colorRange.setHue((short) -40);
        colorRange.setSaturation((short) 50);
        colorRange.setLightness((short) -20);
        colorRange.setMostLeftBorder((short) 300);
    }
}
```
I det här exemplet:
- Vi justerar nyansen till -25, mättnaden till -12 och ljusheten till +67.
-  De`getRange(2)` metoden tillåter oss att justera specifika färgintervall efter önskemål.
## Steg 4: Spara den modifierade PSD-filen
Efter att ha gjort justeringar är nästa steg att spara filen. Detta är en viktig del av vår process, för att säkerställa att de förändringar vi har gjort inte går förlorade.
```java
String psdPathAfterChange = dataDir + "HueSaturationAdjustmentLayerChanged.psd";
im.save(psdPathAfterChange);
```
## Steg 5: Lägg till ett nytt nyans/mättnadsskikt
Därefter kanske du vill lägga till ett nytt Hue/Saturation-justeringslager till en annan PSD-fil. Följ bara samma tillvägagångssätt som du använde tidigare men med olika PSD-filer.
```java
sourceFileName = dataDir + "PhotoExample.psd";
PsdImage img = (PsdImage) Image.load(sourceFileName);
HueSaturationLayer hueLayerNew = img.addHueSaturationAdjustmentLayer();
```
## Steg 6: Ställ in nya nyans-/mättnadsvärden för det nya lagret
Nu när du har skapat det här nya lagret, applicera önskade inställningar för nyans, mättnad och ljushet precis som tidigare.
```java
hueLayerNew.setHue((short) -25);
hueLayerNew.setSaturation((short) -12);
hueLayerNew.setLightness((short) 67);
ColorRangeHsl newColorRange = hueLayerNew.getRange(2);
newColorRange.setHue((short) -160);
newColorRange.setSaturation((short) 100);
newColorRange.setLightness((short) 20);
newColorRange.setMostLeftBorder((short) 300);
```
## Steg 7: Spara den uppdaterade PSD-filen
Slutligen, spara PSD-filen med det tillagda Hue/Saturation-lagret så att du kan se dina ändringar.
```java
String psdPathAfterNewLayerChange = dataDir + "PhotoExampleAddedHueSaturation.psd";
img.save(psdPathAfterNewLayerChange);
```
Grattis! Du har framgångsrikt manipulerat PSD-filer med Aspose.PSD för Java. Nu kan du experimentera med olika bilder och djupare förändringar, vilket ger liv till dina grafiska designprojekt.
## Slutsats
Att arbeta med grafik programmässigt öppnar en värld av möjligheter. Att använda Aspose.PSD för Java för att lägga till och ändra Hue Saturation Adjustment Layers ger flexibilitet och effektivitet som kan effektivisera ditt designarbetsflöde. Oavsett om du förbättrar foton för ett projekt eller skapar fantastiskt visuellt innehåll, kan du avsevärt förbättra din produktion genom att behärska dessa verktyg.
 Utforska gärna fler funktioner i Aspose.PSD genom att dyka in i[dokumentation](https://reference.aspose.com/psd/java/) eller överväg att haka på en[tillfällig licens](https://purchase.aspose.com/temporary-license/) för att testa bibliotekets fulla kraft.
## FAQ's
### Vad är ett lager för nyansmättnadsjustering?
Med ett lager för nyansmättnadsjustering kan du ändra färgegenskaperna för en bild utan att permanent ändra de ursprungliga pixlarna.
### Behöver jag Photoshop installerat för att använda Aspose.PSD?
Nej, Aspose.PSD är ett fristående bibliotek som fungerar oberoende av Photoshop.
### Kan jag använda Aspose.PSD för batchbearbetning?
Ja, du kan automatisera och batchbearbeta flera PSD-filer med Aspose.PSD.
### Är Aspose.PSD gratis?
Aspose.PSD erbjuder en gratis provperiod, men en licens krävs för långvarig användning. Du kan se priser[här](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
