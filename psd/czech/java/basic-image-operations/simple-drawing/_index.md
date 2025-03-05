---
title: Provádějte jednoduché kreslení pomocí Aspose.PSD pro Javu
linktitle: Proveďte jednoduché kreslení
second_title: Aspose.PSD Java API
description: Naučte se kreslit tvary v souborech PSD pomocí Aspose.PSD for Java. Tento podrobný průvodce pokrývá vytváření, přidávání vrstev a kreslení s příklady kódu.
type: docs
weight: 10
url: /cs/java/basic-image-operations/simple-drawing/
---
## Zavedení

Vítejte v tomto podrobném průvodci prováděním jednoduchého kreslení pomocí Aspose.PSD pro Javu! V tomto tutoriálu prozkoumáme základy vytváření nového dokumentu PSD, přidávání vrstev a kreslení tvarů různými barvami. Aspose.PSD for Java je výkonná knihovna, která vám umožňuje programově manipulovat se soubory PSD a poskytuje rozsáhlé funkce pro úlohy grafického designu.

## Předpoklady

Než se pustíte do výukového programu, ujistěte se, že máte splněny následující předpoklady:

- Java Development Kit (JDK) nainstalovaný na vašem počítači.
- Aspose.PSD pro knihovnu Java. Můžete si jej stáhnout z[Aspose.PSD pro dokumentaci Java](https://reference.aspose.com/psd/java/).

## Importujte balíčky

Chcete-li začít, importujte potřebné balíčky do svého projektu Java. Na začátek souboru Java vložte následující kód:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Pen;
import com.aspose.psd.Rectangle;
import com.aspose.psd.brushes.SolidBrush;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
```

## Krok 1: Vytvořte nový dokument

Začněme vytvořením nového dokumentu PSD se zadanou šířkou a výškou:

```java
//ExStart:CreateDocument
String outputDir = "Your Document Directory";
String outPsdFilePath = outputDir + "output.psd";
int width = 100;
int height = 100;

PsdImage image = new PsdImage(width, height);
//ExEnd:CreateDocument
```

## Krok 2: Přidejte vrstvu

Nyní přidejte do dokumentu vrstvu pomocí konstruktoru bez argumentů:

```java
//ExStart:AddLayer
Layer layer = new Layer();
layer.setBottom(height);
layer.setRight(width);
image.addLayer(layer);
//ExEnd:AddLayer
```

## Krok 3: Nakreslete tvary

V tomto kroku použijeme třídu Graphics ke kreslení tvarů na vytvořenou vrstvu:

### Nakreslete obdélník se žlutou barvou

```java
//ExStart:DrawRectangleYellow
Graphics graphic = new Graphics(layer);
graphic.clear(Color.getYellow());
//ExEnd: DrawRectangleYellow
```

### Nakreslete červený obdélník

```java
//ExStart:DrawRedRectangle
graphic.drawRectangle(new Pen(Color.getRed()), new Rectangle(30, 10, 40, 80));
//ExEnd:DrawRedRectangle
```

### Nakreslete modrý obdélník

```java
//ExStart:DrawBlueRectangle
graphic.drawRectangle(new Pen(new SolidBrush(Color.getBlue())), new Rectangle(10, 30, 80, 40));
//ExEnd:DrawBlueRectangle
```

## Krok 4: Uložte změny

Nakonec uložte kopii načteného souboru PSD včetně změn:

```java
//ExStart:SaveChanges
image.save(outPsdFilePath);
//ExEnd:SaveChanges
```

## Závěr

Gratuluji! Úspěšně jste provedli jednoduché kreslení pomocí Aspose.PSD pro Javu. Tento kurz se zabýval vytvářením nového dokumentu, přidáváním vrstev a kreslením obdélníků s různými barvami. Neváhejte a prozkoumejte pokročilejší funkce, které knihovna nabízí pro vaše potřeby grafického designu.

## FAQ

### Q1: Mohu použít Aspose.PSD for Java k manipulaci se stávajícími soubory PSD?

Odpověď 1: Ano, Aspose.PSD for Java poskytuje rozsáhlé funkce pro úpravu a manipulaci se stávajícími soubory PSD.

### Q2: Kde najdu podporu pro Aspose.PSD pro Java?

 A2: Můžete navštívit[Aspose.PSD pro fórum Java](https://forum.aspose.com/c/psd/34) pro jakékoli dotazy týkající se podpory.

### Q3: Je k dispozici bezplatná zkušební verze pro Aspose.PSD pro Java?

 A3: Ano, máte přístup k bezplatné zkušební verzi[zde](https://releases.aspose.com/).

### Q4: Jak mohu zakoupit licenci pro Aspose.PSD pro Java?

 A4: Můžete si koupit licenci od[Nákupní stránka Aspose.PSD](https://purchase.aspose.com/buy).

### Q5: Jsou k dispozici dočasné licence pro Aspose.PSD pro Java?

 A5: Ano, můžete získat dočasnou licenci od[zde](https://purchase.aspose.com/temporary-license/).