---
date: 2026-02-20
description: Naučte se, jak převést PSD na PNG a při tom nastavit barevný režim PSD
  na 16‑bitovou stupnici šedi pomocí Aspose.PSD pro Javu. Podrobný návod krok za krokem
  s ukázkami kódu.
linktitle: Convert PSD to PNG – 16-bit Grayscale – Java
second_title: Aspose.PSD Java API
title: Jak převést PSD na PNG s 16bitovým režimem odstínů šedi v Javě
url: /cs/java/advanced-psd-layer-features-effects/support-16-bit-grayscale-color-mode-psd/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Převod PSD na PNG s 16‑bitovým odstínem šedi v Javě

## Úvod
Když se ponořujete do světa grafického designu a manipulace s obrázky, vědět **how to convert PSD to PNG** je jako mít tajnou zbraň. Použití 16‑bitového odstínu šedi přidává neuvěřitelnou hloubku a bohatost tónů, což vaše obrázky učiní výraznějšími. V tomto tutoriálu vás provedeme tím, jak **set PSD color mode** na 16‑bitový odstín šedi a poté **export PSD as PNG** pomocí Aspose.PSD pro Java. Připravení posunout svůj workflow s obrázky na vyšší úroveň? Pojďme začít.

## Rychlé odpovědi
- **What does “convert PSD to PNG” involve?** Načtení PSD, volitelná změna jeho barevného režimu a uložení jako PNG soubor.  
- **Which Aspose class handles the conversion?** `PsdImage` pro načtení a `PngOptions` pro uložení.  
- **Do I need a special license?** Zkušební verze funguje pro testování; placená licence je vyžadována pro produkci.  
- **Can I keep the 16‑bit depth in PNG?** Ano, použitím `PngColorType.GrayscaleWithAlpha`.  
- **What IDEs are supported?** Jakékoli Java IDE – IntelliJ IDEA, Eclipse, VS Code, atd.

## Proč převádět PSD na PNG s 16‑bitovým odstínem šedi?
* **Preserve tonal detail:** 16‑bit grayscale ukládá 65 536 odstínů šedi, což je mnohem více než 256 odstínů 8‑bitového obrázku.  
* **Broad compatibility:** PNG je široce podporován v prohlížečích, mobilních aplikacích i desktopových nástrojích, přičemž zachovává vysoce kvalitní data.  
* **Lossless workflow:** Převod pomocí Aspose.PSD zajišťuje, že nedojde k nechtěným artefaktům komprese, což je ideální pro archivaci nebo další zpracování.

## Požadavky
Než začneme, ujistěte se, že máte vše připravené, abyste z tohoto tutoriálu získali maximum. Budete potřebovat:

1. **Java Development Kit (JDK)** – Ujistěte se, že máte nainstalovanou nejnovější verzi. Můžete ji stáhnout z [Oracle's site](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. **Aspose.PSD for Java Library** – Toto je engine, který nám umožní manipulovat se soubory PSD. Stáhněte jej ze [Aspose download page](https://releases.aspose.com/psd/java/).  
3. **An IDE** – IntelliJ IDEA, Eclipse nebo Visual Studio Code budou fungovat bez problémů.  
4. **Basic Java knowledge** – Znalost syntaxe Javy usnadní jednotlivé kroky.  
5. **A sample PSD file** – Buď vytvořte soubor v Adobe Photoshopu, nebo si stáhněte zdarma ukázkový soubor online.

Připravení? Skvělé! Naimportujme potřebné balíčky a začněme kódovat.

## Import balíčků
Pro zahájení přidejte požadované importy Aspose.PSD do vašeho Java souboru:

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

## Krok 1: Definujte své adresáře
Nejprve nastavte složky pro zdroj a výstup. To programu říká, kde má číst původní PSD a kam má zapisovat převedené soubory.

```java
String sourceDir = "Your Source Directory"; // Change to your source directory
String outputDir = "Your Document Directory"; // Change to your output directory
```

Nahraďte řetězce zástupných znaků skutečnými cestami na vašem počítači.

## Krok 2: Vytvořte metodu pro zpracování obrázku
Zabalíme logiku převodu do znovupoužitelné metody. Přijímá všechny parametry, které můžete chtít upravit, jako je barevný režim, bitová hloubka a komprese.

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

Tato metoda vám umožní **set PSD color mode** a následně **export PSD as PNG** v jednom průběhu.

## Krok 3: Definujte cesty k souborům a načtěte PSD
Uvnitř metody vytvořte úplné cesty k souborům a načtěte původní 16‑bitový grayscale PSD:

```java
String filePath = sourceDir + file + ".psd";
String postfix = Enum.getName(ColorModes.class, colorMode) + channelBitsCount + "_" +
                 channelsCount + "_" + Enum.getName(CompressionMethod.class, compression);
String exportPath = outputDir + file + postfix + ".psd";
String pngExportPath = outputDir + file + postfix + ".png";
// Load a predefined 16-bit grayscale PSD
PsdImage image = (PsdImage)Image.load(filePath);
```

`postfix` vám pomáhá sledovat nastavení použité pro každý exportovaný soubor.

## Krok 4: Zpracujte vrstvu nebo celý obrázek
Nyní buď kreslíme na konkrétní vrstvu, nebo na celý obrázek. V tomto příkladu přidáváme jemný šedý okraj, aby byl výsledek lépe viditelný.

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

Obdélník je vypočítán dynamicky, aby zůstal vycentrovaný bez ohledu na velikost obrázku.

## Krok 5: Uložte upravený PSD soubor
Po kreslení uložíme PSD s přesně tím barevným režimem a bitovou hloubkou, kterou jste zadali. To je jádro **setting PSD color mode** před převodem.

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

## Krok 6: Převod PSD na PNG
Na závěr načteme nově uložený PSD a exportujeme jej jako PNG. Použitím `PngColorType.GrayscaleWithAlpha` zachováme 16‑bitovou hloubku v PNG souboru.

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

Nyní jste úspěšně **converted PSD to PNG** a zachovali jste vysoce kvalitní 16‑bitová data odstínu šedi.

## Časté problémy a řešení
| Problém | Proč se to děje | Řešení |
|---------|----------------|--------|
| **“Unsupported color type” exception** | Pokus o uložení PSD s nepodporovanou konfigurací kanálů. | Ujistěte se, že `channelBitsCount` odpovídá skutečné bitové hloubce (16) a `channelsCount` je správný pro odstín šedi (1). |
| **File not found** | Nesprávná cesta ke zdrojovému adresáři. | Zkontrolujte řetězec `sourceDir` a ověřte, že PSD soubor existuje. |
| **Output PNG appears black** | PNG uložený bez zpracování alfa kanálu. | Použijte `PngColorType.GrayscaleWithAlpha` jak je uvedeno výše. |

## Často kladené otázky

**Q: What is 16-bit grayscale color mode?**  
A: Poskytuje 65 536 odstínů šedi, což přináší mnohem více tonálního detailu než standardní 8‑bit (256 odstínů).

**Q: Can I use Aspose.PSD for non‑grayscale images?**  
A: Rozhodně! Aspose.PSD podporuje RGB, CMYK, Lab a mnoho dalších barevných režimů.

**Q: Is there a trial version of Aspose.PSD?**  
A: Ano, můžete vyzkoušet bezplatnou zkušební verzi Aspose.PSD. Stačí přejít na [Aspose download page](https://releases.aspose.com/).

**Q: Where can I find more examples of using Aspose.PSD?**  
A: Můžete se podívat na [documentation](https://reference.aspose.com/psd/java/) pro podrobnější příklady a tutoriály.

**Q: How do I purchase a license for Aspose.PSD?**  
A: Licenci můžete zakoupit na [Aspose purchase page](https://purchase.aspose.com/buy).

**Poslední aktualizace:** 2026-02-20  
**Testováno s:** Aspose.PSD for Java 24.12 (nejnovější v době psaní)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}