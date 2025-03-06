---
title: Vrstva úprav vykreslování křivek v souborech PSD - Java
linktitle: Vrstva úprav vykreslování křivek v souborech PSD - Java
second_title: Aspose.PSD Java API
description: Naučte se vykreslovat a upravovat vrstvy úprav křivek v souborech PSD pomocí Aspose.PSD for Java s tímto podrobným průvodcem krok za krokem.
weight: 16
url: /cs/java/psd-layer-management-effects/render-curves-adjustment-layer-psd/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Vrstva úprav vykreslování křivek v souborech PSD - Java

## Zavedení

Vrstva úprav křivek Photoshopu je jako mávnutím kouzelného proutku pro vylepšení obrázků. Představte si, že jste umělec ladící barvy a tóny svého mistrovského díla – každá úprava křivky vám umožní ovládat světlo a vyvážení barev s neuvěřitelnou přesností. Pokud pracujete se soubory PSD a potřebujete s těmito křivkami manipulovat programově, Aspose.PSD for Java je vaším nástrojem. V této příručce si projdeme, jak vykreslit a upravit vrstvy úprav křivek v souborech PSD pomocí Aspose.PSD for Java. Ať už aktualizujete tóny obrázků nebo exportujete své výsledky, tento výukový program pokryje vše, co potřebujete, abyste mohli začít.

## Předpoklady

Než se ponoříme do specifik kódování, ujistíme se, že máte vše nastaveno. Zde je to, co potřebujete:

1. Java Development Kit (JDK): Ujistěte se, že máte v systému nainstalovaný JDK. Aspose.PSD pro Java vyžaduje Java 8 nebo vyšší.
   
2.  Aspose.PSD for Java Library: Stáhněte si knihovnu Aspose.PSD for Java z[Aspose stránku vydání](https://releases.aspose.com/psd/java/). 

3. IDE (Integrated Development Environment): Bude fungovat jakékoli IDE kompatibilní s Java, jako IntelliJ IDEA nebo Eclipse.

4. Základní znalosti programování v Javě: Pochopení syntaxe Java a základních programovacích konceptů vám pomůže pokračovat ve výukovém programu.

5. Soubor PSD: Soubor PSD s vrstvou úprav křivek, kterou chcete upravit. 

Jakmile máte tyto předpoklady na místě, jste připraveni začít manipulovat se soubory PSD.

## Importujte balíčky

Pro začátek musíte naimportovat potřebné balíčky z Aspose.PSD. Tyto knihovny budou zpracovávat operace se soubory PSD, včetně čtení a úpravy vrstvy křivek.

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.CurvesLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.CurvesContinuousManager;
import com.aspose.psd.fileformats.psd.layers.layerresources.CurvesDiscreteManager;
import com.aspose.psd.imageoptions.PngOptions;
```

## Krok 1: Načtěte soubor PSD

 Nejprve musíte do aplikace načíst soubor PSD. The`PsdImage` třída z Aspose.PSD umožňuje otevírat a manipulovat se soubory PSD.

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "CurvesAdjustmentLayer";
PsdImage im = (PsdImage)Image.load(sourceFileName + ".psd");
```

 Tady, vyměňte`"Your Document Directory/CurvesAdjustmentLayer"` s cestou k vašemu souboru PSD. Tento fragment kódu načte soubor PSD do a`PsdImage` objekt.

## Krok 2: Iterujte přes vrstvy

Soubory PSD mohou obsahovat více vrstev. Chcete-li najít vrstvu úprav křivek a manipulovat s ní, musíte iterovat vrstvy vašeho souboru PSD.

```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof CurvesLayer) {
        CurvesLayer curvesLayer = (CurvesLayer)im.getLayers()[i];
        // Zde se budou řešit další operace
    }
}
```

Tato smyčka kontroluje každou vrstvu, aby určila, zda se jedná o instanci`CurvesLayer`. Pokud ano, můžete pokračovat v úpravě křivek.

## Krok 3: Upravte vrstvu křivek

Jakmile identifikujete vrstvu úprav křivek, můžete upravit její nastavení. Přístup se bude lišit v závislosti na tom, zda vrstva používá diskrétního nebo spojitého správce.

### Úprava správce diskrétních křivek

 Pokud`CurvesLayer` používá a`CurvesDiscreteManager`, můžete upravit body křivky přímo.

```java
if (curvesLayer.isDiscreteManagerUsed()) {
    CurvesDiscreteManager manager = (CurvesDiscreteManager)curvesLayer.getCurvesManager();
    
    for (int k = 10; k < 50; k++) {
        manager.setValueInPosition(0, (byte)k, (byte)(15 + (k * 2)));
    }
}
```

V tomto úryvku upravujeme hodnoty křivek diskrétním způsobem. To zahrnuje nastavení hodnot na různých pozicích, efektivní úpravu tvaru křivky.

### Úprava správce spojitých křivek

 Pro vrstvy používající a`CurvesContinuousManager`, přidáte body křivky.

```java
else {
    CurvesContinuousManager manager = (CurvesContinuousManager)curvesLayer.getCurvesManager();
    manager.addCurvePoint((byte)0, (byte)50, (byte)100);
    manager.addCurvePoint((byte)0, (byte)150, (byte)130);
}
```

Tento kód přidá dva body křivky a upraví tvar křivky pomocí spojitých hodnot. 

## Krok 4: Uložte soubor PSD

Po provedení úprav uložte upravený soubor PSD. Tento krok zajistí uložení všech vašich změn.

```java
String psdPathAfterChange = dataDir + "CurvesAdjustmentLayerChanged";
im.save(psdPathAfterChange + ".psd");
```

Zde určíte cestu, kam bude uložen upravený soubor PSD. 

## Krok 5: Export do PNG

 Chcete-li exportovat upravený soubor PSD jako PNG, nakonfigurujte soubor`PngOptions` a uložte soubor.

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
String pngExportPath = dataDir + "CurvesAdjustmentLayerChanged";
im.save(pngExportPath + ".png", saveOptions);
```

Tento úryvek nastaví možnosti exportu PNG, včetně barevného typu s průhledností alfa, a uloží soubor jako PNG.

## Závěr

Manipulace s vrstvami úprav křivek v souborech PSD pomocí Aspose.PSD pro Java se může na první pohled zdát složitá, ale s těmito podrobnými pokyny zjistíte, že je to zvládnutelné a intuitivní. Podle tohoto průvodce můžete bez námahy vyladit tóny obrázků a exportovat výsledky v různých formátech. Ať už vylepšujete obrázky pro projekt nebo automatizujete dávkové procesy, Aspose.PSD poskytuje nástroje, které potřebujete k snadnému dosažení profesionálních výsledků.

## FAQ

### Co je to vrstva úprav křivek?
Vrstva úprav křivek ve Photoshopu umožňuje upravit jas a kontrast obrazu úpravou křivek RGB. Poskytuje přesnou kontrolu nad tónovými úpravami.

### Mohu použít Aspose.PSD pro Javu s jinými formáty obrázků?
Ano, Aspose.PSD for Java je primárně pro soubory PSD, ale své upravené obrázky můžete exportovat do formátů jako PNG, TIFF a JPEG.

### Potřebuji nainstalovaný Photoshop, abych mohl používat Aspose.PSD pro Javu?
Ne, Aspose.PSD for Java funguje nezávisle na Photoshopu, což vám umožňuje programově manipulovat se soubory PSD.

### Jak mohu získat bezplatnou zkušební verzi Aspose.PSD pro Javu?
 Můžete si stáhnout bezplatnou zkušební verzi Aspose.PSD pro Javu z webu[Aspose stránku vydání](https://releases.aspose.com/psd/java/).

### Kde najdu podporu pro Aspose.PSD pro Javu?
 Pro podporu můžete navštívit[Aspose fórum podpory](https://forum.aspose.com/c/psd/34).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
