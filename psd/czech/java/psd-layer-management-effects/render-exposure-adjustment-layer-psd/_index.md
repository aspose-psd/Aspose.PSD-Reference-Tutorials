---
title: Vrstva úpravy expozice vykreslení v souborech PSD - Java
linktitle: Vrstva úpravy expozice vykreslení v souborech PSD - Java
second_title: Aspose.PSD Java API
description: Naučte se vykreslovat a upravovat vrstvy expozice v souborech PSD pomocí Aspose.PSD for Java. Podrobný průvodce s příklady kódu pro úpravu a přidávání vrstev expozice.
type: docs
weight: 15
url: /cs/java/psd-layer-management-effects/render-exposure-adjustment-layer-psd/
---
## Zavedení

Pracujete se soubory Photoshop PSD a potřebujete upravit expozici nebo přidat vrstvu úpravy expozice programově? Ať už upravujete stávající vrstvy nebo přidáváte nové, Aspose.PSD pro Java poskytuje výkonný a intuitivní způsob, jak tyto úkoly zvládnout. V této příručce si projdeme, jak používat Aspose.PSD pro Java k vykreslení a úpravě vrstev úprav expozice v souborech PSD. Na konci tohoto tutoriálu budete vědět, jak upravit nastavení expozice ve stávajících vrstvách a přidat nové vrstvy úpravy expozice do souborů PSD. Pojďme se ponořit!

## Předpoklady

Než se pustíme do výukového programu, ujistěte se, že máte následující předpoklady:

1. Java Development Kit (JDK): Na vašem počítači musíte mít nainstalovaný JDK. Tato příručka předpokládá, že máte alespoň JDK 8.
2.  Aspose.PSD for Java: Pro práci se soubory PSD potřebujete knihovnu Aspose.PSD. Můžete si jej stáhnout z[zde](https://releases.aspose.com/psd/java/).
3. Základní znalost Javy: Znalost programování v Javě vám pomůže snadno se orientovat.
4. IDE nebo textový editor: K psaní a spouštění kódu Java použijte libovolné IDE, jako je IntelliJ IDEA, Eclipse nebo textový editor podle svého výběru.

## Importujte balíčky

Nejprve importujme potřebné balíčky z Aspose.PSD pro Javu. Tento krok zajišťuje, že náš kód může využívat funkce knihovny pro manipulaci se soubory PSD.

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.ExposureLayer;
import com.aspose.psd.imageoptions.PngOptions;
```

## Krok 1: Načtěte soubor PSD

Chcete-li začít, musíte do aplikace načíst soubor PSD. Můžete to udělat takto:

```java
String dataDir = "Your Document Directory";  // Definujte adresář dokumentů
String sourceFileName = dataDir + "ExposureAdjustmentLayer.psd";  // Cesta k zdrojovému souboru PSD

PsdImage im = (PsdImage) Image.load(sourceFileName);  // Načtěte soubor PSD
```

 V tomto fragmentu kódu nahraďte`"Your Document Directory"` s cestou, kde jsou umístěny vaše soubory PSD. The`Image.load()` metoda načte soubor PSD do instance`PsdImage`, který umožňuje manipulovat s jeho vrstvami.

## Krok 2: Upravte existující vrstvu úpravy expozice

Jakmile je soubor PSD načten, můžete přistupovat ke stávajícím vrstvám a upravovat je. Pokud soubor obsahuje vrstvu úpravy expozice, můžete upravit její vlastnosti:

```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof ExposureLayer) {
        ExposureLayer expLayer = (ExposureLayer) im.getLayers()[i];
        expLayer.setExposure(2);  // Upravte úroveň expozice
        expLayer.setOffset(-0.25f);  // Nastavte offset
        expLayer.setGammaCorrection(0.5f);  // Upravte gama korekci
    }
}
```

 této smyčce iterujeme přes všechny vrstvy souboru PSD. Pokud najdeme`ExposureLayer` , upravíme jej`Exposure`, `Offset` a`GammaCorrection` vlastnosti. To vám umožní doladit vizuální výstup vrstvy úpravy expozice.

## Krok 3: Uložte upravený soubor PSD

Po provedení změn je třeba uložit aktualizovaný soubor PSD:

```java
String psdPathAfterChange = dataDir + "ExposureAdjustmentLayerChanged.psd";  // Cesta k uložení upraveného souboru PSD

im.save(psdPathAfterChange);  // Uložte změny do souboru PSD
```

Tento řádek uloží upravený soubor PSD do zadané cesty a zachová vaše úpravy expozice.

## Krok 4: Exportujte jako PNG

Chcete-li exportovat aktualizovaný soubor PSD jako PNG, postupujte takto:

```java
String pngExportPath = dataDir + "ExposureAdjustmentLayerChanged.png";  // Cesta k uložení souboru PNG

PngOptions saveOptions = new PngOptions();  // Vytvořte možnosti PNG
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);  // Nastavte typ barvy na Truecolor s Alpha

im.save(pngExportPath, saveOptions);  // Uložit jako PNG
```

 Zde,`PngOptions` se používá ke konfiguraci nastavení exportu PNG.`PngColorType.TruecolorWithAlpha` zajišťuje, že si soubor PNG zachová barevnou hloubku a průhlednost.

## Krok 5: Přidejte novou vrstvu pro úpravu expozice

Pokud chcete do existujícího souboru PSD přidat novou vrstvu úpravy expozice, můžete tak učinit pomocí následujícího kódu:

```java
String sourceFileName = dataDir + "PhotoExample.psd";  // Cesta k zdrojovému souboru PSD

PsdImage img = (PsdImage) Image.load(sourceFileName);  // Načtěte soubor PSD

ExposureLayer newLayer = img.addExposureAdjustmentLayer(2, -0.25f, 2f);  // Přidejte novou vrstvu úpravy expozice

String psdPathAfterChange = dataDir + "PhotoExampleAddedExposure.psd";  // Cesta k uložení upraveného souboru PSD
String pngExportPath = dataDir + "PhotoExampleAddedExposure.png";  // Cesta k uložení souboru PNG

img.save(psdPathAfterChange);  // Uložte změny do souboru PSD

PngOptions options = new PngOptions();  // Vytvořte možnosti PNG
options.setColorType(PngColorType.TruecolorWithAlpha);  // Nastavte typ barvy na Truecolor s Alpha

img.save(pngExportPath, options);  // Uložit jako PNG
```

tomto kroku se do souboru PSD přidá nová vrstva úpravy expozice se zadanými hodnotami expozice, offsetu a gama korekce. Aktualizované soubory PSD a PNG se poté uloží.

## Závěr

A tady to máte! Naučili jste se vykreslovat a upravovat vrstvy expozice v souborech PSD pomocí Aspose.PSD for Java. Probrali jsme, jak upravit stávající vrstvy expozice, přidat nové a exportovat svou práci jako soubory PNG. Ať už upravujete fotografie nebo připravujete návrhové podklady, tyto dovednosti rozšíří vaši schopnost programově spravovat soubory PSD. Šťastné kódování!

## FAQ

### Co je Aspose.PSD for Java?

Aspose.PSD for Java je knihovna, která umožňuje vytvářet, upravovat a převádět soubory PSD programově pomocí Javy. Poskytuje komplexní funkce pro práci s dokumenty Photoshopu.

### Mohu použít Aspose.PSD pro Javu k manipulaci s jinými typy vrstev?

Ano, Aspose.PSD for Java podporuje různé typy vrstev, včetně textových vrstev, vrstev úprav a obrazových vrstev, což umožňuje rozsáhlou manipulaci se soubory PSD.

### Jak mohu začít s Aspose.PSD pro Javu?

 Můžete začít stažením knihovny z[webové stránky](https://releases.aspose.com/psd/java/) a s odkazem na[dokumentace](https://reference.aspose.com/psd/java/) pro podrobné návody a příklady.

### Je k dispozici bezplatná zkušební verze pro Aspose.PSD pro Javu?

 Ano, je k dispozici bezplatná zkušební verze. Můžete si jej stáhnout[zde](https://releases.aspose.com/).

### Jak mohu získat podporu pro Aspose.PSD pro Java?

 Pro podporu můžete navštívit[Aspose fórum podpory](https://forum.aspose.com/c/psd/34) kde můžete klást otázky a získat pomoc od komunity.