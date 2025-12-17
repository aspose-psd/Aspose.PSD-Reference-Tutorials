---
date: 2025-12-17
description: Naučte se, jak převést PSD na PNG a zároveň nastavit barevný režim PSD
  na 16‑bitovou odstín šedé pomocí Aspose.PSD pro Javu. Průvodce krok za krokem s
  ukázkami kódu.
linktitle: Convert PSD to PNG – 16-bit Grayscale – Java
second_title: Aspose.PSD Java API
title: Jak převést PSD na PNG s 16bitovým odstínem šedi v Javě
url: /cs/java/advanced-psd-layer-features-effects/support-16-bit-grayscale-color-mode-psd/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Převod PSD na PNG s 16‑bitovým odstínem šedi v Javě

## Úvod
Když se ponoříte do světa grafického designu a manipulace s obrázky, pochopení toho, jak **převést PSD na PNG**, je jako mít tajnou zbraň. Zejména použití 16‑bitového odstínu šedi dodá vašim obrázkům úžasnou hloubku a detail, který je skutečně „rozsvítí“. V tomto tutoriálu vás provedeme, jak **nastavit barvy PSD** na 16‑bitový odstín šedi a poté **exportovat PSD jako PNG** pomocí Aspose.PSD pro Java. Připravení posunout svůj pracovní postup s obrázky na vyšší úroveň? Pojďme na to.

## Rychlé odpovědi
- **Co zahrnuje „převod PSD na PNG“?** Načtení PSD, volitelná změna barevného režimu a uložení jako soubor PNG.  
- **Která třída Aspose provádí převod?** `PsdImage` pro načtení a `PngOptions` pro uložení.  
- **Potřebuji speciální licenci?** Zkušební verze funguje pro testování; placená licence je vyžadována pro produkci.  
- **Mohu zachovat 16‑bitovou hloubku v PNG?** Ano, pomocí `PngColorType.GrayscaleWithAlpha`.  
- **Jaká IDE jsou podporována?** Jakékoli Java IDE – IntelliJ IDEA, Eclipse, VS Code atd.

## Požadavky
Než začneme, ujistěte se, že máte vše připravené, abyste z tohoto tutoriálu vytěžili maximum. Budete potřebovat:

1. **Java Development Kit (JDK)** – Ujistěte se, že máte nainstalovanou nejnovější verzi. Můžete ji stáhnout z [Oracle's site](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. **Aspose.PSD for Java Library** – Toto je motor, který nám umožní manipulovat se soubory PSD. Stáhněte jej ze [Aspose download page](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse nebo Visual Studio Code budou naprosto v pořádku.  
4. **Základní znalost Javy** – Znalost syntaxe Javy vám usnadní jednotlivé kroky.  
5. **Ukázkový soubor PSD** – Buď jej vytvořte v Adobe Photoshopu, nebo si stáhněte zdarma dostupnou ukázku online.

Připravení? Skvělé! Naimportujme potřebné balíčky a začněme kódovat.

## Import balíčků
Abychom mohli začít, přidejte potřebné importy Aspose.PSD do svého Java souboru:

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

Tyto importy vám poskytují přístup k funkcím, které budete používat k manipulaci se soubory PSD, nastavení barevného režimu a exportu výsledku jako PNG.

## Krok 1: Definujte své adresáře
Nejprve nastavte složky pro zdrojové a výstupní soubory. Tím programu řeknete, kde má číst původní PSD a kam má zapisovat převedené soubory.

```java
String sourceDir = "Your Source Directory"; // Change to your source directory
String outputDir = "Your Document Directory"; // Change to your output directory
```

Nahraďte zástupné řetězce skutečnými cestami na vašem počítači.

## Krok 2: Vytvořte metodu pro zpracování obrazu
Zabalíme logiku převodu do znovupoužitelné metody. Přijímá všechny parametry, které můžete chtít ladit, jako je barevný režim, bitová hloubka a komprese.

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

Tato metoda vám umožní **nastavit barvy PSD** a poté **exportovat PSD jako PNG** v jednom toku.

## Krok 3: Definujte cesty k souborům a načtěte PSD
Uvnitř metody sestavte úplné cesty k souborům a načtěte původní 16‑bitový odstín šedi PSD:

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

Obdélník je vypočítán dynamicky, takže zůstává vycentrovaný bez ohledu na velikost obrázku.

## Krok 5: Uložte upravený soubor PSD
Po nakreslení uložíme PSD s přesně tím barevným režimem a bitovou hloubkou, které jste zadali. Toto je jádro **nastavení barev PSD** před převodem.

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
Nakonec načteme nově uložený PSD a exportujeme jej jako PNG. Použitím `PngColorType.GrayscaleWithAlpha` zachováme 16‑bitovou hloubku v souboru PNG.

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

Nyní jste úspěšně **převzeli PSD na PNG** a přitom si zachovali vysoce kvalitní 16‑bitová data odstínu šedi.

## Časté problémy a řešení
| Problém | Proč se to děje | Řešení |
|-------|----------------|-----|
| **“Unsupported color type” exception** | Pokus o uložení PSD s nepodporovanou konfigurací kanálů. | Ujistěte se, že `channelBitsCount` odpovídá skutečné bitové hloubce (16) a `channelsCount` je správný pro odstín šedi (1). |
| **File not found** | Nesprávná cesta ke zdrojovému adresáři. | Zkontrolujte řetězec `sourceDir` a ověřte, že soubor PSD existuje. |
| **Output PNG appears black** | PNG uložený bez správné manipulace s alfa kanálem. | Použijte `PngColorType.GrayscaleWithAlpha`, jak je ukázáno výše. |

## Často kladené otázky

**Q: Co je 16‑bitový odstín šedi?**  
A: Poskytuje 65 536 odstínů šedi, což přináší mnohem více tónových detailů než standardní 8‑bitový (256 odstínů).

**Q: Mohu použít Aspose.PSD pro obrázky, které nejsou odstínem šedi?**  
A: Rozhodně! Aspose.PSD podporuje RGB, CMYK, Lab a mnoho dalších barevných režimů.

**Q: Existuje zkušební verze Aspose.PSD?**  
A: Ano, můžete vyzkoušet bezplatnou zkušební verzi Aspose.PSD. Stačí navštívit [Aspose download page](https://releases.aspose.com/).

**Q: Kde najdu více příkladů použití Aspose.PSD?**  
A: Podívejte se do [documentation](https://reference.aspose.com/psd/java/), kde najdete podrobnější příklady a tutoriály.

**Q: Jak si mohu zakoupit licenci pro Aspose.PSD?**  
A: Licenci můžete zakoupit na [Aspose purchase page](https://purchase.aspose.com/buy).

---

**Last Updated:** 2025-12-17  
**Testováno s:** Aspose.PSD for Java 24.12 (nejnovější v době psaní)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}