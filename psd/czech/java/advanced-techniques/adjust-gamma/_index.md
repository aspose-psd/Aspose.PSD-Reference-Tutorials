---
date: 2026-02-27
description: Naučte se, jak upravit gamu při zpracování obrazu v Javě s Aspose.PSD,
  převést PSD na TIFF a opravit vybledlé obrázky v stručném tutoriálu.
linktitle: Adjust Gamma of an Image
second_title: Aspose.PSD Java API
title: Jak upravit gama v Java zpracování obrazu s Aspose.PSD
url: /cs/java/advanced-techniques/adjust-gamma/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak upravit gama v Java zpracování obrazu s Aspose.PSD

## Úvod

Pokud pracujete na **java image processing**, naučit se **jak upravit gama** je základní technika pro zlepšení jasu a kontrastu bez ztráty detailů. V tomto tutoriálu vás provedeme použitím **Aspose.PSD for Java** k aplikaci korekce gama na soubor PSD, **převodu PSD na TIFF** a vyhnutí se **vybledlému obrazu**. Uvidíte, proč je tento přístup rychlý, spolehlivý a ideální pro server‑side image pipelines.

## Rychlé odpovědi
- **Co dělá korekce gama?** Přemapuje hodnoty luminance tak, aby tmavé oblasti byly světlejší nebo světlé oblasti tmavší, přičemž zachovává celkový detail.  
- **Která knihovna provádí zpracování?** Aspose.PSD for Java poskytuje dedikovanou metodu `adjustGamma` pro rastrové obrázky.  
- **Mohu převést PSD na TIFF ve stejném toku?** Ano – po úpravě gama můžete obrázek přímo uložit do TIFF pomocí `TiffOptions`.  
- **Potřebuji licenci pro vývoj?** Bezplatná zkušební verze funguje pro testování; pro produkční použití je vyžadována komerční licence.  
- **Jaká verze Javy je podporována?** Aspose.PSD podporuje Java 8 a novější.

## Jak upravit gama v Java zpracování obrazu
Úprava gama je základní součástí každého **java image processing tutorial**, který se zabývá jasem nebo kontrastem. Níže rozkládáme kroky, vysvětlujeme, proč je každý řádek důležitý, a ukazujeme, jak proces začlenit do vašeho existujícího kódu.

## Co je Java korekce gama?
Korekce gama mění nelineární vztah mezi kódovanými hodnotami pixelů a zobrazovaným jasem. Úpravou gama křivky můžete **odstranit problémy s vybledlým obrazem** nebo zvýraznit detaily ve stínech bez přeexponování světel.

## Proč použít Aspose.PSD pro korekci gama?
Aspose.PSD funguje jako výkonná **java image processing library**, která abstrahuje složitosti formátu PSD. Zpracovává barevné profily, cachování a poskytuje jednoduché volání `adjustGamma`, což ji činí ideální pro **java gamma correction** a **convert PSD to TIFF** workflow.

## Předpoklady

1. **Java Development Environment** – nainstalována Java 8 nebo novější.  
2. **Aspose.PSD Library** – stáhněte a přidejte JAR do svého projektu. Viz oficiální [documentation](https://reference.aspose.com/psd/java/).  
3. **Ukázkový obrázek** – soubor PSD, který chcete zpracovat (např. `sample.psd`).  

## Import balíčků

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## Krok 1: Načtení obrázku

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

**Tip:** Cachování rastrových dat jednou snižuje paměťové zatížení při aplikaci více úprav po sobě.

## Krok 2: Úprava gama

```java
// Adjust the gamma
rasterImage.adjustGamma(2.2f, 2.2f, 2.2f);
```

Můžete předat různé hodnoty pro červený, zelený a modrý kanál, pokud potřebujete úpravy specifické pro kanál.

## Krok 3: Vytvoření TiffOptions

```java
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

Nastavení 8‑bitového vzorku (`{8,8,8}`) udržuje velikost TIFF souboru rozumnou a zároveň zachovává barevnou věrnost.

## Krok 4: Uložení výsledného obrázku

```java
// Save the resultant image to TIFF format
String destName = dataDir + "AdjustGamma_out.tiff";
rasterImage.save(destName, tiffOptions);
```

Po uložení můžete TIFF předat do downstream systémů, jako jsou tiskové služby nebo webové API.

## Běžné případy použití

- **Automatizované grafické pipeline** – Úprava gama za běhu před generováním náhledových obrázků.  
- **Nástroje pro hromadný převod** – Převod velkých archivů PSD na TIFF při normalizaci jasu.  
- **Webové služby** – Poskytnutí endpointu, který přijme PSD, aplikuje korekci gama a vrátí TIFF pro klienta.

## Běžné problémy a řešení

| Problém | Proč k tomu dochází | Jak opravit |
|---------|---------------------|-------------|
| **Obrázek vypadá vybledle** | Hodnota gama příliš vysoká (např. > 2.5) | Snižte faktor gama na hodnotu mezi 1.8 a 2.2. |
| **`rasterImage.isCached()` vrací false** | Obrázek ještě není načten do paměti | Zavolejte `rasterImage.cacheData()` před úpravou gama. |
| **Velikost TIFF souboru je velká** | Bits per sample nastaven na 16‑bit | Použijte 8‑bitový vzorek (`{8,8,8}`) jako v příkladu. |

## Často kladené otázky

**Q: Mohu použít různé hodnoty gama pro každý barevný kanál?**  
A: Ano – metoda `adjustGamma` přijímá samostatné float hodnoty pro červený, zelený a modrý kanál.

**Q: Je možné řetězit více úprav obrazu před uložením?**  
A: Rozhodně. Můžete provádět změnu velikosti, ořez nebo barevné korekce sekvenčně na stejném `RasterImage` instance.

**Q: Podporuje Aspose.PSD soubory PSD s více stránkami?**  
A: Ano, každá vrstva může být přístupná a zpracována samostatně.

**Q: Do jakých formátů mohu exportovat kromě TIFF?**  
A: Aspose.PSD podporuje PNG, JPEG, BMP a mnoho dalších formátů prostřednictvím jejich příslušných options tříd.

**Q: Jak se vyhnout vybledlému obrazu po korekci gama?**  
A: Začněte s mírnou hodnotou gama (kolem 2.0) a náhled výsledku; pokud je obrázek příliš světlý, snižte hodnotu.

## Závěr

Gratulujeme! Úspěšně jste se naučili **jak upravit gama** v **java image processing** workflow, převést PSD na TIFF a vyhnout se běžným úskalím, jako je **vybledlý obraz**. Tento vzor vám poskytuje detailní kontrolu nad jasem a kontrastem, což je ideální pro automatizované grafické pipeline, webové služby nebo desktopové utility.

---

**Poslední aktualizace:** 2026-02-27  
**Testováno s:** Aspose.PSD 24.11 for Java  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}