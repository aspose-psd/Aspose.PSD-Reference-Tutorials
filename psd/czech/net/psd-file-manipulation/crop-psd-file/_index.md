---
title: Oříznutí souborů PSD pomocí Aspose.PSD pro .NET
linktitle: Oříznutí souborů PSD pomocí Aspose.PSD pro .NET
second_title: Aspose.PSD .NET API
description: Prozkoumejte umění ořezávání souborů PSD v .NET s Aspose.PSD, všestrannou sadou nástrojů. Zvyšte svou hru manipulace s obrázky bez námahy.
type: docs
weight: 19
url: /cs/net/psd-file-manipulation/crop-psd-file/
---
## Zavedení
V oblasti vývoje .NET vyniká Aspose.PSD jako výkonná sada nástrojů pro bezproblémovou manipulaci se soubory PSD (Photoshop Document). Pokud jde o manipulaci s obrázky, oříznutí je základní operací a Aspose.PSD zjednodušuje tento proces pro vývojáře .NET. V tomto tutoriálu prozkoumáme, jak oříznout soubory PSD pomocí Aspose.PSD pro .NET, a poskytneme vám průvodce krok za krokem.
## Předpoklady
Než se ponoříte do výukového programu, ujistěte se, že máte následující předpoklady:
-  Aspose.PSD pro .NET: Ujistěte se, že máte nainstalovanou knihovnu. Můžete si jej stáhnout z[Aspose.PSD pro dokumentaci .NET](https://reference.aspose.com/psd/net/).
- Vývojové prostředí: Nastavte své vývojové prostředí .NET, včetně sady Visual Studio nebo libovolného preferovaného IDE.
## Importovat jmenné prostory
Začněte importováním potřebných jmenných prostorů do vašeho projektu:
```csharp
using Aspose.PSD.FileFormats.Png;
using Aspose.PSD.ImageOptions;
```
## Krok 1: Nastavte svůj projekt
Vytvořte nový .NET projekt nebo otevřete existující ve vámi preferovaném IDE.
## Krok 2: Zahrňte knihovnu Aspose.PSD
 Přidejte do projektu odkaz na knihovnu Aspose.PSD. Můžete to provést stažením knihovny z[Stránka ke stažení Aspose.PSD](https://releases.aspose.com/psd/net/).
## Krok 3: Inicializujte Aspose.PSD
Ve svém kódu inicializujte Aspose.PSD načtením souboru PSD:
```csharp
string dataDir = "Your Document Directory";
string sourceFileName = dataDir + "1.psd";
using (RasterImage image = Image.Load(sourceFileName) as RasterImage)
{
    // Váš kód zde
}
```
## Krok 4: Ořízněte soubor PSD
Implementujte správnou metodu oříznutí pro soubory PSD. Zadejte parametry oříznutí pomocí objektu Rectangle:
```csharp
image.Crop(new Rectangle(10, 30, 100, 100));
```
Upravte hodnoty v konstruktoru Obdélník podle vašich požadavků na oříznutí.
## Krok 5: Uložte oříznutý obrázek
Uložte oříznutý obrázek ve formátu PSD i PNG:
```csharp
string exportPathPsd = dataDir + "CropTest.psd";
string exportPathPng = dataDir + "CropTest.png";
image.Save(exportPathPsd, new PsdOptions());
image.Save(exportPathPng, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
```
## Závěr

Gratuluji! Úspěšně jste se naučili, jak oříznout soubory PSD pomocí Aspose.PSD pro .NET. Tento jednoduchý, ale výkonný proces lze bez problémů integrovat do vašich aplikací .NET pro efektivní manipulaci s obrázky.

## FAQ

### Q1: Je Aspose.PSD kompatibilní s nejnovějšími frameworky .NET?

Odpověď 1: Ano, Aspose.PSD je pravidelně aktualizován, aby byla zajištěna kompatibilita s nejnovějšími frameworky .NET.

### Q2: Mohu použít Aspose.PSD pro komerční projekty?

 A2: Rozhodně! Aspose.PSD je k dispozici pro komerční použití. Můžete si jej zakoupit[zde](https://purchase.aspose.com/buy).

### Q3: Je k dispozici bezplatná zkušební verze?

 A3: Ano, můžete prozkoumat Aspose.PSD s bezplatnou zkušební verzí. Stáhněte si to[zde](https://releases.aspose.com/).

### Q4: Kde najdu podporu pro Aspose.PSD?

 A4: Máte-li jakékoli dotazy nebo pomoc, navštivte[Fórum Aspose.PSD](https://forum.aspose.com/c/psd/34).

### Q5: Potřebuji dočasnou licenci pro testovací účely?

 A5: Ano, pokud potřebujete dočasnou licenci, můžete ji získat[zde](https://purchase.aspose.com/temporary-license/).