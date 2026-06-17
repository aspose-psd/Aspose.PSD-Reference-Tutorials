---
date: 2026-02-20
description: Lär dig hur du stöder length‑record‑egenskaper och batchbearbetar PSD‑filer
  med Aspose.PSD för Java. Steg‑för‑steg‑guide med kodexempel.
linktitle: Support Length Record Data Properties in PSD - Java
second_title: Aspose.PSD Java API
title: Stöd för Length Record‑egenskaper – Modifiera PSD‑vektorshapes (Java)
url: /sv/java/advanced-psd-layer-features-effects/support-length-record-data-properties-psd/
weight: 14
---

 sure code block placeholders remain unchanged.

Let's craft.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Stöd för LengthRecord‑egenskaper – Modifiera PSD‑vektorshapes (Java)

## Introduktion
Om du behöver **modifiera PSD‑vektorshapes** programatiskt, ger Aspose.PSD för Java‑biblioteket dig full kontroll över Photoshop‑filer direkt från din Java‑kod. I den här handledningen går vi igenom allt du behöver veta för att **stöda LengthRecord‑egenskaper** – ett nödvändigt steg när du vill redigera lager med vektorformer. När du är klar kommer du kunna öppna en PSD, justera dess vektor‑formegenskaper och spara den uppdaterade filen utan att lämna din IDE. Låt oss dyka ner!

## Snabba svar
- **Vad betyder “modifiera PSD‑vektorshapes”?** Att justera geometri, banoperationer eller andra egenskaper för vektorbaserade lager i en PSD‑fil.  
- **Vilket bibliotek hanterar detta?** Aspose.PSD för Java.  
- **Behöver jag en licens?** En gratis provversion fungerar för utvärdering; en kommersiell licens krävs för produktion.  
- **Hur lång tid tar implementeringen?** Ungefär 10‑15 minuter för ett grundläggande skript som modifierar former.  
- **Vilka är huvudförutsättningarna?** Java JDK, Aspose.PSD för Java och en exempel‑PSD‑fil.

## Vad betyder “stöda LengthRecord‑egenskaper”?
Att stöda LengthRecord‑egenskaper innebär att komma åt och uppdatera `LengthRecord`‑objekten som beskriver varje vektor‑bana i en PSD. Genom att ändra dessa poster kan du kontrollera hur former kombineras, skär varandra eller subtraheras.

## Varför använda Aspose.PSD för Java för att stöda LengthRecord‑egenskaper?
- **Ingen Photoshop behövs** – arbeta direkt med PSD‑filer på vilken server som helst.  
- **Rik API** – få åtkomst till lager, resurser och vektordata med starkt typade klasser.  
- **Plattformsoberoende** – kör på Windows, Linux eller macOS med vilken JDK som helst.  
- **Prestandafokuserad** – effektiv minneshantering och snabba sparoperationer.  

## Förutsättningar
1. **Java Development Kit (JDK)** – ladda ner från [Oracle's website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) eller använd din föredragna pakethanterare.  
2. **Aspose.PSD för Java** – hämta den senaste JAR‑filen från [Aspose releases page](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse eller någon annan Java‑kompatibel editor.  
4. **En PSD‑fil** – skapa en i Photoshop eller hämta en exempel‑PSD för experiment.  
5. **Grundläggande Java‑kunskaper** – bekantskap med klasser, objekt och undantagshantering.

## Importera paket
Först importerar du de klasser du behöver för att arbeta med PSD‑filer och vektorform‑resurser.

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.LayerResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.VsmsResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.LengthRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.PathOperations;
```

## Steg 1: Ange käll‑ och målmappar
Definiera var den ursprungliga PSD‑filen finns och var du vill spara den modifierade filen.

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
Vektorform‑data finns i en `VsmsResource`. Loopa igenom det andra lagrets resurser för att hitta den.

```java
VsmsResource resource = null;
for (LayerResource layerResource : psdImage.getLayers()[1].getResources()) {
    if (layerResource instanceof VsmsResource) {
        resource = (VsmsResource) layerResource;
        break;
    }
}
```

## Steg 4: Kom åt Length‑poster
Varje `LengthRecord` representerar en distinkt vektor‑bana. Hämta de poster du avser att modifiera.

```java
LengthRecord lengthRecord0 = (LengthRecord) resource.getPaths()[2];
LengthRecord lengthRecord1 = (LengthRecord) resource.getPaths()[7];
LengthRecord lengthRecord2 = (LengthRecord) resource.getPaths()[11];
```

## Steg 5: Modifiera ban‑operations‑egenskaper
Nu kan du **modifiera PSD‑vektorshapes** genom att ändra deras `PathOperations`. Detta bestämmer hur former interagerar (t.ex. exkludering, skärning, subtraktion).

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

## Steg 7: Rensa upp resurser
Dispose‑a `PsdImage` för att frigöra minne.

```java
psdImage.dispose();
```

## Hur man batch‑processar PSD‑filer med stöda LengthRecord‑egenskaper
Om du behöver applicera samma vektor‑formjusteringar på många PSD‑filer, omslut koden ovan i en loop som itererar över en katalog med filer. Uppdatera `inPsdFilePath` och `outPsdFilePath` för varje iteration, så kan du **batch‑processa PSD‑filer** effektivt.

## Vanliga fallgropar & tips
- **Null‑kontroller** – verifiera alltid att `resource` inte är `null` innan du kommer åt banor.  
- **Index‑gränser för banor** – säkerställ att de index du använder (`[2]`, `[7]`, `[11]`) finns i den specifika PSD‑filen du redigerar.  
- **Licens** – att köra utan en giltig licens kommer att lägga till ett vattenstämpel i den sparade PSD‑filen.  

## Slutsats
Du har nu ett komplett, end‑to‑end‑exempel på hur du **modifierar PSD‑vektorshapes** genom att stöda LengthRecord‑egenskaper med Aspose.PSD för Java. Oavsett om du automatiserar asset‑pipelines eller bygger ett anpassat designverktyg, ger dessa API:er dig flexibiliteten att manipulera vektorlager utan manuellt Photoshop‑arbete. Utforska vidare genom att experimentera med andra `PathOperations` eller kombinera flera `LengthRecord`‑redigeringar för komplexa former.

## Vanliga frågor

**Q: Hur hanterar jag en PSD som saknar vektorform‑lager?**  
A: `VsmsResource` kommer att vara frånvarande, så `resource` förblir `null`. Lägg till en kontroll och hoppa över modifieringssteget eller informera användaren.

**Q: Kan jag ändra andra egenskaper som fyllningsfärg eller linjebredd?**  
A: Ja, `LengthRecord` erbjuder ytterligare set‑metoder för fyllning, linje och opacitet. Se API‑dokumentationen för fullständig information.

**Q: Är det möjligt att batch‑processa flera PSD‑filer?**  
A: Absolut. Omslut koden i en loop som itererar över en katalog med PSD‑filer och justera in‑ och ut‑sökvägarna varje gång.

**Q: Måste jag stänga strömmar manuellt när jag läser från en filsökväg?**  
A: Metoden `Image.load` hanterar filströmmar internt, men om du laddar från ett `InputStream` bör du komma ihåg att stänga det efter användning.

**Q: Vilken version av Aspose.PSD krävs för dessa API:er?**  
A: Klasserna `LengthRecord` och `PathOperations` finns tillgängliga sedan Aspose.PSD 20.10. Det rekommenderas att använda den senaste versionen.

---

**Senast uppdaterad:** 2026-02-20  
**Testad med:** Aspose.PSD för Java 24.11  
**Författare:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}