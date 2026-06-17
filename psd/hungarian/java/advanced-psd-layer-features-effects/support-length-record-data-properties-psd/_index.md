---
date: 2026-02-20
description: Tanulja meg, hogyan támogassa a hossz rekord tulajdonságokat, és kötegelt
  módon dolgozza fel a PSD fájlokat az Aspose.PSD for Java segítségével. Lépésről
  lépésre útmutató kódrészletekkel.
linktitle: Support Length Record Data Properties in PSD - Java
second_title: Aspose.PSD Java API
title: Hossz rekord tulajdonságok támogatása – PSD vektor alakzatok módosítása (Java)
url: /hu/java/advanced-psd-layer-features-effects/support-length-record-data-properties-psd/
weight: 14
---

/products-backtop-button >}}

Now translate each piece.

We must keep code block placeholders as is.

Let's produce final markdown.

Be careful with Hungarian special characters.

Proceed.

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hossz Rekord Tulajdonságok Támogatása – PSD Vektor Alakzatok Módosítása (Java)

## Bevezetés
Ha **programozottan szeretnél PSD vektor alakzatokat módosítani**, az Aspose.PSD for Java könyvtár teljes irányítást ad a Photoshop fájlok felett közvetlenül a Java kódból. Ebben az útmutatóban végigvezetünk mindenen, amit tudnod kell a **hossz rekord tulajdonságok támogatásához** – egy alapvető lépés, ha vektor alakzat rétegeket szeretnél szerkeszteni. A végére képes leszel megnyitni egy PSD‑t, finomhangolni a vektor alakzat tulajdonságait, és elmenteni a frissített fájlt anélkül, hogy elhagynád az IDE‑det. Merüljünk el benne!

## Gyors válaszok
- **Mit jelent a „PSD vektor alakzatok módosítása”?** A geometria, útvonal‑műveletek vagy egyéb tulajdonságok módosítása a PSD‑ben lévő vektor‑alapú rétegeken.  
- **Melyik könyvtár kezeli ezt?** Aspose.PSD for Java.  
- **Szükségem van licencre?** Egy ingyenes próba a kiértékeléshez elegendő; a kereskedelmi licenc szükséges a termeléshez.  
- **Mennyi időt vesz igénybe a megvalósítás?** Körülbelül 10‑15 perc egy alap alakzat‑módosító szkripthez.  
- **Mik a fő előfeltételek?** Java JDK, Aspose.PSD for Java és egy minta PSD fájl.

## Mi az a „hossz rekord tulajdonságok támogatása”?
A hossz rekord tulajdonságok támogatása azt jelenti, hogy hozzáférsz és frissíted a `LengthRecord` objektumokat, amelyek minden egyes vektor útvonalat leírnak egy PSD‑ben. Ezeknek a rekordoknak a módosítása lehetővé teszi, hogy szabályozd, hogyan kombinálódnak, metszik vagy vonják ki egymásból az alakzatok.

## Miért használjuk az Aspose.PSD for Java‑t a hossz rekord tulajdonságok támogatásához?
- **Nincs szükség Photoshopra** – közvetlenül dolgozhatsz PSD fájlokkal bármely szerveren.  
- **Gazdag API** – rétegekhez, erőforrásokhoz és vektor adatokhoz férhetsz hozzá erősen típusos osztályokkal.  
- **Kereszt‑platform** – futtatható Windows, Linux vagy macOS rendszeren bármely JDK‑val.  
- **Teljesítmény‑orientált** – hatékony memória‑kezelés és gyors mentési műveletek.  

## Előfeltételek
1. **Java Development Kit (JDK)** – töltsd le a [Oracle weboldaláról](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) vagy használd a kedvenc csomagkezelődet.  
2. **Aspose.PSD for Java** – szerezd be a legújabb JAR‑t a [Aspose kiadási oldaláról](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse vagy bármely Java‑kompatibilis szerkesztő.  
4. **PSD fájl** – hozz létre egyet a Photoshopban, vagy vegyél egy mintát a kísérletezéshez.  
5. **Alap Java ismeretek** – osztályok, objektumok és kivételkezelés ismerete.

## Csomagok importálása
Először importáld azokat az osztályokat, amelyekre a PSD fájlok és a vektor alakzat erőforrások kezeléséhez szükséged lesz.

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.LayerResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.VsmsResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.LengthRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.PathOperations;
```

## 1. lépés: Forrás‑ és kimeneti könyvtárak beállítása
Határozd meg, hol található az eredeti PSD, és hová szeretnéd menteni a módosított fájlt.

```java
String sourceDir = "Your Source Directory";
String outputDir = "Your Document Directory";
String inPsdFilePath = sourceDir + "PathOperationsShape.psd";
String outPsdFilePath = outputDir + "out_PathOperationsShape.psd";
```

## 2. lépés: PSD fájl betöltése
Használd az `Image.load` metódust a fájl megnyitásához, majd cast-eld `PsdImage`‑re a PSD‑specifikus funkciókhoz.

```java
PsdImage psdImage = (PsdImage) Image.load(inPsdFilePath);
```

## 3. lépés: Vsms erőforrás megtalálása a rétegben
A vektor alakzat adatok egy `VsmsResource`‑ban tárolódnak. Iterálj a második réteg erőforrásain, hogy megtaláld.

```java
VsmsResource resource = null;
for (LayerResource layerResource : psdImage.getLayers()[1].getResources()) {
    if (layerResource instanceof VsmsResource) {
        resource = (VsmsResource) layerResource;
        break;
    }
}
```

## 4. lépés: Hossz rekordok elérése
Minden `LengthRecord` egy különálló vektor útvonalat képvisel. Szerezd meg azokat, amelyeket módosítani szeretnél.

```java
LengthRecord lengthRecord0 = (LengthRecord) resource.getPaths()[2];
LengthRecord lengthRecord1 = (LengthRecord) resource.getPaths()[7];
LengthRecord lengthRecord2 = (LengthRecord) resource.getPaths()[11];
```

## 5. lépés: Útvonal‑művelet tulajdonságok módosítása
Most már **módosíthatod a PSD vektor alakzatokat** a `PathOperations` változtatásával. Ez határozza meg, hogyan lépnek kölcsönhatásba az alakzatok (pl. kizárás, metszés, kivonás).

```java
lengthRecord0.setPathOperations(PathOperations.ExcludeOverlappingShapes);
lengthRecord1.setPathOperations(PathOperations.IntersectShapeAreas);
lengthRecord2.setPathOperations(PathOperations.SubtractFrontShape);
```

## 6. lépés: Módosított PSD fájl mentése
Mentsd el a változtatásokat egy új fájlba.

```java
psdImage.save(outPsdFilePath);
```

## 7. lépés: Erőforrások felszabadítása
A `PsdImage` eldobásával szabadítsd fel a memóriát.

```java
psdImage.dispose();
```

## Hogyan batch‑feldolgozzuk a PSD fájlokat a hossz rekord tulajdonságok támogatásával
Ha ugyanazokat a vektor‑alakzat módosításokat sok PSD‑re szeretnéd alkalmazni, csomagold be a fenti kódot egy ciklusba, amely egy könyvtár fájljait iterálja. Minden iterációban állítsd be az `inPsdFilePath` és `outPsdFilePath` értékeket, és **batch‑feldolgozhatod a PSD fájlokat** hatékonyan.

## Gyakori hibák és tippek
- **Null ellenőrzések** – mindig ellenőrizd, hogy a `resource` nem `null`, mielőtt útvonalakat érnél el.  
- **Útvonal index határok** – győződj meg róla, hogy a használt indexek (`[2]`, `[7]`, `[11]`) léteznek az adott PSD‑ben.  
- **Licenc** – érvényes licenc hiányában a mentett PSD‑be vízjel kerül beágyazásra.  

## Összegzés
Most már egy teljes, vég‑től‑végig példát birtokolsz arra, hogyan **módosíthatod a PSD vektor alakzatokat** a hossz rekord tulajdonságok támogatásával az Aspose.PSD for Java‑val. Akár eszközcsővezeték‑automatizálást, akár egyedi tervezőeszközt építesz, ezek az API‑k rugalmasságot biztosítanak a vektor rétegek manipulálásához Photoshop manuális használata nélkül. További felfedezéshez próbáld ki a különböző `PathOperations`‑t, vagy kombináld több `LengthRecord` szerkesztését összetett alakzatokhoz.

## Gyakran Ismételt Kérdések

**Q: Hogyan kezelem azt a PSD‑t, amely nem tartalmaz vektor alakzat rétegeket?**  
A: A `VsmsResource` hiányzik, így a `resource` `null` marad. Adj hozzá egy ellenőrzést, és hagyd ki a módosítási lépést, vagy értesítsd a felhasználót.

**Q: Módosíthatok más tulajdonságokat is, például kitöltő színt vagy vonalvastagságot?**  
Igen, a `LengthRecord` további settereket biztosít a kitöltés, vonal és átlátszóság beállításához. Tekintsd meg az API dokumentációt a részletekért.

**Q: Lehetséges több PSD fájl batch‑feldolgozása?**  
Természetesen. Csomagold a kódot egy ciklusba, amely egy PSD‑könyvtárat iterál, és minden alkalommal állítsd be a bemeneti és kimeneti útvonalakat.

**Q: Kézzel kell-e bezárni a stream‑eket, ha fájl útvonalról töltök be?**  
Az `Image.load` metódus belsőleg kezeli a fájl‑streameket, de ha `InputStream`‑ből töltöd be, ne felejtsd el később bezárni.

**Q: Mely Aspose.PSD verzió szükséges ezekhez az API‑khoz?**  
A `LengthRecord` és `PathOperations` osztályok az Aspose.PSD 20.10‑től elérhetők. Ajánlott a legújabb verzió használata.

---

**Utoljára frissítve:** 2026-02-20  
**Tesztelve:** Aspose.PSD for Java 24.11  
**Szerző:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}