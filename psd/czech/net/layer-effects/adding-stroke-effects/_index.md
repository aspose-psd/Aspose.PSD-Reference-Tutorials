---
title: Přidání efektů tahu do vrstev v Aspose.PSD pro .NET
linktitle: Přidání tahových efektů do vrstev
second_title: Aspose.PSD .NET API
description: Vylepšete estetiku obrazu pomocí Aspose.PSD pro .NET. Naučte se přidávat efekty tahu krok za krokem. Stáhněte si, kupte nebo vyzkoušejte bezplatnou zkušební verzi.
weight: 10
url: /cs/net/layer-effects/adding-stroke-effects/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Přidání efektů tahu do vrstev v Aspose.PSD pro .NET

## Zavedení

Vítejte v tomto podrobném tutoriálu o přidávání efektů tahu do vrstev v Aspose.PSD pro .NET. Zlepšení vizuální přitažlivosti vašich obrázků je hračkou s efektem tahu a Aspose.PSD to umožňuje vývojářům .NET bezproblémově. V této příručce vás provedeme celým procesem a poskytneme jasné kroky a příklady, které vám pomohou zvládnout tuto výkonnou funkci.

## Předpoklady

Než se pustíme do výukového programu, ujistěte se, že máte splněny následující předpoklady:

- Aspose.PSD pro .NET: Stáhněte a nainstalujte knihovnu Aspose.PSD z[webové stránky](https://releases.aspose.com/psd/net/).

- Adresář dokumentů: Připravte adresář obsahující dokument PSD, na který chcete aplikovat efekty tahu.

- Výstupní adresář: Mít samostatný adresář pro ukládání výstupních obrázků s efekty tahu.

- Visual Studio: Ujistěte se, že máte nastaveno Visual Studio nebo jiné preferované vývojové prostředí .NET.

## Importovat jmenné prostory

Do svého projektu .NET zahrňte potřebné obory názvů, abyste mohli využít funkce Aspose.PSD:

```csharp
using System;
using System.IO;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers.FillSettings;
using Aspose.PSD.FileFormats.Psd.Layers.LayerEffects;
using Aspose.PSD.ImageLoadOptions;
using Aspose.PSD.ImageOptions;
```

## Krok 1: Vložte dokument PSD

```csharp
string srcFile = Path.Combine(SourceDir, "AddStrokeEffect.psd");
string outputFilePng = Path.Combine(OutputDir, "AddStrokeEffect.png");

using (var psdImage = (PsdImage)Image.Load(srcFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    // Zde je váš kód pro načtení dokumentu PSD
}
```

## Krok 2: Přidejte efekt barevného tahu

```csharp
// Přidá barevnou výplň na pozici Uvnitř
strokeEffect = psdImage.Layers[1].BlendingOptions.AddStroke(FillType.Color);
strokeEffect.Size = 7;
strokeEffect.Position = StrokePosition.Inside;
colorFillSettings = strokeEffect.FillSettings as IColorFillSettings;
colorFillSettings.Color = Color.Green;
```

## Krok 3: Vnější pozice

```csharp
// Přidá barevnou výplň na pozici Vně
strokeEffect = psdImage.Layers[2].BlendingOptions.AddStroke(FillType.Color);
strokeEffect.Size = 7;
strokeEffect.Position = StrokePosition.Outside;
colorFillSettings = strokeEffect.FillSettings as IColorFillSettings;
colorFillSettings.Color = Color.Green;
```

## Krok 4: Středová pozice

```csharp
// Přidá barevnou výplň na pozici Střed
strokeEffect = psdImage.Layers[3].BlendingOptions.AddStroke(FillType.Color);
strokeEffect.Size = 7;
strokeEffect.Position = StrokePosition.Center;
colorFillSettings = strokeEffect.FillSettings as IColorFillSettings;
colorFillSettings.Color = Color.Green;
```

Opakujte podobné kroky pro výplně přechodem a vzorem a odpovídajícím způsobem upravte nastavení.

## Závěr

Gratuluji! Úspěšně jste se naučili, jak přidat efekty tahu do vrstev pomocí Aspose.PSD pro .NET. Experimentujte s různými nastaveními, abyste dosáhli požadovaného vizuálního efektu ve svých obrázcích.

## FAQ

### Q1: Mohu aplikovat efekty tahu pouze na určité vrstvy?

Odpověď 1: Ano, můžete cílit na konkrétní vrstvy úpravou indexu vrstvy v kódu.

### Q2: Je Aspose.PSD kompatibilní s nejnovějším rámcem .NET?

A2: Rozhodně! Aspose.PSD je navržen tak, aby se hladce integroval s nejnovějšími frameworky .NET.

### Q3: Jak mohu přizpůsobit barvu tahu?

 A3: Jednoduše upravte`Color` vlastnost v kódu k dosažení požadované barvy tahu.

### Q4: Podporuje Aspose.PSD dávkové zpracování pro více souborů PSD?

A4: Ano, můžete procházet více soubory PSD a použít efekt tahu pomocí podobného přístupu.

### Q5: Mohu použít zkušební verzi před zakoupením Aspose.PSD?

 A5: Určitě! Chyťte se[zkušební verze zdarma](https://releases.aspose.com/) prozkoumat možnosti Aspose.PSD před nákupem.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
