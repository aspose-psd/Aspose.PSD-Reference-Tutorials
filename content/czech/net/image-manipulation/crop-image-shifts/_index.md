---
title: Oříznutí obrázků pomocí posunů v Aspose.PSD pro .NET
linktitle: Oříznutí obrázků pomocí posunů
second_title: Aspose.PSD .NET API
description: Naučte se bez námahy ořezávat obrázky pomocí Aspose.PSD pro .NET. Postupujte podle našeho podrobného průvodce pro přesné úpravy obrazu.
type: docs
weight: 12
url: /cs/net/image-manipulation/crop-image-shifts/
---
## Úvod

V oblasti vývoje .NET vyniká Aspose.PSD jako výkonná sada nástrojů pro úlohy zpracování obrazu. Jednou z jeho pozoruhodných vlastností je schopnost přesně ořezávat obrázky díky funkci „Cropping by Shifts“. V tomto podrobném průvodci vás provedeme procesem bezproblémového oříznutí obrázků pomocí Aspose.PSD pro .NET.

## Předpoklady

Než se pustíte do výukového programu, ujistěte se, že máte splněny následující předpoklady:

-  Aspose.PSD for .NET Library: Ujistěte se, že máte nainstalovanou knihovnu. Pokud ne, můžete si jej stáhnout z[stránka vydání](https://releases.aspose.com/psd/net/).

- Prostředí .NET: Ujistěte se, že máte na svém počítači nastavené vývojové prostředí .NET.

- Ukázkový obrázek: Připravte si ukázkový obrázek ve formátu PSD, se kterým chcete pracovat.

## Importovat jmenné prostory

Začněte importováním potřebných jmenných prostorů do vašeho projektu .NET. Tyto jmenné prostory poskytují přístup k třídám a metodám Aspose.PSD potřebným pro oříznutí obrázku.

```csharp
using Aspose.PSD.ImageOptions;
```

## Krok 1: Definujte svůj adresář dokumentů

Nastavte cestu k adresáři vašeho dokumentu, kde budou umístěny zdrojové a cílové soubory.

```csharp
string dataDir = "Your Document Directory";
```

## Krok 2: Načtěte zdrojový obrázek

Vložte obrázek PSD, který chcete oříznout. Nezapomeňte nahradit "sample.psd" názvem vašeho zdrojového souboru.

```csharp
string sourceFile = dataDir + @"sample.psd";
string destName = dataDir + @"CroppingByShifts_out.jpg";
```

## Krok 3: Uložte obrazová data do mezipaměti pro lepší výkon

Před oříznutím je vhodné uložit data obrázku do mezipaměti pro lepší výkon.

```csharp
using (RasterImage rasterImage = (RasterImage)Image.Load(sourceFile))
{
    if (!rasterImage.IsCached)
    {
        rasterImage.CacheData();
    }
```

## Krok 4: Definujte hodnoty posunu pro oříznutí

Zadejte hodnoty posunu pro levou, pravou, horní a spodní stranu obrazu. Upravte tyto hodnoty na základě vašich požadavků na oříznutí.

```csharp
int leftShift = 10;
int rightShift = 10;
int topShift = 10;
int bottomShift = 10;
```

## Krok 5: Použijte oříznutí a uložte výsledky

 Využijte`Crop` metoda pro použití zadaných posunů a uložení oříznutého obrázku do cílového souboru.

```csharp
rasterImage.Crop(leftShift, rightShift, topShift, bottomShift);
rasterImage.Save(destName, new JpegOptions());
}
```

## Závěr

Gratulujeme! Úspěšně jste se naučili ořezávat obrázky po směnách pomocí Aspose.PSD pro .NET. Tato výkonná funkce vám poskytuje přesnost a kontrolu potřebnou pro různé úlohy zpracování obrazu.

## FAQ

### Q1: Mohu oříznout obrázky různých formátů, nejen PSD?

Odpověď 1: Ano, Aspose.PSD podporuje různé formáty obrázků, což vám umožňuje oříznout obrázky ve formátech jako JPEG, PNG a dalších.

### Q2: Je před zakoupením Aspose.PSD pro .NET k dispozici zkušební verze?

 A2: Určitě! Sadu nástrojů můžete prozkoumat pomocí bezplatné zkušební verze[tady](https://releases.aspose.com/).

### Q3: Jak získám dočasnou licenci pro Aspose.PSD pro .NET?

 A3: Můžete získat dočasnou licenci pro testovací účely[tady](https://purchase.aspose.com/temporary-license/).

### Q4: Kde najdu další podporu a diskuse týkající se Aspose.PSD?

 A4: Navštivte[Fórum Aspose.PSD](https://forum.aspose.com/c/psd/34) za podporu a poutavé diskuze.

### Q5: Mohu zakoupit Aspose.PSD pro .NET přímo z webu?

 A5: Ano, můžete si knihovnu bezpečně zakoupit od[nákupní stránku](https://purchase.aspose.com/buy).
