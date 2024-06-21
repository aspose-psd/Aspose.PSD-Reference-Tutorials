---
title: Zvládnutí MLST Resource Handling v Aspose.PSD pro .NET
linktitle: Manipulace se zdroji MLST
second_title: Aspose.PSD .NET API
description: Naučte se manipulovat se stavy vrstev v souborech Photoshopu pomocí Aspose.PSD pro .NET. Postupujte podle našeho podrobného průvodce pro efektivní manipulaci se zdroji MLST.
type: docs
weight: 14
url: /cs/net/psd-file-manipulation/mlst-resources/
---
## Úvod
Vítejte v podrobném tutoriálu o práci se zdroji MLST (Multiple Layer States) v Aspose.PSD pro .NET. Aspose.PSD for .NET je výkonná knihovna, která poskytuje rozsáhlé možnosti pro práci se soubory Photoshopu. V tomto tutoriálu se zaměříme na podporu zdrojů MLST, které nabízejí nízkoúrovňový mechanismus pro efektivní manipulaci se stavy vrstev.
## Předpoklady
Než se pustíme do výukového programu, ujistěte se, že máte splněny následující předpoklady:
-  Aspose.PSD for .NET Library: Ujistěte se, že máte nainstalovanou knihovnu. Pokud ne, můžete si jej stáhnout z[Stránka pro stahování Aspose.PSD pro .NET](https://releases.aspose.com/psd/net/).
- Dokumenty a výstupní adresáře: Nastavte si adresář dokumentů (`baseDir`) a výstupní adresář (`outputDir`) v poskytnutém kódu.
## Importovat jmenné prostory
Ve svém projektu .NET zahrňte potřebné jmenné prostory pro práci s Aspose.PSD:
```csharp
using System;
using System.IO;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers;
using Aspose.PSD.FileFormats.Psd.Layers.LayerResources;
using Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures;
```
## Krok 1: Nastavte cesty k adresáři
```csharp
string baseDir = "Your Document Directory";
string outputDir = "Your Output Directory";
```
Ujistěte se, že jste nahradili "Váš adresář dokumentů" a "Váš výstupní adresář" skutečnými cestami ve vašem projektu.
## Krok 2: Načtěte obrázek PSD
```csharp
string sourceFile = Path.Combine(baseDir, "image1219.psd");
string outputPsd = Path.Combine(outputDir, "output_image1219.psd");
using (PsdImage image = (PsdImage)Image.Load(sourceFile))
{
    // Kód pro manipulaci bude přidán v následujících krocích.
}
```
## Krok 3: Přístup ke zdroji MLST
```csharp
Layer layer1 = image.Layers[1];
ShmdResource shmdResource = (ShmdResource)layer1.Resources[8];
MlstResource mlstResource = (MlstResource)shmdResource.SubResources[0];
```
## Krok 4: Manipulujte se stavy vrstev
```csharp
ListStructure layerStatesList = (ListStructure)mlstResource.Items[1];
DescriptorStructure layersStateOnFrame1 = (DescriptorStructure)layerStatesList.Types[1];
BooleanStructure layerEnabled = (BooleanStructure)layersStateOnFrame1.Structures[0];
// Zakázat vrstvu 1 na snímku 1
layerEnabled.Value = false;
```
## Krok 5: Uložte upravený obrázek
```csharp
image.Save(outputPsd);
```
## Krok 6: Vyčistěte
```csharp
File.Delete(outputPsd);
Console.WriteLine("SupportOfMlstResource executed successfully");
```
## Závěr

Gratulujeme! Úspěšně jste se naučili, jak zacházet se zdroji MLST v Aspose.PSD pro .NET. Tato funkce poskytuje robustní mechanismus pro programovou manipulaci se stavy vrstev v souborech Photoshopu.

## FAQ

### Q1: Mohu použít Aspose.PSD for .NET pro práci se soubory PSD vytvořenými v různých verzích Photoshopu?

Odpověď 1: Ano, Aspose.PSD for .NET podporuje soubory PSD vytvořené v různých verzích Photoshopu.

### Q2: Je k dispozici bezplatná zkušební verze pro Aspose.PSD pro .NET?

 A2: Ano, můžete si stáhnout bezplatnou zkušební verzi z[stránka vydání](https://releases.aspose.com/).

### Q3: Kde najdu podrobnou dokumentaci k Aspose.PSD pro .NET?

A3: Dokumentace je k dispozici.[tady](https://reference.aspose.com/psd/net/).

### Q4: Jak mohu získat podporu pro Aspose.PSD pro .NET?

 A4: Navštivte[Aspose.PSD fóra](https://forum.aspose.com/c/psd/34) za podporu komunity.

### Q5: Jak mohu zakoupit licenci pro Aspose.PSD pro .NET?

 A5: Můžete si koupit licenci.[tady](https://purchase.aspose.com/buy).