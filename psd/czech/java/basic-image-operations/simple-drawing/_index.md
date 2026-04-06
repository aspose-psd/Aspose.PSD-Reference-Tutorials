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

## Úvod

Vítejte v tomto krok‑za‑krokem průvodci, jak **nakreslit červený obdélník** pomocí Aspose.PSD pro Java! V tomto tutoriálu vás provedeme vytvořením nového dokumentu PSD, přidáním vrstev a kreslením tvarů s vlastními barvami. Ať už automatizujete grafické zdroje nebo budujete backend design-toolu, tento tutoriál vám poskytne základní stavební bloky.

## Rychlé odpovědi
- **Jaká je hlavní třída pro vytvoření souboru PSD?** `PsdImage`
- **Která metoda vymaže barvu pozadí vrstvy?** `Graphics.clear(Color)`
- **Jak nakreslíte červený obdélník?** `graphic.drawRectangle(new Pen(Color.getRed()), new Rectangle(...))`
- **Potřebuji licenci pro vývoj?** Bezplatná zkušební verze funguje pro testování; licence je vyžadována pro produkci.
- **Mohu manipulovat s existujícími soubory PSD pomocí stejného API?** Ano, Aspose.PSD podporuje plnou úpravu PSD.

## Co je nakreslení červeného obdélníku v souboru PSD?

Kreslení červeného obdélníku znamená použití objektu `Graphics` k vykreslení obdélníkového tvaru vyplněného nebo obrysu červenou barvou na konkrétní vrstvu PSD obrázku. Tato operace je běžná pro zvýraznění oblastí, vytváření míst nebo přidávání jednoduchých grafických prvků programově.

## Proč používat Aspose.PSD pro Javu k manipulaci se soubory PSD?

Aspose.PSD poskytuje čisté Java API, které vám umožní číst, upravovat a zapisovat soubory Photoshop PSD bez instalace Photoshopu. Podporuje správu vrstev, manipulaci s barvami a vektorové kreslení, což z něj představuje ideální řešení pro server-side zpracování obrázků, automatizované pipeline aktiv a generování vlastních grafik.

## Předpoklady

- Java Development Kit (JDK) nainstalovaný na vašem počítači.
- Knihovna Aspose.PSD pro Java. Můžete si ji stáhnout z [Aspose.PSD for Java Documentation](https://reference.aspose.com/psd/java/).

## Importujte balíčky

Chcete-li začít, importujte požadované třídy do svého projektu Java:

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

## Krok 2: Přidejte vrstvu

Dále přidejte novou prázdnou vrstvu, která pokrývá celou šířku a výšku obrázku. Vrstvy jsou nezbytné pro oddělení kreslicích operací.

```java
//ExStart:AddLayer
Layer layer = new Layer();
layer.setBottom(height);
layer.setRight(width);
image.addLayer(layer);
//ExEnd:AddLayer
```

## Krok 3: Nakreslete tvary

Budeme používat třídu `Graphics` k manipulaci s pixely vrstvami. jsou tři příklady, které ukazují vymazání pozadí a kreslení obdélníků s různými barvami.

### Vymazat barvu vrstvy (nastavit pozadí na žlutou)

```java
//ExStart:DrawRectangleYellow
Graphics graphic = new Graphics(layer);
graphic.clear(Color.getYellow());
//ExEnd:DrawRectangleYellow
```

### Nakreslete červený obdélník (primární zaměření)

```java
//ExStart:DrawRedRectangle
graphic.drawRectangle(new Pen(Color.getRed()), new Rectangle(30, 10, 40, 80));
//ExEnd:DrawRedRectangle
```

### Nakreslete modrý obdélník (další příklad)

```java
//ExStart:DrawBlueRectangle
graphic.drawRectangle(new Pen(new SolidBrush(Color.getBlue())), new Rectangle(10, 30, 80, 40));
//ExEnd:DrawBlueRectangle
```

## Krok 4: Uložte změny

Nakonec zapište upravený PSD obrázek na disk. Soubor bude obsahovat novou vrstvu a nakreslené tvary.

```java
//ExStart:SaveChanges
image.save(outPsdFilePath);
//ExEnd:SaveChanges
```

## Běžné problémy a řešení

- **Vrstva není po kreslení viditelné:** nahrazuje se, že vrstva je přidána do obrázku **před** vytvořením objektu `Graphics`.
- **Barvy se zobrazuje nesprávně:** Ověřte, že používáte`Color.getRed()` (nebo jiné statické metody) místo vlastních hodnot RGB, které mohou být mimo rozsah.
- **Soubor se neuložil:** Potvrďte, že cesta `outputDir` existuje a aplikace má oprávnění k zápisu.

## Často kladené otázky

### Q1: Mohu použít Aspose.PSD for Java k manipulaci se stávajícími soubory PSD?

A1: Ano, Aspose.PSD pro Java poskytuje rozsáhlou funkčnost pro úpravu a manipulaci s existujícími soubory PSD.

### Q2: Kde najdu podporu pro Aspose.PSD pro Javu?

A2: Můžete navštívit [Aspose.PSD for Java Forum](https://forum.aspose.com/c/psd/34) pro jakékoli dotazy související s podporou.

### Q3: Je k dispozici bezplatná zkušební verze pro Aspose.PSD pro Javu?

A3: Ano, můžete získat bezplatnou zkušební verzi [zde](https://releases.aspose.com/).

### Q4: Jak mohu zakoupit licenci pro Aspose.PSD pro Java?

A4: Licence je k zakoupení na [Nákupní stránka Aspose.PSD](https://purchase.aspose.com/buy).

### Q5: Jsou k dispozici dočasné licence pro Aspose.PSD pro Java?

A5: Ano, dočasnou licenci můžete získat [zde](https://purchase.aspose.com/temporary-license/).

## Další často kladené otázky

**O: Mohu kreslit jiné tvary než obdélníky?**
A: Ano, třída `Graphics` také podporuje kreslení elips, čar a vlastních cest.

**O: Podporuje Aspose.PSD průhlednost v kreslených tvarech?**
A: Rozhodně; můžete použít `SolidBrush` s ARGB barvou pro zahrnutí alfa průhlednosti.

**Q: Je možné upravit neprůhlednost vrstvy?**
A: Ano, každý objekt `Layer` má metodu `setOpacity`, která přijímá hodnotu od 0 do 255.

**Q: Jak načtu existující PSD soubor místo vytvoření nového?**
A: Použijte `PsdImage image = (PsdImage)Image.load("path/to/file.psd");` před manipulací s vrstvami.

## Závěr

Nyní jste se naučili, jak **nakreslit červený obdélník** a další základní tvary v PSD souboru pomocí Aspose.PSD pro Java. Vytvořením dokumentu, přidáním vrstev, vymazáním jejího pozadí a kreslením pomocí API `Graphics` můžete automatizovat mnoho úkolů grafického designu. Prozkoumejte dál experimentováním s různými štětci, efekty vrstev a formátů souborů.

---

**Poslední aktualizace:** 27. 12. 2025
**Testováno s:** Aspose.PSD pro Java 24.12 (nejnovější v době psaní tohoto článku)
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}