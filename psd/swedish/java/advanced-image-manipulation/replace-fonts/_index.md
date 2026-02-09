---
date: 2026-02-09
description: Lär dig hur du använder Aspose PSD-teckensnittssubstitution i Java för
  att hantera PSD-filer med saknade teckensnitt, snabbt ersätta saknade teckensnitt
  i PSD och exportera bilder.
linktitle: Replace Fonts
second_title: Aspose.PSD Java API
title: Aspose PSD-teckensnittssubstitution i Java – Ersätt saknade teckensnitt
url: /sv/java/advanced-image-manipulation/replace-fonts/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose PSD Font Substitution i Java

## Introduktion

Om du behöver byta ut saknade eller oönskade typsnitt i en Photoshop (PSD)-fil, gör **Aspose PSD font substitution** det smärtfritt. I Java‑applikationer kan du ladda en PSD, tala om för Aspose vilket reservtypsnitt som ska användas, och sedan spara resultatet i valfritt format. Denna handledning guidar dig genom hela **aspose psd font substitution**‑arbetsflödet, från att konfigurera ditt projekt till att exportera den uppdaterade bilden, så att du på ett pålitligt sätt kan hantera saknade teckensnitt i PSD‑scenarier utan att öppna Photoshop.

## Snabba svar
- **Vilket bibliotek hanterar teckensnittsersättning?** Aspose.PSD for Java  
- **Hur lång tid tar implementeringen?** About 5‑10 minutes for a basic scenario  
- **Vilket typsnitt används som standardreserv?** You can set any TrueType font, e.g., “Arial”  
- **Kan jag spara till andra format än PNG?** Yes – PSD, JPEG, BMP, etc., are supported  
- **Behöver jag en licens för produktion?** A valid Aspose.PSD license is required for non‑trial use  

## Vad är Aspose PSD Font Substitution?

Aspose PSD font substitution är processen att ange ett ersättningstypsnitt som biblioteket kommer att använda när det stöter på ett saknat eller ej stödd typsnitt i en PSD‑fil. Detta säkerställer att textlager renderas korrekt utan manuell redigering i Photoshop och låter dig **hantera saknade teckensnitt i PSD**‑filer automatiskt.

## Varför använda Aspose.PSD för Java?

- **Full‑featured PSD handling** – lager, masker, effekter och text är alla åtkomliga via API‑et.  
- **Cross‑platform** – fungerar på alla OS som stödjer Java.  
- **No external dependencies** – biblioteket hanterar teckensnittsersättning internt, så du behöver inte leverera extra typsnitt med din app.  

## Hur man ersätter saknade teckensnitt i PSD med Aspose PSD

Nedan följer en steg‑för‑steg‑guide som visar **hur man ersätter saknade teckensnitt i PSD**‑filer med ett anpassat reservtypsnitt.

## Förutsättningar

- **Java Development Kit (JDK)** – version 8 eller högre installerad.  
- **Aspose.PSD for Java** – ladda ner den senaste JAR‑filen från [release page](https://releases.aspose.com/psd/java/).  
- **En IDE** – IntelliJ IDEA, Eclipse eller någon annan editor du föredrar.  

## Importera paket

Börja med att importera de klasser du behöver. Detta ger dig åtkomst till bildladdning, laddningsalternativ och sparfunktionalitet.

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.PngOptions;
```

## Steg 1: Ange din dokumentkatalog

Definiera mappen som innehåller käll‑PSD‑filen. Ersätt platshållaren med den faktiska sökvägen på din maskin.

```java
String dataDir = "Your Document Directory";
```

## Steg 2: Ladda bilden med ett ersättningsteckensnitt

Skapa en `PsdLoadOptions`‑instans, ange standardreservtypsnittet (t.ex. **Arial**) och ladda PSD‑filen. Aspose kommer automatiskt att tillämpa reservtypsnittet när ett saknat typsnitt påträffas.

```java
PsdLoadOptions psdLoadOptions = new PsdLoadOptions(); 
psdLoadOptions.setDefaultReplacementFont("Arial");

PsdImage psdImage = (PsdImage)Image.load(dataDir + "Cloud_AzPlat_Banner3A_SB_EN_US_160x600_chinese_font.psd", psdLoadOptions);
```

## Steg 3: Spara den ersatta bilden

Efter teckensnittsersättningen kan du exportera bilden i vilket stödformat som helst. Här sparar vi den som PNG, men du kan också välja JPEG, BMP eller till och med skriva tillbaka till PSD.

```java
PngOptions pngOptions = new PngOptions();
psdImage.save(dataDir + "replaced_font.png", pngOptions);
```

## Vanliga problem och lösningar

| Problem | Orsak | Lösning |
|---------|-------|---------|
| Text blir förvrängd efter ersättning | Reservtypsnittet innehåller inte de nödvändiga tecknen | Välj ett typsnitt som stödjer det behövda Unicode‑intervallet (t.ex. “Arial Unicode MS”). |
| `OutOfMemoryError` på stora PSD‑filer | Laddar en mycket högupplöst fil utan tillräckligt heap‑minne | Öka JVM‑heap‑storleken (`-Xmx2g`) eller ladda bilden i ett strömningsläge om det finns tillgängligt. |
| Licensundantag | Användning av provversionen i produktion | Applicera en giltig permanent eller tillfällig licens innan bilden laddas. |

## Vanliga frågor

**Q: Kan jag ersätta teckensnitt i andra bildformat än PSD?**  
A: Ja. Även om huvudfallet är PSD, stödjer Aspose.PSD även PNG, JPEG, BMP och TIFF, vilket möjliggör teckensnittsersättning där textlager finns.

**Q: Är standardreservtypsnittet obligatoriskt?**  
A: Nej. Du kan ange vilket TrueType‑typsnitt du föredrar, eller utelämna inställningen så att Aspose använder sitt interna standardtypsnitt.

**Q: Finns det licenskrav för att använda Aspose.PSD?**  
A: En kommersiell licens krävs för produktionsdistributioner. Se [purchase page](https://purchase.aspose.com/buy) för detaljer.

**Q: Kan jag få en tillfällig licens för testning?**  
A: Absolut. Aspose erbjuder gratis tillfälliga licenser för utvärdering – besök [temporary license page](https://purchase.aspose.com/temporary-license/).

**Q: Var kan jag hitta ytterligare support eller diskutera Aspose.PSD‑relaterade problem?**  
A: Community‑forumet är en bra plats att ställa frågor: [Aspose.PSD forum](https://forum.aspose.com/c/psd/34).

**Q: Hur hanterar jag PSD‑filer som innehåller flera saknade teckensnitt?**  
A: Ange standardreservtypsnittet en gång (som visas) – det kommer att tillämpas på *alla* saknade teckensnitt under laddningsoperationen.

**Q: Är det möjligt att ersätta teckensnitt efter att bilden har sparats?**  
A: Teckensnittsersättning måste ske under laddningsfasen. För att ändra teckensnitt senare, ladda om PSD‑filen med ett annat reservtypsnitt och spara igen.

## Slutsats

Du har nu sett ett komplett **aspose psd font substitution**‑arbetsflöde i Java—från att importera rätt klasser, konfigurera ett reservtypsnitt, ladda PSD‑filen till att exportera den korrigerade bilden. Inkludera detta mönster i dina bildbehandlings‑pipelines för att säkerställa konsekvent typografi i alla dina PSD‑tillgångar och för att **hantera saknade teckensnitt i PSD** automatiskt.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Senast uppdaterad:** 2026-02-09  
**Testad med:** Aspose.PSD for Java 24.12 (senaste vid skrivtillfället)  
**Författare:** Aspose  

---