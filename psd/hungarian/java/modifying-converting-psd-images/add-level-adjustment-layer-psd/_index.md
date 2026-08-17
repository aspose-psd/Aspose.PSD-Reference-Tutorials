---
date: 2026-03-07
description: Tanulja meg, hogyan állíthatja be a szinteket egy Szintkorrekció réteg
  hozzáadásával PSD‑fájlokban az Aspose.PSD for Java használatával. Gyorsan sajátítsa
  el a tónuskorrekciókat.
linktitle: Add Level Adjustment Layer in PSD
second_title: Aspose.PSD Java API
title: Hogyan állítsuk be a szinteket – Szintkorrekciós réteg hozzáadása PSD-ben
url: /hu/java/modifying-converting-psd-images/add-level-adjustment-layer-psd/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Szintkorrekciós réteg hozzáadása PSD-ben

## Bevezetés
Ha szeretné megtudni, **hogyan állítsa be a szinteket** a Photoshop dokumentumaiban, a Szintkorrekciós réteg a tökéletes eszköz. Lehetővé teszi az árnyékok, középtónusok és csúcsfények finomhangolását anélkül, hogy véglegesen megváltoztatná az eredeti pixeleket. Ebben az útmutatóban lépésről‑lépésre bemutatjuk, hogyan adjon hozzá Szintkorrekciós réteget egy PSD fájlhoz az Aspose.PSD for Java segítségével, így néhány lépésben professzionális tónusvezérlést érhet el.

## Gyors válaszok
- **Mit csinál egy Szintkorrekciós réteg?** Nem destruktív módon módosítja a kép tónustartományát.  
- **Melyik könyvtárat használja?** Aspose.PSD for Java.  
- **Szükségem van licencre?** Fejlesztéshez egy ingyenes próba verzió elegendő; termeléshez licenc szükséges.  
- **Mennyi időt vesz igénybe a megvalósítás?** Körülbelül 10‑15 perc egy alap beállításhoz.  
- **Több csatornát is tudok beállítani?** Igen, minden színcsatorna bemeneti/kimeneti szintjei külön-külön állíthatók.

## Mi az a Szintkorrekciós réteg?
A Szintkorrekciós réteg lehetővé teszi a kép tónusegyensúlyának korrekcióját a bemeneti árnyékok, középtónusok és csúcsfények, valamint a kimeneti szintek beállításával. Mivel saját rétegen él, láthatóságát be‑ vagy kikapcsolhatja, vagy törölheti anélkül, hogy az alatta lévő műalkotást befolyásolná.

## Miért adjunk hozzá Szintkorrekciós réteget az Aspose.PSD‑vel?
- **Automatizálás:** Szintbeállítások integrálása kötegelt feldolgozási folyamatokba.  
- **Kereszt‑platform:** Bármely, Java‑t támogató operációs rendszeren működik.  
- **Pontosság:** Programozottan hozzáférhet minden csatorna beállításához a pontos eredményekért.  

## Előfeltételek
1. Java Development Kit (JDK). Ha nincs telepítve, töltse le az [Oracle weboldaláról](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) vagy használja az OpenJDK‑t.  
2. Aspose.PSD for Java könyvtár – a legújabb JAR letölthető erről a [letöltési hivatkozásról](https://releases.aspose.com/psd/java/).  
3. Alapvető Java programozási ismeretek.  
4. IDE, például IntelliJ IDEA, Eclipse vagy NetBeans, az Aspose.PSD JAR‑rel a projekt classpath‑ában.

## Csomagok importálása
Mielőtt elkezdenénk a kód írását, importálnunk kell a szükséges csomagokat az Aspose.PSD könyvtárból. Így tehetjük:
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.LevelsLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.LevelChannel;
```
Ezek az importálások hozzáférést biztosítanak a PSD fájlok betöltéséhez, a szintkorrekciós rétegek kezeléséhez és az egyes csatorna beállítások manipulálásához.

## Hogyan állítsuk be a szinteket PSD fájlban
Az alábbi lépés‑ről‑lépésre útmutató pontosan megmutatja, **hogyan állítsa be a szinteket** programozottan.

### 1. lépés: Állítsa be a fájl útvonalait
Határozza meg, hol található a forrás‑PSD, és hová mentse a szerkesztett fájlt.
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "LevelsAdjustmentLayer.psd";
String psdPathAfterChange = dataDir + "LevelsAdjustmentLayerChanged.psd";
```
Cserélje le a `"Your Document Directory"`‑t a gépén lévő tényleges mappára.

### 2. lépés: PSD fájl betöltése
Hozzon létre egy `PsdImage` példányt a forrásfájlból.
```java
PsdImage im = (PsdImage) Image.load(sourceFileName);
```
Most már teljes hozzáférése van a PSD‑ben lévő összes réteghez.

### 3. lépés: Rétegek bejárása
Keresse meg a módosítani kívánt Szintkorrekciós réteget.
```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof LevelsLayer) {
        LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
        // Further manipulation will go here...
    }
}
```
Az `instanceof LevelsLayer` ellenőrzés biztosítja, hogy csak szintkorrekciós rétegekkel dolgozunk.

### 4. lépés: Szintcsatorna beállítások módosítása
Finomhangolja a kiválasztott csatorna bemeneti és kimeneti értékeit.
```java
LevelChannel channel = levelsLayer.getChannel(0);
channel.setInputMidtoneLevel(2.0f);
channel.setInputShadowLevel((short) 10);
channel.setInputHighlightLevel((short) 230);
channel.setOutputShadowLevel((short) 20);
channel.setOutputHighlightLevel((short) 200);
```
- **Bemeneti középszint:** A középtónus tartományát eltolja.  
- **Bemeneti árnyék szint:** Sötétíti vagy világosítja az árnyékokat.  
- **Bemeneti csúcsfény szint:** A legvilágosabb részeket szabályozza.  
- **Kimeneti árnyék/csúcsfény szintek:** Meghatározzák a végső kimeneti tartományt.

Nyugodtan kísérletezzen különböző értékekkel, hogy lássa, hogyan befolyásolják a képet.

### 5. lépés: Módosított PSD fájl mentése
Mentse el a változtatásokat egy új fájlba.
```java
im.save(psdPathAfterChange);
```
Az frissített PSD‑t a `psdPathAfterChange`‑ben megadott helyen találja.

## Gyakori problémák és megoldások
- **Fájl nem található:** Ellenőrizze, hogy a `dataDir` a megfelelő mappára mutat‑e, és hogy a forrás‑PSD létezik‑e.  
- **ClassCastException:** Győződjön meg arról, hogy a betöltött fájl valóban PSD, más formátumokhoz más osztályok szükségesek.  
- **Licenc hibák:** Használjon érvényes Aspose.PSD licencet a termelési buildhez; a próba verzió fejlesztéshez működik.

## Összegzés
Most már tudja, **hogyan állítsa be a szinteket** egy Szintkorrekciós réteg hozzáadásával és konfigurálásával PSD fájlban az Aspose.PSD for Java segítségével. Ez a technika pontos kontrollt ad a tónusegyensúly felett, miközben a munkafolyamat teljesen automatizált marad. Folytassa a kísérletezést különböző csatornaértékekkel, és fedezze fel a kötegelt feldolgozást, hogy ugyanazokat a beállításokat több képre is alkalmazza.

## Gyakran feltett kérdések

**Q: Mi az a Szintkorrekciós réteg?**  
A: Ez egy nem destruktív réteg, amely lehetővé teszi a kép tónustartományának (árnyékok, középtónusok, csúcsfények) módosítását.

**Q: Használhatom az Aspose.PSD‑t licenc vásárlása nélkül?**  
A: Igen, a könyvtárat ingyenes próba verzióval értékelheti, de a kereskedelmi felhasználáshoz licenc szükséges.

**Q: Hol találom az Aspose.PSD dokumentációját?**  
A: A dokumentációt [itt](https://reference.aspose.com/psd/java/) találja.

**Q: Van közösségi támogatás az Aspose termékekhez?**  
A: Természetesen! Kérdéseket tehet fel és segítséget kaphat az [Aspose fórumon](https://forum.aspose.com/c/psd/34).

**Q: Hogyan szerezhetek ideiglenes licencet az Aspose.PSD‑hez?**  
A: Ideiglenes licencet [itt](https://purchase.aspose.com/temporary-license/) igényelhet.

---

**Last Updated:** 2026-03-07  
**Tested With:** Aspose.PSD latest version (Java)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}