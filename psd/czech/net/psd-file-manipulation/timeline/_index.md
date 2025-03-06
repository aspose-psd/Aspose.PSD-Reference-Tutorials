---
title: Práce s časovou osou v Aspose.PSD pro .NET
linktitle: Práce s časovou osou
second_title: Aspose.PSD .NET API
description: Vylepšete manipulaci s obrázky PSD pomocí třídy Aspose.PSD for .NET Timeline. Ovládejte vlastnosti rámce, stavy vrstev a uvolněte kreativní možnosti bez námahy.
weight: 16
url: /cs/net/psd-file-manipulation/timeline/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Práce s časovou osou v Aspose.PSD pro .NET

## Zavedení
dynamickém světě grafického designu a manipulace s obrázky je schopnost ovládat a manipulovat s časovou osou obrázků zásadní. Aspose.PSD for .NET poskytuje výkonné řešení se svou třídou Timeline. Tato funkce na vysoké úrovni umožňuje uživatelům provádět změny na časové ose PsdImage, jako je změna zpoždění snímku, úprava stavu vrstev na konkrétních snímcích a další.
## Předpoklady
Než se ponoříte do vzrušujících možností, které nabízí třída Timeline, ujistěte se, že máte splněny následující předpoklady:
-  Aspose.PSD for .NET Library: Ujistěte se, že máte nainstalovanou knihovnu Aspose.PSD for .NET. Můžete si jej stáhnout z[Aspose.PSD pro dokumentaci .NET](https://reference.aspose.com/psd/net/).
-  Dokument a výstupní adresáře: Definujte cesty pro váš dokument a výstupní adresáře v kódu. Upravte`baseDir` a`outputDir` proměnné podle struktury vašeho projektu.
Nyní se podívejme, jak používat třídu Timeline krok za krokem.
## Importovat jmenné prostory
Chcete-li začít pracovat s třídou Timeline, importujte do kódu potřebné jmenné prostory:
```csharp
using System;
using System.Collections.Generic;
using System.IO;
using Aspose.PSD.FileFormats.Core.Blending;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers.Animation;
```
## Krok 1: Načtěte obrázek PSD
Začněte načtením obrázku PSD ze zadaného zdrojového souboru. Ujistěte se, že je správně nastavena cesta ke zdrojovému souboru:
```csharp
string sourceFile = Path.Combine(baseDir, "image1219.psd");
using (PsdImage psdImage = (PsdImage)Image.Load(sourceFile))
{
    //Zde je váš kód pro další operace
}
```
## Krok 2: Přístup k časové ose
Po načtení obrázku PSD přejděte na časovou osu pomocí následujícího kódu:
```csharp
Timeline timeline = psdImage.Timeline;
```
## Krok 3: Změňte způsob likvidace
Manipulujte s metodou likvidace konkrétního snímku. V tomto příkladu změníme způsob vyřazení snímku 1:
```csharp
timeline.Frames[0].DisposalMethod = FrameDisposalMethod.DoNotDispose;
```
## Krok 4: Upravte Frame Delay
Upravte zpoždění konkrétního snímku. Zde změníme zpoždění snímku 2 na 15:
```csharp
timeline.Frames[1].Delay = 15;
```
## Krok 5: Upravte stav vrstvy
Změňte krytí vrstvy 1 na konkrétním snímku. V tomto případě nastavíme krytí na 50 na snímku 2:
```csharp
LayerState layerState11 = timeline.Frames[1].LayerStates[1];
layerState11.Opacity = 50;
```
## Krok 6: Přesuňte vrstvu
Přesuňte „Vrstvu 1“ do levého dolního rohu na konkrétním snímku (v tomto příkladu snímek 3):
```csharp
LayerState layerState21 = timeline.Frames[2].LayerStates[1];
layerState21.PositionOffset = new Point(-50, 230);
```
## Krok 7: Přidejte nový rámeček
Přidejte na časovou osu nový snímek:
```csharp
List<Frame> frames = new List<Frame>(timeline.Frames);
frames.Add(new Frame());
timeline.Frames = frames.ToArray();
```
## Krok 8: Změňte režim prolnutí
Změňte režim prolnutí 'Vrstva 1' na konkrétním snímku (v tomto případě snímek 4):
```csharp
LayerState layerState31 = timeline.Frames[3].LayerStates[1];
layerState31.BlendMode = BlendMode.Dissolve;
```
## Krok 9: Uložte změny
Aplikujte změny zpět na instanci PsdImage a uložte upravený obrázek PSD:
```csharp
psdImage.Save(outputPsd);
```
## Krok 10: Vyčistěte
Nakonec proveďte vyčištění odstraněním dočasného výstupního souboru:
```csharp
File.Delete(outputPsd);
```
## Závěr

Na závěr, třída Timeline v Aspose.PSD pro .NET umožňuje vývojářům mít podrobnou kontrolu nad časovou osou obrázků PSD. Prostřednictvím řady jednoduchých kroků můžete manipulovat s vlastnostmi rámečku, stavy vrstev a dalšími, čímž se vám otevírá říše kreativních možností.

## FAQ

### Q1: Je Aspose.PSD pro .NET vhodný pro začátečníky?

A1: Rozhodně! Aspose.PSD for .NET poskytuje uživatelsky přívětivé rozhraní a komplexní dokumentaci, takže je přístupný jak pro začátečníky, tak pro zkušené vývojáře.

### Q2: Mohu použít změny časové osy na obrázky GIF?

A2: Třída Timeline je speciálně navržena pro obrázky PSD. Informace o manipulaci s GIF naleznete v Aspose.GIF pro .NET.

### Otázka 3: Kde mohu najít další podporu nebo diskutovat o problémech?

 A3: Navštivte[Fórum Aspose.PSD](https://forum.aspose.com/c/psd/34) za podporu komunity a diskuse o problémech.

### Q4: Jak mohu získat dočasnou licenci pro Aspose.PSD pro .NET?

 A4: Získejte dočasnou licenci[zde](https://purchase.aspose.com/temporary-license/).

### Q5: Jaké jsou hlavní výhody používání Aspose.PSD pro .NET?

Odpověď 5: Aspose.PSD for .NET nabízí pokročilé možnosti zpracování obrazu, manipulaci se soubory PSD a vysoce výkonné vykreslování.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
