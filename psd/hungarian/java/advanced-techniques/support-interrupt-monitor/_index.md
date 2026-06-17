---
date: 2026-06-08
description: Ismerje meg, hogyan menthet PSD-t PNG-ként az Aspose.PSD for Java használatával,
  és szükség esetén megszakíthatja a konverziót. Hatékonyan kezelje a képfeldolgozási
  munkafolyamatot.
keywords:
- save psd as png
- how to interrupt conversion
- psd to png conversion
- manage image workflow
linktitle: Támogatás az Interrupt Monitor-hoz
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
title: Hogyan menthet PSD-t PNG-ként az Interrupt Monitor segítségével az Aspose.PSD
  for Java-ban
url: /hu/java/advanced-techniques/support-interrupt-monitor/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD mentése PNG-ként az Interrupt Monitor segítségével az Aspose.PSD for Java-ban

## Bevezetés

Ha **PSD-t PNG-ként** szeretnél menteni, miközben teljes ellenőrzést szeretnél a hosszú ideig futó konverziók felett, az Aspose.PSD for Java Interrupt Monitor pontosan ezt biztosítja. Ebben az útmutatóban végigvezetünk a monitor beállításán, egy PSD fájl PNG‑re konvertálásán, és a művelet biztonságos megszakításán, ha szükséges. Emellett megmutatjuk, hogyan illeszkedik ez egy tipikus képfeldolgozási munkafolyamatba, és miért elengedhetetlen a megbízható alkalmazások számára.

## Gyors válaszok
- **Meg tudom szakítani a PSD‑t PNG‑re konvertálást?** Igen, használja a `InterruptMonitor`‑t a folyamat igény szerinti leállításához.  
- **Melyik metódus ment PSD‑t PNG‑ként?** Hívja a `save(outputPath, new PngOptions())`‑t.  
- **Szükségem van licencre a termeléshez?** Kereskedelmi licenc szükséges; ingyenes próba elérhető.  
- **Mely Java verzió támogatott?** A Java 8 és újabb verziók teljes mértékben támogatottak.  
- **A könyvtár szálbiztos?** A konverziók külön szálakon futtathatók; a monitor biztonságosan kezeli a megszakításokat.

## Előfeltételek

Mielőtt belemerülnél az Interrupt Monitor használatának részleteibe, győződj meg róla, hogy a következő előfeltételek rendelkezésre állnak:

- **Java fejlesztői környezet:** Állíts be egy Java fejlesztői környezetet a rendszereden.  
- **Aspose.PSD könyvtár:** Szerezd be az Aspose.PSD for Java könyvtárat. Letöltheted [itt](https://releases.aspose.com/psd/java/). A fő Aspose oldalt is meglátogathatod [itt](https://releases.aspose.com/).  
- **Dokumentum könyvtár:** Legyen egy kijelölt könyvtár a PSD dokumentumaid számára.

## Csomagok importálása

Kezdd a szükséges csomagok importálásával a Java projektedbe. Ez biztosítja, hogy hozzáférj az Aspose.PSD funkciókhoz.

```java
import com.aspose.psd.ImageOptionsBase;

import static com.aspose.psd.examples.Utils.Utils.getDateTime;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.multithreading.InterruptMonitor;
import com.aspose.psd.system.Threading.ThreadStart;
import java.io.File;
```

Most bontsuk le a példakódot egy lépésről‑lépésre útmutatóba, amely bemutatja az Interrupt Monitor beépítését az Aspose.PSD for Java projektedbe.

## Hogyan menthetünk PSD-t PNG‑ként az Interrupt Monitor használatával?

`PsdImage` egy memóriába betöltött PSD dokumentumot képvisel.  
`SaveImageWorker` egy külön szálban végzi a képkonverziót.  

Töltsd be a PSD fájlt a `new PsdImage("source.psd")` paranccsal, csatolj egy `InterruptMonitor`‑t a `SaveImageWorker`‑hez, és hívd a `save("output.png", new PngOptions())`‑t. A monitor figyeli a leállítási kérést, és tisztán megszakítja a konverziót, ezáltal néhány ezredmásodperc alatt visszaadja az irányítást az alkalmazásodnak.

### 1. lépés: Állítsd be a dokumentum könyvtárát

```java
String dataDir = "Your Document Directory";
```

Győződj meg róla, hogy a „Your Document Directory” helyett a tényleges útvonalat adod meg, ahol a PSD dokumentumaid tárolva vannak.

### 2. lépés: Képbeállítások és kimeneti útvonal meghatározása

```java
ImageOptionsBase saveOptions = new PngOptions();
String source = dataDir + "big2.psb";
String output = dataDir + "big_out.png";
```

Add meg a képbeállításokat, a forrás PSD fájlt, és a kívánt kimeneti útvonalat a konvertált képhez.

### 3. lépés: Interrupt Monitor és SaveImageWorker inicializálása

Az `InterruptMonitor` osztály figyeli a futó konverziót, és megszakíthatja, amikor a `requestInterrupt()` hívásra kerül.  

```java
InterruptMonitor monitor = new InterruptMonitor();
SaveImageWorker worker = new SaveImageWorker(source, output, saveOptions, monitor);
```

Hozz létre `InterruptMonitor` és `SaveImageWorker` példányokat, összekapcsolva a monitort a képkonverziós munkával.

### 4. lépés: Képkonverziós szál indítása

```java
Thread thread = new Thread(worker.ThreadProc());
try {
    thread.start();
    // Add a timeout to allow for potential interruption
    Thread.sleep(3000);
```

Indíts egy új szálat a képkonverziós folyamat számára, és adj meg egy időkorlátot a megszakítás előrejelzéséhez.

### 5. lépés: A folyamat megszakítása

`monitor.requestInterrupt()` hívása jelzi a monitor számára, hogy megszakítsa a folyamatban lévő konverziót.  

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

Használd az `InterruptMonitor`‑t a képkonverziós folyamat megszakításához, és várd meg, amíg a megszakítás befejeződik. Végül takaríts fel a kimeneti fájl törlésével.

## Miért használjuk az Interrupt Monitor‑t PSD‑t PNG‑re konvertáláskor?

Az Aspose.PSD **30+ kimeneti formátumot** támogat, beleértve a PNG, JPEG, BMP és TIFF formátumokat, és **akár 500 MB‑os fájlokat** képes feldolgozni anélkül, hogy a teljes dokumentumot a memóriába töltené. Az interrupt monitor hozzáadásával csökkented a CPU pazarlást és javítod a válaszkészséget a kötegelt feldolgozási csővezetékekben, különösen, ha egy **konverzió meghaladja** a várt **idő**korlátot.

## Gyakori problémák és megoldások

- **A konverzió végtelenül lefagy:** Győződj meg róla, hogy a monitor **a `save` hívása előtt** van csatolva.  
- **A kimeneti fájl megszakítás után sérült:** A monitor tisztán megszakítja; azonban mindig ellenőrizd, hogy a fájl létezik-e, mielőtt használod.  
- **Szálbiztonsági aggodalmak:** Futtasd minden konverziót saját szálban; a monitor csak a hozzá tartozó munkát érinti.

## Gyakran ismételt kérdések

**Q1: Mi az az Interrupt Monitor az Aspose.PSD for Java-ban?**  
A: Az Interrupt Monitor lehetővé teszi a fejlesztők számára, hogy szüneteltessék vagy megszakítsák a hosszú ideig futó képkonverziókat, valós idejű kontrollt biztosítva az erőforrás-felhasználás felett.

**Q2: Hogyan szerezhetem be az Aspose.PSD könyvtárat Java-hoz?**  
A: Letöltheted az Aspose.PSD for Java könyvtárat [itt](https://releases.aspose.com/psd/java/).

**Q3: Elérhető ingyenes próba az Aspose.PSD for Java-hoz?**  
A: Igen, egy ingyenes próbát felfedezhetsz az Aspose.PSD [itt](https://releases.aspose.com/).

**Q4: Hol találhatok támogatást az Aspose.PSD for Java-hoz?**  
A: Látogasd meg az Aspose.PSD for Java támogatási fórumot [itt](https://forum.aspose.com/c/psd/34).

**Q5: Hogyan vásárolhatok licencet az Aspose.PSD for Java-hoz?**  
A: Licencet vásárolhatsz az Aspose.PSD for Java-hoz [itt](https://purchase.aspose.com/buy).

**Q6: Tudok több PSD fájlt párhuzamosan PNG‑re konvertálni?**  
A: Igen, indíts egy külön szálat minden fájlhoz, és csatolj egy egyedi `InterruptMonitor`‑t minden konverziós munkához.

**Q7: Kezeli a könyvtár a színprofilokat a PSD‑t PNG‑re konvertálás során?**  
A: Teljesen; az Aspose.PSD megőrzi a beágyazott ICC profilokat, és automatikusan alkalmazza őket a kimeneti PNG-re.

**Utoljára frissítve:** 2026-06-08  
**Tesztelve a következővel:** Aspose.PSD 23.12 for Java  
**Szerző:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Kapcsolódó útmutatók

- [PSD mentése PNG‑ként és Rendering Drop Shadow alkalmazása az Aspose.PSD for Java-ban](/psd/java/advanced-image-manipulation/rendering-drop-shadow/)
- [PSD exportálása PNG‑re és új reguláris réteg hozzáadása az Aspose.PSD for Java használatával](/psd/java/advanced-image-effects/add-new-regular-layer/)
- [Interrupt Monitor támogatása PSD fájlokban – Java](/psd/java/psd-layer-management-effects/support-interrupt-monitor-psd-files/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}