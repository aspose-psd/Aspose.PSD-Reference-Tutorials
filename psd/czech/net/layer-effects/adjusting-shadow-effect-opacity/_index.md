---
title: Úprava krytí stínového efektu v Aspose.PSD pro .NET
linktitle: Úprava krytí stínového efektu
second_title: Aspose.PSD .NET API
description: Naučte se, jak upravit neprůhlednost stínového efektu v Aspose.PSD pro .NET pomocí tohoto komplexního kurzu.
type: docs
weight: 15
url: /cs/net/layer-effects/adjusting-shadow-effect-opacity/
---
## Zavedení

Vítejte v našem podrobném průvodci nastavením krytí stínového efektu v Aspose.PSD pro .NET! V tomto tutoriálu vás provedeme procesem využití vlastnosti Opacity DropShadowEffect. Aspose.PSD for .NET je výkonná knihovna, která vám umožní bezproblémově pracovat se soubory PSD ve vašich aplikacích .NET.

## Předpoklady

Než se pustíme do výukového programu, ujistěte se, že máte následující:

-  Knihovna Aspose.PSD for .NET: Ujistěte se, že máte v projektu nainstalovanou knihovnu Aspose.PSD for .NET. Můžete si jej stáhnout[zde](https://releases.aspose.com/psd/net/).

- Adresář dokumentů: Nastavte adresář pro váš vstupní soubor PSD.

- Výstupní adresář: Vytvořte adresář, do kterého se budou ukládat výsledné obrázky.

## Importovat jmenné prostory

Ve svém projektu .NET se ujistěte, že importujete potřebné jmenné prostory:

```csharp
using System;
using System.IO;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers;
using Aspose.PSD.FileFormats.Psd.Layers.LayerEffects;
using Aspose.PSD.ImageOptions;
```

## Krok 1: Načtěte soubor PSD

 Začněte načtením souboru PSD pomocí`Image.Load` metoda:

```csharp
string inputFile = Path.Combine(baseDir, "input.psd");
using (PsdImage psdImage = (PsdImage)Image.Load(inputFile, new LoadOptions()))
{
    // Zde je váš kód pro další zpracování
}
```

## Krok 2: Otevřete vrstvu a přidejte efekt vrženého stínu

Načtěte požadovanou vrstvu ze souboru PSD a přidejte efekt vrženého stínu:

```csharp
Layer workLayer = psdImage.Layers[1];
DropShadowEffect dropShadowEffect = workLayer.BlendingOptions.AddDropShadow();
dropShadowEffect.Distance = 0;
dropShadowEffect.Size = 8;
```

## Krok 3: Upravte neprůhlednost a uložte obrázky

Nyní upravte vlastnost opacity a uložte obrázky s různými krytími:

```csharp
// Příklad s neprůhledností = 20
dropShadowEffect.Opacity = 20;
psdImage.Save(outputImage20, new PngOptions());

// Příklad s neprůhledností = 200
dropShadowEffect.Opacity = 200;
psdImage.Save(outputImage200, new PngOptions());
```

## Krok 4: Vyčistěte

Po uložení obrázků proveďte vyčištění odstraněním dočasných souborů:

```csharp
File.Delete(outputImage20);
File.Delete(outputImage200);
```

## Závěr

Gratuluji! Úspěšně jste upravili neprůhlednost stínového efektu v Aspose.PSD pro .NET. Tento tutoriál poskytuje přímočarý návod, jak vylepšit obrázky PSD různými krytími stínů.

## FAQ

### Q1: Mohu použít tento návod na jiné formáty obrázků?

Odpověď 1: Ne, tento tutoriál konkrétně pojednává o úpravě krytí stínového efektu v souborech PSD pomocí Aspose.PSD pro .NET.

### Q2: Existují další vlastnosti stínu, které lze upravit?

A2: Ano, Aspose.PSD pro .NET nabízí různé vlastnosti pro jemné doladění stínových efektů.

### Q3: Jak mohu získat dočasnou licenci pro Aspose.PSD pro .NET?

 A3: Můžete získat dočasnou licenci[zde](https://purchase.aspose.com/temporary-license/).

### Q4: Je Aspose.PSD for .NET kompatibilní s .NET Core?

Odpověď 4: Ano, Aspose.PSD for .NET je kompatibilní s .NET Framework i .NET Core.

### Q5: Kde najdu podporu komunity pro Aspose.PSD pro .NET?

 A5: Navštivte[Aspose.PSD fóra](https://forum.aspose.com/c/psd/34) za podporu komunity a diskuze.