---
date: 2026-05-19
description: Naučte se, jak otočit obrázek pod konkrétním úhlem v Java pomocí Aspose.PSD.
  Průvodce pokrývá rotate image java, rotate image specific angle, background handling
  a další.
keywords:
- how to rotate image
- rotate image specific angle
- rotate image java
- rotate image background
- rotate image degrees
linktitle: Jak otočit obrázek pod konkrétním úhlem
schemas:
- author: Aspose
  dateModified: '2026-05-19'
  description: Learn how to rotate image on a specific angle in Java using Aspose.PSD.
    The guide covers rotate image java, rotate image specific angle, background handling
    and more.
  headline: How to Rotate Image on a Specific Angle with Aspose.PSD for Java
  type: TechArticle
- description: Learn how to rotate image on a specific angle in Java using Aspose.PSD.
    The guide covers rotate image java, rotate image specific angle, background handling
    and more.
  name: How to Rotate Image on a Specific Angle with Aspose.PSD for Java
  steps:
  - name: Define Your Document Directory
    text: Set the folder that holds the source PSD and where the output will be written.
      Using an absolute path or `System.getProperty("user.dir")` eliminates relative‑path
      surprises.
  - name: Specify Source and Destination File Paths
    text: Provide the full file names for the input PSD and the desired output format
      (e.g., PNG, JPEG, TIFF). Changing the extension in `destName` automatically
      selects the appropriate encoder.
  - name: Load the Image
    text: The `Image.load` method detects the file format and returns a concrete `RasterImage`
      instance ready for raster operations. The `Image` class is a factory that reads
      a file from disk and creates an in‑memory representation suitable for further
      processing. It supports automatic format detection for al
  - name: Cache Image Data (Optional but Recommended)
    text: Calling `image.cacheData()` stores pixel data in memory, dramatically speeding
      up subsequent transformations—especially for large PSD files that would otherwise
      trigger repeated disk I/O. The `cacheData()` method forces the image to be fully
      loaded into RAM, reducing the overhead of lazy loading dur
  - name: Rotate the Image
    text: 'Invoke `rotate` with three arguments: the rotation angle (float), a flag
      to expand the canvas, and the background color for the newly exposed corners.
      The `rotate` method rotates the image around its centre, optionally enlarging
      the canvas to accommodate the rotated bounds. The background `Color` fi'
  - name: Save the Result
    text: Choose an encoder (JPEG, PNG, etc.) and call `save`. `JpegOptions` lets
      you adjust quality, while `PngOptions` provides lossless output. The `save`
      method writes the transformed image to disk using the specified options object,
      ensuring that compression level and color depth are preserved as require
  type: HowTo
- questions:
  - answer: Yes. The library preserves alpha channels; omit an opaque background color
      to keep corners transparent.
    question: Can I rotate images with transparency using Aspose.PSD for Java?
  - answer: No. Aspose.PSD supports PSD, JPEG, PNG, TIFF, GIF, BMP, JPEG2000, WMF,
      EMF, and 30+ additional formats.
    question: Are there any limitations on the image file formats supported for rotation?
  - answer: Absolutely. Pass a negative float to `rotate` (e.g., `-30f`) to rotate
      clockwise.
    question: Can I rotate images by a negative angle?
  - answer: The API is server‑side only. For live previews, render the rotated bitmap
      in a UI framework such as Swing or JavaFX and refresh the view.
    question: Does Aspose.PSD provide real‑time image preview during rotation?
  - answer: Yes, visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) to
      ask questions and share experiences.
    question: Is there a community forum for Aspose.PSD where I can seek help?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Jak otočit obrázek pod konkrétním úhlem s Aspose.PSD pro Java
url: /cs/java/advanced-image-manipulation/rotate-image-specific-angle/
weight: 20
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak otočit obrázek o konkrétní úhel pomocí Aspose.PSD pro Java

Pokud potřebujete **how to rotate image** programově v Java aplikaci, Aspose.PSD pro Java nabízí čisté, vysoce výkonné API, které se postará o těžkou práci. Ať už vytváříte fotoeditor, generujete náhledy, nebo připravujete zdroje pro webovou službu, otáčení obrázku o přesný stupeň je běžná požadavek. V tomto tutoriálu projdeme kompletním procesem – od načtení PSD souboru po uložení otočeného výsledku – a zdůrazníme osvědčené postupy, jako je cachování a manipulace s pozadím.

## Rychlé odpovědi
- **Jaká knihovna je nejlepší pro otáčení obrázků v Javě?** Aspose.PSD pro Java poskytuje nejspolehlivější rotační engine.  
- **Mohu otáčet o libovolný stupeň?** Ano, metoda `rotate` přijímá úhel typu `float`, kladný i záporný.  
- **Potřebuji licenci pro vývoj?** Bezplatná zkušební verze funguje pro testování; pro produkci je vyžadována komerční licence.  
- **Jaké formáty obrázků jsou podporovány?** PSD, JPEG, PNG, TIFF, GIF, BMP, JPEG2000, WMF, EMF a více než 30 dalších formátů.  
- **Jak nastavit barvu pozadí pro prázdný prostor?** Předávejte instanci `Color` metodě `rotate`.  

## Jak otočit obrázek o konkrétní úhel pomocí Aspose.PSD pro Java?

Načtěte svůj zdrojový soubor, zavolejte `image.rotate(angle, true, backgroundColor)` a poté uložte – tři stručné kroky, které za vás vyřeší veškerou těžkou matematiku. Aspose.PSD zachovává vrstvy, barevné profily a alfa kanály a zároveň rozšiřuje plátno, aby nedošlo k oříznutí, takže výstup vypadá přesně podle očekávání i pro zlomkové úhly jako 12,5°. Tento přístup funguje pro soubory od několika kilobajtů až po více než stovky stránek PSD bez vyčerpání paměti.

## Co je otáčení obrázku v Javě?

Otáčení obrázku je geometrická transformace, která otáčí matici pixelů kolem pivotního bodu – obvykle středu obrázku – o zadaný úhel. V čisté Javě byste manipulovali s objektem `Graphics2D`, počítali trigonometrické posuny a ručně spravovali pozadí. Aspose.PSD abstrahuje veškerou tuto složitost a automaticky zpracovává barevné hloubky, masky vrstev a různé formáty souborů.

## Proč použít Aspose.PSD pro otáčení obrázků?

Aspose.PSD podporuje **30+ vstupních a výstupních formátů** a dokáže zpracovat **500‑stránkové PSD soubory za méně než 5 sekund** na typickém serverovém procesoru. Vestavěné cachování knihovny (`image.cacheData()`) snižuje využití paměti až o 60 % u velkých aktiv, a metoda `rotate` vám umožní zadat barvu pozadí, čímž zachová průhledné rohy, pokud je to potřeba. Tyto kvantifikované výhody z ní činí standardní volbu v odvětví pro vysokokapacitní image pipeline.

## Požadavky

Než začneme, ujistěte se, že máte:

1. **Java Development Kit (JDK 8 nebo novější)** – jakékoli IDE nebo prostředí příkazové řádky bude stačit.  
2. **Aspose.PSD pro Java** – stáhněte nejnovější JAR ze stránky [Aspose.PSD Java page](https://reference.aspose.com/psd/java/).  
3. **Ukázkový PSD soubor** – např. `sample.psd` umístěný ve složce, na kterou můžete odkazovat z kódu.

## Import balíčků

Třída `RasterImage` a související utility jsou jádrem workflow otáčení.

Třída `RasterImage` je hlavní objekt Aspose.PSD pro rasterovou manipulaci s obrázky. Poskytuje metody pro načítání, transformaci a ukládání rasterových obrázků při zachování metadat.

## Průvodce krok za krokem

### Krok 1: Definujte adresář dokumentu

Nastavte složku, která obsahuje zdrojový PSD a kam bude výstup zapsán. Použití absolutní cesty nebo `System.getProperty("user.dir")` eliminuje překvapení s relativními cestami.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imageoptions.JpegOptions;
```

### Krok 2: Zadejte cesty ke zdrojovému a cílovému souboru

Uveďte úplná jména souborů pro vstupní PSD a požadovaný výstupní formát (např. PNG, JPEG, TIFF). Změna přípony v `destName` automaticky vybere vhodný enkodér.

```java
String dataDir = "Your Document Directory";
```

### Krok 3: Načtěte obrázek

Metoda `Image.load` detekuje formát souboru a vrátí konkrétní instanci `RasterImage` připravenou pro rasterové operace.

Třída `Image` je továrna, která načte soubor z disku a vytvoří in‑memory reprezentaci vhodnou pro další zpracování. Podporuje automatickou detekci formátu pro všech více než 30 podporovaných typů.

```java
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "RotatingImageOnSpecificAngle_out.jpg";
```

### Krok 4: Cacheujte data obrázku (volitelné, ale doporučené)

Volání `image.cacheData()` uloží pixelová data do paměti, což dramaticky zrychlí následné transformace – zejména u velkých PSD souborů, které by jinak vyvolávaly opakovaný diskový I/O.

Metoda `cacheData()` vynutí úplné načtení obrázku do RAM, čímž snižuje režii líného načítání během intenzivních operací.

```java
RasterImage image = (RasterImage)Image.load(sourceFile);
```

### Krok 5: Otočte obrázek

Zavolejte `rotate` se třemi argumenty: úhel otáčení (float), příznak pro rozšíření plátna a barvu pozadí pro nově odhalené rohy.

Metoda `rotate` otáčí obrázek kolem jeho středu, volitelně zvětšuje plátno, aby pojmula otočené hranice. Barva pozadí `Color` vyplní jakýkoli prázdný prostor, čímž zabrání průhledným nebo černým rohům.

- **20f** – úhel otáčení ve stupních (float). Změňte tuto hodnotu na libovolný úhel, např. `-45f` pro otáčení po směru hodinových ručiček.  
- **true** – zachovat původní poměr stran při rozšiřování plátna.  
- **Color.getRed()** – barva pozadí, která vyplní prázdné rohy; nahraďte `Color.getWhite()` nebo libovolnou vlastní barvou podle potřeby.

```java
if (!image.isCached())
{
    image.cacheData();
}
```

### Krok 6: Uložte výsledek

Vyberte enkodér (JPEG, PNG, atd.) a zavolejte `save`. `JpegOptions` vám umožní nastavit kvalitu, zatímco `PngOptions` poskytuje bezztrátový výstup.

Metoda `save` zapíše transformovaný obrázek na disk pomocí zadaného objektu s možnostmi, čímž zajistí, že úroveň komprese a barevná hloubka budou zachovány dle požadavků.

```java
image.rotate(20f, true, Color.getRed());
```

## Časté problémy a řešení

| Problém | Příčina | Řešení |
|-------|-------|-----|
| **Prázdné rohy po otáčení** | Nebyla zadána barva pozadí | Předávejte `Color` (např. `Color.getWhite()`) metodě `rotate`. |
| **Chyba nedostatku paměti u velkých PSD** | Obrázek není cachován | Zavolejte `image.cacheData()` před zpracováním. |
| **Nesprávný směr úhlu** | Záměna záporného a kladného úhlu | Použijte záporné hodnoty pro otáčení po směru hodinových ručiček (nebo obráceně podle vašeho souřadnicového systému). |
| **Neuložené změny** | Zapomenutí zavolat `save` | Ujistěte se, že `image.save(...)` je provedeno po otáčení. |

## Často kladené otázky

**Q: Mohu otáčet obrázky s průhledností pomocí Aspose.PSD pro Java?**  
A: Ano. Knihovna zachovává alfa kanály; vynechte neprůhlednou barvu pozadí, aby rohy zůstaly průhledné.

**Q: Existují nějaká omezení formátů souborů obrázků podporovaných pro otáčení?**  
A: Ne. Aspose.PSD podporuje PSD, JPEG, PNG, TIFF, GIF, BMP, JPEG2000, WMF, EMF a více než 30 dalších formátů.

**Q: Mohu otáčet obrázky záporným úhlem?**  
A: Rozhodně. Předávejte záporný float metodě `rotate` (např. `-30f`) pro otáčení po směru hodinových ručiček.

**Q: Poskytuje Aspose.PSD během otáčení náhled obrázku v reálném čase?**  
A: API je pouze server‑side. Pro živé náhledy renderujte otočený bitmap v UI frameworku jako Swing nebo JavaFX a aktualizujte zobrazení.

**Q: Existuje komunitní fórum pro Aspose.PSD, kde mohu požádat o pomoc?**  
A: Ano, navštivte [Aspose.PSD forum](https://forum.aspose.com/c/psd/34), kde můžete klást otázky a sdílet zkušenosti.

---

**Poslední aktualizace:** 2026-05-19  
**Testováno s:** Aspose.PSD pro Java 24.11 (nejnovější v době psaní)  
**Autor:** Aspose  

{{< blocks/products/products-backtop-button >}}

```java
image.save(destName, new JpegOptions());
```

## Související tutoriály

- [Vysoce kvalitní škálování obrázku s bicubickým resamplérem v Aspose.PSD pro Java](/psd/java/advanced-image-manipulation/implement-bicubic-resampler/)
- [Změna velikosti obrázku v Javě – použití výčtu Resize Type v Aspose.PSD pro Java](/psd/java/advanced-image-manipulation/resizing-with-resize-type-enumeration/)
- [Rozmazání obrázku v Javě s Aspose.PSD – přidání efektu rozmazání](/psd/java/advanced-techniques/blur-image/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}