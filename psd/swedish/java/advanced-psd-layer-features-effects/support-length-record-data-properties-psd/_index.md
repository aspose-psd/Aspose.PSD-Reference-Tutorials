---
date: 2025-12-17
description: Lär dig hur du modifierar PSD-vektorgrafik genom att stödja längdpostdataegenskaper
  med Aspose.PSD för Java. Steg‑för‑steg‑guide med kodexempel.
linktitle: Support Length Record Data Properties in PSD - Java
second_title: Aspose.PSD Java API
title: Hur man modifierar PSD-vektorformer – Stöd för Length Record Data‑egenskaper
  i Java
url: /sv/java/advanced-psd-layer-features-effects/support-length-record-data-properties-psd/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Stöd Längdpostdataegenskaper i PSD - Java

## Introduktion
Om du behöver **modify PSD vector shapes** programmässigt, ger Aspose.PSD for Java‑biblioteket dig full kontroll över Photoshop‑filer direkt från din Java‑kod. I den här handledningen går vi igenom allt du behöver veta för att stödja length record data properties—ett viktigt steg när du vill redigera lager med vektorformer. I slutet kommer du kunna öppna en PSD, justera dess vektorformsegenskaper och spara den uppdaterade filen utan att lämna din IDE. Låt oss dyka ner!

## Snabba svar
- **What does “modify PSD vector shapes” mean?** Att justera geometrin, path‑operationerna eller andra egenskaper hos vektorbaserade lager i en PSD‑fil.  
- **Which library handles this?** Aspose.PSD for Java.  
- **Do I need a license?** En gratis provversion fungerar för utvärdering; en kommersiell licens krävs för produktion.  
- **How long does the implementation take?** Ungefär 10‑15 minuter för ett grundläggande skript som modifierar former.  
- **What are the main prerequisites?** Java JDK, Aspose.PSD for Java och en exempel‑PSD‑fil.

## Vad är “modify PSD vector shapes”?
Att modifiera PSD‑vektorformer innebär att ändra den underliggande vektor‑path‑datan—såsom length records och path‑operationer—så att den visuella framställningen av formerna uppdateras i enlighet med detta. Detta är särskilt användbart för automatiserade grafik‑pipelines, batch‑bearbetning eller anpassade designverktyg.

## Varför använda Aspose.PSD for Java för att modify PSD vector shapes?
- **No Photoshop required** – arbeta direkt med PSD‑filer på vilken server som helst.  
- **Rich API** – få åtkomst till lager, resurser och vektordata med starkt typade klasser.  
- **Cross‑platform** – kör på Windows, Linux eller macOS med vilken JDK som helst.  
- **Performance‑focused** – effektiv minneshantering och snabba sparoperationer.

## Förutsättningar
1. **Java Development Kit (JDK)** – ladda ner från [Oracle's website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) eller använd din föredragna paket‑hanterare.  
2. **Aspose.PSD for Java** – hämta den senaste JAR‑filen från [Aspose releases page](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse eller någon annan Java‑kompatibel editor.  
4. **A PSD file** – skapa en i Photoshop eller hämta en exempel‑PSD för att experimentera med.  
5. **Basic Java knowledge** – bekantskap med klasser, objekt och undantagshantering.

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

## Steg 1: Ställ in dina käll‑ och målmappar
Definiera var den ursprungliga PSD‑filen finns och var du vill spara den modifierade filen.

```java
String sourceDir = "Your Source Directory";
String outputDir = "Your Document Directory";
String inPsdFilePath = sourceDir + "PathOperationsShape.psd";
String outPsdFilePath = outputDir + "out_PathOperationsShape.psd";
```

## Steg 2: Ladda PSD‑filen
Använd `Image.load` för att öppna filen och kasta den till `PsdImage` för PSD‑specifika funktioner.

```java
PsdImage psdImage = (PsdImage) Image.load(inPsdFilePath);
```

## Steg 3: Hitta Vsms‑resursen i lagret
Vektorform‑data finns inuti en `VsmsResource`. Loopa igenom det andra lagrets resurser för att hitta den.

```java
VsmsResource resource = null;
for (LayerResource layerResource : psdImage.getLayers()[1].getResources()) {
    if (layerResource instanceof VsmsResource) {
        resource = (VsmsResource) layerResource;
        break;
    }
}
```

## Steg 4: Åtkomst till Length Records
Varje `LengthRecord` representerar en distinkt vektor‑path. Hämta de du avser att modifiera.

```java
LengthRecord lengthRecord0 = (LengthRecord) resource.getPaths()[2];
LengthRecord lengthRecord1 = (LengthRecord) resource.getPaths()[7];
LengthRecord lengthRecord2 = (LengthRecord) resource.getPaths()[11];
```

## Steg 5: Modifiera Path Operation‑egenskaper
Nu kan du **modify PSD vector shapes** genom att ändra deras `PathOperations`. Detta bestämmer hur former interagerar (t.ex. exkludering, korsning, subtraktion).

```java
lengthRecord0.setPathOperations(PathOperations.ExcludeOverlappingShapes);
lengthRecord1.setPathOperations(PathOperations.IntersectShapeAreas);
lengthRecord2.setPathOperations(PathOperations.SubtractFrontShape);
```

## Steg 6: Spara den modifierade PSD‑filen
Skriv dina ändringar till en ny fil.

```java
psdImage.save(outPsdFilePath);
```

## Steg 7: Rensa resurser
Avsluta `PsdImage` för att frigöra minne.

```java
psdImage.dispose();
```

## Vanliga fallgropar & tips
- **Null checks** – verifiera alltid att `resource` inte är `null` innan du får åtkomst till paths.  
- **Path index bounds** – säkerställ att de index du använder (`[2]`, `[7]`, `[11]`) finns för den specifika PSD‑fil du redigerar.  
- **License** – att köra utan en giltig licens kommer att bädda in ett vattenstämpel i den sparade PSD‑filen.  

## Slutsats
Du har nu ett komplett, end‑to‑end‑exempel på hur du **modify PSD vector shapes** genom att stödja length record data properties med Aspose.PSD for Java. Oavsett om du automatiserar asset‑pipelines eller bygger ett anpassat designverktyg, ger dessa API:er dig flexibiliteten att manipulera vektorlager utan manuellt Photoshop‑arbete. Utforska vidare genom att experimentera med andra `PathOperations` eller kombinera flera `LengthRecord`‑ändringar för komplexa former.

## Vanliga frågor
### What is Aspose.PSD for Java?
Aspose.PSD for Java är ett bibliotek som låter utvecklare manipulera och arbeta med Photoshop‑PSD‑filer programmässigt med Java.

### Can I use Aspose.PSD in a free project?
Ja, du kan prova biblioteket gratis med en provversion som finns på Aspose‑webbplatsen.

### What types of modifications can I make to PSD files?
Du kan manipulera lager, former, texter, path‑operationer och mycket mer i PSD‑filer.

### Is Aspose.PSD compatible with other programming languages?
Ja, Aspose erbjuder olika bibliotek för olika programmeringsspråk, inklusive .NET och Python.

### Where can I find the documentation for Aspose.PSD?
Du kan komma åt den fullständiga dokumentationen [here](https://reference.aspose.com/psd/java/).

## Vanligt förekommande frågor

**Q: How do I handle a PSD that contains no vector shape layers?**  
A: `VsmsResource` kommer att vara frånvarande, så `resource` förblir `null`. Lägg till en kontroll och hoppa över modifieringssteget eller informera användaren.

**Q: Can I change other properties like fill color or stroke width?**  
A: Ja, `LengthRecord` erbjuder ytterligare set‑metoder för fyllning, linjebredd och opacitet. Se API‑dokumentationen för fullständig information.

**Q: Is it possible to batch‑process multiple PSD files?**  
A: Absolut. Inkludera koden i en loop som itererar över en katalog med PSD‑filer och justera in‑ och ut‑sökvägarna varje gång.

**Q: Do I need to close streams manually when loading from a file path?**  
A: Metoden `Image.load` hanterar fil‑strömmar internt, men om du laddar från en `InputStream` bör du stänga den efter användning.

**Q: What version of Aspose.PSD is required for these APIs?**  
A: Klasserna `LengthRecord` och `PathOperations` finns tillgängliga sedan Aspose.PSD 20.10. Det rekommenderas att använda den senaste versionen.

---

**Last Updated:** 2025-12-17  
**Tested With:** Aspose.PSD for Java 24.11  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}