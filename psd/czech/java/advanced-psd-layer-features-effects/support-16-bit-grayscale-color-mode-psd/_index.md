---
date: 2026-09-28
description: Naučte se, jak exportovat PSD jako PNG a nastavit režim barev PSD na
  16‑bitový odstín šedi pomocí Aspose.PSD pro Javu. Podrobný návod krok za krokem
  s ukázkami kódu.
keywords:
- export psd as png
- how to convert psd to png
- 16-bit grayscale java
lastmod: 2026-09-28
linktitle: Export PSD jako PNG – 16‑bitový odstín šedi – Java
og_description: Exportujte PSD jako PNG s 16‑bitovým odstínem šedi pomocí Aspose.PSD
  pro Javu. Postupujte podle tohoto podrobného tutoriálu a zachovejte 65 536 odstínů
  šedi.
og_image_alt: Guide showing how to export PSD as PNG with 16-bit grayscale using Aspose.PSD
  Java
og_title: Export PSD jako PNG s 16‑bitovým odstínem šedi v Javě – Průvodce Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-09-28'
  description: Learn how to export PSD as PNG while setting PSD color mode to 16-bit
    grayscale using Aspose.PSD for Java. Step‑by‑step guide with code examples.
  headline: How to export PSD as PNG with 16‑bit grayscale color mode in Java
  type: TechArticle
- description: Learn how to export PSD as PNG while setting PSD color mode to 16-bit
    grayscale using Aspose.PSD for Java. Step‑by‑step guide with code examples.
  name: How to export PSD as PNG with 16‑bit grayscale color mode in Java
  steps:
  - name: '**Java Development Kit (JDK)** – Install the latest JDK from [Oracle''s
      site](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
    text: '**Java Development Kit (JDK)** – Install the latest JDK from [Oracle''s
      site](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
  - name: '**Aspose.PSD for Java library** – Download the JAR from the [Aspose download
      page](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD for Java library** – Download the JAR from the [Aspose download
      page](https://releases.aspose.com/psd/java/).'
  - name: '**An IDE** – IntelliJ IDEA, Eclipse, or Visual Studio Code works perfectly.'
    text: '**An IDE** – IntelliJ IDEA, Eclipse, or Visual Studio Code works perfectly.'
  - name: '**Basic Java knowledge** – You should be comfortable creating classes,
      handling exceptions, and working with file paths.'
    text: '**Basic Java knowledge** – You should be comfortable creating classes,
      handling exceptions, and working with file paths.'
  - name: '**A sample PSD file** – Create one in Adobe Photoshop or grab a free sample
      online.'
    text: '**A sample PSD file** – Create one in Adobe Photoshop or grab a free sample
      online.'
  type: HowTo
- questions:
  - answer: It provides 65 536 shades of gray, delivering far more tonal detail than
      the standard 8‑bit (256 shades).
    question: What is 16‑bit grayscale color mode?
  - answer: Absolutely! Aspose.PSD supports RGB, CMYK, Lab, Indexed, and many other
      color modes.
    question: Can I use Aspose.PSD for non‑grayscale images?
  - answer: Yes, you can try a free trial version of Aspose.PSD. Just head to the
      [Aspose download page](https://releases.aspose.com/).
    question: Is there a trial version of Aspose.PSD?
  - answer: Check the official [documentation](https://reference.aspose.com/psd/java/)
      for in‑depth tutorials, API references, and sample projects.
    question: Where can I find more Aspose.PSD examples?
  - answer: You can buy a license by visiting the [Aspose purchase page](https://purchase.aspose.com/buy).
    question: How do I purchase a license for Aspose.PSD?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- convert psd
- Aspose.PSD
- Java image processing
title: Jak exportovat PSD jako PNG s 16‑bitovým odstínem šedi v Javě
url: /cs/java/advanced-psd-layer-features-effects/support-16-bit-grayscale-color-mode-psd/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Export PSD jako PNG s 16‑bitovým stupněm šedi v Javě

## Úvod
Exportování PSD jako PNG při zachování 16‑bitového stupně šedi vám poskytne hloubku profesionální fotografie a univerzální kompatibilitu PNG. V tomto průvodci se naučíte, jak **nastavit barvu PSD na 16‑bitový stupeň šedi** a poté **exportovat PSD jako PNG** pomocí Aspose.PSD pro Java. Tutoriál pokrývá vše od předpokladů po řešení problémů, takže můžete tento workflow integrovat do libovolného Java‑založeného obrazového potrubí.

## Rychlé odpovědi
- **Co zahrnuje „export PSD jako PNG“?** Načtěte PSD, volitelně změňte jeho barevný režim a uložte jej jako soubor PNG.  
- **Která třída Aspose provádí konverzi?** `PsdImage` načte PSD a `PngOptions` definuje nastavení výstupu PNG.  
- **Potřebuji licenci pro produkci?** Ano – zkušební verze funguje pro testování, ale pro komerční použití je vyžadována placená licence.  
- **Lze zachovat 16‑bitovou hloubku v PNG?** Rozhodně, použitím `PngColorType.GrayscaleWithAlpha`.  
- **Jaká IDE jsou podporována?** Jakékoli Java IDE – IntelliJ IDEA, Eclipse, VS Code nebo NetBeans.

## Co je export PSD jako PNG?
Export PSD jako PNG je proces převodu dokumentu Adobe Photoshop (PSD) do souboru Portable Network Graphics (PNG) při zachování pixelových dat a barevné hloubky obrázku. Tento převod se běžně používá k sdílení vysoce kvalitních šedých aktiv na webu bez ztráty tónových detailů.

## Proč exportovat PSD jako PNG se 16‑bitovým stupněm šedi?
Exportování do PNG při zachování 16‑bitového stupně šedi uchovává 65 536 odstínů šedi, což poskytuje mnohem bohatší tónovou škálu než 8‑bitové obrázky. Univerzální podpora PNG zajišťuje, že soubory lze zobrazovat v prohlížečích, mobilních aplikacích i desktopových editorech bez ztráty, zatímco bezztrátová komprese Aspose.PSD garantuje, že nejsou zavedeny žádné artefakty.

## Předpoklady
Před zahájením se ujistěte, že máte připravené následující položky:

1. **Java Development Kit (JDK)** – Nainstalujte nejnovější JDK z [Oracle's site](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. **Aspose.PSD for Java library** – Stáhněte JAR ze [Aspose download page](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse nebo Visual Studio Code fungují perfektně.  
4. **Základní znalosti Javy** – Měli byste být schopni vytvářet třídy, zpracovávat výjimky a pracovat s cestami k souborům.  
5. **Ukázkový soubor PSD** – Vytvořte jej v Adobe Photoshop nebo si stáhněte volně dostupný vzor online.

## Jak exportovat PSD jako PNG krok za krokem

## Jak nastavit barvu PSD na 16‑bitový stupeň šedi?
`PsdImage` je třída Aspose.PSD, která načítá a představuje PSD soubor v paměti.  
`ColorMode` je výčtová hodnota, která definuje barevný režim PSD obrázku.  

Načtěte PSD pomocí `PsdImage`, změňte jeho barevný režim pomocí vlastnosti `ColorMode` a poté uložte upravený soubor. Tato operace probíhá kompletně v paměti, čímž eliminuje potřebu mezisouborů a zajišťuje rychlou a efektivní konverzi.

```java
import com.aspose.psd.*;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.ColorModes;
import com.aspose.psd.fileformats.psd.CompressionMethod;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.system.Enum;
```

Tyto importy vám poskytují přístup k funkcionalitám, které budete používat k manipulaci se soubory PSD, nastavení barevného režimu a exportu výsledku jako PNG.

## Jak definovat vstupní a výstupní adresáře?
`File` je třída java.io, která představuje soubor nebo cestu k adresáři v souborovém systému.  

Musíte programu sdělit, kde má číst původní PSD a kam má zapisovat převedený PNG. Použití absolutních nebo relativních cest funguje, ale udržujte je konzistentní napříč prostředími, aby nedocházelo k chybám při řešení cest.

```java
String sourceDir = "Your Source Directory"; // Change to your source directory
String outputDir = "Your Document Directory"; // Change to your output directory
```

Nahraďte zástupné řetězce skutečnými cestami na vašem počítači.

## Jak zabalit logiku konverze do znovupoužitelné metody?
`convertPsdToPng` je vlastní metoda, která zapouzdřuje všechny kroky potřebné k převodu PSD souboru na PNG s volitelnými nastaveními.  

Vytvoření dedikované metody vám umožní znovu použít stejné kroky konverze pro více souborů nebo různé nastavení. Předávejte parametry jako vstupní cesta, cílová složka a volitelná úroveň komprese, čímž učiníte workflow flexibilním a udržovatelným.

```java
class LocalScopeExtension {
    void saveToPsdThenLoadAndSaveToPng(
        String file,
        short colorMode,
        short channelBitsCount,
        short channelsCount,
        short compression,
        int layerNumber) {
```

Tato metoda vám umožní **nastavit barvu PSD** a poté **exportovat PSD jako PNG** v jednom průběhu.

## Jak načíst PSD a použít 16‑bitový stupeň šedi?
`PsdImage` je třída Aspose.PSD, která načítá PSD soubor do paměti.  
`ColorMode.GRAYSCALE_16` je výčtová hodnota, která nastaví obrázek na 16‑bitový stupeň šedi.  
`channelBitsCount` je vlastnost, která určuje počet bitů na kanál.  

Uvnitř konverzní metody sestavte úplné cesty k souborům, vytvořte instanci `PsdImage` a změňte její `ColorMode` na `ColorMode.GRAYSCALE_16`. Vlastnost `channelBitsCount` musí být nastavena na 16, aby se zachovala vysoká bitová hloubka a zajistilo, že obrázek si udrží veškeré tónové informace.

```java
String filePath = sourceDir + file + ".psd";
String postfix = Enum.getName(ColorModes.class, colorMode) + channelBitsCount + "_" +
                 channelsCount + "_" + Enum.getName(CompressionMethod.class, compression);
String exportPath = outputDir + file + postfix + ".psd";
String pngExportPath = outputDir + file + postfix + ".png";
// Load a predefined 16-bit grayscale PSD
PsdImage image = (PsdImage)Image.load(filePath);
```

`postfix` vám pomáhá sledovat nastavení použitá pro každý exportovaný soubor.

## Jak nakreslit jemný okraj na obrázku (volitelný krok)?
`Graphics` je třída, která poskytuje kreslířské možnosti na plátně `PsdImage`.  

Volitelně můžete nakreslit šedý obdélník kolem obrázku, aby byl výstup během testování lépe viditelný. Tento krok demonstruje práci s vrstvami a grafickými objekty a obdélník je vypočítán dynamicky, takže zůstává vycentrovaný bez ohledu na velikost obrázku.

```java
try {
    RasterCachedImage raster = layerNumber >= 0 ? image.getLayers()[layerNumber] : image;
    // Draw a gray inner border around the perimeter of the layer
    Graphics graphics = new Graphics(raster);
    int width = raster.getWidth();
    int height = raster.getHeight();
    Rectangle rect = new Rectangle(
        width / 3,
        height / 3,
        width - (2 * (width / 3)) - 1,
        height - (2 * (height / 3)) - 1);
    graphics.drawRectangle(new Pen(Color.getDarkGray(), 1), rect);
```

Obdélník je vypočítán dynamicky, takže zůstává vycentrovaný bez ohledu na velikost obrázku.

## Jak uložit upravený PSD s novým barevným režimem?
`PsdOptions` je třída, která řídí, jak je PSD soubor uložen, včetně nastavení barevného režimu a bitové hloubky.  

Po kreslení (nebo po přeskočení tohoto kroku) zavolejte `save` na instanci `PsdImage` a předávejte objekt `PsdOptions`, který zachová konfiguraci 16‑bitového stupně šedi. Tím zajistíte, že uložený PSD si zachová požadovaný barevný režim bez ztráty dat.

```java
    // Save a copy of PSD with specific characteristics
    PsdOptions psdOptions = new PsdOptions();
    psdOptions.setColorMode(colorMode);
    psdOptions.setChannelBitsCount(channelBitsCount);
    psdOptions.setChannelsCount(channelsCount);
    psdOptions.setCompressionMethod(compression);
    image.save(exportPath, psdOptions);
}
```

## Jak převést PSD na PNG při zachování 16‑bitové hloubky?
`PngOptions` je třída, která definuje nastavení výstupu PNG, jako je typ barvy a úroveň komprese.  
`PngColorType.GrayscaleWithAlpha` je výčtová hodnota, která ukládá 16‑bitová data šedi s alfa kanálem.  

Načtěte nově uložený PSD, nakonfigurujte `PngOptions` s `PngColorType.GrayscaleWithAlpha` a zavolejte `save`. Tím se v souboru PNG zachová 16‑bitová data šedi, což poskytuje bezztrátový, vysoce kvalitní obrázek vhodný pro další zpracování nebo distribuci.

```java
finally {
    image.dispose();
}
// Load the saved PSD
PsdImage image1 = (PsdImage)Image.load(exportPath);
try {
    // Convert the saved PSD to a grayscale PNG image
    PngOptions pngOptions = new PngOptions();
    pngOptions.setColorType(PngColorType.GrayscaleWithAlpha);
    image1.save(pngExportPath, pngOptions); // here should be no exception
}
finally {
    image1.dispose();
}
```

Nyní jste úspěšně **exportovali PSD jako PNG** při zachování vysoce kvalitních 16‑bitových šedých dat.

## Časté problémy a řešení
| Problém | Proč se to děje | Oprava |
|---------|----------------|--------|
| **“Unsupported color type” exception** | Pokus o uložení PSD s nepodporovanou konfigurací kanálů. | Ujistěte se, že `channelBitsCount` odpovídá skutečné bitové hloubce (16) a `channelsCount` je správný pro šedou (1). |
| **File not found** | Nesprávná cesta ke vstupnímu adresáři. | Zkontrolujte řetězec `sourceDir` a ověřte, že soubor PSD na daném místě existuje. |
| **Output PNG appears black** | PNG uložen bez správného zacházení s alfa kanálem. | Použijte `PngColorType.GrayscaleWithAlpha`, jak je uvedeno výše. |
| **Memory overflow on large PSDs** | Načítání celého souboru do paměti. | Aktivujte režim streamování pomocí `PsdImage.load(inputStream, new LoadOptions())` pro efektivní zpracování velkých souborů. |

## Často kladené otázky

**Q: Co je 16‑bitový stupeň šedi?**  
A: Poskytuje 65 536 odstínů šedi, což přináší mnohem více tónových detailů než standardní 8‑bitový (256 odstínů).

**Q: Mohu použít Aspose.PSD pro ne‑šedé obrázky?**  
A: Rozhodně! Aspose.PSD podporuje RGB, CMYK, Lab, Indexed a mnoho dalších barevných režimů.

**Q: Existuje zkušební verze Aspose.PSD?**  
A: Ano, můžete vyzkoušet bezplatnou zkušební verzi Aspose.PSD. Stačí navštívit [Aspose download page](https://releases.aspose.com/).

**Q: Kde najdu více příkladů Aspose.PSD?**  
A: Podívejte se do oficiální [documentation](https://reference.aspose.com/psd/java/) pro podrobné tutoriály, API reference a ukázkové projekty.

**Q: Jak si mohu zakoupit licenci pro Aspose.PSD?**  
A: Licenci můžete zakoupit na [Aspose purchase page](https://purchase.aspose.com/buy).

---

**Poslední aktualizace:** 2026-09-28  
**Testováno s:** Aspose.PSD for Java 24.12 (nejnovější v době psaní)  
**Autor:** Aspose

## Související tutoriály

- [Převést PSD na PNG s určenou bitovou hloubkou pomocí Aspose.PSD pro Java](/psd/java/optimizing-png-files/specify-png-bit-depth/)
- [Exportovat PSD do PNG s efekty vrstev pomocí Aspose.PSD pro Java](/psd/java/psd-image-modification-conversion/apply-layer-effects-psd-files/)
- [Uložit PSD jako JPEG a podpora RGB barvy s Aspose.PSD Java](/psd/java/advanced-psd-layer-features-effects/support-rgb-color-psd-files/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}