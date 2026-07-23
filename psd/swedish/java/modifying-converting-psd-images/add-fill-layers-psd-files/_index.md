---
date: 2026-03-04
description: Lär dig hur du modifierar PSD‑lager programatiskt genom att lägga till
  fyllnadslager med Aspose.PSD för Java. Följ den här steg‑för‑steg‑guiden för att
  snabbt förbättra dina designer.
linktitle: Modify PSD Layers Programmatically – Add Fill Layers (Java)
second_title: Aspose.PSD Java API
title: Modifiera PSD‑lager programatiskt – Lägg till fyllningslager (Java)
url: /sv/java/modifying-converting-psd-images/add-fill-layers-psd-files/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Modifiera PSD‑lager programatiskt – Lägg till fyllningslager (Java)

Om du vill **modifiera PSD‑lager programatiskt**, är det att lägga till fyllningslager ett av de snabbaste sätten att berika dina Photoshop‑dokument utan att någonsin öppna Photoshop. I den här handledningen går vi igenom de exakta stegen du behöver för att skapa en ny PSD, infoga färg‑, gradient‑ och mönster‑fyllningslager och sedan spara resultatet – allt med Aspose.PSD för Java.

## Snabba svar
- **Vad kan jag uppnå?** Lägg till färg‑, gradient‑ och mönster‑fyllningslager i en PSD‑fil programatiskt.  
- **Vilket bibliotek krävs?** Aspose.PSD för Java (senaste versionen).  
- **Behöver jag en licens?** En gratis provversion fungerar för testning; en kommersiell licens krävs för produktion.  
- **Hur lång tid tar implementeringen?** Ungefär 10‑15 minuter för ett grundexempel.  
- **Vilken Java‑version stöds?** JDK 11 eller senare.

## Vad betyder “modifiera PSD‑lager programatiskt”?
Att modifiera PSD‑lager programatiskt innebär att använda kod för att skapa, redigera eller ta bort lager i ett Photoshop‑dokument, vilket ger dig full kontroll över designflödet utan manuell UI‑interaktion.

## Varför lägga till fyllningslager med Aspose.PSD?
- **Automation** – Generera dussintals PSD‑filer i ett batch‑jobb.  
- **Konsistens** – Applicera exakt samma färg, gradient eller mönster i flera filer.  
- **Snabbhet** – Hoppa över de tidskrävande manuella stegen i Photoshop.  
- **Plattformsoberoende** – Fungerar på alla operativsystem som stödjer Java.

## Förutsättningar
Innan vi dyker ner i koden, se till att du har följande:

1. **Java Development Kit (JDK)** – Installera JDK 11 eller nyare. Du kan ladda ner det från [Oracle‑webbplatsen](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. **Aspose.PSD för Java** – Hämta det senaste biblioteket från den officiella nedladdningssidan [här](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse eller någon annan editor du föredrar.  
4. **Grundläggande Java‑kunskaper** – Bekantskap med klasser och metoder är till hjälp, men handledningen förklarar allt steg‑för‑steg.

## Importera paket
För att börja arbeta med PSD‑filer måste du importera de relevanta Aspose.PSD‑klasserna:

```java
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.filllayers.FillLayer;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
```

Dessa importeringar ger dig åtkomst till `PsdImage`‑objektet (själva dokumentet) och de olika `FillLayer`‑typerna som vi kommer att använda.

## Så modifierar du PSD‑lager programatiskt – Steg‑för‑steg‑guide

### Steg 1: Ställ in din utdata‑katalog
Definiera var den resulterande PSD‑filen ska sparas så att du kan hitta den senare.

```java
String outputDir = "Your Document Directory";
String outPsdFilePath = outputDir + "output.psd";
```

Byt ut `"Your Document Directory"` mot en absolut eller relativ sökväg på din maskin.

### Steg 2: Skapa ett nytt Photoshop‑dokument
Instansiera en tom canvas som kommer att hålla fyllningslagren.

```java
PsdImage psdImage = new PsdImage(100, 100);
```

Parametrarna `100, 100` representerar bredd och höjd i pixlar. Justera dem så att de matchar dina designkrav.

### Steg 3: Lägg till ett färgfyllningslager
Skapa ett fyllningslager med solid färg och ge det ett beskrivande namn.

```java
FillLayer colorFillLayer = FillLayer.createInstance(FillType.Color);
colorFillLayer.setDisplayName("Color Fill Layer");
psdImage.addLayer(colorFillLayer);
```

Du kan senare ändra den faktiska färgen genom att komma åt lagrets fyllningsinställningar (ej visat här för korthet).

### Steg 4: Lägg till ett gradientfyllningslager
Gradientfyllningar ger djup och visuellt intresse.

```java
FillLayer gradientFillLayer = FillLayer.createInstance(FillType.Gradient);
gradientFillLayer.setDisplayName("Gradient Fill Layer");
psdImage.addLayer(gradientFillLayer);
```

Känn dig fri att experimentera med linjära eller radiella gradienter via lagrets inställningar.

### Steg 5: Lägg till ett mönsterfyllningslager
Mönsterfyllningar låter dig mosaikera bilder eller texturer över ett lager.

```java
FillLayer patternFillLayer = FillLayer.createInstance(FillType.Pattern);
patternFillLayer.setDisplayName("Pattern Fill Layer");
patternFillLayer.setOpacity((byte)50);
psdImage.addLayer(patternFillLayer);
```

Att sätta opaciteten till 50 % får mönstret att smälta väl med lagren under.

### Steg 6: Spara din PSD‑fil
Spara ändringarna till disk.

```java
psdImage.save(outPsdFilePath);
```

Öppna den sparade filen i Photoshop eller någon PSD‑visare för att se de tre nya fyllningslagren.

### Steg 7: Rensa resurser
Disposera alltid `PsdImage`‑objektet för att frigöra native‑minne.

```java
psdImage.dispose();
```

## Vanliga problem & tips
- **Ogiltig utdata‑sökväg** – Se till att katalogen finns och att du har skrivrättigheter.  
- **Minnesanvändning** – För mycket stora canvases, anropa `psdImage.dispose()` så snart du är klar med bilden.  
- **Lagerordning** – Lager läggs till överst i stapeln som standard; använd `psdImage.insertLayer(layer, index)` om du behöver en specifik ordning.

## Vanliga frågor

**Q: Vilka typer av fyllningslager kan jag lägga till med Aspose.PSD för Java?**  
A: Du kan lägga till färg‑, gradient‑ och mönster‑fyllningslager.

**Q: Stöder Aspose.PSD andra bildformat?**  
A: Ja, det fungerar med BMP, JPEG, PNG och många fler format.

**Q: Kan jag använda Aspose.PSD gratis?**  
A: Du kan prova en gratis provversion av Aspose.PSD för Java [här](https://releases.aspose.com/).

**Q: Var kan jag hitta mer dokumentation om Aspose.PSD?**  
A: Du kan komma åt den fullständiga dokumentationen [här](https://reference.aspose.com/psd/java/).

**Q: Finns det ett supportcommunity för Aspose.PSD?**  
A: Ja, du kan få hjälp från communityn på Aspose‑forumet [här](https://forum.aspose.com/c/psd/34).

## Slutsats
Du har nu lärt dig hur du **modifierar PSD‑lager programatiskt** genom att lägga till olika fyllningslager med Aspose.PSD för Java. Detta tillvägagångssätt sparar tid, säkerställer konsistens över projekt och öppnar dörren till kraftfulla batch‑processningsscenarier. Experimentera med olika färger, gradienter och mönster för att se hur långt du kan driva automatiserad designskapande.

---

**Senast uppdaterad:** 2026-03-04  
**Testad med:** Aspose.PSD for Java (latest release)  
**Författare:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}