---
title: Přidejte vrstvu pro úpravu sytosti odstínu do PSD
linktitle: Přidejte vrstvu pro úpravu sytosti odstínu do PSD
second_title: Aspose.PSD Java API
description: Naučte se, jak přidat vrstvy úprav sytosti odstínu do PSD pomocí Aspose.PSD pro Java, v tomto komplexním, podrobném tutoriálu. Vylepšete svůj pracovní postup grafického designu.
type: docs
weight: 14
url: /cs/java/modifying-converting-psd-images/add-hue-saturation-adjustment-layer-psd/
---
## Zavedení
Pokud jde o grafický design, manipulace s barvami hraje klíčovou roli – konkrétně vyladění odstínu, sytosti a světlosti může drasticky změnit náladu a kvalitu jakéhokoli obrázku. Jedním z účinných způsobů, jak toho dosáhnout, je použití vrstev úprav ve Photoshopu (soubory PSD). Pokud chcete vylepšit své soubory PSD programově pomocí Javy, pomůže vám knihovna Aspose.PSD! Tento výukový program vás provede kroky k přidání vrstvy pro úpravu sytosti odstínu do vašich souborů PSD, díky čemuž budou vaše pracovní postupy produktivnější a efektivnější.
této příručce pokryjeme vše od importu nezbytných balíčků až po hrubé detaily příkladů kódu.
## Předpoklady
Než se pustíme do kódu, ujistěte se, že máte na svém místě následující:
1.  Java Development Kit (JDK): Ujistěte se, že máte na svém počítači nainstalovaný JDK 8 nebo vyšší. Můžete si jej stáhnout z[Java SE Development Kit ke stažení](https://www.oracle.com/java/technologies/javase-downloads.html).
2.  Aspose.PSD for Java Library: Budete potřebovat knihovnu Aspose.PSD, kterou můžete[stáhnout zde](https://releases.aspose.com/psd/java/). 
3. IDE: Vhodné integrované vývojové prostředí (IDE) jako IntelliJ IDEA nebo Eclipse pro vývoj v Javě.
4. Základní znalost Javy: Znalost programování v Javě je výhodou, ale nebojte se; krok za krokem vás provedeme kódem.
Nyní, když máme naše předpoklady uspořádané, přejděme k zábavnější části – kódování!
## Importujte balíčky
Chcete-li začít pracovat s knihovnou Aspose.PSD, je prvním krokem import potřebných tříd. Zde je návod, jak to udělat v souboru Java:
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.HueSaturationLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.ColorRangeHsl;
```
Ujistěte se, že máte do projektu přidány příslušné knihovny, aby tyto importy fungovaly hladce.
## Krok 1: Nastavte adresář dokumentů
Každý projekt potřebuje výchozí bod a ten náš není výjimkou. Musíte zadat adresář, kde jsou uloženy vaše soubory PSD. To je zásadní pro správné načítání a ukládání obrázků.
```java
String dataDir = "Your Document Directory"; // Aktualizujte tuto cestu k vašemu skutečnému adresáři
```
## Krok 2: Načtěte existující soubor PSD
Abychom mohli manipulovat se stávajícím souborem PSD, musíme jej nejprve načíst do našeho programu. Můžete to udělat takto:
```java
String sourceFileName = dataDir + "HueSaturationAdjustmentLayer.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```
 V tomto kódu aktualizujte`"HueSaturationAdjustmentLayer.psd"` na název vašeho stávajícího souboru PSD, který chcete upravit.
## Krok 3: Upravte vrstvu odstínu/sytosti
Dále projdeme vrstvy našeho načteného obrázku PSD, abychom našli a upravili všechny existující vrstvy odstínu/sytosti. Tento krok zahrnuje úpravu hodnot odstínu, sytosti a světlosti.
```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof HueSaturationLayer) {
        HueSaturationLayer hueLayer = (HueSaturationLayer) im.getLayers()[i];
        hueLayer.setHue((short) -25);
        hueLayer.setSaturation((short) -12);
        hueLayer.setLightness((short) 67);
        ColorRangeHsl colorRange = hueLayer.getRange(2);
        colorRange.setHue((short) -40);
        colorRange.setSaturation((short) 50);
        colorRange.setLightness((short) -20);
        colorRange.setMostLeftBorder((short) 300);
    }
}
```
V tomto příkladu:
- Upravujeme odstín na -25, sytost na -12 a světlost na +67.
-  The`getRange(2)` metoda nám umožňuje vyladit konkrétní barevné rozsahy podle potřeby.
## Krok 4: Uložte upravený soubor PSD
Po provedení úprav je dalším krokem uložení souboru. To je zásadní součástí našeho procesu, který zajišťuje, že změny, které jsme provedli, se neztratí.
```java
String psdPathAfterChange = dataDir + "HueSaturationAdjustmentLayerChanged.psd";
im.save(psdPathAfterChange);
```
## Krok 5: Přidejte novou vrstvu odstínu/sytosti
Dále můžete chtít přidat novou vrstvu úprav odstínu/sytosti do jiného souboru PSD. Postupujte podle stejného přístupu, který jste používali dříve, ale s jinými soubory PSD.
```java
sourceFileName = dataDir + "PhotoExample.psd";
PsdImage img = (PsdImage) Image.load(sourceFileName);
HueSaturationLayer hueLayerNew = img.addHueSaturationAdjustmentLayer();
```
## Krok 6: Nastavte nové hodnoty odstínu/sytosti pro novou vrstvu
Nyní, když jste vytvořili tuto novou vrstvu, použijte požadované nastavení odstínu, sytosti a světlosti stejně jako předtím.
```java
hueLayerNew.setHue((short) -25);
hueLayerNew.setSaturation((short) -12);
hueLayerNew.setLightness((short) 67);
ColorRangeHsl newColorRange = hueLayerNew.getRange(2);
newColorRange.setHue((short) -160);
newColorRange.setSaturation((short) 100);
newColorRange.setLightness((short) 20);
newColorRange.setMostLeftBorder((short) 300);
```
## Krok 7: Uložte aktualizovaný soubor PSD
Nakonec uložte soubor PSD s přidanou vrstvou Hue/Saturation, abyste viděli své změny.
```java
String psdPathAfterNewLayerChange = dataDir + "PhotoExampleAddedHueSaturation.psd";
img.save(psdPathAfterNewLayerChange);
```
Gratuluji! Úspěšně jste manipulovali se soubory PSD pomocí Aspose.PSD for Java. Nyní můžete experimentovat s různými obrázky a hlubšími úpravami a oživit tak své projekty grafického designu.
## Závěr
Práce s grafikou programově otevírá svět možností. Použití Aspose.PSD for Java k přidání a úpravě vrstev úprav sytosti odstínu poskytuje flexibilitu a efektivitu, která může zefektivnit váš pracovní postup návrhu. Ať už vylepšujete fotografie pro projekt nebo vytváříte úžasný vizuální obsah, zvládnutí těchto nástrojů může výrazně zlepšit váš výstup.
 Neváhejte a prozkoumejte další funkce Aspose.PSD tím, že se ponoříte do[dokumentace](https://reference.aspose.com/psd/java/) nebo zvážit zachycení a[dočasná licence](https://purchase.aspose.com/temporary-license/) vyzkoušet plnou sílu knihovny.
## FAQ
### Co je to vrstva pro úpravu sytosti odstínu?
Vrstva pro úpravu sytosti odstínu umožňuje upravit vlastnosti barev obrazu bez trvalé změny původních pixelů.
### Potřebuji nainstalovaný Photoshop, abych mohl používat Aspose.PSD?
Ne, Aspose.PSD je samostatná knihovna, která funguje nezávisle na Photoshopu.
### Mohu použít Aspose.PSD pro dávkové zpracování?
Ano, pomocí Aspose.PSD můžete automatizovat a dávkově zpracovávat více souborů PSD.
### Je Aspose.PSD zdarma?
Aspose.PSD nabízí bezplatnou zkušební verzi, ale pro dlouhodobé používání je nutná licence. Můžete se podívat na ceny[zde](https://purchase.aspose.com/buy).