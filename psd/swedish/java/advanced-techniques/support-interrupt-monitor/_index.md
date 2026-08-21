---
date: 2026-06-08
description: Lär dig hur du sparar PSD som PNG med Aspose.PSD för Java och avbryter
  konverteringen vid behov. Hantera bildarbetsflödet effektivt.
keywords:
- save psd as png
- how to interrupt conversion
- psd to png conversion
- manage image workflow
linktitle: Stöd för Interrupt Monitor
schemas:
- author: Aspose
  dateModified: '2026-06-08'
  description: Learn how to save PSD as PNG using Aspose.PSD for Java and interrupt
    conversion when needed. Manage image workflow efficiently.
  headline: How to Save PSD as PNG with Interrupt Monitor in Aspose.PSD for Java
  type: TechArticle
- description: Learn how to save PSD as PNG using Aspose.PSD for Java and interrupt
    conversion when needed. Manage image workflow efficiently.
  name: How to Save PSD as PNG with Interrupt Monitor in Aspose.PSD for Java
  steps:
  - name: Set Your Document Directory
    text: Ensure to replace “Your Document Directory” with the actual path where your
      PSD documents are stored.
  - name: Define Image Options and Output Path
    text: Specify the image options, source PSD file, and the desired output path
      for the converted image.
  - name: Initialize Interrupt Monitor and SaveImageWorker
    text: The `InterruptMonitor` class watches a running conversion and can interrupt
      it when `requestInterrupt()` is called. Create instances of `InterruptMonitor`
      and `SaveImageWorker`, linking the monitor to the image conversion worker.
  - name: Start Image Conversion Thread
    text: Initiate a new thread for the image conversion process and introduce a timeout
      period to anticipate interruption.
  - name: Interrupt the Process
    text: Calling `monitor.requestInterrupt()` signals the monitor to abort the ongoing
      conversion. Interrupt the image conversion process using the `InterruptMonitor`
      and wait for the interruption to complete. Finally, clean up by deleting the
      output file.
  type: HowTo
- questions:
  - answer: Yes, use `InterruptMonitor` to stop the process on demand.
    question: Can I interrupt a PSD‑to‑PNG conversion?
  - answer: Call `save(outputPath, new PngOptions())`.
    question: Which method saves a PSD as PNG?
  - answer: A commercial license is required; a free trial is available.
    question: Do I need a license for production?
  - answer: Java 8 and later are fully supported.
    question: What Java version is supported?
  - answer: Conversions can run in separate threads; the monitor handles interruptions
      safely.
    question: Is the library thread‑safe?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Hur man sparar PSD som PNG med Interrupt Monitor i Aspose.PSD för Java
url: /sv/java/advanced-techniques/support-interrupt-monitor/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Spara PSD som PNG med Interrupt Monitor i Aspose.PSD för Java

## Introduktion

Om du behöver **spara PSD som PNG** samtidigt som du behåller full kontroll över långvariga konverteringar, ger Aspose.PSD för Javas Interrupt Monitor dig precis det. I den här handledningen går vi igenom hur du ställer in monitorn, konverterar en PSD‑fil till PNG och säkert avbryter operationen när det behövs. Du får också se hur detta passar in i ett typiskt bildbehandlingsflöde och varför det är ett måste för robusta applikationer.

## Snabba svar
- **Kan jag avbryta en PSD‑till‑PNG-konvertering?** Ja, använd `InterruptMonitor` för att stoppa processen på begäran.  
- **Vilken metod sparar en PSD som PNG?** Anropa `save(outputPath, new PngOptions())`.  
- **Behöver jag en licens för produktion?** En kommersiell licens krävs; en gratis provversion finns tillgänglig.  
- **Vilken Java‑version stöds?** Java 8 och senare stöds fullt ut.  
- **Är biblioteket trådsäkert?** Konverteringar kan köras i separata trådar; monitorn hanterar avbrott på ett säkert sätt.

## Förutsättningar

Innan du dyker ner i detaljerna kring användning av Interrupt Monitor, se till att du har följande förutsättningar på plats:

- **Java‑utvecklingsmiljö:** Ställ in en Java‑utvecklingsmiljö på ditt system.  
- **Aspose.PSD‑bibliotek:** Skaffa Aspose.PSD för Java‑biblioteket. Du kan ladda ner det [här](https://releases.aspose.com/psd/java/). Du kan också besöka Aspose‑huvudsidan [här](https://releases.aspose.com/).  
- **Dokumentkatalog:** Ha en avsedd katalog för dina PSD‑dokument.

## Importera paket

Börja med att importera de nödvändiga paketen i ditt Java‑projekt. Detta säkerställer att du har åtkomst till Aspose.PSD‑funktionerna.

```java
import com.aspose.psd.ImageOptionsBase;

import static com.aspose.psd.examples.Utils.Utils.getDateTime;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.multithreading.InterruptMonitor;
import com.aspose.psd.system.Threading.ThreadStart;
import java.io.File;
```

Nu ska vi bryta ner exempel­koden i en steg‑för‑steg‑guide för att införliva Interrupt Monitor i ditt Aspose.PSD för Java‑projekt.

## Hur man sparar PSD som PNG med Interrupt Monitor?

`PsdImage` representerar ett PSD‑dokument som laddats in i minnet.  
`SaveImageWorker` utför bildkonverteringen i en separat tråd.  

Läs in din PSD‑fil med `new PsdImage("source.psd")`, fäst en `InterruptMonitor` på `SaveImageWorker` och anropa `save("output.png", new PngOptions())`. Monitorn övervakar en avbrytningsbegäran och avbryter konverteringen på ett rent sätt, vilket återlämnar kontrollen till din applikation inom några millisekunder.

### Steg 1: Ange din dokumentkatalog

```java
String dataDir = "Your Document Directory";
```

Se till att ersätta “Your Document Directory” med den faktiska sökvägen där dina PSD‑dokument lagras.

### Steg 2: Definiera bildalternativ och utsökväg

```java
ImageOptionsBase saveOptions = new PngOptions();
String source = dataDir + "big2.psb";
String output = dataDir + "big_out.png";
```

Ange bildalternativen, käll‑PSD‑filen och önskad utsökväg för den konverterade bilden.

### Steg 3: Initiera Interrupt Monitor och SaveImageWorker

`InterruptMonitor`‑klassen övervakar en pågående konvertering och kan avbryta den när `requestInterrupt()` anropas.

```java
InterruptMonitor monitor = new InterruptMonitor();
SaveImageWorker worker = new SaveImageWorker(source, output, saveOptions, monitor);
```

Skapa instanser av `InterruptMonitor` och `SaveImageWorker`, och länka monitorn till bildkonverterings‑arbetaren.

### Steg 4: Starta bildkonverteringstråden

```java
Thread thread = new Thread(worker.ThreadProc());
try {
    thread.start();
    // Add a timeout to allow for potential interruption
    Thread.sleep(3000);
```

Initiera en ny tråd för bildkonverteringsprocessen och inför en timeout‑period för att förutse avbrott.

### Steg 5: Avbryt processen

Att anropa `monitor.requestInterrupt()` signalerar monitorn att avbryta den pågående konverteringen.  

```java
    // Interrupt the process
    monitor.interrupt();
    System.out.println("Interrupting the save thread #" + thread.getId() + " at " + getDateTime().toString());

    // Wait for interruption...
    thread.join();
} finally {
    // Delete the output file if it exists
    File f = new File(output);
    if (f.exists()) {
        f.delete();
    }
}
```

Avbryt bildkonverteringsprocessen med `InterruptMonitor` och vänta på att avbrottet slutförs. Till sist, rensa upp genom att ta bort utskriftsfilen.

## Varför använda Interrupt Monitor för PSD‑till‑PNG‑konvertering?

Aspose.PSD stöder **30+ output‑format**, inklusive PNG, JPEG, BMP och TIFF, och kan bearbeta filer upp till **500 MB** utan att ladda hela dokumentet i minnet. Genom att lägga till en interrupt‑monitor minskar du CPU‑slöseri och förbättrar svarstiden i batch‑behandlings‑pipelines, särskilt när en konvertering överskrider förväntade tidsgränser.

## Vanliga problem och lösningar

- **Konverteringen hänger oändligt:** Se till att monitorn är fäst **innan** du anropar `save`.  
- **Utskriftsfilen är korrupt efter avbrott:** Monitorn avbryter rent; dock bör du alltid kontrollera om filen finns innan du använder den.  
- **Trådsäkerhetsproblem:** Kör varje konvertering i en egen tråd; monitorn påverkar endast sin associerade arbetare.

## Vanliga frågor

**Q1: Vad är en Interrupt Monitor i Aspose.PSD för Java?**  
A: Interrupt Monitor låter utvecklare pausa eller avbryta långvariga bildkonverteringar, vilket ger realtidskontroll över resursanvändning.

**Q2: Hur kan jag skaffa Aspose.PSD‑biblioteket för Java?**  
A: Du kan ladda ner Aspose.PSD för Java‑biblioteket [här](https://releases.aspose.com/psd/java/).

**Q3: Finns det en gratis provversion av Aspose.PSD för Java?**  
A: Ja, du kan prova en gratis version av Aspose.PSD [här](https://releases.aspose.com/).

**Q4: Var kan jag hitta support för Aspose.PSD för Java?**  
A: Besök supportforumet för Aspose.PSD för Java [här](https://forum.aspose.com/c/psd/34).

**Q5: Hur kan jag köpa en licens för Aspose.PSD för Java?**  
A: Du kan köpa en licens för Aspose.PSD för Java [här](https://purchase.aspose.com/buy).

**Q6: Kan jag konvertera flera PSD‑filer till PNG parallellt?**  
A: Ja, starta en separat tråd för varje fil och fäst en individuell `InterruptMonitor` till varje konverterings‑arbetare.

**Q7: Hanterar biblioteket färgprofiler under PSD‑till‑PNG‑konvertering?**  
A: Absolut; Aspose.PSD bevarar inbäddade ICC‑profiler och applicerar dem automatiskt på den resulterande PNG‑filen.

---

**Senast uppdaterad:** 2026-06-08  
**Testad med:** Aspose.PSD 23.12 för Java  
**Författare:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Relaterade handledningar

- [Spara PSD som PNG och applicera Rendering Drop Shadow i Aspose.PSD för Java](/psd/java/advanced-image-manipulation/rendering-drop-shadow/)
- [Exportera PSD till PNG & lägg till ett nytt reguljärt lager med Aspose.PSD för Java](/psd/java/advanced-image-effects/add-new-regular-layer/)
- [Stöd för Interrupt Monitor i PSD‑filer – Java](/psd/java/psd-layer-management-effects/support-interrupt-monitor-psd-files/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}