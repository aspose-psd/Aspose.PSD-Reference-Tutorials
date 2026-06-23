---
date: 2026-06-23
description: Ismerje meg, hogyan mentse el a PSD-t PNG-ként, cserélje ki a hiányzó
  betűtípusokat, és exportáljon képeket az Aspose.PSD for Java használatával – gyorsan
  kezelje a hiányzó betűtípusokkal rendelkező PSD fájlokat.
keywords:
- save psd as png
- how to replace fonts
- convert psd to bmp
- export psd to jpeg
- handle missing fonts psd
linktitle: Betűtípusok cseréje
schemas:
- author: Aspose
  dateModified: '2026-06-23'
  description: Learn how to save PSD as PNG, replace missing fonts, and export images
    using Aspose.PSD for Java – handle missing fonts PSD files quickly.
  headline: How to Save PSD as PNG and Replace Missing Fonts in Java with Aspose
  type: TechArticle
- questions:
  - answer: Yes. While the primary use‑case is PSD, Aspose.PSD also supports PNG,
      JPEG, BMP, and TIFF, allowing font replacement wherever text layers exist.
    question: Can I replace fonts in other image formats besides PSD?
  - answer: No. You can set any TrueType font you prefer, or omit the setting to let
      Aspose use its internal default.
    question: Is the default replacement font mandatory?
  - answer: A commercial license is required for production deployments. See the [purchase
      page](https://purchase.aspose.com/buy) for details.
    question: Are there licensing requirements for using Aspose.PSD?
  - answer: Absolutely. Aspose offers free temporary licenses for evaluation – visit
      the [temporary license page](https://purchase.aspose.com/temporary-license/).
    question: Can I obtain a temporary license for testing?
  - answer: 'The community forum is a great place to ask questions: [Aspose.PSD forum](https://forum.aspose.com/c/psd/34).'
    question: Where can I find additional support or discuss Aspose.PSD‑related issues?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Hogyan mentse el a PSD-t PNG-ként, és cserélje ki a hiányzó betűtípusokat Java-ban
  az Aspose segítségével
url: /hu/java/advanced-image-manipulation/replace-fonts/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD mentése PNG-ként – Hiányzó betűkészletek cseréje Java-ban

## Bevezetés

Ha **save PSD as PNG**-t kell végeznie, miközben hiányzó vagy nem kívánt betűtípusokat cserél egy Photoshop (PSD) fájlban, az Aspose PSD betűkészlet helyettesítés egyszerűvé teszi ezt. Java alkalmazásokban betölthet egy PSD-t, megadhatja az Aspose-nak, melyik helyettesítő betűtípust használja, majd exportálhatja a javított képet bármilyen formátumban. Ez az útmutató végigvezeti a teljes munkafolyamaton – a projekt beállításától a frissített PNG exportálásáig – hogy megbízhatóan **handle missing fonts PSD** helyzeteket kezelhessen anélkül, hogy valaha megnyitná a Photoshopot.

## Gyors válaszok

- **Melyik könyvtár kezeli a betűkészlet helyettesítést?** Aspose.PSD for Java  
- **Mennyi időt vesz igénybe a megvalósítás?** Körülbelül 5‑10 perc egy alap esethez  
- **Melyik betűtípust használja alapértelmezett helyettesítőként?** Bármely TrueType betűtípust beállíthat, pl. “Arial”  
- **Menthetek más formátumokba is, mint a PNG?** Igen – a PSD, JPEG, BMP és további formátumok támogatottak  
- **Szükség van licencre a termeléshez?** Érvényes Aspose.PSD licenc szükséges nem‑próba használathoz  

## Mi az Aspose PSD betűkészlet helyettesítés?

Az Aspose PSD betűkészlet helyettesítés egy olyan folyamat, amely során megad egy helyettesítő betűtípust, amelyet a könyvtár használ, amikor hiányzó vagy nem támogatott betűtípust talál egy PSD fájlban. Ez biztosítja, hogy a szövegrétegek helyesen jelenjenek meg manuális Photoshop szerkesztés nélkül, és lehetővé teszi a **handle missing fonts PSD** fájlok automatikus kezelését.

## Miért használjuk az Aspose.PSD for Java-t?

Az Aspose.PSD for Java átfogó, nagy teljesítményű megoldást kínál a Photoshop fájlok közvetlen Java kódból történő kezelésére, ezzel kiküszöbölve a Photoshop szükségességét. Széles körű rétegtípusokat, effektusokat és nagy fájlméreteket támogat, miközben egyszerű API-kat biztosít olyan feladatokhoz, mint a betűkészlet helyettesítés, képkonverzió és metaadatkezelés.

- **Teljes körű PSD kezelés** – az Aspose.PSD támogat **30+ rétegtípust**, **20+ effektust**, és képes **2 GB**-ig terjedő fájlokat feldolgozni anélkül, hogy az egész dokumentumot a memóriába töltené.  
- **Keresztplatformos** – minden olyan operációs rendszeren működik, amely támogatja a Java 8+ verziót.  
- **Nincsenek külső függőségek** – a könyvtár belsőleg kezeli a betűkészlet helyettesítést, így nem kell extra betűtípusokat szállítania az alkalmazásával.  

## Hogyan cseréljünk hiányzó betűkészleteket PSD-ben az Aspose PSD használatával

A hiányzó betűkészletek cseréjéhez először betölti a PSD-t egy a betöltési beállításokban meghatározott helyettesítő betűtípussal, majd rendereli vagy elmenti a képet. A könyvtár automatikusan helyettesíti a hiányzó betűtípusokat a megadott betűtípussal, biztosítva, hogy a vizuális kimenet megfeleljen az elvárásainak manuális szerkesztés nélkül.

## Előfeltételek

- **Java Development Kit (JDK)** – 8 vagy annál újabb verzió telepítve.  
- **Aspose.PSD for Java** – töltse le a legújabb JAR-t a [release page](https://releases.aspose.com/psd/java/) oldalról.  
- **IDE** – IntelliJ IDEA, Eclipse vagy bármely kedvelt szerkesztő.  

## Csomagok importálása

A `PsdImage` osztály egy Photoshop dokumentumot képvisel a memóriában, hozzáférést biztosítva a rétegekhez, szöveghez és a renderelési lehetőségekhez. A `PsdLoadOptions` szabályozza, hogyan olvassa be a fájlt, beleértve a helyettesítő betűtípust, míg a `SaveOptions` (vagy formátum‑specifikus alosztályok) meghatározzák, hogyan íródik ki a kép.

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.PngOptions;
```

## 1. lépés: A dokumentum könyvtár beállítása

Adja meg azt a mappát, amely a forrás PSD fájlt tartalmazza. Cserélje le a helyőrzőt a gépén lévő tényleges útvonalra.

A `File` objektum egyszerűen a feldolgozni kívánt PSD-re mutat; itt nincs szükség további konfigurációra.

```java
String dataDir = "Your Document Directory";
```

## 2. lépés: A kép betöltése helyettesítő betűtípussal

Hozzon létre egy `PsdLoadOptions` példányt, állítsa be az alapértelmezett helyettesítő betűtípust (pl. **Arial**), és töltse be a PSD-t. Az Aspose automatikusan alkalmazza a helyettesítőt, amikor hiányzó betűtípust talál.

A `PsdLoadOptions` lehetővé teszi a betöltési viselkedés meghatározását, beleértve a helyettesítő betűtípust, amely a hiányzó betűtípusokat a importálási fázis során helyettesíti.

```java
PsdLoadOptions psdLoadOptions = new PsdLoadOptions(); 
psdLoadOptions.setDefaultReplacementFont("Arial");

PsdImage psdImage = (PsdImage)Image.load(dataDir + "Cloud_AzPlat_Banner3A_SB_EN_US_160x600_chinese_font.psd", psdLoadOptions);
```

## 3. lépés: A helyettesített kép mentése PNG-ként

A betűkészlet helyettesítése után exportálhatja a képet bármely támogatott formátumban. Itt PNG-ként mentjük, de választhat JPEG-et, BMP-t vagy akár visszaírhatja PSD-be is.

A `PsdImage` `save` metódusa egy `SaveOptions` objektumot fogad; a `PngOptions` használata biztosítja, hogy a kimenet egy veszteségmentes PNG legyen, amely alkalmas webes vagy további feldolgozásra.

```java
PngOptions pngOptions = new PngOptions();
psdImage.save(dataDir + "replaced_font.png", pngOptions);
```

## Hogyan menthetem a PSD-t PNG-ként a betűkészletek helyettesítése után?

Töltse be a PSD-t egy helyettesítő betűtípussal, majd hívja meg a `psdImage.save("output.png", new PngOptions())` metódust. Ez az egy soros mentési művelet egy teljesen renderelt PNG-t ír ki, amely tükrözi a helyettesített betűtípust, lehetővé téve a kép beágyazását bárhol a hiányzó betűkészletek miatti aggodalom nélkül. Győződjön meg róla, hogy a mentés előtt alkalmazta a helyettesítő betűtípust, és opcionálisan állítsa be a PNG tömörítési beállításokat a `PngOptions` objektumon keresztül az optimális fájlméret érdekében.

## Gyakori problémák és megoldások

| Probléma | Ok | Megoldás |
|----------|----|----------|
| A szöveg eltorzul a helyettesítés után | A helyettesítő betűtípus nem tartalmazza a szükséges glypheket | Válasszon egy betűtípust, amely támogatja a szükséges Unicode tartományt (pl. “Arial Unicode MS”). |
| `OutOfMemoryError` nagy PSD-k esetén | Nagyon nagy felbontású fájl betöltése nem elegendő heap memória nélkül | Növelje a JVM heap méretét (`-Xmx2g`), vagy ha elérhető, töltse be a képet streaming módban. |
| Licenc kivétel | A próbaverzió használata éles környezetben | Alkalmazzon érvényes állandó vagy ideiglenes licencet a kép betöltése előtt. |

## Gyakran feltett kérdések

**Q: Cserélhetek betűkészleteket más képformátumokban is a PSD-n kívül?**  
A: Igen. Bár az elsődleges felhasználási eset a PSD, az Aspose.PSD támogatja a PNG, JPEG, BMP és TIFF formátumokat is, lehetővé téve a betűkészlet cseréjét bárhol, ahol szövegrétegek vannak.

**Q: Kötelező az alapértelmezett helyettesítő betűtípus?**  
A: Nem. Beállíthat bármely TrueType betűtípust, vagy elhagyhatja a beállítást, hogy az Aspose a belső alapértelmezettet használja.

**Q: Vannak licencelési követelmények az Aspose.PSD használatához?**  
A: Kereskedelmi licenc szükséges a termelési környezetben történő telepítéshez. A részletekért tekintse meg a [purchase page](https://purchase.aspose.com/buy) oldalt.

**Q: Kaphatok ideiglenes licencet teszteléshez?**  
A: Természetesen. Az Aspose ingyenes ideiglenes licenceket kínál értékeléshez – látogassa meg a [temporary license page](https://purchase.aspose.com/temporary-license/) oldalt.

**Q: Hol találok további támogatást vagy vitathatom az Aspose.PSD‑hez kapcsolódó kérdéseket?**  
A: A közösségi fórum nagyszerű hely a kérdések feltevésére: [Aspose.PSD forum](https://forum.aspose.com/c/psd/34).

**Q: Hogyan kezeljek PSD fájlokat, amelyek több hiányzó betűtípust tartalmaznak?**  
A: Állítsa be egyszer az alapértelmezett helyettesítő betűtípust (ahogy bemutattuk) – ez a *minden* hiányzó betűtípusra alkalmazásra kerül a betöltési művelet során.

**Q: Lehetséges a betűkészletek cseréje a kép mentése után?**  
A: A betűkészlet helyettesítésnek a betöltési fázisban kell megtörténnie. A betűkészletek későbbi módosításához töltse be újra a PSD-t egy másik helyettesítő betűtípussal, majd mentse újra.

## Összegzés

Most már látta a teljes **save psd as png** munkafolyamatot Java-ban – a megfelelő osztályok importálásától, a helyettesítő betűtípus konfigurálásán, a PSD betöltésén, egészen a javított PNG exportálásáig. Alkalmazza ezt a mintát a képfeldolgozó csővezetékekben, hogy biztosítsa a konzisztens tipográfiát minden PSD eszközön, és automatikusan **handle missing fonts PSD**.

---

**Legutóbb frissítve:** 2026-06-23  
**Tesztelve a következővel:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**Szerző:** Aspose

## Kapcsolódó oktatóanyagok

- [Beállítások a hiányzó betűkészletek cseréjéhez az Aspose.PSD for Java-ban](/psd/java/advanced-techniques/settings-replacing-missing-fonts/)
- [PSD mentése PNG-ként és renderelt árnyék alkalmazása az Aspose.PSD for Java-ban](/psd/java/advanced-image-manipulation/rendering-drop-shadow/)
- [Hogyan konvertáljunk PSD-t PNG-re és méretezzünk arányosan az Aspose.PSD for Java-val](/psd/java/advanced-image-manipulation/resize-image-proportionally/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< blocks/products/products-backtop-button >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}