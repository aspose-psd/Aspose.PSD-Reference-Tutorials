---
date: 2026-09-23
description: Lär dig hur du modifierar PSD vector shapes och batch process PSD-filer
  med Aspose.PSD for Java. Detaljerade steg, tips och code placeholders för en komplett
  lösning.
keywords:
- modify psd vector shapes
- batch process psd files
- Aspose.PSD Java
- vector shape editing
lastmod: 2026-09-23
linktitle: Support Length Record Data Properties i PSD - Java
og_description: Lär dig hur du modifierar PSD vector shapes och batch process PSD-filer
  med Aspose.PSD for Java. Step‑by‑step guide med code placeholders och expert tips.
og_image_alt: Guide showing how to edit vector shapes in PSD files using Aspose.PSD
  for Java
og_title: Modifiera PSD vector shapes med Aspose.PSD for Java
schemas:
- author: Aspose
  dateModified: '2026-09-23'
  description: Learn how to modify PSD vector shapes and batch process PSD files using
    Aspose.PSD for Java. Detailed steps, tips, and code placeholders for a complete
    solution.
  headline: Modify PSD vector shapes with Aspose.PSD for Java
  type: TechArticle
- description: Learn how to modify PSD vector shapes and batch process PSD files using
    Aspose.PSD for Java. Detailed steps, tips, and code placeholders for a complete
    solution.
  name: Modify PSD vector shapes with Aspose.PSD for Java
  steps:
  - name: '**Java Development Kit (JDK)** – download from [Oracle''s website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)
      or use your preferred package manager.'
    text: '**Java Development Kit (JDK)** – download from [Oracle''s website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)
      or use your preferred package manager.'
  - name: '**Aspose.PSD for Java** – obtain the latest JAR from the [Aspose releases
      page](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD for Java** – obtain the latest JAR from the [Aspose releases
      page](https://releases.aspose.com/psd/java/).'
  - name: '**IDE** – IntelliJ IDEA, Eclipse, or any Java‑compatible editor.'
    text: '**IDE** – IntelliJ IDEA, Eclipse, or any Java‑compatible editor.'
  - name: '**A PSD file** – create one in Photoshop or grab a sample PSD to experiment
      with.'
    text: '**A PSD file** – create one in Photoshop or grab a sample PSD to experiment
      with.'
  - name: '**Basic Java knowledge** – familiarity with classes, objects, and exception
      handling.'
    text: '**Basic Java knowledge** – familiarity with classes, objects, and exception
      handling.'
  type: HowTo
- questions:
  - answer: The `VsmsResource` will be absent, so `resource` stays `null`. Add a check
      and skip the modification step or inform the user.
    question: How do I handle a PSD that contains no vector shape layers?
  - answer: Yes, `LengthRecord` provides setters for fill, stroke, and opacity. See
      the API docs for the full list.
    question: Can I change other properties like fill color or stroke width?
  - answer: Absolutely. Wrap the code inside a loop that iterates over a directory
      of PSD files, adjusting the input and output paths each time.
    question: Is it possible to batch‑process multiple PSD files?
  - answer: '`Image.load` handles file streams automatically, but if you load from
      an `InputStream`, remember to close it after use.'
    question: Do I need to close streams manually when loading from a file path?
  - answer: The `LengthRecord` and `PathOperations` classes have been available since
      Aspose.PSD 20.10. Using the latest version (24.11 at time of writing) is recommended.
    question: What version of Aspose.PSD is required for these APIs?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- modify psd vector shapes
- Aspose.PSD
- Java image processing
- batch PSD processing
title: Modifiera PSD vector shapes med Aspose.PSD for Java
url: /sv/java/advanced-psd-layer-features-effects/support-length-record-data-properties-psd/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Modifiera PSD vector shapes med Aspose.PSD för Java

## Introduktion
Om du behöver **modifiera PSD vector shapes** programatiskt, ger Aspose.PSD för Java dig full kontroll över Photoshop-filer direkt från din Java-kod. Denna handledning guidar dig genom att stödja length record‑egenskaper — ett viktigt steg när du redigerar lager med vektorshapes. I slutet kommer du kunna öppna en PSD, justera dess vektorshape‑data och spara den uppdaterade filen utan att någonsin starta Photoshop.

## Snabba svar
- **Vad betyder “modify PSD vector shapes”?** Justering av geometri, banoperationer eller andra attribut för vektorbaserade lager i en PSD‑fil.  
- **Vilket bibliotek hanterar detta?** Aspose.PSD för Java.  
- **Behöver jag en licens?** En gratis provversion fungerar för utvärdering; en kommersiell licens krävs för produktion.  
- **Hur lång tid tar implementeringen?** Ungefär 10‑15 minuter för ett grundläggande skript för shape‑modifiering.  
- **Vad är de viktigaste förutsättningarna?** Java JDK, Aspose.PSD för Java och en exempel‑PSD‑fil.

## Vad är “support length record properties”?
Att stödja length record‑egenskaper innebär att komma åt och uppdatera `LengthRecord`‑objekten som beskriver varje vektorväg i en PSD. Dessa poster lagrar information såsom vägens längd, typ och hur den ansluter till andra vägar. Att ändra dem låter dig kontrollera hur former kombineras, skär varandra eller subtraheras, vilket möjliggör exakt vektorredigering.

## Varför använda Aspose.PSD för Java för att stödja length record properties?
Läs in din PSD, redigera vektordata och spara — allt utan Photoshop. Aspose.PSD bearbetar PSD‑filer med flera hundra sidor på under 2 sekunder på en vanlig server, erbjuder över 150 klasser (inklusive 30+ vektorrelaterade typer) och körs på Windows, Linux eller macOS med vilken JDK 11+ som helst. Detta prestandafokuserade bibliotek eliminerar behovet av dyr skrivbordsprogramvara.

## Förutsättningar
1. **Java Development Kit (JDK)** – ladda ner från [Oracle's website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) eller använd din föredragna paket‑hanterare.  
2. **Aspose.PSD for Java** – hämta den senaste JAR‑filen från [Aspose releases page](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse eller någon Java‑kompatibel editor.  
4. **En PSD‑fil** – skapa en i Photoshop eller hämta en exempel‑PSD för att experimentera med.  
5. **Grundläggande Java‑kunskaper** – bekantskap med klasser, objekt och undantagshantering.

## Importera paket
Import‑satserna tar med de centrala Aspose.PSD‑klasserna i scope, såsom `PsdImage`, `VsmsResource` och `LengthRecord`.

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.LayerResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.VsmsResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.LengthRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.PathOperations;
```

## Steg 1: Ställ in dina käll‑ och utmatningskataloger
Definiera var den ursprungliga PSD‑filen finns och var den modifierade filen ska skrivas.

```java
String sourceDir = "Your Source Directory";
String outputDir = "Your Document Directory";
String inPsdFilePath = sourceDir + "PathOperationsShape.psd";
String outPsdFilePath = outputDir + "out_PathOperationsShape.psd";
```

## Steg 2: Läs in PSD‑filen
Använd `Image.load` för att öppna filen och kasta den till `PsdImage` för PSD‑specifika funktioner.

```java
PsdImage psdImage = (PsdImage) Image.load(inPsdFilePath);
```

## Steg 3: Hitta Vsms‑resursen i lagret
`VsmsResource` är behållaren som lagrar vektorshape‑data för ett lager. Loopa igenom det andra lagrets resurser för att hitta den.

```java
VsmsResource resource = null;
for (LayerResource layerResource : psdImage.getLayers()[1].getResources()) {
    if (layerResource instanceof VsmsResource) {
        resource = (VsmsResource) layerResource;
        break;
    }
}
```

## Steg 4: Åtkomst till length‑poster
`LengthRecord` representerar en distinkt vektorväg. Hämta de poster du avser att modifiera.

```java
LengthRecord lengthRecord0 = (LengthRecord) resource.getPaths()[2];
LengthRecord lengthRecord1 = (LengthRecord) resource.getPaths()[7];
LengthRecord lengthRecord2 = (LengthRecord) resource.getPaths()[11];
```

## Steg 5: Modifiera egenskaper för path‑operationer
`PathOperations` definierar hur enskilda former interagerar (t.ex. exkludering, skärning, subtraktion). Att ändra dessa värden uppdaterar den visuella sammansättningen av vektorlager.

```java
lengthRecord0.setPathOperations(PathOperations.ExcludeOverlappingShapes);
lengthRecord1.setPathOperations(PathOperations.IntersectShapeAreas);
lengthRecord2.setPathOperations(PathOperations.SubtractFrontShape);
```

## Steg 6: Spara den modifierade PSD‑filen
Spara dina ändringar till en ny fil.

```java
psdImage.save(outPsdFilePath);
```

## Steg 7: Rensa resurser
Avsluta `PsdImage`‑instansen för att frigöra minne och undvika resursläckor.

```java
psdImage.dispose();
```

## Hur man batch‑processar PSD‑filer med stöd för length record properties
Omge arbetsflödet för en enskild fil i en loop som itererar över en katalog med PSD‑filer, och uppdaterar `inPsdFilePath` och `outPsdFilePath` för varje fil. Detta tillvägagångssätt låter dig applicera identiska vektorshape‑justeringar på dussintals eller hundratals filer på några minuter, idealiskt för automatiserade asset‑pipelines.

## Vanliga fallgropar & tips
- **Null‑kontroller** – verifiera alltid att `resource` inte är `null` innan du kommer åt dess medlemmar.  
- **Path‑indexgränser** – säkerställ att de index du använder (t.ex. `[2]`, `[7]`, `[11]`) finns för den specifika PSD du redigerar.  
- **Licens** – att köra utan en giltig licens inbäddar ett vattenmärke i den sparade PSD‑filen.

## Slutsats
Du har nu ett komplett, end‑to‑end‑exempel på hur du **modifierar PSD vector shapes** genom att stödja length record‑egenskaper med Aspose.PSD för Java. Oavsett om du automatiserar en asset‑pipeline eller bygger ett anpassat designverktyg, ger dessa API:er dig flexibiliteten att manipulera vektorlager utan manuellt Photoshop‑arbete. Experimentera med andra `PathOperations`‑värden eller kombinera flera `LengthRecord`‑redigeringar för att skapa komplexa former.

## Vanliga frågor

**Q: Hur hanterar jag en PSD som inte innehåller några vektorshape‑lager?**  
A: `VsmsResource` kommer att saknas, så `resource` förblir `null`. Lägg till en kontroll och hoppa över modifieringssteget eller informera användaren.

**Q: Kan jag ändra andra egenskaper som fyllnadsfärg eller linjebredd?**  
A: Ja, `LengthRecord` erbjuder set‑metoder för fyllning, linje och opacitet. Se API‑dokumentationen för hela listan.

**Q: Är det möjligt att batch‑processa flera PSD‑filer?**  
A: Absolut. Omge koden i en loop som itererar över en katalog med PSD‑filer och justerar in‑ och ut‑sökvägarna varje gång.

**Q: Måste jag stänga strömmar manuellt när jag laddar från en filsökväg?**  
A: `Image.load` hanterar filströmmar automatiskt, men om du laddar från en `InputStream` bör du komma ihåg att stänga den efter användning.

**Q: Vilken version av Aspose.PSD krävs för dessa API:er?**  
A: `LengthRecord`‑ och `PathOperations`‑klasserna har funnits sedan Aspose.PSD 20.10. Det rekommenderas att använda den senaste versionen (24.11 vid skrivande).

---

**Senast uppdaterad:** 2026-09-23  
**Testat med:** Aspose.PSD for Java 24.11  
**Författare:** Aspose

## Relaterade handledningar

- [Konvertera PSD till PNG och skapa vektormask Java – Vmsk‑resurs i PSD‑filer](/psd/java/advanced-psd-layer-features-effects/support-vmsk-resource-psd-files/)
- [Konvertera PSD till PNG med lager‑maskstöd med Aspose.PSD för Java](/psd/java/advanced-psd-layer-features-effects/support-layer-mask-psd-files/)
- [Lägg till lagerstöd för PSD‑filer](/psd/java/advanced-psd-layer-features-effects/add-layer-support-psd-files/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}