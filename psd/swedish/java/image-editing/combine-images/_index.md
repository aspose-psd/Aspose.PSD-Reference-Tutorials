---
date: 2025-12-30
description: Lär dig hur du skapar en PSD‑fil i Java genom att kombinera två bilder
  med Aspose.PSD. Följ vår steg‑för‑steg‑guide för att snabbt sammanfoga bilder till
  en PSD‑fil.
linktitle: Combine Images
second_title: Aspose.PSD Java API
title: Hur man skapar PSD‑fil i Java – Kombinera bilder med Aspose.PSD
url: /sv/java/image-editing/combine-images/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Skapa PSD-fil i Java – Kombinera bilder med Aspose.PSD

## Introduktion

Om du behöver **skapa en PSD-fil i Java** genom att slå ihop flera bilder, gör Aspose.PSD jobbet enkelt. I den här handledningen går vi igenom hur du kombinerar två bilder till en enda PSD‑canvas, förklarar varför detta tillvägagångssätt är användbart och ger dig färdig‑att‑köra kod. När du är klar kommer du att kunna **kombinera två bilder Java**‑stil och generera en professionellt utseende lagerfil.

## Snabba svar
- **Vilket bibliotek är bäst för att slå ihop bilder till PSD?** Aspose.PSD for Java.  
- **Hur lång tid tar implementeringen?** Ungefär 10‑15 minuter för en grundläggande kombination.  
- **Behöver jag en licens?** En gratis provversion fungerar för testning; en kommersiell licens krävs för produktion.  
- **Kan jag lägga till fler än två bilder?** Ja – upprepa `drawImage`‑anropen för varje extra lager.  
- **Vilken Java‑version stöds?** Java 8 och nyare.

## Förutsättningar

Innan du börjar, se till att du har följande:

1. **Aspose.PSD Library** – ladda ner den från [here](https://releases.aspose.com/psd/java/).  
2. **Java Development Kit (JDK)** – Java 8+ rekommenderas.  
3. **Document Directory** – en mapp på din maskin där källbilderna och den resulterande PSD‑filen ska lagras.

## Importera paket

Börja med att importera de nödvändiga Aspose.PSD‑klasserna i ditt projekt:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;

import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.sources.FileCreateSource;
```

## Steg‑för‑steg guide

### Steg 1: Skapa PSD‑alternativ (förbered filen)

Vi skapar först en `PsdOptions`‑instans som kommer att hålla utdata‑inställningarna.

```java
PsdOptions imageOptions = new PsdOptions();
```

### Steg 2: Ange FileCreateSource (definiera var PSD‑filen ska sparas)

Tilldela ett `FileCreateSource` till alternativen och peka på den önskade resultatfilen.

```java
imageOptions.setSource(new FileCreateSource(dataDir + "Two_images_result_out.psd", false));
```

### Steg 3: Skapa Image‑instans (initiera canvas‑storlek)

Skapa ett `Image`‑objekt med alternativen och specificera en canvas på 600 × 600 pixlar.

```java
Image image = Image.create(imageOptions, 600, 600);
```

### Steg 4: Initiera Graphics och rita den första bilden

Ett `Graphics`‑objekt låter oss måla på canvasen. Vi rensar bakgrunden till vitt och ritar den första källbilden på vänstra halvan.

```java
Graphics graphics = new Graphics(image);
graphics.clear(Color.getWhite());
graphics.drawImage(Image.load(dataDir + "example1.psd"), 0, 0, 300, 600);
```

### Steg 5: Rita den andra bilden (slutför kombinationen)

Nu placerar vi den andra bilden på högra halvan av samma canvas.

```java
graphics.drawImage(Image.load(dataDir + "example2.psd"), 300, 0, 300, 600);
```

### Steg 6: Spara den resulterande PSD‑filen

Till sist sparar vi den kombinerade canvasen till disk.

```java
image.save();
```

Grattis! Du har framgångsrikt **slagit ihop bilder till PSD** och skapat en PSD‑fil i Java.

## Varför kombinera bilder med Aspose.PSD?

- **Layer‑aware** – varje `drawImage`‑anrop lägger till ett separat lager som du kan redigera senare.  
- **Format flexibility** – stöder PSD, PNG, JPEG, BMP och fler.  
- **No native dependencies** – ren Java, fungerar på alla OS som kör JDK.

## Vanliga problem och lösningar

| Problem | Orsak | Åtgärd |
|-------|-------|-----|
| `File not found`‑fel vid inläsning av källbilder | Felaktig `dataDir`‑sökväg | Verifiera att `dataDir` pekar på mappen som innehåller `example1.psd` och `example2.psd`. |
| Utdata‑PSD är tom | `graphics.clear` anropad efter ritning | Säkerställ att `graphics.clear(Color.getWhite())` körs **innan** några `drawImage`‑anrop. |
| Licens‑undantag vid körning | Saknad eller utgången Aspose.PSD‑licens | Applicera en giltig licens med `License license = new License(); license.setLicense("Aspose.PSD.lic");` innan något API‑anrop. |

## Vanliga frågor

### Q1: Är Aspose.PSD kompatibel med alla bildformat?
A1: Aspose.PSD fokuserar främst på PSD‑filformatet. Däremot stöder det flera andra format för in- och utdata.

### Q2: Kan jag utföra ytterligare modifieringar på den kombinerade bilden?
A2: Absolut! Efter att ha kombinerat bilderna kan du vidare manipulera den resulterande PSD‑filen med Aspose.PSD:s omfattande funktioner.

### Q3: Finns det några licenskrav för att använda Aspose.PSD?
A3: Ja, en giltig licens krävs för kommersiell användning. Skaffa den [here](https://purchase.aspose.com/buy).

### Q4: Finns det en gratis provversion av Aspose.PSD?
A4: Ja, du kan utforska Aspose.PSD med en gratis provversion [here](https://releases.aspose.com/).

### Q5: Var kan jag hitta support för frågor relaterade till Aspose.PSD?
A5: Besök [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) för community‑support och diskussioner.

---

**Senast uppdaterad:** 2025-12-30  
**Testad med:** Aspose.PSD 24.11 for Java  
**Författare:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}