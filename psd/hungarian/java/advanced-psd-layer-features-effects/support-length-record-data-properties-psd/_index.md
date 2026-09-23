---
date: 2026-09-23
description: Ismerje meg, hogyan módosíthatja a PSD vektoralakzatokat és batch process
  PSD fájlokat az Aspose.PSD for Java használatával. Részletes lépések, tippek és
  code placeholders egy teljes megoldáshoz.
keywords:
- modify psd vector shapes
- batch process psd files
- Aspose.PSD Java
- vector shape editing
lastmod: 2026-09-23
linktitle: Hossz Rekord Adat Tulajdonságok támogatása a PSD-ben – Java
og_description: Ismerje meg, hogyan módosíthatja a PSD vektoralakzatokat és batch
  process PSD fájlokat az Aspose.PSD for Java használatával. Lépésről‑lépésre útmutató
  code placeholders és szakértői tippek segítségével.
og_image_alt: Guide showing how to edit vector shapes in PSD files using Aspose.PSD
  for Java
og_title: PSD vektoralakzatok módosítása az Aspose.PSD for Java segítségével
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
title: PSD vektoralakzatok módosítása az Aspose.PSD for Java segítségével
url: /hu/java/advanced-psd-layer-features-effects/support-length-record-data-properties-psd/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD vektor alakzatok módosítása az Aspose.PSD for Java segítségével

## Bevezetés
Ha programozott módon **PSD vektor alakzatokat** kell módosítania, az Aspose.PSD for Java teljes irányítást biztosít a Photoshop fájlok felett közvetlenül a Java kódjából. Ez az útmutató végigvezet a length record tulajdonságok támogatásán – ami elengedhetetlen lépés a vektor alakzat rétegek szerkesztésekor. A végére képes lesz PSD-t megnyitni, módosítani a vektor alakzat adatait, és elmenteni a frissített fájlt anélkül, hogy a Photoshopot elindítaná.

## Gyors válaszok
- **Mit jelent a “modify PSD vector shapes”?** A geometria, útvonal műveletek vagy egyéb attribútumok módosítása a PSD-fájlban lévő vektor‑alapú rétegeknél.  
- **Melyik könyvtár kezeli ezt?** Aspose.PSD for Java.  
- **Szükségem van licencre?** Egy ingyenes próba a kiértékeléshez megfelelő; a termeléshez kereskedelmi licenc szükséges.  
- **Mennyi időt vesz igénybe a megvalósítás?** Körülbelül 10‑15 perc egy alap alakzat‑módosító szkripthez.  
- **Mik a fő előfeltételek?** Java JDK, Aspose.PSD for Java, és egy minta PSD fájl.

## Mi az a “support length record properties”?
A length record tulajdonságok támogatása azt jelenti, hogy hozzáférünk és frissítjük a `LengthRecord` objektumokat, amelyek a PSD-n belüli egyes vektor útvonalakat leírják. Ezek a rekordok információkat tárolnak, például az útvonal hosszát, típusát és azt, hogy hogyan kapcsolódik más útvonalakhoz. Ezek módosítása lehetővé teszi a formák kombinálásának, metszésének vagy kivonásának irányítását, ezáltal precíz vektor szerkesztést biztosít.

## Miért használja az Aspose.PSD for Java-t a length record tulajdonságok támogatásához?
Töltse be a PSD-jét, szerkessze a vektor adatokat, és mentse – mindezt Photoshop nélkül. Az Aspose.PSD több száz oldalas PSD-ket kevesebb, mint 2 másodperc alatt dolgoz fel egy tipikus szerveren, több mint 150 osztályt kínál (köztük 30+ vektorral kapcsolatos típust), és Windows, Linux vagy macOS rendszereken fut bármely JDK 11+ verzióval. Ez a teljesítmény‑központú könyvtár megszünteti a költséges asztali szoftverek szükségességét.

## Előfeltételek
1. **Java Development Kit (JDK)** – töltse le a [Oracle weboldaláról](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html), vagy használja a kedvenc csomagkezelőjét.  
2. **Aspose.PSD for Java** – szerezze be a legújabb JAR-t az [Aspose kiadási oldalról](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse vagy bármely Java‑kompatibilis szerkesztő.  
4. **PSD fájl** – hozzon létre egyet a Photoshopban, vagy vegyen egy minta PSD-t a kísérletezéshez.  
5. **Alap Java ismeretek** – osztályok, objektumok és kivételkezelés ismerete.

## Importálás csomagok
Az importálási utasítások a fő Aspose.PSD osztályokat hozzák a láthatóságba, például a `PsdImage`, `VsmsResource` és `LengthRecord` osztályokat.

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.LayerResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.VsmsResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.LengthRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.PathOperations;
```

## 1. lépés: Állítsa be a forrás- és kimeneti könyvtárakat
Határozza meg, hol található az eredeti PSD, és hová lesz írva a módosított fájl.

```java
String sourceDir = "Your Source Directory";
String outputDir = "Your Document Directory";
String inPsdFilePath = sourceDir + "PathOperationsShape.psd";
String outPsdFilePath = outputDir + "out_PathOperationsShape.psd";
```

## 2. lépés: Töltse be a PSD fájlt
Használja az `Image.load` metódust a fájl megnyitásához, és alakítsa át `PsdImage` típusra a PSD‑specifikus funkciókhoz.

```java
PsdImage psdImage = (PsdImage) Image.load(inPsdFilePath);
```

## 3. lépés: Keresse meg a Vsms erőforrást a rétegben
A `VsmsResource` az a tároló, amely egy réteg vektor alakzat adatait tárolja. A második réteg erőforrásain iterálva keresse meg.

```java
VsmsResource resource = null;
for (LayerResource layerResource : psdImage.getLayers()[1].getResources()) {
    if (layerResource instanceof VsmsResource) {
        resource = (VsmsResource) layerResource;
        break;
    }
}
```

## 4. lépés: Hozzáférés a length rekordokhoz
A `LengthRecord` egy különálló vektor útvonalat képvisel. Szerezze meg azokat a rekordokat, amelyeket módosítani kíván.

```java
LengthRecord lengthRecord0 = (LengthRecord) resource.getPaths()[2];
LengthRecord lengthRecord1 = (LengthRecord) resource.getPaths()[7];
LengthRecord lengthRecord2 = (LengthRecord) resource.getPaths()[11];
```

## 5. lépés: Útvonal művelet tulajdonságok módosítása
A `PathOperations` meghatározza, hogyan lépnek kölcsönhatásba az egyes alakzatok (pl. kizárás, metszés, kivonás). Ezeknek az értékeknek a módosítása frissíti a vektor réteg vizuális összetételét.

```java
lengthRecord0.setPathOperations(PathOperations.ExcludeOverlappingShapes);
lengthRecord1.setPathOperations(PathOperations.IntersectShapeAreas);
lengthRecord2.setPathOperations(PathOperations.SubtractFrontShape);
```

## 6. lépés: Módosított PSD fájl mentése
Mentse el a változtatásokat egy új fájlba.

```java
psdImage.save(outPsdFilePath);
```

## 7. lépés: Erőforrások felszabadítása
Szabadítsa fel a `PsdImage` példányt a memória felszabadításához és az erőforrás-szivárgások elkerüléséhez.

```java
psdImage.dispose();
```

## Hogyan dolgozzuk fel kötegelt módon a PSD fájlokat a length record tulajdonságok támogatásával
Tegye a egy‑fájlos munkafolyamatot egy ciklusba, amely egy PSD könyvtáron iterál, frissítve minden fájlra az `inPsdFilePath` és `outPsdFilePath` értékeket. Ez a megközelítés lehetővé teszi azonos vektor‑alakzat módosítások alkalmazását tucatnyi vagy akár több száz fájlra percek alatt, ami ideális az automatizált asset pipeline-okhoz.

## Gyakori buktatók és tippek
- **Null ellenőrzések** – mindig ellenőrizze, hogy a `resource` nem `null`, mielőtt hozzáférne a tagjaihoz.  
- **Útvonal index határok** – győződjön meg arról, hogy a használt indexek (pl. `[2]`, `[7]`, `[11]`) léteznek az adott szerkesztett PSD-ben.  
- **Licenc** – érvényes licenc nélkül a mentett PSD vízjelet kap.

## Összegzés
Most már rendelkezik egy teljes, vég‑től‑végig példával arra, hogyan **módosítsa a PSD vektor alakzatokat** a length record tulajdonságok támogatásával az Aspose.PSD for Java segítségével. Legyen szó asset pipeline automatizálásáról vagy egy egyedi tervezőeszköz építéséről, ezek az API-k rugalmasságot biztosítanak a vektor rétegek manipulálásához Photoshop manuális használata nélkül. Kísérletezzen más `PathOperations` értékekkel, vagy kombináljon több `LengthRecord` módosítást összetett alakzatok létrehozásához.

## Gyakran ismételt kérdések

**Q: Hogyan kezeljek egy PSD-t, amely nem tartalmaz vektor alakzat rétegeket?**  
A: A `VsmsResource` hiányzik, így a `resource` `null` marad. Ellenőrzést kell hozzáadni, és kihagyni a módosítási lépést, vagy értesíteni a felhasználót.

**Q: Változtathatok-e más tulajdonságokat, például kitöltő színt vagy vonalvastagságot?**  
A: Igen, a `LengthRecord` biztosít beállítókat a kitöltéshez, vonalhoz és átlátszatlansághoz. Tekintse meg az API dokumentációt a teljes listáért.

**Q: Lehetséges-e kötegelt feldolgozást végezni több PSD fájlon?**  
A: Teljesen lehetséges. Tegye a kódot egy ciklusba, amely egy PSD fájlok könyvtárán iterál, minden alkalommal módosítva a bemeneti és kimeneti útvonalakat.

**Q: Kézzel kell-e bezárni a stream-eket, ha fájl útvonalról töltök be?**  
A: Az `Image.load` automatikusan kezeli a fájl stream-eket, de ha `InputStream`‑ből tölt be, ne felejtse el a használat után bezárni.

**Q: Melyik Aspose.PSD verzió szükséges ezekhez az API-khoz?**  
A: A `LengthRecord` és `PathOperations` osztályok már az Aspose.PSD 20.10‑től elérhetők. A legújabb verzió (24.11 a írás időpontjában) használata ajánlott.

---

**Last Updated:** 2026-09-23  
**Tested With:** Aspose.PSD for Java 24.11  
**Author:** Aspose

## Kapcsolódó oktatóanyagok

- [PSD konvertálása PNG-re és vektor maszk létrehozása Java – Vmsk erőforrás PSD fájlokban](/psd/java/advanced-psd-layer-features-effects/support-vmsk-resource-psd-files/)
- [PSD konvertálása PNG-re rétegmaszk támogatással az Aspose.PSD for Java használatával](/psd/java/advanced-psd-layer-features-effects/support-layer-mask-psd-files/)
- [Réteg támogatás hozzáadása PSD fájlokhoz](/psd/java/advanced-psd-layer-features-effects/add-layer-support-psd-files/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}