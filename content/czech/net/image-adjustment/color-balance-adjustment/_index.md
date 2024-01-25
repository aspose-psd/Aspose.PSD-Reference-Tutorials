---
title: Použití úpravy vyvážení barev v Aspose.PSD pro .NET
linktitle: Použití úpravy vyvážení barev
second_title: Aspose.PSD .NET API
description: Vylepšete barvy obrazu PSD bez námahy pomocí funkce Color Balance Adjustment Aspose.PSD for .NET. Postupujte podle našeho podrobného průvodce pro ohromující výsledky.
type: docs
weight: 14
url: /cs/net/image-adjustment/color-balance-adjustment/
---
## Úvod

Vítejte v tomto komplexním průvodci o aplikaci Color Balance Adjustment v Aspose.PSD pro .NET! Aspose.PSD je výkonná knihovna .NET, která umožňuje vývojářům efektivně pracovat se soubory PSD. V tomto tutoriálu se zaměříme na funkci Color Balance Adjustment, která vám umožní snadno zlepšit vyvážení barev vašich obrázků PSD.

## Předpoklady

Než se pustíme do výukového programu, ujistěte se, že máte splněny následující předpoklady:

-  Aspose.PSD for .NET Library: Stáhněte a nainstalujte knihovnu z[Web Aspose.PSD](https://releases.aspose.com/psd/net/).
- Vývojové prostředí: Ujistěte se, že máte na svém počítači nastavené funkční vývojové prostředí .NET.
- Soubor PSD: Připravte si soubor PSD, na který chcete použít úpravu vyvážení barev.

## Importovat jmenné prostory

Ve svém projektu .NET zahrňte potřebné jmenné prostory pro použití funkcí Aspose.PSD. Přidejte do kódu následující řádky:

```csharp
using Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers;
```

Nyní si proces úpravy vyvážení barev rozdělíme do několika kroků:

## Krok 1: Načtěte soubor PSD

```csharp
string dataDir = "Your Document Directory";
var filePath = dataDir + "ColorBalance.psd";
var outputPath = dataDir + "ColorBalance_out.psd";

using (var im = (FileFormats.Psd.PsdImage)Image.Load(filePath))
{
    // Kód pro úpravu vyvážení barev bude přidán v následujících krocích.
}
```

## Krok 2: Otevřete a upravte vyvážení barev

```csharp
foreach (var layer in im.Layers)
{
    var cbLayer = layer as ColorBalanceAdjustmentLayer;
    if (cbLayer != null)
    {
        cbLayer.ShadowsCyanRedBalance = 30;
        cbLayer.ShadowsMagentaGreenBalance = -15;
        cbLayer.ShadowsYellowBlueBalance = 40;
        cbLayer.MidtonesCyanRedBalance = -90;
        cbLayer.MidtonesMagentaGreenBalance = -25;
        cbLayer.MidtonesYellowBlueBalance = 20;
        cbLayer.HighlightsCyanRedBalance = -30;
        cbLayer.HighlightsMagentaGreenBalance = 67;
        cbLayer.HighlightsYellowBlueBalance = -95;
        cbLayer.PreserveLuminosity = true;
    }
}
```

## Krok 3: Uložte upravený obrázek

```csharp
im.Save(outputPath);
```

Nyní jste úspěšně aplikovali Color Balance Adjustment na váš soubor PSD pomocí Aspose.PSD for .NET!

## Závěr

Gratulujeme! Naučili jste se, jak zlepšit vyvážení barev vašich obrázků PSD pomocí Aspose.PSD pro .NET. Experimentujte s různými hodnotami vyvážení, abyste dosáhli požadovaných vizuálních efektů.

## FAQ

### Q1: Mohu použít úpravu vyvážení barev na více vrstev?

Odpověď 1: Ano, můžete procházet všemi vrstvami v souboru PSD a podle potřeby upravit vyvážení barev.

### Q2: Je Aspose.PSD for .NET vhodný pro dávkové zpracování souborů PSD?

A2: Rozhodně! Aspose.PSD poskytuje efektivní možnosti dávkového zpracování souborů PSD.

### Q3: Jak mohu získat dočasnou licenci pro Aspose.PSD pro .NET?

 A3: Návštěva[Dočasná licence Aspose.PSD](https://purchase.aspose.com/temporary-license/) pro dočasnou licenci.

### Q4: Kde najdu další příklady a dokumentaci?

 A4: Prozkoumejte[Dokumentace Aspose.PSD](https://reference.aspose.com/psd/net/) pro podrobné příklady a návody.

### Q5: Jaké možnosti podpory jsou k dispozici pro Aspose.PSD pro .NET?

 A5: Navštivte[Fórum Aspose.PSD](https://forum.aspose.com/c/psd/34) za podporu komunity a diskuze.
