---
title: Správa jasu a kontrastu ve vrstvách PSD - Java
linktitle: Správa jasu a kontrastu ve vrstvách PSD - Java
second_title: Aspose.PSD Java API
description: Naučte se bez námahy upravovat jas a kontrast v souborech PSD pomocí Aspose.PSD for Java. Ideální pro vývojáře a grafiky.
type: docs
weight: 21
url: /cs/java/psd-image-modification-conversion/manage-brightness-contrast-psd-layers/
---
## Zavedení

Jste grafik nebo vývojář, který často pracuje se soubory PSD (Photoshop Document)? Zjistili jste, že potřebujete upravit jas a kontrast vrstev v těchto souborech, ale chybí vám know-how k automatizaci tohoto úkolu pomocí Java? Tak to máš štěstí! V tomto tutoriálu se ponoříme do toho, jak spravovat jas a kontrast ve vrstvách PSD pomocí knihovny Aspose.PSD pro Javu. To vám nejen ušetří čas, ale také zlepší váš kreativní pracovní postup. Vyhrňme si rukávy a začněme!

## Předpoklady

Než se vydáme na tuto vzrušující cestu manipulace se soubory PSD pomocí Javy, je nezbytné zajistit, abyste měli vše, co potřebujete, správně nastaveno. Zde je to, co budete potřebovat k úspěšnému dokončení tohoto kurzu:

1.  Java Development Kit (JDK): Ujistěte se, že máte na svém počítači nainstalovaný JDK 8 nebo vyšší. Můžete si jej stáhnout z[Web společnosti Oracle](https://www.oracle.com/java/technologies/javase-jdk8-downloads.html).

2. Aspose.PSD for Java Library: Pro práci se soubory PSD budete potřebovat knihovnu Aspose.PSD. Nejnovější verzi si můžete stáhnout z[stránka vydání](https://releases.aspose.com/psd/java/).

3. IDE dle vašeho výběru: Pro psaní a spouštění kódu Java je preferováno integrované vývojové prostředí (IDE), jako je IntelliJ IDEA, Eclipse nebo NetBeans.

4. Základní znalost Javy: Znalost programování v Javě vám pomůže porozumět úryvkům kódu, se kterými budeme pracovat.

Jakmile splníte tyto předpoklady, jsme připraveni pokračovat. Nyní si vezměte svůj oblíbený editor kódu a pojďme se pustit do kódování!

## Importujte balíčky

Prvním krokem na naší kódovací cestě je import potřebných balíčků. Než budete moci využívat funkce poskytované Aspose.PSD, musíte se ujistit, že knihovna je ve vaší třídě. Můžete to udělat takto:

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.BrightnessContrastLayer;
```

Dokončením těchto kroků připravíte scénu pro efektivní práci se soubory PSD!

Nyní, když máme vše nastaveno, je čas pustit se do hlavní části tutoriálu: úpravy jasu a kontrastu ve vrstvách PSD. Tento proces rozdělíme do jasných kroků, abyste zajistili, že jej budete snadno sledovat.

## Krok 1: Definujte svůj adresář dokumentů

Začněte definováním adresáře, kde jsou umístěny vaše soubory PSD. Tento krok pomáhá při efektivní organizaci souborů.

```java
String dataDir = "Your Document Directory";
```

 Nahradit`"Your Document Directory"` se skutečnou cestou k adresáři vašeho souboru PSD.

## Krok 2: Zadejte názvy zdrojových a cílových souborů

Dále musíte zadat název zdrojového souboru vašeho PSD a cílový soubor, kam bude upravený PSD uložen.

```java
String sourceFileName = dataDir + "BrightnessContrastModern.psd";
String psdPathAfterChange = dataDir + "BrightnessContrastModernChanged.psd";
```

 V tomto příkladu předpokládáme, že máte pojmenovaný soubor PSD`BrightnessContrastModern.psd` ve vašem adresáři.

## Krok 3: Načtěte soubor PSD

Nyní je čas načíst soubor PSD do aplikace, abyste s ním mohli manipulovat.

```java
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

 Tento řádek kódu vytvoří instanci`PsdImage` představující váš soubor PSD. Díky tomu máte nyní přístup ke všem vrstvám PSD.

## Krok 4: Iterujte přes vrstvy

Další krok zahrnuje iteraci každé vrstvy vašeho souboru PSD, abyste našli a upravili nastavení jasu a kontrastu.

```java
for(int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof BrightnessContrastLayer) {
        BrightnessContrastLayer brightnessContrastLayer = (BrightnessContrastLayer)im.getLayers()[i];
```

 The`for` smyčka prochází každou vrstvou PSD. Ověřujeme, zda je vrstva instancí`BrightnessContrastLayer`. To je nezbytné pro zajištění toho, že se pokusíte změnit jas a kontrast pouze ve správných vrstvách.

## Krok 5: Upravte jas a kontrast

 V rámci smyčky nyní můžete nastavit jas a kontrast pro každou z nich`BrightnessContrastLayer`. 

```java
        brightnessContrastLayer.setBrightness(50);
        brightnessContrastLayer.setContrast(50);
    }
}
```

 V tomto příkladu nastavíme jas a kontrast na`50`. Tyto hodnoty můžete upravit podle svých požadavků. Vyšší číslo zvyšuje jas/kontrast, zatímco nižší číslo jej snižuje.

## Krok 6: Uložte změny

Posledním krokem je uložení změn do souboru PSD. Budete chtít zapsat upravený obrázek zpět do určeného cíle.

```java
im.save(psdPathAfterChange);
```

Tento řádek kódu uloží upravený soubor PSD s novým nastavením jasu a kontrastu.

## Závěr

Gratuluji! Úspěšně jste se naučili, jak spravovat jas a kontrast ve vrstvách PSD pomocí Aspose.PSD pro Javu. Automatizací těchto úprav nejen zlepšíte svůj pracovní postup, ale také zvýšíte svou produktivitu. Až budete příště potřebovat vyladit tyto obrázky, budete dobře vybaveni, abyste se s tímto úkolem vypořádali se svými novými dovednostmi v jazyce Java. Takže, co vytvoříte příště?

## FAQ

### Co je Aspose.PSD for Java?
Aspose.PSD for Java je knihovna, která umožňuje vývojářům programově manipulovat se soubory PSD, což umožňuje automatizaci úloh souvisejících s Photoshopem.

### Mohu upravit jas a kontrast více vrstev najednou?
 Ano, přístup použitý v tomto tutoriálu prochází všemi vrstvami v PSD, což vám umožňuje upravit více`BrightnessContrastLayer` instance.

### Jak získám dočasnou licenci pro Aspose.PSD?
 Dočasnou licenci můžete získat na adrese[dočasná licenční stránka](https://purchase.aspose.com/temporary-license/).

### Je k dispozici bezplatná zkušební verze pro Aspose.PSD?
 Ano, můžete si stáhnout bezplatnou zkušební verzi Aspose.PSD z[stránka vydání](https://releases.aspose.com/).

### Kde najdu další podporu pro Aspose.PSD?
 Na jejich stránkách můžete získat podporu pro Aspose.PSD[fórum podpory](https://forum.aspose.com/c/psd/34).