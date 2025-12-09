---
date: 2025-12-06
description: Lär dig hur du roterar en bild 270 grader med Aspose.PSD för Java. Den
  här guiden visar hur du roterar PSD‑filer, vänder bilder och konverterar PSD till
  JPEG.
linktitle: Rotate Image 270 Degrees
second_title: Aspose.PSD Java API
title: Hur man roterar en bild 270 grader med Aspose.PSD för Java
url: /sv/java/advanced-image-manipulation/rotate-image/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Rotera bild 270 grader med Aspose.PSD för Java

## Introduktion

I den här **java‑bildbehandlingshandledningen** får du lära dig hur du **roterar en bild 270 grader** snabbt och pålitligt med Aspose.PSD för Java. Oavsett om du bygger ett foto‑redigeringsverktyg, automatiserar batch‑konverteringar eller bara behöver ändra orienteringen på ett PSD‑lager, gör biblioteket uppgiften enkel. Vi berör också hur du vänder bilder och konverterar den roterade PSD‑filen till JPEG, så att du får ett komplett end‑to‑end‑flöde.

## Snabba svar
- **Vilket bibliotek hanterar rotationen?** Aspose.PSD för Java  
- **Vilken rotationsvinkel används i exemplet?** 270 grader  
- **Kan jag också vända bilden?** Ja – använd `RotateFlipType`‑alternativ som `Rotate90FlipX`  
- **Hur sparar jag resultatet?** I exemplet sparas som JPEG med `JpegOptions`  
- **Behöver jag licens för produktion?** En giltig Aspose.PSD‑licens krävs för kommersiell användning  

## Vad betyder “rotera bild 270 grader”?
Att rotera en bild 270 grader innebär att vrida bilden tre fjärdedelar av en hel cirkel medurs (eller 90 grader moturs). I många grafiska redigeringsscenario motsvarar denna orientering den ursprungliga porträttlayouten efter en serie transformationer.

## Varför använda Aspose.PSD för denna uppgift?
- **Fullt PSD‑stöd** – fungerar med lager, masker och justeringsobjekt.  
- **Ingen inbyggd Photoshop behövs** – kör på vilken Java‑runtime som helst.  
- **Enkel API** – ett enda metodanrop (`rotateFlip`) hanterar rotation och vändning.  
- **Enkel formatkonvertering** – exportera direkt till JPEG, PNG eller andra vanliga format.

## Förutsättningar

Innan du börjar, se till att du har:

- **Aspose.PSD för Java**‑biblioteket installerat. Du kan ladda ner det och se hela API‑referensen [här](https://reference.aspose.com/psd/java/).  
- En Java‑utvecklingsmiljö (JDK 8 eller högre).  
- En exempel‑PSD‑fil som du vill rotera. Uppdatera variabeln `sourceFile` i koden med rätt sökväg till din fil.

## Importera paket

Börja med att importera de nödvändiga klasserna från Aspose.PSD‑paketet:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RotateFlipType;

import com.aspose.psd.imageoptions.JpegOptions;
```

## Så roterar du PSD – Steg 1: Ladda bilden

Skapa en `Image`‑instans som pekar på din käll‑PSD‑fil:

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
Image image = Image.load(sourceFile);
```

## Så roterar du PSD – Steg 2: Rotera bilden 270 grader

Använd metoden `rotateFlip` med `RotateFlipType.Rotate270FlipNone` för att uppnå en 270‑graders rotation utan någon vändning:

```java
image.rotateFlip(RotateFlipType.Rotate270FlipNone);
```

> **Proffstips:** Om du också behöver vända bilden horisontellt eller vertikalt, välj ett annat `RotateFlipType`‑värde som `Rotate90FlipX` eller `Rotate180FlipY`.

## Så roterar du PSD – Steg 3: Konvertera PSD till JPEG och spara

Efter rotationen kan du **konvertera PSD till JPEG** (eller något annat stödd format) med hjälp av rätt options‑klass:

```java
String destName = dataDir + "RotatedImage_out.jpg";
image.save(destName, new JpegOptions());
```

Filen `RotatedImage_out.jpg` innehåller nu det ursprungliga PSD‑innehållet roterat 270 grader och sparat som en JPEG.

## Vanliga problem och lösningar

| Problem | Lösning |
|-------|----------|
| **Bilden visas upp och ner** | Kontrollera att du använde `Rotate270FlipNone`. För en 90‑graders medurs-rotation använd `Rotate90FlipNone`. |
| **Utdatafilen är korrupt** | Säkerställ att målmappen finns och att du har skrivbehörighet. |
| **Licensundantag** | Installera en tillfällig eller permanent Aspose.PSD‑licens innan du laddar bilden i produktion. |

## Vanliga frågor

**Q: Är Aspose.PSD kompatibel med olika bildformat?**  
A: Ja, Aspose.PSD stödjer PSD, JPEG, PNG, BMP, GIF och många andra rasterformat.

**Q: Kan jag använda egna rotationer, inte bara fördefinierade vändningar?**  
A: Absolut! Även om `RotateFlipType` erbjuder vanliga vinklar kan du kombinera flera anrop eller använda transformationsmatriser för godtyckliga vinklar.

**Q: Hur konverterar jag den roterade PSD‑filen till ett annat format, till exempel PNG?**  
A: Byt ut `JpegOptions` mot `PngOptions` (eller motsvarande options‑klass) i `save`‑metoden.

**Q: Var kan jag hitta ytterligare support eller hjälp?**  
A: För community‑hjälp, besök [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34).

**Q: Finns det en gratis provversion?**  
A: Ja, du kan prova Aspose.PSD med en [gratis provversion](https://releases.aspose.com/).

**Q: Hur får jag en tillfällig licens?**  
A: Om du behöver en tillfällig licens kan du skaffa en [här](https://purchase.aspose.com/temporary-license/).

## Slutsats

Du har nu lärt dig hur du **roterar en bild 270 grader** med Aspose.PSD för Java, vänder bilder vid behov och exporterar resultatet till JPEG. Detta enkla arbetsflöde kan integreras i större Java‑baserade bildbehandlingspipelines och ger dig full kontroll över PSD‑manipulation utan att behöva Photoshop.

---

**Senast uppdaterad:** 2025-12-06  
**Testad med:** Aspose.PSD för Java 24.12  
**Författare:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}