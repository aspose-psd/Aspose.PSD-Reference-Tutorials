---
title: Stroke Layer Pattern hozzáadása Java-ban
linktitle: Stroke Layer Pattern hozzáadása Java-ban
second_title: Aspose.PSD Java API
description: Ismerje meg, hogyan adhat hozzá körvonal-rétegmintát PSD-fájlokhoz az Aspose.PSD for Java használatával. Kövesse ezt a lépésenkénti útmutatót a képek egyszerű javításához.
weight: 11
url: /hu/java/java-graphics-drawing/add-stroke-layer-pattern/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Stroke Layer Pattern hozzáadása Java-ban

## Bevezetés
körvonalréteg-minta hozzáadása egy képhez Java nyelven ijesztő feladatnak tűnhet, de az Aspose.PSD for Java segítségével ez egyszerűbb, mint gondolná. Akár grafikát tervez, akár fotószerkesztő alkalmazásokkal dolgozik, ez az útmutató lépésről lépésre végigvezeti a folyamaton. Készen áll az indulásra? Merüljünk el!
## Előfeltételek
Mielőtt elkezdené, szüksége lesz néhány dologra:
- Java Development Kit (JDK): Győződjön meg arról, hogy a JDK telepítve van a rendszeren.
-  Aspose.PSD for Java: Töltse le a könyvtárat innen[itt](https://releases.aspose.com/psd/java/) és vegye fel a projektjébe.
- Egy IDE: Használja kedvenc integrált fejlesztőkörnyezetét (IDE), például az IntelliJ IDEA-t vagy az Eclipse-t.
## Csomagok importálása
Először is importálnia kell a szükséges csomagokat a Java projektbe. Ezek a csomagok elengedhetetlenek az Aspose.PSD használatához.
```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;
import com.aspose.psd.examples.Utils.Assert;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.PatternFillSettings;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.fileformats.psd.layers.layerresources.PattResource;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import java.util.UUID;
```
## 1. lépés: Töltse be a PSD fájlt
A körvonal-rétegminta hozzáadásának első lépése a szerkeszteni kívánt PSD-fájl betöltése.
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```
A PSD-fájl betöltésével mostantól hozzáférhet és kezelheti a rétegeit és hatásait.
## 2. lépés: Készítsen új mintaadatokat
Ezután elő kell készítenie az új mintaadatokat, amelyeket a körvonalrétegre fog alkalmazni.
```java
int[] newPattern = new int[]
{
    Color.getAqua().toArgb(), Color.getRed().toArgb(), Color.getRed().toArgb(), Color.getAqua().toArgb(),
    Color.getAqua().toArgb(), Color.getWhite().toArgb(), Color.getWhite().toArgb(), Color.getAqua().toArgb(),
    Color.getAqua().toArgb(), Color.getWhite().toArgb(), Color.getWhite().toArgb(), Color.getAqua().toArgb(),
    Color.getAqua().toArgb(), Color.getRed().toArgb(), Color.getRed().toArgb(), Color.getAqua().toArgb(),
};
Rectangle newPatternBounds = new Rectangle(0, 0, 4, 4);
UUID guid = UUID.randomUUID();
```
Ez a mintaadat lesz az új körvonal-effektus létrehozásához.
## 3. lépés: A Stroke Effect elérése
A körvonal-effektus módosításához hozzá kell férnie az adott réteghez és annak keverési beállításaihoz.
```java
StrokeEffect patternStroke = (StrokeEffect)im.getLayers()[3].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Normal, patternStroke.getBlendMode());
Assert.areEqual(255, patternStroke.getOpacity());
Assert.areEqual(true, patternStroke.isVisible());
PatternFillSettings fillSettings = (PatternFillSettings)patternStroke.getFillSettings();
Assert.areEqual(FillType.Pattern, fillSettings.getFillType());
```
Ez biztosítja, hogy a megfelelő réteggel és effektussal dolgozzon.
## 4. lépés: Módosítsa a Stroke Effect-et
Most módosítsuk a körvonal-effektust az új mintaadatokkal.
### Frissítse a Stroke Effect tulajdonságait
```java
patternStroke.setOpacity((byte)127);
patternStroke.setBlendMode(BlendMode.Color);
```
### Frissítse a mintaforrást
```java
PattResource resource;
for (int i = 0; i < im.getGlobalLayerResources().length; i++)
{
    if (im.getGlobalLayerResources()[i] instanceof PattResource)
    {
        resource = (PattResource)im.getGlobalLayerResources()[i];
        resource.setPatternId(guid.toString());
        resource.setName("$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0");
        resource.setPattern(newPattern, newPatternBounds);
    }
}
```
Ez a kódrészlet frissíti a mintaerőforrást az új mintaadatokkal.
## 5. lépés: Alkalmazza az új mintát
Végül alkalmazza az új mintát a körvonal-effektusra, és mentse el a változtatásokat.
```java
((PatternFillSettings)patternStroke.getFillSettings()).setPatternName("$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0");
((PatternFillSettings)patternStroke.getFillSettings()).setPatternId(guid.toString() + "\0");
im.save(exportPath);
```
Ez biztosítja az új minta helyes alkalmazását, és a fájl mentését a módosításokkal együtt.
## 6. lépés: Ellenőrizze a változtatásokat
Annak érdekében, hogy minden megfelelően működjön, töltse be újra a fájlt, és ellenőrizze a változtatásokat.
```java
PsdImage img = (PsdImage)Image.load(sourceFileName, loadOptions);
StrokeEffect patternStrokeEffect = (StrokeEffect)img.getLayers()[3].getBlendingOptions().getEffects()[0];
PattResource resource1 = null;
for (int i = 0; i < img.getGlobalLayerResources().length; i++)
{
    if (img.getGlobalLayerResources()[i] instanceof PattResource)
    {
        resource1 = (PattResource)img.getGlobalLayerResources()[i];
    }
}
try
{
    Assert.areEqual(newPattern, resource1.getPatternData());
    Assert.areEqual(newPatternBounds, new Rectangle(0, 0, resource1.getWidth(), resource1.getHeight()));
    Assert.areEqual(guid.toString(), resource1.getPatternId());
    Assert.areEqual(BlendMode.Color, patternStrokeEffect.getBlendMode());
    Assert.areEqual(127, patternStrokeEffect.getOpacity());
    Assert.areEqual(true, patternStrokeEffect.isVisible());
    PatternFillSettings fillSettings1 = (PatternFillSettings)patternStrokeEffect.getFillSettings();
    Assert.areEqual(FillType.Pattern, fillSettings1.getFillType());
}
catch (Exception e)
{
    System.out.println(e.getMessage());
}
```
Ez a lépés ellenőrzi, hogy a mintaadatokat megfelelően alkalmazták-e a körvonal-effektushoz.
## Következtetés
És megvan! Sikeresen hozzáadott egy körvonal-rétegmintát egy PSD-fájlhoz az Aspose.PSD for Java használatával. Az alábbi lépések követésével könnyedén testreszabhatja és javíthatja képeit. Boldog kódolást!
## GYIK
### Mi az Aspose.PSD for Java?
Az Aspose.PSD for Java egy olyan könyvtár, amely lehetővé teszi a fejlesztők számára a PSD (Photoshop Document) fájlok programozott létrehozását, szerkesztését és konvertálását.
### Használhatom az Aspose.PSD for Java-t kereskedelmi projektekben?
 Igen, használhatja kereskedelmi projektekben. Engedélyt vásárolhat innen[itt](https://purchase.aspose.com/buy).
### Elérhető az Aspose.PSD for Java ingyenes próbaverziója?
 Igen, letölthet egy ingyenes próbaverziót a webhelyről[itt](https://releases.aspose.com/).
### Hogyan kaphatok támogatást az Aspose.PSD for Java számára?
 Támogatást kaphat az Aspose közösségi fórumokon[itt](https://forum.aspose.com/c/psd/34).
### Mik az Aspose.PSD for Java rendszerkövetelményei?
A fejlesztéshez telepíteni kell a JDK-t és egy IDE-t. A könyvtár több operációs rendszert támogat, beleértve a Windowst, a Linuxot és a macOS-t.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
