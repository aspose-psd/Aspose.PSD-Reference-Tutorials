---
date: 2026-02-12
description: Lär dig hur du ändrar storlek på bild i Java med Aspose.PSD för Java.
  Steg‑för‑steg‑guide med Resize Type‑enumeration, samt tips om hur du konverterar
  PSD till JPEG.
linktitle: Resizing with Resize Type Enumeration
second_title: Aspose.PSD Java API
title: Ändra bildstorlek i Java – Använda Resize Type‑enumeration i Aspose.PSD för
  Java
url: /sv/java/advanced-image-manipulation/resizing-with-resize-type-enumeration/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ändra storlek på bild Java: Använda Resize Type Enumeration i Aspose.PSD för Java

## Introduction

Att ändra storlek på bilder är ett vanligt krav i Java‑applikationer, och **resize image java**‑operationer blir enkla med Aspose.PSD. I den här handledningen kommer du att lära dig hur du **resize image java** med den kraftfulla Resize Type Enumeration, och du kommer också att se hur du **convert psd to jpeg** efter storleksändring. Oavsett om du bygger ett skrivbordsverktyg eller en server‑sid tjänst, kommer dessa steg att hjälpa dig att på ett pålitligt sätt hantera bilddimensioner och uppnå en högkvalitativ bildändring.

## Quick Answers
- **Vilket bibliotek hanterar resize image java?** Aspose.PSD for Java.  
- **Vilken resize type ger bästa kvalitet?** `ResizeType.LanczosResample`.  
- **Kan jag konvertera PSD till JPEG efter storleksändring?** Ja – spara bara med `JpegOptions`.  
- **Behöver jag en licens för produktion?** En giltig Aspose.PSD‑licens krävs för produktionsanvändning.  
- **Är detta tillvägagångssätt lämpligt för stora batcher?** Absolut; API‑et är optimerat för prestanda.

## What is Resize Image Java?

Termen “resize image java” avser att programatiskt ändra pixeldimensionerna på en bild med Java‑kod. Aspose.PSD tillhandahåller ett koncist API som abstraherar den lågnivå pixelmanipuleringen, så att du kan fokusera på affärslogik istället för bildbehandlingsdetaljer.

## Why Use Resize Type Enumeration?

Resize Type Enumeration ger dig fin‑granulär kontroll över återprovningsalgoritmen, vilket låter dig balansera hastighet och kvalitet. För de flesta applikationer erbjuder `LanczosResample` en bra kompromiss, levererar skarpa resultat utan stor prestandapåverkan. Att välja rätt resize type är nyckeln till att uppnå en högkvalitativ bildändring.

## Prerequisites

Innan du påbörjar den här handledningen, se till att du har följande förutsättningar på plats:

1. **Java Development Environment** – en JDK 8+ installerad och konfigurerad.  
2. **Aspose.PSD Library** – ladda ner och installera Aspose.PSD‑biblioteket från [website](https://releases.aspose.com/psd/java/).  
3. **Sample PSD File** – ha en exempel‑PSD‑fil redo för experiment. Du kan använda filen [sample.psd](Your Document Directory/sample.psd) för den här handledningen.

## Import Packages

För att börja, importera de nödvändiga paketen i ditt Java‑projekt:

```java
import com.aspose.psd.Image;
import com.aspose.psd.ResizeType;

import com.aspose.psd.imageoptions.JpegOptions;
```

## Step 1: Load the Image

Börja med att ladda en befintlig bild i en instans av klassen `RasterImage`. Använd följande kodsnutt:

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);
```

## Step 2: Resize the Image

Nu, ändra storlek på den laddade bilden med hjälp av Resize Type Enumeration. I detta exempel använder vi Lanczos Resample‑metoden, som är idealisk när du **how to resize image** med hög kvalitet:

```java
image.resize(300, 300, ResizeType.LanczosResample);
```

## Step 3: Save the Resized Image

Efter storleksändring, spara bilden med de angivna dimensionerna och den valda resize type. Här demonstrerar vi också **convert psd to jpeg** genom att spara resultatet som en JPEG‑fil:

```java
String destName = dataDir + "ResizingwithResizeTypeEnumeration_out.jpg";
image.save(destName, new JpegOptions());
```

Du har nu genomfört ett komplett **resize image java**‑arbetsflöde som producerar en högkvalitativ bildändring och en färdig‑att‑använda JPEG‑utdata.

## Common Issues and Solutions

- **Bilden blir suddig efter storleksändring** – Prova en annan `ResizeType` såsom `Bicubic` eller `NearestNeighbour` för att se vilken som ger det bästa visuella resultatet för just din bild.  
- **OutOfMemoryError på stora PSD‑filer** – Bearbeta bilden i mindre delar eller öka JVM‑heap‑storleken (`-Xmx`‑flaggan).  

## FAQ's

### Q1: Is Aspose.PSD for Java suitable for both small and large-scale projects?

A1: Absolut! Aspose.PSD for Java är designat för att passa projekt av alla storlekar och erbjuder skalbarhet och effektivitet.

### Q2: Can I use a different resize type other than Lanczos Resample?

A2: Ja, Aspose.PSD for Java erbjuder olika resize types, såsom Nearest Neighbour, Bicubic och fler. Utforska dokumentationen för en komplett lista.

### Q3: Where can I find additional support for Aspose.PSD for Java?

A3: För frågor eller hjälp, besök [Aspose.PSD forum](https://forum.aspose.com/c/psd/34).

### Q4: Is there a free trial available for Aspose.PSD for Java?

A4: Ja, du kan få tillgång till en gratis provversion [here](https://releases.aspose.com/).

### Q5: How can I obtain a temporary license for Aspose.PSD for Java?

A5: För att få en tillfällig licens, besök [this link](https://purchase.aspose.com/temporary-license/).

## Frequently Asked Questions

**Q: Hur konverterar jag programatiskt en PSD‑fil till JPEG utan att ändra storlek?**  
A: Ladda PSD‑filen med `Image.load`, och anropa sedan `image.save("output.jpg", new JpegOptions());`.

**Q: Är det möjligt att behålla original‑DPI när man ändrar storlek?**  
A: Ja, du kan sätta `Resolution`‑egenskapen på `Image`‑objektet innan du sparar.

**Q: Kan jag kedja flera storleksändringar?**  
A: Även om du kan anropa `resize` flera gånger, är det mer effektivt att beräkna de slutgiltiga dimensionerna och ändra storlek en gång.

## Additional FAQ

**Q: Påverkar Resize Type Enumeration bearbetningshastigheten?**  
A: Ja, enklare algoritmer som `NearestNeighbour` är snabbare men kan ge lägre kvalitet, medan `LanczosResample` ger högre kvalitet med en måttlig prestandakostnad.

**Q: Kan jag ändra storlek på bilder i en multi‑threaded miljö?**  
A: Aspose.PSD‑API är trådsäker för endast‑läsliga operationer. För samtidig storleksändring, skapa separata `Image`‑instanser per tråd.

**Q: Hur hanterar jag bilder med alfakanaler vid storleksändring?**  
A: Biblioteket bevarar alfa‑transparens som standard. Om du behöver platta till bilden, sätt bakgrundsfärgen innan du sparar.

---

**Senast uppdaterad:** 2026-02-12  
**Testad med:** Aspose.PSD for Java 24.12  
**Författare:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}