---
date: 2026-03-18
description: Tanulja meg, hogyan változtathatja meg a PNG felbontását Java-ban, és
  hogyan állíthatja be a kép felbontását Java-val az Aspose.PSD for Java segítségével.
  Kövesse ezt a lépésről‑lépésre útmutatót, hogy gyorsan optimalizálja képeit.
linktitle: Change PNG resolution java using Aspose.PSD
second_title: Aspose.PSD Java API
title: PNG felbontás módosítása Java-ban az Aspose.PSD használatával
url: /hu/java/optimizing-png-files/set-png-file-resolution/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PNG felbontás módosítása Java-ban az Aspose.PSD használatával

## Bevezetés
Ha gyorsan és megbízhatóan szeretné **change PNG resolution java** módosítani, jó helyen jár. Ebben az útmutatóban lépésről lépésre bemutatjuk, hogyan állítható be a PNG fájl felbontása az Aspose.PSD for Java segítségével. Akár kötegelt feldolgozó eszközt, webszolgáltatást épít, vagy csak néhány assetet csiszol, ugyanaz a megközelítés mindenhol működik. Vegye elő a kedvenc IDE-jét, és kezdjünk bele!

## Gyors válaszok
- **Melyik könyvtár kezeli a PNG felbontást?** Aspose.PSD for Java  
- **Elsődleges metódus?** `PngOptions.setResolutionSettings`  
- **Tipikus DPI értékek?** 72 × 96 for web‑ready images  
- **Szükségem van licencre?** A trial works for testing; a license is required for production  
- **Támogatott JDK?** Java 8 or higher  

## Mi az a “change PNG resolution java”?
A PNG felbontás Java-ban történő módosítása azt jelenti, hogy megváltoztatjuk a DPI (dots per inch) metaadatot, amely megmondja a böngészőknek és nyomtatóknak, mekkora méretben jelenjen meg a kép. A pixeladatok változatlanok maradnak, de a felbontási címke frissül, ami befolyásolhatja a nyomtatási méretet és minőséget.

## Miért használja az Aspose.PSD-t ehhez a feladathoz?
Az Aspose.PSD egy magas szintű API-t biztosít, amely elrejti az alacsony szintű PNG kezelést, így a fájlformátum sajátosságai helyett az üzleti logikára koncentrálhat. Támogat több száz PSD funkciót, bármely Java‑t futtató platformon működik, és nem igényel natív könyvtárakat.

## Előfeltételek
1. **Java Development Kit (JDK) 8+** – a kód bármely friss JDK-n fut.  
2. **Aspose.PSD for Java** – töltse le a [letöltési hivatkozásról](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse vagy VS Code Java támogatással.  
4. **Minta PSD fájl** – ezt PNG‑re konvertáljuk és módosítjuk a felbontását.  
5. **Alap Java ismeretek** – a kódrészleteket extra magyarázat nélkül is megérti.  

## Csomagok importálása
Miután minden előkészítve van, importálja a szükséges osztályokat. Ezek az importok hozzáférést biztosítanak a kép betöltéséhez, a felbontás beállításához és a PNG exportálási lehetőségekhez.

```java
import com.aspose.psd.Image;
import com.aspose.psd.ResolutionSetting;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

## 1. lépés: Java projekt beállítása
Hozzon létre egy új Java projektet (vagy Maven/Gradle modult), és adja hozzá az Aspose.PSD JAR‑t a build útvonalához. Ha Maven‑t használ, adja hozzá a megfelelő függőséget az Aspose tárolóból.

## 2. lépés: Dokumentumkönyvtár meghatározása
Adja meg a programnak, hol találja a forrás PSD fájlt, és hová írja a kimeneti PNG‑t.

```java
String dataDir = "Your Document Directory"; // Update with your folder path
```

Cserélje le a `"Your Document Directory"` értéket a `sample.psd`‑t tartalmazó abszolút vagy relatív útvonalra.

## 3. lépés: PSD kép betöltése
Használja a `PsdImage` osztályt a PSD fájl lemezről történő beolvasásához.

```java
PsdImage psdImage = (PsdImage) Image.load(dataDir + "sample.psd");
```

Győződjön meg róla, hogy a fájlnév megegyezik a ténylegesen feldolgozni kívánt PSD‑vel.

## 4. lépés: PNG beállítások létrehozása és konfigurálása
Itt történik a tényleges **change PNG resolution java**. Létrehozzuk a `PngOptions` példányt, és a `ResolutionSetting`‑en keresztül állítjuk be a vízszintes és függőleges DPI értékeket.

```java
PngOptions options = new PngOptions();
options.setResolutionSettings(new ResolutionSetting(72, 96)); // 72 DPI horizontal, 96 DPI vertical
```

Nyugodtan cserélje le a `72` és `96` értékeket bármilyen, a céleszköznek megfelelő értékre. Ez a **set image resolution java** művelet magja.

## 5. lépés: Az eredmény PNG mentése
Végül exportálja a PSD‑t PNG‑ként az új felbontási metaadatokkal.

```java
psdImage.save(dataDir + "SettingResolution_output.png", options);
```

A `SettingResolution_output.png` fájl ugyanabban a mappában jelenik meg, most már a megadott DPI értékeket tartalmazza.

## Gyakori hibák és tippek
- **Helytelen útvonal** – Ellenőrizze, hogy a `dataDir` fájlelválasztóval (`/` vagy `\`) végződik-e.  
- **Nem támogatott DPI** – A legtöbb böngésző figyelmen kívül hagyja a 300‑nál nagyobb DPI értékeket; tartsa őket ésszerűen.  
- **Memóriahasználat** – Nagy PSD‑k jelentős RAM‑ot fogyaszthatnak; fontolja meg a `psdImage` felszabadítását a mentés után (`psdImage.dispose()`).  

## Következtetés
Most megtanulta, hogyan **change PNG resolution java** az Aspose.PSD segítségével. A `ResolutionSetting` finomhangolásával szabályozhatja, hogyan értelmezik a nyomtatók és a tervezőeszközök a PNG‑ket anélkül, hogy a pixeladatokat módosítaná. Fedezzen fel további lehetőségeket, például tömörítési szintet, színmélységet vagy kötegelt feldolgozást, hogy tovább automatizálja a munkafolyamatát.

A mélyebb kutatáshoz tekintse meg a hivatalos [Aspose.PSD dokumentáció](https://reference.aspose.com/psd/java/).

## GyIK
### Milyen formátumokra konvertálhatom a PSD fájlokat az Aspose.PSD for Java használatával?
A PSD fájlokat konvertálhatja olyan formátumokra, mint a PNG, JPEG, BMP és TIFF.  

### Szükségem van licencre az Aspose.PSD for Java használatához?
Igen, bár elérhető egy ingyenes próba, a további használathoz érvényes licenc szükséges a tesztelés után.  

### Több alkalommal is módosíthatom a felbontást egy programban?
Természetesen! Különböző `PngOptions` példányokat hozhat létre különböző export beállításokhoz ugyanazon alkalmazáson belül.  

### Mi van, ha a PSD fájlom sérült?
Az Aspose.PSD számos gyakori problémát kezel, de ha a fájl súlyosan sérült, előfordulhat, hogy nem töltődik be. Mindig tartson biztonsági másolatot.  

### Az Aspose.PSD alkalmas nagy teljesítményű alkalmazásokhoz?
Igen, úgy tervezték, hogy nagy fájlokat hatékonyan kezeljen, és alkalmas a teljesítmény‑igényes képfeldolgozási feladatokra.  

## Gyakran Ismételt Kérdések
**Q: Hogyan állíthatok programozottan különböző DPI‑t a vízszintes és függőleges tengelyekhez?**  
A: Használja a `new ResolutionSetting(horizontalDpi, verticalDpi)` kifejezést, ahogyan a PNG beállítási példában látható.  

**Q: Kötegelt feldolgozhatok több PSD fájlt egy futtatás során?**  
A: Igen – a betöltési, beállítási és mentési lépéseket egy ciklusba helyezve, amely a fájlkészletén iterál.  

**Q: Befolyásolja a DPI módosítása a fájlméretet?**  
A: Általában nem; a DPI metaadat. A fájlméret csak akkor változik, ha a tömörítést vagy a pixelméreteket módosítja.  

**Q: Van mód arra, hogy kiolvassam egy meglévő PNG aktuális DPI‑jét?**  
A: Töltse be a PNG‑t a `Image.load()` segítségével, és vizsgálja meg a `image.getResolutionSettings()` értéket (PNG fájlok esetén elérhető).  

**Q: Mely JDK verziók támogatottak hivatalosan?**  
A: Az Aspose.PSD for Java támogatja a JDK 8‑tól a JDK 21‑ig terjedő verziókat.  

---
**Utolsó frissítés:** 2026-03-18  
**Tesztelve ezzel:** Aspose.PSD for Java 24.10  
**Szerző:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}