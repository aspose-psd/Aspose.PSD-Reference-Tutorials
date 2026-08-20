---
date: 2026-05-29
description: Naučte se převádět PSD na PNG načítáním obrázků ze streamu pomocí Aspose.PSD
  for Java. Tento podrobný návod na zpracování obrázků v Javě vám ukáže, jak efektivně
  číst, převádět a ukládat soubory PSD.
keywords:
- convert psd to png
- how to load psd
- read image from memory
- save image to stream
- java image processing tutorial
linktitle: Načítání obrázků ze streamu
schemas:
- author: Aspose
  dateModified: '2026-05-29'
  description: Learn to convert PSD to PNG by loading images from a stream with Aspose.PSD
    for Java. This step‑by‑step Java image processing tutorial shows you how to read,
    convert, and save PSD files efficiently.
  headline: Convert PSD to PNG – Load Images from Stream (Java)
  type: TechArticle
- questions:
  - answer: Absolutely. The library’s streaming architecture lets you loop through
      thousands of PSD files, convert each to PNG, and write directly to output streams
      without excessive memory consumption.
    question: Is Aspose.PSD for Java suitable for batch image processing?
  - answer: Yes, you can explore a free trial version [here](https://releases.aspose.com/).
    question: Can I try Aspose.PSD for Java before purchasing?
  - answer: Join the community at the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34)
      for assistance and discussions.
    question: Where can I find support for Aspose.PSD for Java?
  - answer: Obtain a temporary license [here](https://purchase.aspose.com/temporary-license/)
      for testing Aspose.PSD for Java.
    question: Do I need a temporary license for testing purposes?
  - answer: Visit the [purchase page](https://purchase.aspose.com/buy) to acquire
      Aspose.PSD for Java.
    question: Where can I purchase Aspose.PSD for Java?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Převod PSD na PNG – Načítání obrázků ze streamu (Java)
url: /cs/java/advanced-techniques/loading-images-from-stream/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Převést PSD na PNG – Načíst obrázky ze streamu (Java)

## Úvod

V tomto tutoriálu se dozvíte, jak **převést PSD na PNG** načtením PSD obrázku přímo z Java `InputStream`. Aspose.PSD pro Java usnadňuje čtení souboru PSD z paměti, jeho transformaci a zápis výsledku zpět do streamu jako PNG obrázek. Provedeme vás každým krokem, vysvětlíme, proč je každé volání API důležité, a poskytneme tipy, jak se vyhnout běžným úskalím.

## Rychlé odpovědi
- **Jaký je nejjednodušší způsob, jak převést PSD na PNG v Javě?** Načtěte PSD pomocí `Image.load(stream)`, přetypujte na `PsdImage` a poté zavolejte `save(outputStream, new PngOptions())`.  
- **Potřebuji licenci pro spuštění kódu?** Dočasná licence funguje pro testování; pro produkci je vyžadována plná licence.  
- **Mohu zpracovávat velké soubory PSD bez vysoké spotřeby paměti?** Ano – Aspose.PSD zpracovává soubory ve streamovacím režimu, zvládá soubory až do 2 GB, aniž by načítal celý dokument do paměti.  
- **Které verze Javy jsou podporovány?** Java 8 až Java 21 jsou plně podporovány.  
- **Kde najdu více příkladů?** Oficiální [dokumentace](https://reference.aspose.com/psd/java/) obsahuje desítky ukázek kódu.

## Co je převod PSD na PNG?
**Convert PSD to PNG** je proces čtení souboru Photoshop (.psd) a exportu jeho rastrových obrazových dat do formátu Portable Network Graphics (PNG). Pomocí Aspose.PSD se tato konverze provádí v paměti, takže můžete číst ze streamů nebo do nich zapisovat, aniž byste se dotýkali souborového systému.

## Proč používat Aspose.PSD pro Java?
Aspose.PSD podporuje **více než 30 vstupních a výstupních formátů** a dokáže zpracovat **více než stovky stránek PSD souborů až do 2 GB**, přičemž spotřeba paměti zůstává pod 200 MB. Knihovna poskytuje čistě Java API, což znamená, že nejsou potřeba žádné nativní knihovny ani instalace Photoshopu, což je ideální pro server‑side pipeline zpracování obrázků.

## Požadavky

Před začátkem se ujistěte, že máte:

- Základní zkušenosti s vývojem v Javě.  
- Nainstalovanou knihovnu Aspose.PSD pro Java – stáhněte ji z [webu Aspose](https://releases.aspose.com/psd/java/).  
- IDE pro Javu nebo nástroj pro sestavení (Maven/Gradle) připravený přidat JAR Aspose.PSD do vašeho projektu.

## Import balíčků

`Image` třída je základní třídou Aspose.PSD představující libovolný rastrový obrázek. `PsdImage` poskytuje specifické funkce Photoshopu, jako jsou vrstvy a kanály. `PngOptions` vám umožňuje nastavit specifické volby pro PNG. `FileInputStream` a `FileOutputStream` jsou standardní Java I/O třídy pro čtení ze souborů a zápis do nich.

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.system.io.FileMode;
import com.aspose.psd.system.io.FileStream;
import com.aspose.psd.system.io.MemoryStream;
import java.io.FileInputStream;
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
```

## Krok 1: Nastavte adresář dokumentů

Ujistěte se, že máte určený adresář pro vaše zdrojové PSD soubory a výstupní obrázky. V kódu nahraďte `"Your Document Directory"` skutečnou absolutní cestou na vašem počítači.

```java
String dataDir = "Your Document Directory";
```

## Krok 2: Definujte cesty ke zdroji a cíli

Určete cestu k PSD souboru jako zdroj a požadovanou výstupní cestu pro výsledný PNG obrázek. Toto jasné oddělení pomáhá, když později přejdete na čtení z databáze nebo HTTP požadavku.

```java
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "result.png";
```

## Krok 3: Vytvořte vstupní stream a načtěte obrázek

`FileInputStream` čte surové bajty ze souboru na disku. Statická metoda `Image.load(InputStream)` načte obrázek z daného streamu a vrátí instanci `Image`.

```java
FileInputStream inputStream = new FileInputStream(sourceFile);
Image image = Image.load(inputStream);
```

## Krok 4: Převod obrázku na PsdImage

`PsdImage` představuje dokument Photoshopu, odhaluje vrstvy, kanály a další PSD‑specifická data. Přetypujte obecný `Image` na `PsdImage`, abyste mohli pracovat s těmito funkcemi.

```java
PsdImage psdImage = (PsdImage)image;
```

## Krok 5: Uložte obrázek do streamu s PNG možnostmi

`FileOutputStream` zapisuje surové bajty do souboru. `PngOptions` konfiguruje úroveň komprese, typ barev a prokládání (interlacing) pro PNG výstup.

```java
FileOutputStream outputStream = new FileOutputStream(destName);
psdImage.save(outputStream, new PngOptions());
```

Gratulujeme! Úspěšně jste **převzeli PSD na PNG** načtením obrázku ze streamu pomocí Aspose.PSD pro Java.

## Časté problémy a řešení

- **OutOfMemoryError u velmi velkých PSD souborů** – Ujistěte se, že používáte streamingové API (`Image.load(InputStream)`) a vyhněte se volání `save` na objektech `PsdImage`, které byly plně rasterizovány v paměti.  
- **Chybějící vrstvy po konverzi** – Ověřte, že pracujete s instancí `PsdImage`; obecné objekty `Image` ztrácejí informace o vrstvách.  
- **Nesprávné barvy nebo průhlednost** – Nastavte `pngOptions.setColorType(PngColorType.TruecolorWithAlpha)`, aby se zachovaly alfa kanály.

## Často kladené otázky

**Q: Je Aspose.PSD pro Java vhodný pro hromadné zpracování obrázků?**  
A: Rozhodně. Streamingová architektura knihovny vám umožní procházet tisíce PSD souborů, převádět je na PNG a zapisovat přímo do výstupních streamů bez nadměrné spotřeby paměti.

**Q: Můžu vyzkoušet Aspose.PSD pro Java před zakoupením?**  
A: Ano, můžete si prohlédnout bezplatnou zkušební verzi [zde](https://releases.aspose.com/).

**Q: Kde najdu podporu pro Aspose.PSD pro Java?**  
A: Připojte se ke komunitě na [fóru Aspose.PSD](https://forum.aspose.com/c/psd/34) pro pomoc a diskuse.

**Q: Potřebuji dočasnou licenci pro testovací účely?**  
A: Získejte dočasnou licenci [zde](https://purchase.aspose.com/temporary-license/) pro testování Aspose.PSD pro Java.

**Q: Kde mohu zakoupit Aspose.PSD pro Java?**  
A: Navštivte [stránku nákupu](https://purchase.aspose.com/buy) a pořiďte si Aspose.PSD pro Java.

---

**Poslední aktualizace:** 2026-05-29  
**Testováno s:** Aspose.PSD for Java 24.12  
**Autor:** Aspose

## Související tutoriály

- [Uložit obrázky do streamu s Aspose.PSD pro Java](/psd/java/advanced-techniques/save-images-to-stream/)
- [Uložit obrázky na disk s Aspose.PSD pro Java](/psd/java/advanced-techniques/save-images-to-disk/)
- [Převést PSD na rastrové formáty obrázků s Aspose.PSD pro Java](/psd/java/advanced-techniques/convert-psd-to-raster-formats/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< blocks/products/products-backtop-button >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}