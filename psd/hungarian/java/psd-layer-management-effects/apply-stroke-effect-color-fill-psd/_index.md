---
date: 2026-04-03
description: Tanulja meg, hogyan menthet PSD‑t PNG‑ként vonalhatással és színkitöltéssel
  az Aspose.PSD for Java használatával. Ez a lépésről‑lépésre útmutató gyorsan bemutatja
  a PSD PNG‑re exportálását.
keywords:
- save psd as png
- export psd to png
- set stroke color
- apply layer effects
- customize stroke width
linktitle: PSD mentése PNG‑ként vonalhatással – Java
second_title: Aspose.PSD Java API
title: PSD mentése PNG-ként vonalhatással – Java
url: /hu/java/psd-layer-management-effects/apply-stroke-effect-color-fill-psd/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD mentése PNG-ként vonalhatással és színkitöltéssel – Java

## Bevezetés

Ebben az útmutatóban megtanulja, hogyan **mentse a PSD-t PNG-ként**, miközben vonalhatást alkalmaz színkitöltéssel az Aspose.PSD for Java segítségével. Akár tapasztalt fejlesztő vagy, akár most kezd, ez a lépésről‑lépésre tutorial egyszerűvé teszi a feladat elvégzését. Mindent lefedünk a környezet beállításától a végső kép exportálásáig, így gyorsan **exportálhatja a PSD-t PNG-be** saját projektjeiben.

## Gyors válaszok
- **Mi a tutorial célja?** Bemutatja, hogyan menthet egy PSD fájlt PNG-ként egy testreszabható vonalhatás alkalmazása után.  
- **Melyik könyvtárat használja?** Aspose.PSD for Java.  
- **Szükségem van licencre?** Egy ingyenes próba a teszteléshez működik; licenc szükséges a termeléshez.  
- **Módosíthatom a vonal színét?** Igen – bármilyen színt beállíthat a `ColorFillSettings` segítségével.  
- **Lehetséges a kötegelt feldolgozás?** Természetesen – a kódot egy ciklusba ágyazva több PSD fájlt is feldolgozhat.

## Mi az a „PSD mentése PNG‑ként”?
A PSD PNG‑ként való mentése azt jelenti, hogy a Photoshop natív réteges fájlját egy lapos, web‑barát képfájlformátummá konvertálja, miközben megőrzi a vizuális hűséget. Ez akkor hasznos, ha PSD tartalmat kell megjeleníteni weboldalakon, mobilalkalmazásokban vagy bármely platformon, amely közvetlenül nem támogatja a PSD fájlokat.

## Miért alkalmazzunk vonalhatást színkitöltéssel?
A vonalhatás éles körvonalat ad a réteg tartalmához, így a grafikák kiemelkednek a komplex háttér előtt. A testreszabott kitöltőszín kombinálásával márkázott képeket, UI elemeket emelhet ki, vagy figyelemfelkeltő bélyegképeket hozhat létre Photoshop elhagyása nélkül.

## Előfeltételek

1. **Java Development Kit (JDK) 8+** – győződjön meg róla, hogy a `java` elérhető a PATH‑ban.  
2. **Aspose.PSD for Java** – töltse le a [weboldalról](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse vagy bármely kedvenc szerkesztő.  
4. **Minta PSD** – egy fájl, amely már tartalmaz vonalhatást (vagy adjon hozzá egyet Photoshopban).  
5. **Alap Java ismeretek** – néhány sor kódot fog írni, de semmi haladó.

Miután ezek készen állnak, elkezdhetjük a kódolást.

## Csomagok importálása

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.fillsettings.ColorFillSettings;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```

Ezek az importok tartalmazzák az összes szükséges osztályt a PSD betöltéséhez, a vonal módosításához, valamint a PSD és PNG kimenetek mentéséhez.

## Hogyan mentse a PSD-t PNG‑ként vonalhatással

### 1. lépés: PSD fájl betöltése

Először mutasson a mappára, amely a forrás PSD‑jét tartalmazza.

```java
String dataDir = "Your Document Directory";
```

Cserélje le a `"Your Document Directory"`-t a gépén lévő tényleges útvonalra.

Most töltse be a fájlt, miközben megőrzi a meglévő effektus erőforrásokat:

```java
String sourceFileName = dataDir + "StrokeComplex.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```

### 2. lépés: Vonal színének beállítása (és opcionálisan a szélesség testreszabása)

Az alábbi ciklus végigjárja az összes réteget, lekéri az első `StrokeEffect`‑et, és megváltoztatja a kitöltőszínét. A `StrokeEffect` objektumon a `setWidth` vagy `setPosition` metódusokkal is módosíthatja a **vonalvastagság testreszabását**, ha szükséges.

```java
for (int i = 0; i < im.getLayers().length; i++) {
    StrokeEffect effect = (StrokeEffect) im.getLayers()[i].getBlendingOptions().getEffects()[0];
    ColorFillSettings settings = (ColorFillSettings) effect.getFillSettings();
    // Set the stroke color – change to any Color you like
    settings.setColor(Color.getDeepPink());
}
```

> **Pro tipp:** A `Color.getDeepPink()` csak egy példa. Használja a `new Color(r, g, b)`‑t egyedi RGB értékekhez.

### 3. lépés: Módosított PSD mentése (opcionális)

Ha szeretne egy PSD verziót megtartani a frissített vonallal, mentse így:

```java
String exportPath = dataDir + "StrokeComplexRendering.psd";
im.save(exportPath, new PsdOptions());
```

### 4. lépés: Kép exportálása PNG‑ként (a „PSD mentése PNG‑ként” fő lépés)

Végül konvertálja a szerkesztett PSD‑t egy web‑használatra kész PNG fájlba:

```java
String exportPathPng = dataDir + "StrokeComplexRendering.png";
PngOptions option = new PngOptions();
option.setColorType(PngColorType.TruecolorWithAlpha);

im.save(exportPathPng, option);
```

A PNG megőrzi a korábban beállított mélyrózsaszín vonalat, és a `TruecolorWithAlpha` opció biztosítja az átlátszóság megőrzését.

## Gyakori problémák és megoldások

| Probléma | Ok | Megoldás |
|----------|----|----------|
| **`ArrayIndexOutOfBoundsException`** | A rétegnek nincs effektusa, vagy az első effektus nem `StrokeEffect`. | Ellenőrizze, hogy a réteg valóban tartalmaz vonalat, vagy iteráljon a `getEffects()`‑en a megfelelő típus megtalálásához. |
| A szín nem változik | Lehet, hogy a beállítások másolatát szerkeszti az eredeti helyett. | Győződjön meg róla, hogy közvetlenül a `effect.getFillSettings()`‑ből castolja a `ColorFillSettings`‑t. |
| A PNG üresnek jelenik meg | A PSD réteg rasterizálása nélkül lett betöltve. | Hívja meg a `im.save(..., new PngOptions())`‑t minden módosítás után; kerülje el az eredeti `im` mentését a változtatások előtt. |

## Gyakran ismételt kérdések

**Q: Alkalmazhatok több effektust egyetlen rétegre az Aspose.PSD for Java használatával?**  
A: Igen, elérheti a réteg keverési beállításait, és annyi effektust adhat hozzá, amennyire szükség van, beleértve árnyékokat, ragyogásokat és vonalakat.

**Q: Lehetséges automatizálni a folyamatot több PSD fájlra?**  
A: Teljesen. A betöltési, effektus‑alkalmazási és mentési logikát egy `for‑each` ciklusba ágyazva, amely egy könyvtárban lévő fájlokon iterál.

**Q: Hogyan vonhatom vissza a PSD fájlra végzett módosításokat?**  
A: Töltse be újra az eredeti fájlt a módosítások mentése előtt; az Aspose.PSD nem biztosít visszavonási veremet.

**Q: Testreszabhatom a vonal vastagságát és pozícióját?**  
A: Igen. Használja a `effect.setWidth(float)` és `effect.setPosition(StrokeEffect.Position)` metódusokat a vastagság és elhelyezés (belső, külső vagy középső) szabályozásához.

**Q: Ingyenes-e az Aspose.PSD for Java könyvtár használata?**  
A: Egy ingyenes próba elérhető értékeléshez. A teljes funkcionalitáshoz megvásárolt licenc szükséges. Tekintse meg a [vásárlási lehetőségeket](https://purchase.aspose.com/buy) a részletekért.

---

**Utoljára frissítve:** 2026-04-03  
**Tesztelve:** Aspose.PSD 24.12 for Java  
**Szerző:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}