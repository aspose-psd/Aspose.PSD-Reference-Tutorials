---
date: 2026-03-15
description: Lär dig hur du skapar PSD‑filer, genererar PSD‑färgpalett och ställer
  in PSD‑färgläge med Aspose.PSD för Java i den här steg‑för‑steg‑guiden.
linktitle: Create Indexed PSD Files using Aspose.PSD for Java
second_title: Aspose.PSD Java API
title: Hur man skapar PSD-filer med Aspose.PSD för Java
url: /sv/java/modifying-converting-psd-images/create-indexed-psd-files/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hur man skapar PSD-filer med Aspose.PSD för Java

## Introduktion
Om du någonsin har undrat **hur man skapar PSD**-filer programatiskt, är du på rätt plats. Aspose.PSD för Java ger dig full kontroll över Photoshop-dokument, så att du kan generera, redigera och spara PSD-filer utan att någonsin öppna Photoshop. I den här handledningen går vi igenom hur man skapar en **indexed PSD**-fil, ställer in PSD-färgläget och genererar en anpassad färgpalett – allt med tydlig, steg‑för‑steg Java‑kod. Oavsett om du bygger en grafikpipeline, automatiserar skapandet av resurser eller bara experimenterar, kommer koncepten här att hjälpa dig att förverkliga dina visuella idéer.

## Snabba svar
- **Vilket bibliotek behöver jag?** Aspose.PSD for Java
- **Kan jag skapa en indexed PSD?** Ja, genom att sätta färgläget till `Indexed`
- **Behöver jag ha Photoshop installerat?** Nej, Aspose.PSD fungerar oberoende
- **Vilken Java-version krävs?** JDK 8 eller senare
- **Hur stor kan duken vara?** Vilken storlek som helst; detta exempel använder 500 × 500 px

## Vad är en Indexed PSD-fil?
En indexed PSD lagrar färger i en palett istället för fullfärgsvärden för varje pixel. Detta minskar filstorleken och är idealiskt för grafik med begränsade färger, såsom ikoner eller UI‑resurser. Genom att generera en anpassad palett styr du exakt vilka färger som visas i den färdiga bilden.

## Varför generera en PSD-färgpalett?
Att skapa en **PSD color palette** låter dig:
- Hålla filstorlekar små för webb‑ eller mobilanvändning  
- Säkerställa konsekvent varumärkesprofil genom att begränsa färgerna till din företagspalett  
- Snabba upp rendering i applikationer som stödjer indexed‑bilder

## Förutsättningar
Innan vi dyker ner i koden, se till att du har följande:

1. **Grundläggande kunskaper i Java** – du bör vara bekväm med klasser, metoder och objektinstansering.  
2. **Java Development Kit (JDK) 8+** – installerat och konfigurerat i din IDE.  
3. **IDE (IntelliJ IDEA, Eclipse, etc.)** – valfritt men starkt rekommenderat för enklare felsökning.  
4. **Aspose.PSD for Java Library** – ladda ner den **[here](https://releases.aspose.com/psd/java/)** och lägg till JAR‑filen i ditt projekts classpath.  
5. **Grundläggande grafisk design‑koncept** – förståelse för färglägen, paletter och grundläggande former hjälper dig att följa med.

## Importera paket
Innan vi fortsätter med koden, låt oss säkerställa att alla nödvändiga paket är importerade i ditt Java‑program. Här är vad du behöver:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.Pen;
import com.aspose.psd.Rectangle;
import com.aspose.psd.fileformats.psd.ColorModes;
import com.aspose.psd.fileformats.psd.CompressionMethod;
import com.aspose.psd.fileformats.psd.PsdColorPalette;
import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.sources.FileCreateSource;
```

Dessa importeringar gör att du kan arbeta med PSD‑alternativ, färger och grafikmanipulation via Aspose.PSD.

Nu ska vi gå igenom koden steg‑för‑steg för **how to create PSD**‑filer med ett indexed‑färgläge.

## Steg 1: Ställ in din dokumentkatalog
Först, definiera var den genererade PSD‑filen ska sparas.

```java
String dataDir = "Your Document Directory";
```

Ersätt `"Your Document Directory"` med en absolut eller relativ sökväg, t.ex. `"/Users/YourName/Documents/"`.

## Steg 2: Skapa en instans av PsdOptions
`PsdOptions` innehåller alla inställningar för filen du ska generera.

```java
PsdOptions createOptions = new PsdOptions();
```

## Steg 3: Ställ in grundläggande egenskaper för PsdOptions
Här specificerar vi utdata‑platsen, **set psd color mode** till `Indexed`, och PSD‑versionen.

```java
createOptions.setSource(new FileCreateSource(dataDir + "Newsample_out.psd", false));
createOptions.setColorMode(ColorModes.Indexed);
createOptions.setVersion(5);
```

- **Source** – den fullständiga sökvägen till den nya filen.  
- **Color Mode** – `Indexed` talar om för Aspose.PSD att använda en palettbaserad bild.  
- **Version** – PSD‑formatversion (5 fungerar för de flesta moderna Photoshop‑versioner).

## Steg 4: Skapa en färgpalett (Generate PSD Color Palette)
Definiera de färger som kommer att vara tillgängliga i den indexed‑bilden.

```java
Color[] palette = { Color.getRed(), Color.getGreen(), Color.getBlue(), Color.getYellow() };
createOptions.setPalette(new PsdColorPalette(palette));
createOptions.setCompressionMethod(CompressionMethod.RLE);
```

- `palette`‑arrayen kan innehålla upp till 256 `Color`‑objekt.  
- `CompressionMethod.RLE` ger effektiv förlustfri komprimering för indexed‑bilder.

## Steg 5: Skapa PSD‑bildens duk
Nu skapar vi en tom PSD med de dimensioner vi vill ha.

```java
Image psd = Image.create(createOptions, 500, 500);
```

Detta skapar en 500 × 500 pixel‑duk som använder paletten som definierades tidigare.

## Steg 6: Rita grafik på PSD‑filen
Lägg till visuellt innehåll – här ritar vi en enkel röd ellips på en vit bakgrund.

```java
Graphics graphics = new Graphics(psd);
graphics.clear(Color.getWhite());
graphics.drawEllipse(new Pen(Color.getRed(), 6), new Rectangle(0, 0, 400, 400));
```

- `clear(Color.getWhite())` fyller bakgrunden med vitt.  
- `drawEllipse` ritar en röd ellips med en 6‑pixel penseldrag.

## Steg 7: Spara PSD‑filen
Till sist sparas bilden till disk.

```java
psd.save();
```

Filen `Newsample_out.psd` kommer att visas i den katalog du angav tidigare.

## Vanliga problem & tips
- **Palette Size** – Om du behöver fler än 4 färger, lägg helt enkelt till dem i `palette`‑arrayen (upp till 256).  
- **File Permissions** – Säkerställ att Java‑processen har skrivbehörighet till `dataDir`.  
- **Incorrect Color Mode** – Att glömma `createOptions.setColorMode(ColorModes.Indexed)` kommer att producera en RGB‑PSD istället för en indexed‑PSD.

## Vanliga frågor

**Q: Vad är Aspose.PSD för Java?**  
A: Aspose.PSD för Java är ett bibliotek som möjliggör manipulation av PSD‑ (Photoshop)‑filer programatiskt med Java.

**Q: Kan jag använda Aspose.PSD gratis?**  
A: Ja, du kan få tillgång till en gratis provversion av Aspose.PSD **[here](https://releases.aspose.com/)**.

**Q: Behöver jag ha Photoshop installerat för att arbeta med Aspose.PSD?**  
A: Nej, du kan skapa och manipulera PSD‑filer utan Photoshop, eftersom Aspose.PSD hanterar alla operationer oberoende.

**Q: Hur får jag en tillfällig licens för Aspose.PSD?**  
A: Du kan begära en tillfällig licens **[here](https://purchase.aspose.com/temporary-license/)**.

**Q: Var kan jag få support för Aspose.PSD?**  
A: Du kan få support via Aspose‑forumet **[here](https://forum.aspose.com/c/psd/34)**.

## Slutsats
Du har just lärt dig **how to create PSD**‑filer med ett indexed‑färgläge, genererat en anpassad palett och lagt till enkel grafik – allt med Aspose.PSD för Java. Med dessa byggstenar kan du gå vidare till mer komplexa teckningar, lagerhantering och batch‑behandling. För djupare utforskning, kolla in den officiella API‑referensen **[here](https://reference.aspose.com/psd/java/)** och fortsätt experimentera med olika paletter och ritprimitive.

---

**Senast uppdaterad:** 2026-03-15  
**Testad med:** Aspose.PSD for Java 24.12 (latest)  
**Författare:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}