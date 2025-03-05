---
title: Oříznutí souborů PSD při převodu na PNG v Aspose.PSD pro .NET
linktitle: Oříznutí souborů PSD při převodu do PNG
second_title: Aspose.PSD .NET API
description: Naučte se, jak bez námahy oříznout soubory PSD pomocí Aspose.PSD pro .NET. Postupujte podle našeho podrobného průvodce pro bezproblémový převod do formátu PNG.
type: docs
weight: 18
url: /cs/net/psd-file-manipulation/crop-psd-conversion-png/
---
## Zavedení
V oblasti vývoje .NET je manipulace a konverze obrázků běžným úkolem. Aspose.PSD for .NET poskytuje výkonnou sadu nástrojů pro zefektivnění tohoto procesu. Jedním z častých požadavků je oříznutí souborů PSD před jejich převedením na PNG. V tomto tutoriálu krok za krokem se ponoříme do procesu pomocí Aspose.PSD pro .NET.
## Předpoklady
Než se vydáme na tuto cestu, ujistěte se, že máte následující:
-  Aspose.PSD for .NET Library: Stáhněte a nainstalujte knihovnu z[Aspose.PSD pro dokumentaci .NET](https://reference.aspose.com/psd/net/).
- Ukázkový soubor PSD: Připravte si soubor PSD k experimentování. Pokud žádný nemáte, můžete použít ukázku poskytnutou v tutoriálu.
- Prostředí .NET: Ujistěte se, že máte nastavené funkční vývojové prostředí .NET.
- Adresář dokumentů: Zadejte cestu k adresáři dokumentů v kódu.
## Importovat jmenné prostory
Ve svém projektu .NET zahrňte potřebné jmenné prostory pro Aspose.PSD pro .NET:
```csharp
using Aspose.PSD.ImageOptions;
```
## Krok 1: Načtěte obrázek PSD
```csharp
// Cesta k adresáři dokumentů.
string dataDir = "Your Document Directory";
string srcPath = dataDir + @"sample.psd";
// Načtěte existující obrázek PSD
using (RasterImage image = (RasterImage)Image.Load(srcPath))
{
    // Zde bude váš kód pro další kroky
}
```
## Krok 2: Definujte obdélník pro oříznutí
```csharp
// Vytvořte instanci třídy Rectangle předáním x, y, šířky a výšky
Rectangle cropRectangle = new Rectangle(0, 0, 350, 450);
```
## Krok 3: Ořízněte obrázek
```csharp
// Zavolejte metodu oříznutí třídy Image a předejte instanci třídy obdélník
image.Crop(cropRectangle);
```
## Krok 4: Zadejte možnosti PNG
```csharp
// Vytvořte instanci třídy PngOptions
PngOptions pngOptions = new PngOptions();
```
## Krok 5: Uložte oříznutý obrázek jako PNG
```csharp
// Zavolejte metodu uložení, zadejte výstupní cestu a PngOptions pro převod souboru PSD na PNG a uložení výstupu
string destName = dataDir + @"export.png";
image.Save(destName, pngOptions);
```
## Závěr

Gratuluji! Úspěšně jste se naučili, jak oříznout soubory PSD při jejich převodu na PNG pomocí Aspose.PSD for .NET. Tato schopnost může být neocenitelná v různých scénářích zpracování obrazu.

## FAQ

### Q1: Mohu tuto knihovnu použít v komerčním projektu?

 Odpověď 1: Ano, Aspose.PSD pro .NET je k dispozici pro komerční použití. Viz[Licencování Aspose.PSD](https://purchase.aspose.com/buy) pro podrobnosti.

### Q2: Je k dispozici bezplatná zkušební verze?

A2: Rozhodně! Můžete prozkoumat bezplatnou zkušební verzi[zde](https://releases.aspose.com/).

### Q3: Kde najdu podporu pro Aspose.PSD pro .NET?

 A3: Navštivte[Fórum Aspose.PSD](https://forum.aspose.com/c/psd/34) pro jakoukoli pomoc nebo dotazy.

### Q4: Jak získám dočasnou licenci?

 A4: Pokud potřebujete dočasnou licenci, můžete ji získat[zde](https://purchase.aspose.com/temporary-license/).

### Q5: Jsou v dokumentaci k dispozici nějaké příklady nebo výukové programy?

 A5: Ano, můžete najít komplexní dokumentaci a příklady[zde](https://reference.aspose.com/psd/net/).