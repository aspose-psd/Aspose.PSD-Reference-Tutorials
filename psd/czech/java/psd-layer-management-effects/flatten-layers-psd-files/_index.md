---
title: Sloučit vrstvy v souborech PSD pomocí Aspose.PSD Java
linktitle: Sloučit vrstvy v souborech PSD pomocí Aspose.PSD Java
second_title: Aspose.PSD Java API
description: Sloučit a sloučit vrstvy v souborech PSD bez námahy pomocí Aspose.PSD pro Java. Postupujte podle tohoto podrobného průvodce pro zjednodušení správy souborů PSD.
weight: 13
url: /cs/java/psd-layer-management-effects/flatten-layers-psd-files/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Sloučit vrstvy v souborech PSD pomocí Aspose.PSD Java

## Zavedení

Už jste někdy zjistili, že pracujete se soubory Photoshopu a přáli jste si jednodušší způsob, jak spravovat tyto složité vrstvy? Tak to máš štěstí! Dnes se ponoříme do světa Aspose.PSD for Java, mocného nástroje, díky kterému je práce se soubory PSD programově hračkou. Jednou z užitečných funkcí, kterou prozkoumáme, je zploštění vrstev. Ať už chcete sloučit celý obrázek nebo selektivně sloučit konkrétní vrstvy, Aspose.PSD pro Java vás pokryje. Tento tutoriál vás provede procesem krok za krokem a zajistí, že budete připraveni se svými soubory PSD s jistotou pracovat.

## Předpoklady

Než se pustíme do kódu, ujistěte se, že máte vše, co potřebujete:

1. Java Development Kit (JDK): Ujistěte se, že máte v systému nainstalovaný JDK 8 nebo vyšší.
2.  Aspose.PSD for Java: Stáhněte si a přidejte knihovnu Aspose.PSD do svého projektu. Můžete to najít[zde](https://releases.aspose.com/psd/java/).
3. Integrované vývojové prostředí (IDE): IDE jako IntelliJ IDEA nebo Eclipse vám usnadní práci s kódováním.
4. Základní znalost Javy: I když je tento tutoriál vhodný pro začátečníky, některé základní znalosti Javy vám pomohou snáze pokračovat.
5. Ukázkový soubor PSD: Připravte si soubor PSD, se kterým můžete experimentovat. K demonstraci procesu zploštění použijeme jeden s více vrstvami.

Nyní, když jsme dostali to podstatné z cesty, pojďme k zábavnější části – práci s kódem!

## Importujte balíčky

Chcete-li začít, budete muset importovat potřebné balíčky do svého projektu Java. Tyto balíčky vám umožní pracovat se soubory PSD pomocí Aspose.PSD for Java.

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
```

Tyto importy nám umožní načíst soubory PSD, manipulovat s vrstvami a uložit změny. Nyní si rozdělme proces sloučení vrstev do zvládnutelných kroků.

## Krok 1: Zploštění celého obrázku PSD

Prvním úkolem je zploštit celý PSD obraz. To je užitečné, když chcete zkombinovat všechny vrstvy do jedné vrstvy, což usnadňuje správu a export obrazu.

### 1.1 Načtěte soubor PSD

 Nejprve načteme soubor PSD do našeho programu. Tento soubor by měl být umístěn ve vašem projektovém adresáři, který budeme nazývat`Your Document Directory`.

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "ThreeRegularLayersSemiTransparent.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

Tento fragment kódu načte soubor PSD s názvem`ThreeRegularLayersSemiTransparent.psd` z vašeho zadaného adresáře.

### 1.2 Vyrovnat obrázek

Dále celý obrázek srovnáme. Sloučení spojí všechny viditelné vrstvy do jediné vrstvy pozadí.

```java
im.flattenImage();
```

S touto jednou vložkou jsou všechny vrstvy v souboru PSD sloučeny do jedné.

### 1.3 Uložte sloučený obrázek

Nakonec sloučený obrázek uložíme do nového souboru.

```java
String exportPath = dataDir + "ThreeRegularLayersSemiTransparentFlattened.psd";
im.save(exportPath);
```

 Tím se sloučený soubor PSD uloží pod novým názvem`ThreeRegularLayersSemiTransparentFlattened.psd`. Gratuluji! Právě jste srovnali svůj první PSD obrázek pomocí Aspose.PSD pro Javu.

## Krok 2: Sloučení konkrétních vrstev

Někdy možná nebudete chtít sloučit celý obrázek, ale sloučit pouze určité vrstvy. Pojďme se podívat, jak toho můžete dosáhnout.

### 2.1 Znovu načtěte soubor PSD

Protože provádíme jinou operaci, začněte znovu načtením souboru PSD.

```java
PsdImage img = (PsdImage) Image.load(sourceFileName);
```

Tím se načte stejný soubor PSD, připravený pro operace specifické pro vrstvu.

### 2.2 Identifikujte a vyberte vrstvy

Chcete-li sloučit konkrétní vrstvy, nejprve identifikujte a vyberte vrstvy, které chcete sloučit.

```java
Layer bottomLayer = img.getLayers()[0];
Layer middleLayer = img.getLayers()[1];
Layer topLayer = img.getLayers()[2];
```

Zde vybíráme první, druhou a třetí vrstvu souboru PSD. Tyto vrstvy jsou uloženy v poli a můžete k nim přistupovat pomocí jejich indexu.

### 2.3 Sloučit vrstvy

Nyní sloučíme vybrané vrstvy. Začneme sloučením spodní a střední vrstvy, poté spojíme výsledek s horní vrstvou.

```java
Layer layer1 = img.mergeLayers(bottomLayer, middleLayer);
Layer layer2 = img.mergeLayers(layer1, topLayer);
```

Tento kód postupně slučuje vrstvy, což vede k jedné kombinované vrstvě.

### 2.4 Nahraďte existující vrstvy sloučenou vrstvou

Po sloučení je třeba nahradit stávající vrstvy v obrázku nově sloučenou vrstvou.

```java
img.setLayers(new Layer[]{layer2});
```

Tento krok zajistí, že obrázek nyní bude obsahovat pouze sloučenou vrstvu.

### 2.5 Uložte aktualizovaný soubor PSD

Nakonec uložte aktualizovaný soubor PSD se sloučenými vrstvami.

```java
exportPath = dataDir + "ThreeRegularLayersSemiTransparentFlattenedLayerByLayer.psd";
img.save(exportPath);
```

Tím se uloží PSD se sloučenými vrstvami pod novým názvem, což vám umožní zachovat původní soubor nedotčený.

## Závěr

Práce s vrstvami v souborech PSD může často vypadat jako navigace v labyrintu, ale s Aspose.PSD pro Javu je to jako mít mapu v rukou. Ať už potřebujete sloučit celý obrázek nebo pečlivě sloučit vybrané vrstvy, Aspose.PSD zjednodušuje proces a mění to, co může být skličující úkol, na přímou operaci. Podle tohoto návodu byste nyní měli být pohodlní při manipulaci s vrstvami v souborech PSD pomocí Javy. Proč to tedy nezkusit se svými vlastními projekty a neuvidíte, kolik času a úsilí ušetříte?

## FAQ

### Mohu vrátit zpět zploštění vrstev v Aspose.PSD?  
Ne, jakmile sloučíte vrstvy pomocí Aspose.PSD, akce je nevratná. Vždy je dobré ponechat si zálohu původního souboru.

### Je možné srovnat pouze viditelné vrstvy?  
 Ano, můžete ovládat, které vrstvy se mají sloučit na základě jejich viditelnosti. Před použitím se ujistěte, že jsou viditelné pouze vrstvy, které chcete narovnat`flattenImage` metoda.

### Snižuje sloučení vrstev velikost souboru?  
Sloučení vrstev může zmenšit velikost souboru, zejména pokud existuje mnoho složitých vrstev. Přesná redukce však závisí na obsahu vrstev.

### Mohu sloučit vrstvy s různými režimy prolnutí?  
Ano, pomocí Aspose.PSD můžete sloučit vrstvy s různými režimy prolnutí a výsledná vrstva si zachová vzhled sloučených vrstev.

### Co se stane, když se pokusím sloučit vrstvy, které spolu nesousedí?  
Aspose.PSD umožňuje sloučit libovolné vrstvy bez ohledu na jejich pořadí v zásobníku vrstev. Proces slučování zkombinuje vybrané vrstvy podle specifikace.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
