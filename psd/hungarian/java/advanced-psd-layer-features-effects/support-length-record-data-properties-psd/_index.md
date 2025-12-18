---
date: 2025-12-17
description: Tanulja meg, hogyan módosíthatja a PSD vektoros alakzatokat a hossz rekord
  adat tulajdonságok támogatásával az Aspose.PSD for Java használatával. Lépésről
  lépésre útmutató kódrészletekkel.
linktitle: Support Length Record Data Properties in PSD - Java
second_title: Aspose.PSD Java API
title: Hogyan módosítsuk a PSD vektoros alakzatokat – Hossz rekord adat tulajdonságok
  támogatása Java-ban
url: /hu/java/advanced-psd-layer-features-effects/support-length-record-data-properties-psd/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hossz Rekord Adat Tulajdonságok Támogatása a PSD-ben – Java

## Bevezetés
Ha programozott módon **módosítani szeretné a PSD vektoros alakzatokat**, az Aspose.PSD for Java könyvtár teljes irányítást biztosít a Photoshop fájlok felett közvetlenül a Java kódjából. Ebben az útmutatóban végigvezetünk minden szükséges lépésen a hossz rekord adat tulajdonságok támogatásához – ami elengedhetetlen, ha vektoros alakzatrétegeket szeretne szerkeszteni. A végére képes lesz megnyitni egy PSD-t, finomhangolni a vektoros alakzat tulajdonságait, és elmenteni a frissített fájlt anélkül, hogy elhagyná a fejlesztői környezetet. Merüljünk el benne!

## Gyors válaszok
- **Mit jelent a “modify PSD vector shapes”?** A geometria, útvonal műveletek vagy egyéb tulajdonságok módosítása a PSD‑ben lévő vektor‑alapú rétegeknél.  
- **Melyik könyvtár kezeli ezt?** Aspose.PSD for Java.  
- **Szükségem van licencre?** Egy ingyenes próba verzió elegendő értékeléshez; a kereskedelmi licenc szükséges a termeléshez.  
- **Mennyi időt vesz igénybe a megvalósítás?** Körülbelül 10‑15 perc egy alap alakzat‑módosító szkripthez.  
- **Mik a fő előfeltételek?** Java JDK, Aspose.PSD for Java és egy minta PSD fájl.

## Mi az a “modify PSD vector shapes”?
A PSD vektoros alakzatok módosítása magában foglalja a mögöttes vektor‑útvonal adatok – például hossz rekordok és útvonal műveletek – megváltoztatását, hogy a formák vizuális megjelenése ennek megfelelően frissüljön. Ez különösen hasznos automatizált grafikai csővezetékek, kötegelt feldolgozás vagy egyedi tervezőeszközök esetén.

## Miért használja az Aspose.PSD for Java‑t a PSD vektoros alakzatok módosításához?
- **Nincs szükség Photoshopra** – dolgozzon közvetlenül PSD fájlokkal bármely szerveren.  
- **Gazdag API** – férjen hozzá rétegekhez, erőforrásokhoz és vektoradatokhoz erősen típusos osztályokkal.  
- **Cross‑platform** – futtatható Windows, Linux vagy macOS rendszeren bármely JDK‑val.  
- **Teljesítmény‑orientált** – hatékony memória kezelés és gyors mentési műveletek.

## Előfeltételek
1. **Java Development Kit (JDK)** – töltsön le a [Oracle weboldaláról](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) vagy használja a kedvenc csomagkezelőjét.  
2. **Aspose.PSD for Java** – szerezze be a legújabb JAR‑t a [Aspose kiadási oldalról](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse vagy bármely Java‑kompatibilis szerkesztő.  
4. **PSD fájl** – hozzon létre egyet a Photoshopban, vagy vegyen egy mintát a kísérletezéshez.  
5. **Alap Java ismeretek** – osztályok, objektumok és kivételkezelés ismerete.

## Csomagok importálása
Először importálja azokat az osztályokat, amelyekre a PSD fájlok és a vektoros alakzat erőforrások kezeléséhez szüksége lesz.

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.LayerResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.VsmsResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.LengthRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.PathOperations;
```

## 1. lépés: Állítsa be a forrás- és kimeneti könyvtárakat
Határozza meg, hol található az eredeti PSD, és hová szeretné menteni a módosított fájlt.

```java
String sourceDir = "Your Source Directory";
String outputDir = "Your Document Directory";
String inPsdFilePath = sourceDir + "PathOperationsShape.psd";
String outPsdFilePath = outputDir + "out_PathOperationsShape.psd";
```

## 2. lépés: Töltse be a PSD fájlt
Használja a `Image.load` metódust a fájl megnyitásához, majd castolja `PsdImage`‑re a PSD‑specifikus funkciókhoz.

```java
PsdImage psdImage = (PsdImage) Image.load(inPsdFilePath);
```

## 3. lépés: Keresse meg a Vsms erőforrást a rétegben
A vektoros alakzat adat a `VsmsResource`‑ban tárolódik. Iteráljon a második réteg erőforrásain, hogy megtalálja.

```java
VsmsResource resource = null;
for (LayerResource layerResource : psdImage.getLayers()[1].getResources()) {
    if (layerResource instanceof VsmsResource) {
        resource = (VsmsResource) layerResource;
        break;
    }
}
```

## 4. lépés: Hozzáférés a Length Record‑okhoz
Minden `LengthRecord` egy különálló vektor‑útvonalat képvisel. Szerezze meg azokat, amelyeket módosítani kíván.

```java
LengthRecord lengthRecord0 = (LengthRecord) resource.getPaths()[2];
LengthRecord lengthRecord1 = (LengthRecord) resource.getPaths()[7];
LengthRecord lengthRecord2 = (LengthRecord) resource.getPaths()[11];
```

## 5. lépés: Path Operation tulajdonságok módosítása
Most már **módosíthatja a PSD vektoros alakzatokat** a `PathOperations` megváltoztatásával. Ez határozza meg, hogyan lépnek kölcsönhatásba a formák (pl. kizárás, metszet, kivonás).

```java
lengthRecord0.setPathOperations(PathOperations.ExcludeOverlappingShapes);
lengthRecord1.setPathOperations(PathOperations.IntersectShapeAreas);
lengthRecord2.setPathOperations(PathOperations.SubtractFrontShape);
```

## 6. lépés: A módosított PSD fájl mentése
Mentse el a változtatásokat egy új fájlba.

```java
psdImage.save(outPsdFilePath);
```

## 7. lépés: Erőforrások felszabadítása
Szabadítsa fel a memóriát a `PsdImage` eldobásával.

```java
psdImage.dispose();
```

## Gyakori hibák és tippek
- **Null ellenőrzések** – mindig ellenőrizze, hogy a `resource` nem `null`, mielőtt útvonalakat érne el.  
- **Útvonal index határok** – győződjön meg arról, hogy a használt indexek (`[2]`, `[7]`, `[11]`) léteznek az adott PSD‑ben.  
- **Licenc** – érvényes licenc nélkül a mentett PSD‑be vízjel kerül beágyazásra.  

## Összegzés
Most már rendelkezik egy teljes, vég‑től‑végig példával arra, hogyan **módosítsa a PSD vektoros alakzatokat** a hossz rekord adat tulajdonságok támogatásával az Aspose.PSD for Java segítségével. Legyen szó eszközcsővezetékek automatizálásáról vagy egyedi tervezőeszköz építéséről, ezek az API‑k rugalmasságot biztosítanak a vektor‑rétegek manuális Photoshop munka nélkül történő manipulálásához. Kísérletezzen további `PathOperations`‑okkal vagy kombinálja több `LengthRecord` módosítását összetett formák létrehozásához.

## 常見問題解答

**Q: Hogyan kezeljek egy PSD‑t, amely nem tartalmaz vektoros alakzat rétegeket?**  
A: A `VsmsResource` hiányzik, így a `resource` `null` marad. Ellenőrizze ezt, és hagyja ki a módosítási lépést, vagy tájékoztassa a felhasználót.

**Q: Megváltoztathatom más tulajdonságokat is, például a kitöltő színt vagy a vonalvastagságot?**  
A: Igen, a `LengthRecord` további beállítókat biztosít a kitöltés, vonal és átlátszóság módosításához. Tekintse meg az API dokumentációt a részletekért.

**Q: Lehetséges több PSD fájlt kötegelt módon feldolgozni?**  
A: Természetesen. A kódot helyezze egy ciklusba, amely egy PSD‑k könyvtárát iterálja, minden alkalommal beállítva a bemeneti és kimeneti útvonalakat.

**Q: Kézzel kell bezárni a stream‑eket, ha fájlvonalról töltök be?**  
A: A `Image.load` metódus belsőleg kezeli a fájl stream‑eket, de ha `InputStream`‑ből tölt be, azt a használat után manuálisan kell bezárni.

**Q: Mely Aspose.PSD verzió szükséges ezekhez az API‑khoz?**  
A: A `LengthRecord` és a `PathOperations` osztályok az Aspose.PSD 20.10‑es verziójától érhetők el. Ajánlott a legújabb verzió használata.

---

**Last Updated:** 2025-12-17  
**Tested With:** Aspose.PSD for Java 24.11  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}