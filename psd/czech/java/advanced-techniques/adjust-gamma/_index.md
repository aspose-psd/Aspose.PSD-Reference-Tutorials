---
date: 2025-12-21
description: Naučte se provádět zpracování obrázků v Javě úpravou gama obrázku pomocí
  Aspose.PSD. Krok za krokem průvodce převodem PSD na TIFF a aplikací korekce gama.
linktitle: Adjust Gamma of an Image
second_title: Aspose.PSD Java API
title: Zpracování obrázků v Javě – Úprava gama pomocí Aspose.PSD
url: /cs/java/advanced-techniques/adjust-gamma/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java Image Processing – Úprava gama pomocí Aspose.PSD

## Úvod

Pokud pracujete na **java image processing**, úprava gama obrázku je základní technikou pro zlepšení jasu a kontrastu bez ztráty detailů. V tomto tutoriálu vás provedeme, jak použít **Aspose.PSD for Java** k aplikaci korekce gama na soubor PSD a následnému exportu výsledku jako TIFF obrázek. Uvidíte, proč je tento přístup rychlý, spolehlivý a ideální pro server‑side image pipelines.

## Rychlé odpovědi
- **Co dělá korekce gama?** Přemapuje hodnoty luminance tak, aby tmavé oblasti byly jasnější nebo světlé oblasti tmavší při zachování celkových detailů.  
- **Která knihovna zpracování provádí?** Aspose.PSD for Java poskytuje vyhrazenou metodu `adjustGamma` pro rastrové obrázky.  
- **Mohu převést PSD na TIFF ve stejném toku?** Ano – po úpravě gama můžete obrázek uložit přímo do TIFF pomocí `TiffOptions`.  
- **Potřebuji licenci pro vývoj?** Bezplatná zkušební verze funguje pro testování; pro produkční použití je vyžadována komerční licence.  
- **Jaká verze Javy je podporována?** Aspose.PSD podporuje Java 8 a novější.

## Co je java image processing?

Java image processing označuje manipulaci, analýzu a transformaci vizuálních dat pomocí Java knihoven. Úkoly zahrnují změnu velikosti, filtrování, korekci barev a konverzi formátů – vše lze automatizovat v desktopových nebo webových aplikacích.

## Proč použít Aspose.PSD pro korekci gama?

Aspose.PSD nabízí API na vysoké úrovni, které abstrahuje složitost formátu PSD, což vám umožní soustředit se na samotné úpravy obrázku. Zajišťuje cachování, barevné profily a poskytuje jednoduché volání `adjustGamma`, což ho činí ideálním pro **image gamma correction** a **convert psd to tiff** pracovní postupy.

## Předpoklady

Před ponořením se do tutoriálu se ujistěte, že máte nastaveny následující předpoklady:

1. **Java Development Environment** – Ujistěte se, že máte na svém systému nainstalováno Java vývojové prostředí.  
2. **Aspose.PSD Library** – Stáhněte a integrujte knihovnu Aspose.PSD do svého Java projektu. Potřebné zdroje najdete v [documentation](https://reference.aspose.com/psd/java/).  
3. **Sample Image** – Připravte ukázkový PSD obrázek, který použijete pro aplikaci úpravy gama.

## Importování balíčků

Pro zahájení procesu importujte požadované balíčky ve svém Java projektu. Tím připravíte prostředí pro plynulé využití funkcí Aspose.PSD.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## Krok 1: Načtení obrázku

Začněte načtením ukázkového PSD obrázku do instance třídy `RasterImage`. Toto je základ pro následné úpravy gama.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);

// Cast object of Image to RasterImage
RasterImage rasterImage = (RasterImage)image;

// Check if RasterImage is cached for better performance
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

## Krok 2: Úprava gama

Nyní upravte gama načteného obrázku pomocí metody `adjustGamma`. Jemně dolaďte hodnoty gama podle vašich požadavků.

```java
// Adjust the gamma
rasterImage.adjustGamma(2.2f, 2.2f, 2.2f);
```

## Krok 3: Vytvoření TiffOptions

Vytvořte instanci `TiffOptions` pro výsledný obrázek. Nastavte různé vlastnosti, jako jsou bity na vzorek a fotometrické možnosti, aby výstup odpovídal vašim specifikacím.

```java
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

## Krok 4: Uložení výsledného obrázku

Uložte upravený obrázek do formátu TIFF pomocí dříve definovaného `TiffOptions`.

```java
// Save the resultant image to TIFF format
String destName = dataDir + "AdjustGamma_out.tiff";
rasterImage.save(destName, tiffOptions);
```

## Časté problémy a řešení

| Problém | Proč se vyskytuje | Jak opravit |
|---------|-------------------|-------------|
| **Obrázek vypadá vyplavený** | Hodnota gama příliš vysoká (např. > 2.5) | Snižte faktor gama na hodnotu mezi 1.8 a 2.2. |
| **`rasterImage.isCached()` vrací false** | Obrázek ještě není načten do paměti | Zavolejte `rasterImage.cacheData()` před úpravou gama. |
| **Velikost TIFF souboru je velká** | Bity na vzorek nastaveny na 16‑bit | Použijte 8‑bitový vzorek (`{8,8,8}`) jak je ukázáno v příkladu. |

## Často kladené otázky

**Q: Mohu použít různé hodnoty gama pro každý barevný kanál?**  
A: Ano – metoda `adjustGamma` přijímá samostatné float hodnoty pro červený, zelený a modrý kanál.

**Q: Je možné řetězit více úprav obrázku před uložením?**  
A: Rozhodně. Můžete provádět změnu velikosti, ořezávání nebo korekce barev postupně na stejné instanci `RasterImage`.

**Q: Podporuje Aspose.PSD soubory PSD s více stránkami?**  
A: Ano, každá vrstva může být přístupná a zpracována samostatně.

**Q: Do jakých formátů mohu exportovat kromě TIFF?**  
A: Aspose.PSD podporuje PNG, JPEG, BMP a mnoho dalších formátů prostřednictvím jejich příslušných tříd možností.

## Závěr

Gratulujeme! Úspěšně jste provedli **java image processing** úpravou gama souboru PSD a jeho exportem jako TIFF obrázku pomocí Aspose.PSD for Java. Tento pracovní postup vám poskytuje detailní kontrolu nad jasem a kontrastem obrázku, což ho činí ideálním pro automatizované grafické pipeline, webové služby nebo desktopové nástroje.

---

**Last Updated:** 2025-12-21  
**Tested With:** Aspose.PSD 24.11 for Java  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

## FAQ

### Q1: Kde mohu najít dokumentaci k Aspose.PSD?

A1: Dokumentaci můžete získat na [https://reference.aspose.com/psd/java/](https://reference.aspose.com/psd/java/).

### Q2: Jak stáhnu Aspose.PSD pro Java?

A2: Knihovnu stáhněte z [https://releases.aspose.com/psd/java/](https://releases.aspose.com/psd/java/).

### Q3: Kde mohu zakoupit Aspose.PSD?

A3: Navštivte [https://purchase.aspose.com/buy](https://purchase.aspose.com/buy) pro nákup Aspose.PSD.

### Q4: Je k dispozici bezplatná zkušební verze?

A4: Ano, můžete vyzkoušet bezplatnou verzi na [https://releases.aspose.com/](https://releases.aspose.com/).

### Q5: Kde mohu získat podporu pro Aspose.PSD?

A5: Pro podporu navštivte fórum Aspose.PSD na [https://forum.aspose.com/c/psd/34](https://forum.aspose.com/c/psd/34).