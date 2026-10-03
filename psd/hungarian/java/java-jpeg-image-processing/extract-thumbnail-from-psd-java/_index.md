---
date: 2026-10-03
description: Ismerje meg, hogyan lehet miniaturát kinyerni PSD-ből Java-ban az Aspose.PSD
  használatával. Ez a lépésről‑lépésre útmutató bemutatja a beállítást, a kódrészleteket,
  és a miniaturák JPEG képként való mentését.
keywords:
- extract thumbnail from psd
- java aspose psd
- psd thumbnail extraction
lastmod: 2026-10-03
linktitle: Miniatűr kinyerése PSD-ből Java-ban
og_description: Ismerje meg, hogyan kell miniaturát kinyerni PSD-ből Java-ban az Aspose.PSD-vel.
  Ez az útmutató végigvezeti a beállításon, a fájl betöltésén, a miniaturák kinyerésén,
  és a JPEG képként való mentésen.
og_image_alt: Screenshot showing Java code extracting a thumbnail from a PSD file
  using Aspose.PSD
og_title: Miniatűr kinyerése PSD-ből Java-ban az Aspose.PSD használatával
schemas:
- author: Aspose
  dateModified: '2026-10-03'
  description: Learn how to extract thumbnail from PSD in Java using Aspose.PSD. This
    step‑by‑step guide covers setup, code snippets, and saving the thumbnail as a
    JPEG image.
  headline: Extract thumbnail from PSD in Java
  type: TechArticle
- questions:
  - answer: Aspose.PSD is a Java library that enables programmatic creation, manipulation,
      and conversion of PSD and other raster image formats without requiring Adobe
      Photoshop.
    question: What is Aspose.PSD?
  - answer: You can refer to the [documentation](https://reference.aspose.com/psd/java/)
      for detailed API references and examples.
    question: Where can I find more documentation on Aspose.PSD for Java?
  - answer: Yes, you can download a [free trial](https://releases.aspose.com/) to
      evaluate the library’s capabilities.
    question: Can I try Aspose.PSD for free before purchasing?
  - answer: Temporary licenses are available from the [temporary license](https://purchase.aspose.com/temporary-license/)
      page.
    question: How can I obtain a temporary license for Aspose.PSD?
  - answer: Yes, Aspose.PSD can be used in both personal and commercial projects under
      its licensing terms.
    question: Is Aspose.PSD suitable for commercial use?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java image processing
- aspose.psd
- thumbnail extraction
title: Miniatűr kinyerése PSD-ből Java-ban
url: /hu/java/java-jpeg-image-processing/extract-thumbnail-from-psd-java/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD-ből bélyegkép kinyerése Java-ban

## Bevezetés
A PSD fájlból bélyegkép kinyerése lehetővé teszi, hogy gyors előnézeteket generáljon a teljes felbontású kép betöltése nélkül. Java-ban az Aspose.PSD egyszerűvé és hatékonnyá teszi ezt a folyamatot. Ebben az oktatóanyagban megtanulja, hogyan állítsa be a könyvtárat, hogyan találja meg a bélyegkép erőforrást, és hogyan mentse JPEG fájlként – mindezt néhány kódsorral.

## Gyors válaszok
- **Melyik könyvtár kezeli a PSD bélyegképeket?** Aspose.PSD for Java.
- **Hány kódsorra van szükség?** Körülbelül öt sor a betöltéshez, kinyeréshez és mentéshez.
- **Kinyerhetek bélyegképeket nagy PSD fájlokból?** Igen, az Aspose.PSD 500 MB-ig terjedő fájlokat dolgoz fel a teljes memória betöltése nélkül.
- **Szükségem van licencre a fejlesztéshez?** Egy ingyenes próba a kiértékeléshez elegendő; a termeléshez licenc szükséges.
- **Milyen kimeneti formátumok támogatottak?** A kinyert bélyegkép menthető JPEG, PNG vagy BMP formátumban.

## Mi az a PSD-ből bélyegkép kinyerése?
A PSD-ből bélyegkép kinyerése a Photoshop (PSD) dokumentumban beágyazott kis előnézeti kép olvasásának folyamata. Ez az előnézet erőforrásként van tárolva, és önállóan menthető katalógusba vagy megjelenítés céljából. A bélyegkép általában alacsony felbontású ábrázolás, amelyet az alkalmazások a teljes méretű kép betöltése nélkül használnak gyors vizuális összefoglaló megjelenítésére.

## Miért használja az Aspose.PSD-t ehhez a feladathoz?
Az Aspose.PSD **30+ képformátumot** támogat, és akár **500 MB**-ig terjedő PSD fájlokat is képes kezelni, miközben alacsony memóriahasználatot biztosít, mivel az erőforrásokat igény szerint olvassa. Az API erős hibakezelést is nyújt, így megbízhatóan kinyerhetőek a bélyegképek még sérült fájlokból is.

## Előkövetelmények
- Telepített Java Development Kit (JDK).
- Az Aspose.PSD for Java könyvtár letöltve innen: [Aspose.PSD for Java download](https://releases.aspose.com/psd/java/).
- Alapvető ismeretek a Java szintaxisról és a projekt beállításáról.

## Hogyan nyer ki bélyegképet egy PSD fájlból Java-ban?
Töltse be a PSD fájlt a `PsdImage` osztállyal, keresse meg a `ThumbnailResource`-t, és mentse a képadatait JPEG-ként. Az Aspose.PSD elrejti az alacsony szintű elemzést, így csak a `getResources()`-t kell meghívnia, majd a kinyert képen a `save()`-t. Ez a megközelítés minden olyan PSD-re működik, amely tartalmaz bélyegképet, a fájlmérettől függetlenül.

## Csomagok importálása
`Image` az alaposztály a képek betöltéséhez. `PsdImage` egy PSD dokumentumot képvisel. A `ThumbnailResource` és a `Thumbnail4Resource` a bélyegkép erőforrásokat jelölik. A `JpegOptions` a JPEG mentési beállításokat határozza meg.

```text
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
import com.aspose.psd.imageoptions.JpegOptions;
```
```

## 1. lépés: PSD fájl betöltése
Először hozzon létre egy `PsdImage` példányt, amely az Ön PSD fájljára mutat. A konstruktor csak a fejlécet és a szükséges erőforrásokat olvassa be, így a memóriahasználat minimális.

```text
```java
String dataDir = "Your_Document_Directory/";
PsdImage image = (PsdImage)Image.load(dataDir + "your_file.psd");
```
```

Cserélje le a `"Your_Document_Directory/"`-t arra a könyvtárra, ahol a PSD fájlja található, és a `"your_file.psd"`-t a PSD fájl nevére.

## 2. lépés: képi erőforrások bejárása
Az Aspose.PSD a bélyegképeket `ThumbnailResource` objektumokként tárolja a kép erőforrásgyűjteményében. Iteráljon végig a gyűjteményen, ellenőrizze az erőforrás típusát, és rögzítse az első található bélyegképet.

```text
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource) {
        ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
        
        // Extract thumbnail data
        int[] data = thumbnail.getThumbnailArgb32Data();
        
        // Create a new image with the extracted thumbnail data
        PsdImage extractedThumbnailImage = new PsdImage(thumbnail.getWidth(), thumbnail.getHeight());
        extractedThumbnailImage.saveArgb32Pixels(extractedThumbnailImage.getBounds(), data);
        
        // Save the extracted thumbnail as a separate JPEG file
        extractedThumbnailImage.save(dataDir + "extracted_thumbnail.jpg", new JpegOptions());
        
        // Output success message
        System.out.println("Thumbnail extracted and saved successfully.");
        
        break; // Exit the loop once thumbnail is found and processed
    }
}
```
```

## 3. lépés: kinyert bélyegkép mentése
Miután megvan a bélyegkép, hívja meg a `save` metódust a lemezre írásához. Választhat JPEG, PNG vagy BMP formátumot; a JPEG a leggyakoribb a webes előnézetekhez.

## 4. lépés: különböző bélyegkép típusok kezelése
Ha egy PSD több bélyegkép változatot tartalmaz, például `Thumbnail4Resource`, bővítse a cikluslogikát, hogy minden típust ellenőrizzen. Az API külön osztályokat biztosít minden erőforráshoz, így kiválaszthatja a szükséges felbontást.

## Gyakori problémák és megoldások
- **Nincs bélyegkép:** Nem minden PSD fájl tartalmaz előnézetet. Ellenőrizze a forrásfájlt a Photoshop „File → File Info” paneljén.
- **Nem támogatott formátum hiba:** Győződjön meg arról, hogy a legújabb Aspose.PSD verziót használja; a régebbi kiadások hiányozhatnak a újabb bélyegkép erőforrás típusokból.
- **Memóriahiány nagy fájlok esetén:** Használja a `PsdImage.load(..., LoadOptions)`-t a `LoadOptions.setLoadResourcesOnly(true)` beállítással, hogy elkerülje a teljes képadat betöltését, ha csak a bélyegképre van szüksége.

## Gyakran ismételt kérdések

**Q: Mi az Aspose.PSD?**  
A: Az Aspose.PSD egy Java könyvtár, amely lehetővé teszi a PSD és más raszteres képformátumok programozott létrehozását, manipulálását és konvertálását Adobe Photoshop nélkül.

**Q: Hol találok további dokumentációt az Aspose.PSD for Java-hoz?**  
A: A részletes API referenciákért és példákért tekintse meg a [documentation](https://reference.aspose.com/psd/java/) oldalt.

**Q: Próbálhatom ingyenesen az Aspose.PSD-t vásárlás előtt?**  
A: Igen, letölthet egy [free trial](https://releases.aspose.com/) verziót a könyvtár képességeinek kiértékeléséhez.

**Q: Hogyan szerezhetek ideiglenes licencet az Aspose.PSD-hez?**  
A: Ideiglenes licencek elérhetők a [temporary license](https://purchase.aspose.com/temporary-license/) oldalon.

**Q: Alkalmas-e az Aspose.PSD kereskedelmi felhasználásra?**  
A: Igen, az Aspose.PSD személyes és kereskedelmi projektekben egyaránt használható a licencfeltételek szerint.

**Utolsó frissítés:** 2026-10-03  
**Tesztelve ezzel:** Aspose.PSD for Java 24.12  
**Szerző:** Aspose

## Kapcsolódó oktatóanyagok

- [Hogyan konvertáljon PSD-t raszteres képformátumokra az Aspose.PSD for Java segítségével](/psd/java/advanced-techniques/convert-psd-to-raster-formats/)
- [PSD mentése JPEG-ként és RGB szín támogatása az Aspose.PSD Java-val](/psd/java/advanced-psd-layer-features-effects/support-rgb-color-psd-files/)
- [Kép átméretezése az Aspose.PSD for Java-val – Alakzatok rajzolása és alapvető képműveletek](/psd/java/basic-image-operations/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}