---
title: Správa vrstvy úprav fotografického filtru v PSD - Java
linktitle: Správa vrstvy úprav fotografického filtru v PSD - Java
second_title: Aspose.PSD Java API
description: Naučte se spravovat vrstvy úprav fotografického filtru v souborech PSD pomocí Aspose.PSD for Java. Postupujte podle tohoto průvodce pro snadné úpravy a přidávání filtrů.
weight: 24
url: /cs/java/psd-image-modification-conversion/manage-photo-filter-adjustment-layer-psd/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Správa vrstvy úprav fotografického filtru v PSD - Java

## Zavedení
Jste vývojář, který chce vylepšit své možnosti úpravy grafiky pomocí Javy? Tak to jste na správném místě! Dnes se ponoříme do toho, jak spravovat vrstvy úprav fotografického filtru pomocí Aspose.PSD pro Java. Tato výkonná knihovna umožňuje bezproblémovou manipulaci se soubory PSD, což umožňuje efektivní pracovní postup v grafickém designu. Ať už chcete přidat efekty nebo upravit stávající vrstvy, máme pro vás podrobného průvodce, který celý proces zjednodušuje.
## Předpoklady
Než se vydáme na tuto cestu, ujistěte se, že máte vše, co potřebujete, v provozu:
### Základní software
1.  Java Development Kit (JDK): Ujistěte se, že máte na svém počítači nainstalovanou kompatibilní verzi JDK. Můžete si jej stáhnout z[Web společnosti Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
2.  Aspose.PSD for Java: Pro manipulaci se soubory PSD budete potřebovat knihovnu Aspose.PSD. Můžete si jej stáhnout z[Aspose stránku vydání](https://releases.aspose.com/psd/java/) Nezapomeňte se podívat na[Založte dokumentaci](https://reference.aspose.com/psd/java/) pro více podrobností.
3. IDE (Integrované vývojové prostředí): Dobré IDE jako IntelliJ IDEA nebo Eclipse vám usnadní práci s kódováním.
### Pochopení základů
Prospěšná bude znalost programování v jazyce Java a základní pochopení toho, jak soubory PSD fungují. Pokud s používáním knihoven v Javě začínáte, je dobré si zvyknout na import a používání frameworků.
## Importujte balíčky
Abychom mohli začít, musíme importovat potřebné třídy z knihovny Aspose.PSD. Zde je jednoduchý příkaz k importu, který budete potřebovat na začátku svého souboru Java:
```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.PhotoFilterLayer;
```
Jednoduše to vložte na začátek svého souboru Java a můžete začít pracovat s obrázky PSD!
## Úprava existující vrstvy fotografického filtru
### Krok 1: Nastavte datový adresář
 Nejprve musíte definovat adresář, kde jsou uloženy vaše soubory PSD. Nahradit`"Your Document Directory"` se skutečnou cestou. Takto si vše uspořádáte:
```java
String dataDir = "Your Document Directory";
```
### Krok 2: Načtěte soubor PSD
 Nyní načteme soubor PSD, který chcete upravit. Ujistěte se`PhotoFilterAdjustmentLayer.psd`existuje ve vašem zadaném adresáři.
```java
String sourceFileName = dataDir + "PhotoFilterAdjustmentLayer.psd";
```
### Krok 3: Inicializujte objekt obrázku
Pomocí vestavěné funkce Aspose načteme obrázek do našeho projektu:
```java
PsdImage im = (PsdImage) Image.load(sourceFileName);
```
### Krok 4: Iterujte přes vrstvy
 Dále prozkoumáme vrstvy v souboru PSD. Naším cílem je najít`PhotoFilterLayer`:
```java
for(int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof PhotoFilterLayer) {
        PhotoFilterLayer photoLayer = (PhotoFilterLayer) im.getLayers()[i];
        // Proveďte změny ve vrstvě
    }
}
```
### Krok 5: Přizpůsobte vrstvu fotografického filtru
 Tady se děje kouzlo! Můžete upravit`Color` a`Density`. Můžeme například nastavit barvu na zářivou červenou a upravit hustotu:
```java
photoLayer.setColor(Color.fromArgb(255, 60, 60));
photoLayer.setDensity(78);
photoLayer.setPreserveLuminosity(false);
```
### Krok 6: Uložte upravený soubor PSD
Nakonec změny uložte a vytvořte nový soubor PSD s vašimi úpravami:
```java
String psdPathAfterChange = dataDir + "PhotoFilterAdjustmentLayerChanged.psd";
im.save(psdPathAfterChange);
```
Právě jste upravili vrstvu úprav fotografického filtru v souboru PSD.
## Přidání nové vrstvy fotografického filtru
### Krok 1: Nastavte cestu k adresáři
Stejně jako dříve začneme s definováním našeho datového adresáře:
```java
String dataDir = "Your Document Directory";
```
### Krok 2: Načtěte zdrojový soubor
Pro tento příklad načtěte jiný soubor PSD, kam chceme přidat nový filtr fotografií:
```java
String sourceFileName = dataDir + "PhotoExample.psd";
```
### Krok 3: Znovu inicializujte objekt obrázku
 Musíme vytvořit nový`PsdImage` instance, takže načteme soubor:
```java
PsdImage img = (PsdImage) Image.load(sourceFileName);
```
### Krok 4: Přidejte vrstvu fotografického filtru
Nyní můžeme přidat novou vrstvu fotografického filtru s přizpůsobenou barvou. Zde je návod, jak se to dělá:
```java
PhotoFilterLayer layer = img.addPhotoFilterLayer(Color.fromArgb(25, 255, 35));
```
### Krok 5: Uložte nový soubor PSD
Opět je čas uložit naše změny. Zde je řádek, jak to udělat:
```java
String psdPathAfterChange = dataDir + "PhotoExampleAddedPhotoFilter.psd";
img.save(psdPathAfterChange);
```
Úspěšně jste přidali novou vrstvu fotografického filtru do souboru PSD.
## Závěr
Správa vrstev úprav fotografického filtru v souborech PSD pomocí Aspose.PSD pro Java je nejen přímočará, ale také otevírá svět možností pro grafické úpravy. Podle těchto podrobných průvodců můžete vylepšit své soubory PSD pomocí živých filtrů a vytvořit úžasnou grafiku. Otestujte tyto funkce ve svých aplikacích; jistě zjistíte, že je to efektivní pro vaše projekty!
## FAQ
### Co je Aspose.PSD?
Aspose.PSD je knihovna .NET a Java pro vytváření, úpravu a konverzi souborů PSD.
### Mohu vyzkoušet Aspose.PSD zdarma?
 Ano, Aspose nabízí bezplatnou zkušební verzi. Podívejte se na to[zde](https://releases.aspose.com/).
### Kde najdu dokumentaci?
 Kompletní dokumentaci naleznete na[Referenční stránka Aspose](https://reference.aspose.com/psd/java/).
### Jak mohu zakoupit Aspose.PSD?
 Software si můžete koupit od[tento odkaz](https://purchase.aspose.com/buy).
### Je k dispozici podpora pro Aspose.PSD?
 Absolutně! Podporu můžete získat prostřednictvím fóra podpory Aspose[zde](https://forum.aspose.com/c/psd/34).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
