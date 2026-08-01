---
date: 2026-08-01
description: Naučte se, jak upravit gammu v Java zpracování obrazu s Aspose.PSD, převést
  PSD na TIFF a opravit vybledlé obrázky v stručném tutoriálu.
keywords:
- how to adjust gamma
- fix washed out image
- java image processing
- convert psd to tiff
- server side image processing
lastmod: 2026-08-01
linktitle: Upravit gammu obrázku
og_description: Naučte se, jak upravit gammu v Java zpracování obrazu pomocí Aspose.PSD
  – rychlé server‑side knihovny, která opravuje vybledlé obrázky a převádí PSD na
  TIFF během několika řádků kódu.
og_image_alt: 'Guide: Adjust gamma in Java images with Aspose.PSD, convert PSD to
  TIFF'
og_title: jak upravit gammu – Java zpracování s Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-08-01'
  description: Learn how to adjust gamma in Java image processing with Aspose.PSD,
    convert PSD to TIFF, and fix washed‑out images in a concise tutorial.
  headline: How to Adjust Gamma in Java Image Processing with Aspose.PSD
  type: TechArticle
- description: Learn how to adjust gamma in Java image processing with Aspose.PSD,
    convert PSD to TIFF, and fix washed‑out images in a concise tutorial.
  name: How to Adjust Gamma in Java Image Processing with Aspose.PSD
  steps:
  - name: '**Java Development Environment** – Java 8 or later installed.'
    text: '**Java Development Environment** – Java 8 or later installed.'
  - name: '**Aspose.PSD Library** – Download and add the JAR to your project. See
      the official [documentation](https://reference.aspose.com/psd/java/).'
    text: '**Aspose.PSD Library** – Download and add the JAR to your project. See
      the official [documentation](https://reference.aspose.com/psd/java/).'
  - name: '**Sample Image** – A PSD file you want to process (e.g., `sample.psd`).'
    text: '**Sample Image** – A PSD file you want to process (e.g., `sample.psd`).'
  type: HowTo
- questions:
  - answer: Yes – the `adjustGamma` method accepts separate float values for red,
      green, and blue channels.
    question: Can I apply different gamma values to each colour channel?
  - answer: Absolutely. You can perform resizing, cropping, or colour corrections
      sequentially on the same `RasterImage` instance.
    question: Is it possible to chain multiple image adjustments before saving?
  - answer: Yes, each layer can be accessed and processed individually.
    question: Does Aspose.PSD support multi‑page PSD files?
  - answer: Aspose.PSD supports PNG, JPEG, BMP, and many other formats via their respective
      options classes.
    question: What format can I export to besides TIFF?
  - answer: Start with a moderate gamma (around 2.0) and preview the result; adjust
      downwards if the image looks too bright.
    question: How do I avoid a washed‑out image after gamma correction?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- adjust gamma
- Aspose.PSD
- Java image processing
- PSD to TIFF
- server side processing
title: Jak upravit gammu v Java zpracování obrazu s Aspose.PSD
url: /cs/java/advanced-techniques/adjust-gamma/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak upravit gama v Java zpracování obrazu s Aspose.PSD

## Úvod

Pokud pracujete na **java image processing**, naučit se **how to adjust gamma** je základní technika pro zlepšení jasu a kontrastu bez ztráty detailů. V tomto tutoriálu vás provedeme tím, jak použít **Aspose.PSD for Java** k aplikaci korekce gama na soubor PSD, **convert PSD to TIFF**, a vyhnout se **washed‑out image**. Uvidíte, proč je tento přístup rychlý, spolehlivý a ideální pro **server‑side image processing** pipeline.

## Rychlé odpovědi
- **Co dělá korekce gama?** Přemapuje hodnoty luminance tak, aby tmavé oblasti byly světlejší nebo světlé oblasti tmavší, přičemž zachovává celkový detail.  
- **Která knihovna zpracování provádí?** Aspose.PSD for Java poskytuje dedikovanou metodu `adjustGamma` pro rastrové obrázky.  
- **Mohu převést PSD na TIFF ve stejném toku?** Ano – po úpravě gama můžete obrázek uložit přímo do TIFF pomocí `TiffOptions`.  
- **Potřebuji licenci pro vývoj?** Bezplatná zkušební verze funguje pro testování; pro produkční použití je vyžadována komerční licence.  
- **Jaká verze Javy je podporována?** Aspose.PSD podporuje Java 8 a novější.

## Co je Java Gamma Correction?

Korekce gama mění nelineární vztah mezi zakódovanými hodnotami pixelů a zobrazeným jasem. Úpravou křivky gama můžete **fix washed out image** problémy nebo vylepšit detaily ve stínech bez přeexponování světel. Funguje tak, že na každý pixel aplikuje funkci mocninného zákona, která zesvětlí tmavé tóny a stlačí světla, což vede k přirozenějšímu vizuálnímu vzhledu.

## Proč použít Aspose.PSD pro Gamma Correction?

Aspose.PSD je **java image processing library**, která abstrahuje složitosti formátu PSD. Podporuje zpracování souborů až do 2 GB, zvládá více než 50 různých formátů obrázků a poskytuje jednoduché volání `adjustGamma`, což z ní činí ideální řešení pro **java gamma correction** a **convert PSD to TIFF** pracovní postupy.

## Požadavky

1. **Java Development Environment** – Java 8 nebo novější nainstalováno.  
2. **Aspose.PSD Library** – Stáhněte a přidejte JAR do svého projektu. Viz oficiální [documentation](https://reference.aspose.com/psd/java/).  
3. **Sample Image** – PSD soubor, který chcete zpracovat (např. `sample.psd`).  

## Importovat balíčky

Před zahájením importujte nezbytné jmenné prostory, které vám poskytují přístup k manipulaci s rastrem a možnostmi formátu souboru.

## Krok 1: Načíst obrázek

Třída `RasterImage` představuje rasterizovaná data pixelů vrstvy PSD v paměti. Načtení obrázku jednou a jeho cachování snižuje zatížení paměti při následných úpravách.

## Krok 2: Upravit Gamu

Načtěte svůj PSD pomocí `new RasterImage("sample.psd")` a zavolejte `rasterImage.adjustGamma(2.0f)` — tento jediný řádek aplikuje gamu 2.0 na všechny barevné kanály, zesvětluje stíny a zachovává světla nedotčená. Můžete předat samostatné hodnoty pro červenou, zelenou a modrou, pokud jsou vyžadovány úpravy specifické pro kanál.

## Krok 3: Vytvořit TiffOptions

`TiffOptions` vám umožňuje řídit kompresi, bity na vzorek a další nastavení specifická pro TIFF. Nastavení 8‑bitového vzorku (`{8,8,8}`) udržuje velikost TIFF souboru rozumnou a zachovává barevnou věrnost.

## Krok 4: Uložit výsledný obrázek

Zavolejte `rasterImage.save("output.tif", tiffOptions)`, abyste zapsali zpracovaný obrázek na disk. Po uložení můžete TIFF předat následným systémům, jako jsou tiskové služby nebo webová API.

## Běžné případy použití

- **Automated graphics pipelines** – Upravit gamu za běhu před generováním náhledů.  
- **Batch conversion tools** – Převádět velké archivy PSD na TIFF při normalizaci jasu.  
- **Web services** – Poskytnout koncový bod, který přijme PSD, aplikuje korekci gama a vrátí TIFF pro konzumaci klientem.

## Běžné problémy a řešení

| Problém | Proč se to děje | Jak opravit |
|---------|----------------|-------------|
| **Obrázek vypadá vybledle** | Hodnota gama je příliš vysoká (např. > 2.5) | Snižte faktor gama na hodnotu mezi 1.8 a 2.2. |
| **`rasterImage.isCached()` returns false** | Obrázek ještě není načten do paměti | Zavolejte `rasterImage.cacheData()` před úpravou gama. |
| **Velikost TIFF souboru je velká** | Bity na vzorek nastaveny na 16‑bit | Použijte 8‑bitový vzorek (`{8,8,8}`) jak je ukázáno v příkladu. |

## Často kladené otázky

**Q: Mohu použít různé hodnoty gama pro každý barevný kanál?**  
A: Ano – metoda `adjustGamma` přijímá samostatné float hodnoty pro červený, zelený a modrý kanál.

**Q: Je možné řetězit více úprav obrázku před uložením?**  
A: Rozhodně. Můžete provádět změnu velikosti, ořezávání nebo korekce barev postupně na stejné instanci `RasterImage`.

**Q: Podporuje Aspose.PSD soubory PSD s více stránkami?**  
A: Ano, každá vrstva může být přístupná a zpracována samostatně.

**Q: Do jakých formátů mohu exportovat kromě TIFF?**  
A: Aspose.PSD podporuje PNG, JPEG, BMP a mnoho dalších formátů prostřednictvím jejich příslušných tříd možností.

**Q: Jak se vyhnout vybledlému obrázku po korekci gama?**  
A: Začněte s mírnou hodnotou gama (kolem 2.0) a prohlédněte výsledek; snižte ji, pokud obrázek vypadá příliš jasně.

## Závěr

Gratulujeme! Úspěšně jste se naučili **how to adjust gamma** v **java image processing** pracovním postupu, převedli PSD na TIFF a vyhnuli se běžným úskalím, jako je **washed‑out image**. Tento vzor vám poskytuje jemnou kontrolu nad jasem a kontrastem, což jej činí ideálním pro automatizované grafické pipeline, webové služby nebo desktopové utility.

---

**Last Updated:** 2026-08-01  
**Tested With:** Aspose.PSD 24.11 for Java  
**Author:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Související tutoriály

- [Java Image Processing Tutorial - Úprava jasu obrázku s Aspose.PSD pro Java](/psd/java/advanced-techniques/adjust-brightness/)
- [Jak převést PSD na TIFF a upravit kontrast s Aspose.PSD pro Java](/psd/java/advanced-techniques/adjust-contrast/)
- [Převod PSD na obrázek v Javě – Použití úpravných vrstev s Aspose.PSD](/psd/java/advanced-psd-layer-features-effects/apply-adjustment-layers-psd-files/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

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

```java
// Adjust the gamma
rasterImage.adjustGamma(2.2f, 2.2f, 2.2f);
```

```java
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

```java
// Save the resultant image to TIFF format
String destName = dataDir + "AdjustGamma_out.tiff";
rasterImage.save(destName, tiffOptions);
```