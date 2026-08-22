---
date: 2026-07-22
description: Naučte se, jak uložit PSD jako PNG, zachovat průhlednost PNG a otáčet
  vrstvy PSD v Javě s Aspose.PSD. Průvodce krok za krokem, vysvětlení bez kódu a tipy
  na řešení problémů.
keywords:
- save psd as png
- export psd layers png
- convert photoshop file png
- psd to png transparency
lastmod: 2026-07-22
linktitle: uložte PSD jako PNG a otáčejte vrstvy v Javě pomocí Aspose.PSD
og_description: uložte PSD jako PNG s Aspose.PSD pro Javu. Zachovejte průhlednost,
  otáčejte vrstvy a exportujte PNG pomocí několika řádků kódu – ideální pro automatizované
  pracovní postupy.
og_image_alt: 'Developer guide: save PSD as PNG and rotate layers using Aspose.PSD
  for Java'
og_title: uložte PSD jako PNG a otáčejte vrstvy v Javě pomocí Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-07-22'
  description: Learn how to save psd as png, preserve PNG transparency, and rotate
    PSD layers in Java with Aspose.PSD. Step‑by‑step guide, code‑free explanations,
    and troubleshooting tips.
  headline: save psd as png and rotate layers in Java using Aspose.PSD
  type: TechArticle
- description: Learn how to save psd as png, preserve PNG transparency, and rotate
    PSD layers in Java with Aspose.PSD. Step‑by‑step guide, code‑free explanations,
    and troubleshooting tips.
  name: save psd as png and rotate layers in Java using Aspose.PSD
  steps:
  - name: Set Up Your Java Project
    text: Create a new Java project in your IDE and add the Aspose.PSD JAR to the
      project’s build path.
  - name: Import Required Classes
    text: '`PsdImage` is the core class that represents a Photoshop document in memory.
      `PngOptions` controls PNG‑specific settings, and `RotateFlipType` defines rotation
      and flip operations. These imports give you access to image loading, rotation,
      and PNG‑specific options.'
  - name: Define File Paths
    text: Specify where your source PSD lives and where the output files should be
      written. Using absolute paths during testing avoids “file not found” errors.
      > **Pro tip:** Store paths in a configuration file for easier maintenance in
      larger projects.
  - name: Load the PSD File
    text: '`PsdImage` loads the entire Photoshop document, including all layers, masks,
      and effects, into a manipulable object. Now `im` represents the whole PSD, ready
      for transformations.'
  - name: Rotate the Image (How to rotate PSD)
    text: '`RotateFlipType` enumerates all supported rotations and flips. In this
      example we rotate 270° and flip both axes, which swaps width and height while
      mirroring the image. Feel free to experiment with other values such as `Rotate90FlipNone`
      or `Rotate180FlipX`.'
  - name: Save the Rotated Image as PNG (save PSD as PNG)
    text: Configure `PngOptions` to keep transparency (`PngColorType.TruecolorWithAlpha`)
      and then call `save`. The PNG retains layer transparency, ensuring it works
      seamlessly in web or mobile apps. The resulting PNG preserves alpha channels,
      making it suitable for compositing or further processing.
  - name: Save the Modified PSD (optional)
    text: If you also need a new PSD with the rotation applied, you can save the modified
      `PsdImage` back to disk. You now have both a PNG preview and an updated PSD
      file.
  type: HowTo
- questions:
  - answer: Yes, you can call `layer.rotateFlip(RotateFlipType.Rotate90FlipNone)`
      after iterating through `im.getLayers()`.
    question: Can I rotate a specific layer in a PSD file?
  - answer: The library handles most files efficiently, but extremely large PSDs (>500
      MB) may require additional memory or streaming options.
    question: Is there any performance limitation with Aspose.PSD for Java?
  - answer: Aspose offers a free trial, but a paid license is needed for production.
      See the [temporary license](https://purchase.aspose.com/temporary-license/)
      for testing.
    question: Is Aspose.PSD free to use?
  - answer: Comprehensive docs are available at [Aspose.PSD Documentation](https://reference.aspose.com/psd/java/).
    question: Where can I find detailed documentation?
  - answer: Get help via the [Aspose Support Forum](https://forum.aspose.com/c/psd/34).
    question: What if I encounter issues while using Aspose.PSD?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- convert PSD
- Aspose.PSD
- Java image processing
- rotate PSD layers
title: uložte PSD jako PNG a otáčejte vrstvy v Javě pomocí Aspose.PSD
url: /cs/java/advanced-psd-layer-features-effects/rotate-layers-psd-files/
weight: 21
---

## Související tutoriály

- [Uložit PSD jako PNG a použít stínování při vykreslování v Aspose.PSD pro Java](/psd/java/advanced-image-manipulation/rendering-drop-shadow/)
- [Jak komprimovat PNG soubory pomocí Aspose.PSD pro Java](/psd/java/optimizing-png-files/compress-png-files/)
- [Jak otočit obrázek v Javě s Aspose.PSD](/psd/java/advanced-image-manipulation/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< blocks/products/pf/main-wrap-class >}}

# Uložit PSD jako PNG a otáčet vrstvy v Javě pomocí Aspose.PSD

## Úvod
Pokud potřebujete **uložit PSD jako PNG** a zároveň otáčet vrstvy, tento průvodce je pro vás. Ať už vytváříte nástroj pro dávkové zpracování, webovou službu, která potřebuje manipulaci s obrázky za běhu, nebo jen automatizujete designový workflow, programové řešení šetří čas a odstraňuje závislost na Adobe Photoshopu. V tomto tutoriálu si ukážeme **jak otočit vrstvy PSD** a exportovat výsledek jako PNG pomocí knihovny Aspose.PSD pro Java. Pojďme si zahnout rukávy a spustit váš designový workflow hladce!

## Rychlé odpovědi
- **Jakou knihovnu mohu použít?** Aspose.PSD for Java  
- **Mohu najednou otočit a uložit PSD jako PNG?** Ano – otočte PSD a poté uložte jako PNG  
- **Potřebuji licenci?** Bezplatná zkušební verze funguje pro testování; placená licence je vyžadována pro produkci  
- **Která verze Javy je podporována?** Java 8 a novější  
- **Je výstup PNG průhledný?** Ano, když nastavíte `PngColorType.TruecolorWithAlpha`

## Co je „převod PSD na PNG“?
Převod dokumentu Photoshop (PSD) na PNG obrázek extrahuje vizuální obsah – včetně vrstev, masek a alfa kanálů – do široce podporovaného rastrového formátu, který zachovává průhlednost. To činí PNG ideálním pro webové grafiky, miniatury a následné zpracování obrázků. Výsledný PNG lze použít přímo na webových stránkách, v mobilních aplikacích nebo jej dále zpracovávat jinými knihovnami.

## Proč použít Aspose.PSD pro Java k uložení PSD jako PNG a otáčení vrstev PSD?
Aspose.PSD vám umožní **uložit PSD jako PNG** a otáčet vrstvy bez instalace Photoshopu. Podporuje **více než 50 vstupních a výstupních formátů**, zpracovává stovky‑stránkové PSD soubory s méně než 200 MB RAM a běží na Windows, Linuxu i macOS. API vyžaduje jen několik volání metod a poskytuje výsledky vysoké věrnosti s vestavěnou podporou efektů vrstev, masek a alfa kanálů.

## Požadavky
Než se pustíme do kódu, ujistěte se, že máte následující:

- **Java Development Kit (JDK)** – stáhněte z [Oracle website](https://www.oracle.com/java/technologies/javase-downloads.html).  
- **Integrované vývojové prostředí (IDE)** – IntelliJ IDEA, Eclipse nebo NetBeans jsou v pořádku.  
- **Knihovna Aspose.PSD pro Java** – získat nejnovější JAR ze [release page](https://releases.aspose.com/psd/java/).  
- **Základní znalost Javy** – znalost tříd, objektů a zpracování výjimek.

## Průvodce krok za krokem

### Krok 1: Nastavte svůj Java projekt
Vytvořte nový Java projekt ve svém IDE a přidejte Aspose.PSD JAR do cesty sestavení projektu.

### Krok 2: Importujte požadované třídy
`PsdImage` je hlavní třída představující dokument Photoshop v paměti. `PngOptions` řídí nastavení specifická pro PNG a `RotateFlipType` definuje operace otáčení a převrácení.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RotateFlipType;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

Tyto importy vám umožní načíst obrázek, provést otáčení a nastavit možnosti pro PNG.

### Krok 3: Definujte cesty k souborům
Určete, kde se nachází váš zdrojový PSD a kam mají být výstupní soubory zapsány. Použití absolutních cest během testování zabraňuje chybám „soubor nenalezen“.

```java
String dataDir = "Your Document Directory"; // Change this to your actual document directory.
String sourceFile = dataDir + "1.psd"; // Source PSD file
String pngPath = dataDir + "RotateFlipTest2617.png"; // Output PNG file path
String psdPath = dataDir + "RotateFlipTest2617.psd"; // Output PSD file path
```

> **Pro tip:** Ukládejte cesty do konfiguračního souboru pro snadnější údržbu ve větších projektech.

### Krok 4: Načtěte soubor PSD
`PsdImage` načte celý dokument Photoshop, včetně všech vrstev, masek a efektů, do manipulovatelného objektu.

```java
PsdImage im = (PsdImage) Image.load(sourceFile);
```

Nyní `im` představuje celý PSD, připravený na transformace.

### Krok 5: Otočte obrázek (Jak otočit PSD)
`RotateFlipType` enumeruje všechny podporované otáčení a převrácení. V tomto příkladu otáčíme o 270° a převracíme obě osy, což prohodí šířku a výšku při zrcadlení obrázku.

```java
int flipType = RotateFlipType.Rotate270FlipXY; // Choose the rotation type
im.rotateFlip(flipType); // Rotate the image
```

Klidně experimentujte s jinými hodnotami, např. `Rotate90FlipNone` nebo `Rotate180FlipX`.

### Krok 6: Uložte otočený obrázek jako PNG (uložit PSD jako PNG)
Nastavte `PngOptions` tak, aby zachovával průhlednost (`PngColorType.TruecolorWithAlpha`) a poté zavolejte `save`. PNG si zachová průhlednost vrstev, což zajišťuje bezproblémové použití ve webu nebo mobilních aplikacích.

```java
PngOptions options = new PngOptions();
options.setColorType(PngColorType.TruecolorWithAlpha); // Preserve transparency
im.save(pngPath, options); // Save the rotated image
```

Výsledný PNG zachovává alfa kanály, takže je vhodný pro kompozici nebo další zpracování.

### Krok 7: Uložte upravený PSD (volitelné)
Pokud potřebujete také nový PSD s aplikovaným otáčením, můžete upravený `PsdImage` uložit zpět na disk.

```java
im.save(psdPath);
```

Nyní máte jak PNG náhled, tak aktualizovaný PSD soubor.

## Časté problémy a řešení
- **Soubor nenalezen:** Ověřte, že `dataDir` končí oddělovačem cesty (`/` nebo `\`).  
- **OutOfMemoryError u velkých PSD:** Zvyšte velikost haldy JVM (`-Xmx2g`).  
- **Ztráta průhlednosti:** Ujistěte se, že je nastaven `PngColorType.TruecolorWithAlpha`; jinak bude PNG uloženo bez alfa kanálu.  
- **Otočení PSD obrázku nefunguje podle očekávání:** Zkontrolujte konstantu `RotateFlipType`, kterou jste vybrali; některé konstanty kombinují otočení a převrácení v jednom kroku.

## Často kladené otázky

**Q: Mohu otočit konkrétní vrstvu v souboru PSD?**  
A: Ano, můžete zavolat `layer.rotateFlip(RotateFlipType.Rotate90FlipNone)` po iteraci přes `im.getLayers()`.

**Q: Existuje nějaké omezení výkonu u Aspose.PSD pro Java?**  
A: Knihovna zvládá většinu souborů efektivně, ale extrémně velké PSD (>500 MB) mohou vyžadovat více paměti nebo streamingové možnosti.

**Q: Je Aspose.PSD zdarma?**  
A: Aspose nabízí bezplatnou zkušební verzi, ale pro produkci je potřeba placená licence. Viz [temporary license](https://purchase.aspose.com/temporary-license/) pro testování.

**Q: Kde najdu podrobnou dokumentaci?**  
A: Kompletní dokumentace je k dispozici na [Aspose.PSD Documentation](https://reference.aspose.com/psd/java/).

**Q: Co když narazím na problémy při používání Aspose.PSD?**  
A: Získat pomoc můžete na [Aspose Support Forum](https://forum.aspose.com/c/psd/34).

**Q: Zachovává převod PSD na PNG efekty vrstev?**  
A: Ano, když uložíte s `PngColorType.TruecolorWithAlpha`, většina vizuálních efektů je rasterizována do PNG.

**Q: Mohu hromadně zpracovávat více souborů PSD?**  
A: Ano. Zabalte kód do smyčky, která iteruje přes adresář PSD souborů.

**Q: Je možné nastavit úroveň komprese PNG?**  
A: `PngOptions` poskytuje metodu `setCompressionLevel(int)` pro jemné ladění velikosti výstupu.

**Q: Musím zavřít objekt obrázku?**  
A: `PsdImage` implementuje `Closeable`; použijte try‑with‑resources nebo zavolejte `im.close()` v bloku `finally`.

**Q: Bude mít otočený PNG stejné rozměry jako originál?**  
A: Otočení o 90° nebo 270° prohodí šířku a výšku, takže PNG automaticky odráží novou orientaci.

## Závěr
Využitím Aspose.PSD pro Java můžete **uložit PSD jako PNG**, **zachovat průhlednost PNG** a **otočit vrstvy PSD** pomocí několika řádků kódu. Tento přístup eliminuje potřebu Photoshopu, urychluje automatizované workflow a dává vám plnou kontrolu nad výstupem obrázku. Vyzkoušejte to ve svých projektech a uvidíte, kolik času ušetříte!

---

**Last Updated:** 2026-07-22  
**Tested With:** Aspose.PSD for Java 24.11  
**Author:** Aspose  

{{< blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/products-backtop-button >}}