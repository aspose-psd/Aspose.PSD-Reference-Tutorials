---
date: 2026-03-07
description: Lär dig hur du lägger till text i PSD‑filer vid körning med Java och
  Aspose.PSD. Följ den här steg‑för‑steg‑guiden för att snabbt skapa ett textlager
  i en PSD.
linktitle: Add Text Layer on Runtime in PSD Files using Java
second_title: Aspose.PSD Java API
title: Lägg till text i PSD-filer vid körning med Java
url: /sv/java/modifying-converting-psd-images/add-text-layer-runtime-psd-files/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Lägg till text i PSD-filer vid körning med Java

## Introduktion
Om du någonsin har redigerat ett Photoshop‑dokument manuellt vet du hur kraftfulla lager kan vara. Tänk om du kunde **lägga till text i PSD**‑filer automatiskt från ditt Java‑program? Med Aspose.PSD för Java‑biblioteket kan du skapa ett textlager i en PSD vid körning, vilket öppnar dörren för batch‑bearbetning, dynamisk grafikgenerering och automatiserade varumärkesflöden. I den här handledningen går vi igenom hela processen, från att sätta upp projektet till att spara den uppdaterade filen.

## Snabba svar
- **Vilket bibliotek behöver jag?** Aspose.PSD för Java.  
- **Kan jag lägga till text i en befintlig PSD?** Ja – ladda bara filen, lägg till ett `TextLayer` och spara.  
- **Behöver jag en licens för produktion?** En kommersiell licens krävs för icke‑utvärderingsbruk.  
- **Vilken Java‑version stöds?** JDK 8 eller högre (vi rekommenderar den senaste LTS).  
- **Är detta lämpligt för webb‑back‑ends?** Absolut – API‑et fungerar i alla Java‑baserade servermiljöer.

## Vad innebär “add text to PSD”?
Att lägga till text i en PSD betyder att programatiskt skapa ett nytt textlager i ett Photoshop‑dokument. Lagret beter sig som vilket annat Photoshop‑textlager som helst: du kan flytta det, redigera dess innehåll och applicera stil – allt utan att öppna Photoshop.

## Varför skapa ett textlager i en PSD med Java?
- **Automation** – Generera marknadsföringsmaterial, vattenstämplar eller produktetiketter i bulk.  
- **Konsistens** – Säkerställ samma teckensnitt, storlek och placering i tusentals filer.  
- **Integration** – Kombinera med andra Java‑tjänster (e‑handel, rapportering, CI‑pipelines) för att leverera grafik i realtid.

## Förutsättningar
Innan du skriver kod, se till att du har:

1. **Java Development Kit (JDK)** – Installera JDK 8 eller nyare. Du kan [ladda ner den här](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. **Aspose.PSD för Java** – Hämta den senaste JAR‑filen från [Aspose releases page](https://releases.aspose.com/psd/java/).  
3. **IDE (valfritt men hjälpsamt)** – IntelliJ IDEA, Eclipse eller någon annan editor du föredrar.  
4. **Grundläggande Java‑kunskaper** – Du bör vara bekväm med klasser, objekt och fil‑I/O.  
5. **Ett exempel‑PSD** – För den här guiden använder vi `OneLayer.psd` placerad i en mapp du själv väljer.

## Importera paket
Först importerar du de klasser du behöver för att arbeta med PSD‑filer och textlager.

```java
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.TextLayer;
```

Dessa importeringar ger dig åtkomst till kärnfunktionaliteten i Aspose.PSD.

## Steg‑för‑steg‑guide

### Steg 1: Ställ in din dokumentkatalog
Definiera mappen som innehåller din käll‑PSD och där utdata ska sparas.

```java
String dataDir = "Your Document Directory"; 
```

Ersätt `"Your Document Directory"` med den absoluta eller relativa sökvägen till dina filer.

### Steg 2: Läs in din käll‑PSD‑fil
Läs in den befintliga PSD‑filen i minnet med `Image.load()`.

```java
String sourceFileName = dataDir + "OneLayer.psd"; 
Image img = Image.load(sourceFileName);
```

Om sökvägen är korrekt representerar `img` nu det inlästa Photoshop‑dokumentet.

### Steg 3: Casta till `PsdImage`
Eftersom vi arbetar med Photoshop‑specifika funktioner castar vi den generiska `Image`‑klassen till `PsdImage`.

```java
PsdImage im = (PsdImage)img;
```

Casten låser upp metoder som `addTextLayer()`.

### Steg 4: Definiera rektangeln för textlagret
Ange var den nya texten ska placeras. Rektangeln definierar position (x, y) och storlek (bredd, höjd).

```java
Rectangle rect = new Rectangle(
    (int)(im.getWidth() * 0.25),
    (int)(im.getHeight() * 0.25),
    (int)(im.getWidth() * 0.5),
    (int)(im.getHeight() * 0.5)
);
```

Justera gärna beräkningarna för att passa ditt layoutbehov.

### Steg 5: Lägg till textlagret
Skapa själva textlagret inom den definierade rektangeln.

```java
TextLayer layer = im.addTextLayer("Added text", rect);
```

Ersätt `"Added text"` med den sträng du vill ska visas i PSD‑filen. Detta är där vi **skapar textlager PSD** programatiskt.

### Steg 6: Spara din uppdaterade PSD‑fil
Skriv det modifierade dokumentet till en ny fil så att du inte skriver över originalet.

```java
String psdPath = dataDir + "ImageWithTextLayer.psd";
im.save(psdPath);
```

Efter körning hittar du `ImageWithTextLayer.psd` i mål‑mappen, nu med det nya textlagret.

## Vanliga problem & lösningar
| Problem | Orsak | Lösning |
|-------|--------|-----|
| **`NullPointerException` on `im.addTextLayer`** | PSD har inte laddats korrekt (fel sökväg). | Verifiera att `sourceFileName` pekar på en befintlig PSD. |
| **Texten syns inte** | Rektangeln placerad utanför duken eller lagret är dolt. | Justera rektangelkoordinaterna eller kontrollera lagrets synlighet med `layer.setVisible(true)`. |
| **LicenseException** | Biblioteket används utan en giltig licens i produktion. | Skaffa en kommersiell licens och sätt den via `License license = new License(); license.setLicense("Aspose.PSD.lic");`. |

## Vanliga frågor

**Q: Kan jag lägga till flera textlager?**  
A: Ja – upprepa helt enkelt Steg 4 och 5 för varje textstycke du vill infoga.

**Q: Hur formaterar jag texten (teckensnitt, storlek, färg)?**  
A: Klassen `TextLayer` har en metod `getTextData()` där du kan ändra `Font`, `FontSize`, `Color` och andra stilinställningar. Se Aspose.PSD API‑dokumentationen för fullständig information.

**Q: Vad händer om min PSD redan har många lager?**  
A: Aspose.PSD hanterar komplexa lagerstrukturer. Du kan rikta in dig på specifika grupper eller infoga det nya textlagret på ett önskat index med överlagrade versioner av `addTextLayer`.

**Q: Är detta tillvägagångssätt lämpligt för webbapplikationer?**  
A: Absolut. Så länge din server kör Java kan du generera eller modifiera PSD‑filer i realtid och leverera dem till klienter.

**Q: Var kan jag få hjälp om jag stöter på problem?**  
A: Besök [Aspose support forums](https://forum.aspose.com/c/psd/34) där både communityn och Aspose‑ingenjörer kan hjälpa dig.

## Slutsats
Du har nu sett hur enkelt det är att **lägga till text i PSD**‑filer vid körning med Java och Aspose.PSD. Denna teknik ger dig möjlighet att automatisera grafisk skapelse, anpassa resurser och integrera Photoshop‑nivåredigering i vilken Java‑baserad lösning som helst. Utforska resten av Aspose.PSD‑API‑et för att lägga till former, rasterlager eller till och med applicera filter för ännu rikare automation.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Senast uppdaterad:** 2026-03-07  
**Testad med:** Aspose.PSD för Java 24.12 (senaste vid skrivtillfället)  
**Författare:** Aspose  

---