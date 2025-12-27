---
date: 2025-12-27
description: Naučte se, jak kreslit červený obdélník a další tvary v souborech PSD
  pomocí Aspose.PSD pro Javu. Tento krok‑za‑krokem průvodce pokrývá vytváření dokumentů,
  přidávání vrstev a kreslení s ukázkami kódu.
linktitle: Perform Simple Drawing
second_title: Aspose.PSD Java API
title: Nakreslete červený obdélník pomocí Aspose.PSD pro Javu
url: /cs/java/basic-image-operations/simple-drawing/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Nakreslete červený obdélník pomocí Aspose.PSD pro Java

## Introduction

Vítejte v tomto krok‑za‑krokem průvodci, jak **nakreslit červený obdélník** pomocí Aspose.PSD pro Java! V tomto tutoriálu vás provedeme vytvořením nového PSD dokumentu, přidáním vrstvy a kreslením tvarů s vlastními barvami. Ať už automatizujete grafické zdroje nebo budujete backend design‑toolu, tento tutoriál vám poskytne základní stavební bloky.

## Quick Answers
- **Jaká je hlavní třída pro vytvoření PSD souboru?** `PsdImage`
- **Která metoda vymaže barvu pozadí vrstvy?** `Graphics.clear(Color)`
- **Jak nakreslíte červený obdélník?** `graphic.drawRectangle(new Pen(Color.getRed()), new Rectangle(...))`
- **Potřebuji licenci pro vývoj?** Bezplatná zkušební verze funguje pro testování; licence je vyžadována pro produkci.
- **Mohu manipulovat s existujícími PSD soubory pomocí stejného API?** Ano, Aspose.PSD podporuje plnou úpravu PSD.

## What is drawing a red rectangle in a PSD file?

Kreslení červeného obdélníku znamená použití objektu `Graphics` k vykreslení obdélníkového tvaru vyplněného nebo obrysem červenou barvou na konkrétní vrstvu PSD obrázku. Tato operace je běžná pro zvýraznění oblastí, vytváření zástupných míst nebo přidávání jednoduchých grafických prvků programově.

## Why use Aspose.PSD for Java to manipulate PSD files?

Aspose.PSD poskytuje čisté Java API, které vám umožní číst, upravovat a zapisovat Photoshop PSD soubory bez nutnosti instalace Photoshopu. Podporuje správu vrstev, manipulaci s barvami a vektorové kreslení, což z něj činí ideální řešení pro server‑side zpracování obrázků, automatizované pipeline aktiv a generování vlastních grafik.

## Prerequisites

- Java Development Kit (JDK) nainstalovaný na vašem počítači.  
- Knihovna Aspose.PSD pro Java. Můžete ji stáhnout z [Aspose.PSD for Java Documentation](https://reference.aspose.com/psd/java/).

## Import Packages

To start, import the required classes into your Java project:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Pen;
import com.aspose.psd.Rectangle;
import com.aspose.psd.brushes.SolidBrush;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
```

## Step 1: Create a New Document

Nejprve vytvořte nový PSD dokument s požadovanou velikostí plátna. Tento dokument bude hostit vrstvu, na kterou budeme kreslit.

```java
//ExStart:CreateDocument
String outputDir = "Your Document Directory";
String outPsdFilePath = outputDir + "output.psd";
int width = 100;
int height = 100;

PsdImage image = new PsdImage(width, height);
//ExEnd:CreateDocument
```

## Step 2: Add a Layer

Dále přidejte novou prázdnou vrstvu, která pokrývá celou šířku a výšku obrázku. Vrstvy jsou nezbytné pro oddělení kreslicích operací.

```java
//ExStart:AddLayer
Layer layer = new Layer();
layer.setBottom(height);
layer.setRight(width);
image.addLayer(layer);
//ExEnd:AddLayer
```

## Step 3: Draw Shapes

Budeme používat třídu `Graphics` k manipulaci s pixely vrstvy. Níže jsou tři příklady, které ukazují vymazání pozadí a kreslení obdélníků s různými barvami.

### Clear Layer Color (set background to yellow)

```java
//ExStart:DrawRectangleYellow
Graphics graphic = new Graphics(layer);
graphic.clear(Color.getYellow());
//ExEnd:DrawRectangleYellow
```

### Draw a Red Rectangle (primary focus)

```java
//ExStart:DrawRedRectangle
graphic.drawRectangle(new Pen(Color.getRed()), new Rectangle(30, 10, 40, 80));
//ExEnd:DrawRedRectangle
```

### Draw a Blue Rectangle (additional example)

```java
//ExStart:DrawBlueRectangle
graphic.drawRectangle(new Pen(new SolidBrush(Color.getBlue())), new Rectangle(10, 30, 80, 40));
//ExEnd:DrawBlueRectangle
```

## Step 4: Save the Changes

Nakonec zapište upravený PSD obrázek na disk. Soubor bude obsahovat novou vrstvu a nakreslené tvary.

```java
//ExStart:SaveChanges
image.save(outPsdFilePath);
//ExEnd:SaveChanges
```

## Common Issues and Solutions

- **Vrstva není po kreslení viditelná:** Ujistěte se, že vrstva je přidána do obrázku **před** vytvořením objektu `Graphics`.
- **Barvy se zobrazují nesprávně:** Ověřte, že používáte `Color.getRed()` (nebo jiné statické metody) místo vlastních RGB hodnot, které mohou být mimo rozsah.
- **Soubor se neuložil:** Potvrďte, že cesta `outputDir` existuje a aplikace má oprávnění k zápisu.

## Frequently Asked Questions

### Q1: Can I use Aspose.PSD for Java to manipulate existing PSD files?

A1: Ano, Aspose.PSD pro Java poskytuje rozsáhlou funkčnost pro úpravu a manipulaci s existujícími PSD soubory.

### Q2: Where can I find support for Aspose.PSD for Java?

A2: Můžete navštívit [Aspose.PSD for Java Forum](https://forum.aspose.com/c/psd/34) pro jakékoli dotazy související s podporou.

### Q3: Is there a free trial available for Aspose.PSD for Java?

A3: Ano, můžete získat bezplatnou zkušební verzi [zde](https://releases.aspose.com/).

### Q4: How can I purchase a license for Aspose.PSD for Java?

A4: Licence je k zakoupení na [Aspose.PSD Purchase Page](https://purchase.aspose.com/buy).

### Q5: Are temporary licenses available for Aspose.PSD for Java?

A5: Ano, dočasnou licenci můžete získat [zde](https://purchase.aspose.com/temporary-license/).

## Additional Frequently Asked Questions

**Q: Mohu kreslit jiné tvary než obdélníky?**  
A: Ano, třída `Graphics` také podporuje kreslení elips, čar a vlastních cest.

**Q: Podporuje Aspose.PSD průhlednost v kreslených tvarech?**  
A: Rozhodně; můžete použít `SolidBrush` s ARGB barvou pro zahrnutí alfa průhlednosti.

**Q: Je možné upravit neprůhlednost vrstvy?**  
A: Ano, každý objekt `Layer` má metodu `setOpacity`, která přijímá hodnotu od 0 do 255.

**Q: Jak načtu existující PSD soubor místo vytvoření nového?**  
A: Použijte `PsdImage image = (PsdImage)Image.load("path/to/file.psd");` před manipulací s vrstvami.

## Conclusion

Nyní jste se naučili, jak **nakreslit červený obdélník** a další základní tvary v PSD souboru pomocí Aspose.PSD pro Java. Vytvořením dokumentu, přidáním vrstvy, vymazáním jejího pozadí a kreslením pomocí API `Graphics` můžete automatizovat mnoho úkolů grafického designu. Prozkoumejte dál experimentováním s různými štětci, efekty vrstev a formáty souborů.

---

**Last Updated:** 2025-12-27  
**Tested With:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}