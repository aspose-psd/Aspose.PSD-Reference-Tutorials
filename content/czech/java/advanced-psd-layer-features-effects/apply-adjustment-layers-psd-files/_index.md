---
title: Aplikujte vrstvy úprav v souborech PSD pomocí Java
linktitle: Aplikujte vrstvy úprav v souborech PSD pomocí Java
second_title: Aspose.PSD Java API
description: Naučte se aplikovat vrstvy úprav v souborech PSD pomocí Aspose.PSD for Java v tomto úplném podrobném průvodci pro vývojáře.
type: docs
weight: 15
url: /cs/java/advanced-psd-layer-features-effects/apply-adjustment-layers-psd-files/
---
## Zavedení
Jste vývojář Java a chcete vylepšit obrázky uložené v souborech PSD? Pokud ano, jste na správném místě! V tomto článku prozkoumáme, jak aplikovat vrstvy úprav v souborech PSD pomocí knihovny Aspose.PSD pro Javu. Ať už pracujete na osobním projektu nebo na profesionální aplikaci, pochopení toho, jak manipulovat se soubory PSD, může výrazně zvýšit možnosti vašeho softwaru. 

## Předpoklady
Než se pustíme do kódu a začneme aplikovat tyto vrstvy úprav, je potřeba splnit několik předpokladů:
1. Java Development Kit (JDK): Ujistěte se, že máte na svém počítači nainstalovaný JDK. Můžete si jej stáhnout z[Web společnosti Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
2.  Knihovna Aspose.PSD: Pokud jste to ještě neudělali, budete si muset stáhnout knihovnu Aspose.PSD pro Javu. Můžete to najít[zde](https://releases.aspose.com/psd/java/).
3. Vývojové prostředí: Nastavte integrované vývojové prostředí Java (IDE), jako je IntelliJ IDEA nebo Eclipse, kde budete psát a spouštět svůj kód.
4. Základní znalost Javy: Obecná znalost programování v Javě vám pomůže hladce pokračovat.
5. Soubory PSD: Mějte po ruce několik souborů PSD pro účely testování. Některé můžete vytvořit pomocí Adobe Photoshopu nebo si stáhnout ukázkové soubory z internetu.
## Importujte balíčky
Než začneme kódovat, ujasněme si, které balíčky potřebujeme importovat. Aspose.PSD nám umožňuje pracovat se soubory Photoshopu mnoha způsoby, takže se chopme tříd nezbytných pro práci s obrázky PSD a vrstvami úprav.
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.AdjustmentLayer;
```
Nyní, když máme naše balíčky na místě, pojďme si příklady rozebrat krok za krokem!
## Krok 1: Načtěte soubor PSD
Prvním krokem na naší cestě je načtení souboru PSD. Toto je soubor, se kterým budeme pracovat, abychom použili naše vrstvy úprav.
```java
String dataDir = "Your Document Directory";
String sourceFileName1 = dataDir + "ChannelMixerAdjustmentLayer.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName1);
```
 V tomto úryvku definujeme adresář, kde jsou umístěny naše soubory PSD, a načteme konkrétní soubor, se kterým chceme manipulovat. Nezapomeňte vyměnit`"Your Document Directory"` se skutečnou cestou k souborům PSD na vašem počítači.
## Krok 2: Iterujte přes vrstvy
Nyní, když jsme načetli soubor PSD, budeme chtít iterovat jeho vrstvy, abychom našli naše vrstvy úprav.
```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof AdjustmentLayer) {
        AdjustmentLayer adjustmentLayer = (AdjustmentLayer) im.getLayers()[i];
        
        if (adjustmentLayer != null) {
            adjustmentLayer.mergeLayerTo(im.getLayers()[0]);
        }
    }
}
```
 V tomto kroku procházíme každou vrstvu v souboru PSD, abychom identifikovali všechny vrstvy`AdjustmentLayer` typ. Pokud nějakou najdeme, sloučíme ji se základní vrstvou, což je obvykle první vrstva (`im.getLayers()[0]`). Tento proces slučování efektivně aplikuje úpravy na náš obraz. 
## Krok 3: Uložte upravený soubor PSD
Po úpravě vrstev je zásadní uložit provedené změny. Udělejme to v dalším kroku.
```java
String exportPath1 = dataDir + "ChannelMixerAdjustmentLayerChanged.psd";
im.save(exportPath1);
```
 Zde zadáme cestu exportu pro náš upravený soubor PSD a zavoláme`save()` způsob zápisu našich změn na disk.
## Krok 4: Vrstva pro úpravu úrovní
Zopakujme postup pro jiný typ vrstvy úprav: vrstvu úprav Úrovně. 
### Načtěte PSD vrstvu pro úpravu úrovní
```java
String sourceFileName2 = dataDir + "LevelsAdjustmentLayerRgb.psd";
PsdImage img = (PsdImage) Image.load(sourceFileName2);
```
Stejně jako předtím načteme soubor PSD obsahující naši vrstvu úprav Úrovně. 
### Iterujte přes vrstvy úrovní
Dále projdeme vrstvy znovu, stejně jako předtím, ale nyní pracujeme s jiným souborem PSD.
```java
for (int i = 0; i < img.getLayers().length; i++) {
    if (img.getLayers()[i] instanceof AdjustmentLayer) {
        AdjustmentLayer adjustmentLayer = (AdjustmentLayer) img.getLayers()[i];
        
        if (adjustmentLayer != null) {
            adjustmentLayer.mergeLayerTo(img.getLayers()[0]);
        }
    }
}
```
Tento kód funguje podobně jako předchozí iterace; vyhledává vrstvy úprav v aktuálním souboru PSD, což nám umožňuje použít jakékoli dostupné úpravy.
## Uložte vrstvu PSD pro úpravu úrovní
Nakonec tento nový soubor po použití úprav uložíme.
```java
String exportPath2 = dataDir + "LevelsAdjustmentLayerRgbChanged.psd";
img.save(exportPath2);
```
Nyní jsme úspěšně zpracovali vrstvu úprav Úrovně!
## Závěr
Gratuluji! Právě jste se naučili, jak aplikovat vrstvy úprav v souborech PSD pomocí Javy a knihovny Aspose.PSD. Ať už jste ladili barvy nebo upravovali úrovně, nyní máte základní dovednosti pro programovou manipulaci se soubory PSD.
Použití Aspose.PSD může výrazně zefektivnit pracovní postupy při úpravách obrázků, což umožňuje automatizaci a přizpůsobení způsobem, který tradiční nástroje nemusí. Neváhejte dále prozkoumávat knihovnu a experimentovat s různými typy vrstev, abyste viděli, jaké kreativní možnosti jsou tam venku.
## FAQ
### Co je knihovna Aspose.PSD?
Aspose.PSD je knihovna, která umožňuje vývojářům načítat, manipulovat a ukládat soubory Photoshop PSD v aplikacích Java.
### Mohu používat Aspose.PSD zdarma?
 Ano! Aspose vám nabízí bezplatnou zkušební verzi, abyste mohli prozkoumat jejich knihovnu. Můžete se přihlásit[zde](https://releases.aspose.com/).
### Potřebuji nainstalovaný Photoshop, abych mohl používat Aspose.PSD?
Ne, nepotřebujete Photoshop. Aspose.PSD pracuje nezávisle na programové manipulaci se soubory PSD.
### Kde najdu dokumentaci k Aspose.PSD?
Můžete navštívit stránku dokumentace[zde](https://reference.aspose.com/psd/java/) prozkoumat funkce, třídy a metody.
### Jak získám podporu pro produkty Aspose?
 K podpoře se můžete dostat přes[Aspose fórum](https://forum.aspose.com/c/psd/34) kde můžete klást otázky a hledat řešení.