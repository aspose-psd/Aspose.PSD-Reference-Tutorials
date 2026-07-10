---
date: 2026-03-28
description: Lär dig hur du skapar ett nytt PSD‑lager och hanterar dess skapelsedatum
  och -tid med Aspose.PSD för Java. Denna steg‑för‑steg‑guide täcker laddning, läsning,
  validering och tillägg av lager.
linktitle: Create New PSD Layer and Manage Creation DateTime in Java
second_title: Aspose.PSD Java API
title: Skapa nytt PSD‑lager och hantera skapelsedatum och tid i Java
url: /sv/java/psd-image-modification-conversion/manage-layer-creation-datetime-psd/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Skapa nytt PSD‑lager och hantera skapelsedatum/tid i Java

## Introduktion
När du arbetar med Photoshop (PSD)-filer programatiskt, är förmågan att **create new PSD layer**-objekt och hålla reda på deras skapelsestämplar en verklig spelväxlare. Oavsett om du bygger ett versionskontrollsystem för designresurser, automatiserar batch‑redigeringar, eller bara behöver en revisionsspårning för samarbetsprojekt, så låter kunskapen om hur man läser och sätter lagrets skapelsedatum dig behålla full provenance för varje förändring. I den här handledningen går vi igenom hela processen med Aspose.PSD för Java — från att ladda en PSD, hämta ett lags skapelsedatum, validera det, till slut att lägga till ett helt nytt justeringslager.

## Snabba svar
- **Vilket bibliotek hanterar PSD‑filer i Java?** Aspose.PSD for Java  
- **Kan jag läsa ett lags skapelsedatum?** Ja, med `layer.getLayerCreationDateTime()`  
- **Är det möjligt att lägga till ett nytt justeringslager?** Absolut – `im.addLevelsAdjustmentLayer()` skapar ett  
- **Behöver jag en licens för produktionsanvändning?** En kommersiell licens krävs för icke‑testdistributioner  
- **Vilken Java‑version stöds?** JDK 8 eller senare  

## Vad betyder “create new PSD layer”?
Att skapa ett nytt PSD‑lager innebär att programatiskt infoga ett nytt lagerobjekt — såsom ett justerings-, text- eller pixellager — i ett befintligt PSD‑dokument. Denna operation låter dig utöka eller ändra bilden utan att manuellt öppna Photoshop.

## Varför hantera lagrets skapelsedatum/tid?
Att spåra skapelsedatum/tid för varje lager hjälper dig att:
- **Revidera ändringar** – veta exakt när ett lager lades till.  
- **Synkronisera resurser** mellan team genom att jämföra tidsstämplar.  
- **Automatisera arbetsflöden** som beror på tidsbaserade regler (t.ex. dölja lager äldre än en månad).

## Förutsättningar
Innan du dyker in, se till att du har följande redo:

1. **Java Development Kit (JDK)** – version 8 eller senare.  
2. **IDE** – IntelliJ IDEA, Eclipse, NetBeans, eller någon editor du föredrar.  
3. **Aspose.PSD for Java** – du kan [ladda ner den här](https://releases.aspose.com/psd/java/) för installation.  
4. **Basic Java knowledge** – om du är ny på Java, inga problem; koden är fullt kommenterad.

Har du allt? Fantastiskt! Låt oss hoppa in i den roliga koddelen.

## Importera paket
Först importerar du de Aspose.PSD‑klasser och Java‑verktyg du behöver. Dessa importeringar ger dig åtkomst till bildhantering, lagermanipulation och datumformatering.

```java
import com.aspose.psd.Image;
import com.aspose.psd.examples.Utils.Assert;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import java.text.DateFormat;
import java.text.SimpleDateFormat;
import java.util.Date;
```

## Steg 1: Ställ in din dokumentkatalog
Ange mappen som innehåller PSD‑filen du vill arbeta med. Ersätt platshållaren med den absoluta sökvägen på din maskin.

```java
String dataDir = "Your Document Directory";
```

## Steg 2: Ladda PSD‑filen
Skapa en `PsdImage`‑instans genom att ladda målfilen. Detta objekt är ingångspunkten för alla lageroperationer.

```java
String sourceName = dataDir + "OneLayer.psd";
PsdImage im = (PsdImage) Image.load(sourceName);
```

## Steg 3: Åtkomst till lagret och dess skapelsedatum
Hämta det första lagret (index 0) och hämta dess skapelsestämpel. Detta är datumet du senare kommer att jämföra eller logga.

```java
Layer layer = im.getLayers()[0];
Date creationDateTime = layer.getLayerCreationDateTime();
```

## Steg 4: Formatera skapelsedatumet
Konvertera det råa `Date`‑objektet till en mänskligt läsbar sträng. Justera mönstret om du föredrar ett annat format.

```java
DateFormat dateFormat = new SimpleDateFormat("yyyy/MM/dd HH:mm:ss");
```

## Steg 5: Validera skapelsedatumet
För demonstration jämför vi det hämtade datumet med ett förväntat värde. I verkliga projekt kan du jämföra mot en databaspost eller en konfigurationsfil.

```java
Date expectedDateTime = new Date("2018/7/17 8:57:24");
Assert.areEqual(expectedDateTime, creationDateTime);
```

## Steg 6: Skapa ett nytt lager
Nu skapar vi faktiskt **create new PSD layer**‑objekt. Här lägger vi till ett Levels‑justeringslager, vilket låter dig justera tonområden utan att ändra de ursprungliga pixlarna.

```java
Date now = new Date();
Layer createdLayer = im.addLevelsAdjustmentLayer();
```

> **Proffstips:** Variabeln `now` fångar ögonblicket då du lägger till lagret, vilket du senare kan lagra som metadata om du behöver en anpassad tidsstämpel.

## Vanliga problem och lösningar
| Problem | Varför det händer | Lösning |
|-------|----------------|-----|
| `NullPointerException` on `layer.getLayerCreationDateTime()` | PSD‑filen har inga lager eller lagerindexet är utanför intervallet. | Verifiera `im.getLayers().length > 0` innan åtkomst. |
| Datumavvikelse vid validering | `Date`‑konstruktorn tolkar strängar på ett lokalanpassat sätt. | Använd `SimpleDateFormat.parse("2018/07/17 08:57:24")` för pålitlig parsning. |
| Nytt lager syns inte i Photoshop | Justeringslagret kan vara dolt som standard. | Anropa `createdLayer.setVisible(true);` efter skapandet. |

## Slutsats
Du vet nu hur du **create new PSD layer**‑objekt, läser deras skapelsestämplar, validerar dessa stämplar och lägger till justeringslager — allt med Aspose.PSD för Java. Denna funktion öppnar dörren till sofistikerad automatisering, revisionsspår och samarbetsarbetsflöden i vilken Java‑baserad bildbehandlingspipeline som helst.

Om du gillade den här handledningen, utforska andra Aspose.PSD‑funktioner som att slå ihop lager, applicera filter eller exportera till olika format. Möjligheterna är oändliga!

## Vanliga frågor
### Vad är Aspose.PSD?  
Aspose.PSD är ett kraftfullt bibliotek för att programatiskt arbeta med Photoshop (PSD)-filer.

### Kan jag använda Aspose.PSD gratis?  
Ja! Du kan börja med en gratis provversion tillgänglig [här](https://releases.aspose.com/).

### Behöver jag köpa en licens för långsiktig användning?  
Ja, du kan skaffa en licens [här](https://purchase.aspose.com/buy) när du är redo.

### Var kan jag hitta mer information om Aspose.PSD?  
Du kan kolla [dokumentationen](https://reference.aspose.com/psd/java/) för detaljerade guider och API‑referenser.

### Hur kan jag få support om jag stöter på problem med Aspose.PSD?  
Känn dig fri att besöka [supportforumet](https://forum.aspose.com/c/psd/34) för gemenskapsassistans.

---

**Senast uppdaterad:** 2026-03-28  
**Testad med:** Aspose.PSD for Java 24.10  
**Författare:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}