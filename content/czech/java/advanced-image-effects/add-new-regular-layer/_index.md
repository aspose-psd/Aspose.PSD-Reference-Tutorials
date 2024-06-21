---
title: Přidejte do PSD novou běžnou vrstvu pomocí Aspose.PSD pro Javu
linktitle: Přidejte do PSD novou běžnou vrstvu
second_title: Aspose.PSD Java API
description: Naučte se, jak přidat novou běžnou vrstvu do souborů PSD pomocí Aspose.PSD for Java. Postupujte podle našeho podrobného průvodce pro bezproblémovou manipulaci s PSD.
type: docs
weight: 11
url: /cs/java/advanced-image-effects/add-new-regular-layer/
---
## Úvod

Vítejte v tomto komplexním tutoriálu o použití Aspose.PSD pro Java k přidání nové běžné vrstvy do souboru PSD. Aspose.PSD je výkonná Java knihovna, která umožňuje vývojářům efektivně manipulovat a pracovat s PSD soubory. V tomto tutoriálu vás provedeme procesem přidání nové běžné vrstvy do souboru PSD a poskytneme podrobné kroky a příklady kódu.

## Předpoklady

Než se pustíte do výukového programu, ujistěte se, že máte splněny následující předpoklady:

- Vývojové prostředí Java: Ujistěte se, že máte ve svém systému nastavené vývojové prostředí Java.
-  Knihovna Aspose.PSD: Stáhněte a nainstalujte knihovnu Aspose.PSD for Java. Knihovnu najdete[tady](https://releases.aspose.com/psd/java/).

## Importujte balíčky

Chcete-li začít, importujte potřebné balíčky do svého projektu Java. Tyto balíčky jsou nezbytné pro práci s funkcemi Aspose.PSD. Na začátek souboru Java vložte následující řádky:

```java
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```

## Krok 1: Načtěte soubor PSD

Načtěte soubor PSD, který chcete upravit, pomocí následujícího kódu:

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "OneLayer.psd";
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

## Krok 2: Připravte datová pole a obdélníky

Připravte dvě pole int a dva objekty Rectangle následovně:

```java
int[] data1 = new int[2500];
int[] data2 = new int[2500];
Rectangle rect1 = new Rectangle(0, 0, 50, 50);
Rectangle rect2 = new Rectangle(0, 0, 100, 25);
```

## Krok 3: Inicializujte data vrstvy

Inicializujte datová pole s výchozí hodnotou:

```java
for (int i = 0; i < 2500; i++) {
    data1[i] = -10000000;
    data2[i] = -10000000;
}
```

## Krok 4: Přidejte běžné vrstvy

Přidejte do obrázku PSD dvě běžné vrstvy:

```java
Layer layer1 = im.addRegularLayer();
layer1.setLeft(25);
layer1.setTop(25);
layer1.setRight(75);
layer1.setBottom(75);
layer1.saveArgb32Pixels(rect1, data1);

Layer layer2 = im.addRegularLayer();
layer2.setLeft(25);
layer2.setTop(150);
layer2.setRight(1255);
layer2.setBottom(175);
layer2.saveArgb32Pixels(rect2, data2);
```

## Krok 5: Uložte PSD a PNG

Uložte upravený PSD a další soubor PNG:

```java
im.save(exportPath, new PsdOptions());
im.save(exportPathPng, new PngOptions());
```

Gratulujeme! Úspěšně jste přidali novou běžnou vrstvu do souboru PSD pomocí Aspose.PSD for Java.

## Závěr

V tomto tutoriálu jsme se zabývali procesem přidávání nové běžné vrstvy do souboru PSD pomocí Aspose.PSD pro Javu. Tato výkonná knihovna zjednodušuje manipulaci s PSD a zpřístupňuje ji vývojářům Java. Experimentujte s různými parametry a funkcemi, abyste prozkoumali plný potenciál Aspose.PSD.

## FAQ

### Q1: Je Aspose.PSD kompatibilní s Java 8?

A1: Ano, Aspose.PSD podporuje Java 8 a novější verze.

### Q2: Mohu použít transformace na přidané vrstvy?

A2: Rozhodně! Aspose.PSD poskytuje řadu možností transformace pro vrstvy.

### Q3: Kde najdu další dokumentaci Aspose.PSD?

 A3: Můžete nahlédnout do dokumentace.[tady](https://reference.aspose.com/psd/java/).

### Q4: Jak mohu získat dočasnou licenci pro Aspose.PSD?

 A4: Návštěva[tento odkaz](https://purchase.aspose.com/temporary-license/) pro dočasné licenční možnosti.

### Q5: Existují nějaká komunitní fóra pro podporu Aspose.PSD?

 A5: Ano, můžete najít podporu a diskuse.[tady](https://forum.aspose.com/c/psd/34).