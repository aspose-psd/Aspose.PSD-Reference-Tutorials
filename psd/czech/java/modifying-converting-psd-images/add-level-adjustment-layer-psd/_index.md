---
title: Přidejte vrstvu pro úpravu úrovně v PSD
linktitle: Přidejte vrstvu pro úpravu úrovně v PSD
second_title: Aspose.PSD Java API
description: Naučte se, jak efektivně přidat vrstvu úpravy úrovně do vašich souborů PSD pomocí Aspose.PSD for Java. Zvyšte své dovednosti v oblasti úpravy obrázků.
weight: 16
url: /cs/java/modifying-converting-psd-images/add-level-adjustment-layer-psd/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Přidejte vrstvu pro úpravu úrovně v PSD

## Zavedení
Pokud jde o úpravy obrázků, správa úrovní může znamenat velký rozdíl v živosti a jasnosti vašich fotografií. Jedním z užitečných nástrojů v arzenálu Photoshopu je „Vrstva úprav úrovně“, která vám umožňuje vyladit tónový rozsah a vyvážení barev vašich obrázků. V této příručce vás provedeme tím, jak implementovat vrstvu úpravy úrovně v souboru PSD pomocí Aspose.PSD for Java. Vezměte si své Java IDE.
## Předpoklady
Než skočíte do světa úprav úrovní, budete muset nastavit několik věcí, abyste zajistili hladkou jízdu:
1.  Java Development Kit (JDK): Ujistěte se, že máte na svém počítači nainstalovanou sadu JDK. Pokud ji nemáte, můžete si ji vzít z[Web společnosti Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) nebo použijte OpenJDK.
2.  Aspose.PSD for Java Library: Chcete-li manipulovat se soubory PSD, budete si muset stáhnout knihovnu Aspose.PSD. Z tohoto můžete získat nejnovější verzi[odkaz ke stažení](https://releases.aspose.com/psd/java/) a ujistěte se, že jste zahrnuli JAR do knihovny vašeho projektu.
3. Základní znalost Javy: Základní znalost programování v Javě vám pomůže, protože v tomto tutoriálu se budeme ponořit do úryvků kódu.
4. Nastavení IDE: K zápisu a spouštění kódu můžete použít libovolné Java IDE, jako je IntelliJ IDEA, Eclipse nebo NetBeans. Jen se ujistěte, že jste nastavili svůj Java projekt a přidali knihovnu Aspose.PSD.

## Importujte balíčky
Než začneme psát náš kód, musíme naimportovat potřebné balíčky z knihovny Aspose.PSD. Můžete to udělat takto:
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.LevelsLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.LevelChannel;
```
Importováním těchto balíčků budeme mít přístup ke třídám nezbytným pro načítání, úpravy a ukládání našich souborů PSD.

Nyní si tento proces rozdělíme na stravitelné kroky. Pokračujte v procházení načítáním souboru PSD, úpravou úrovní a uložením změn. 
## Krok 1: Nastavte cesty k souborům
Prvním krokem je definovat, kde se náš soubor PSD nachází a kam chceme upravený výstup uložit. Cestu k adresáři můžete přizpůsobit svým potřebám.
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "LevelsAdjustmentLayer.psd";
String psdPathAfterChange = dataDir + "LevelsAdjustmentLayerChanged.psd";
```
 Tady, vyměňte`"Your Document Directory"`se skutečnou cestou ve vašem systému, kde je uložen váš soubor PSD. Tím se připraví půda pro všechno, co budeme dělat dál.
## Krok 2: Načtěte soubor PSD
 Nyní načteme soubor PSD pomocí`PsdImage` třída. Tento krok je nezbytný, protože nám umožňuje přistupovat k vrstvám a manipulovat s nimi.
```java
PsdImage im = (PsdImage) Image.load(sourceFileName);
```
 Když zavoláte`Image.load()` , přečte soubor PSD a vytvoří instanci`PsdImage` se kterými můžete pracovat.
## Krok 3: Iterujte přes vrstvy
Protože chceme upravit vrstvu úpravy úrovně, budeme muset procházet každou vrstvou v našem souboru PSD. To nám pomáhá najít konkrétní vrstvu, kterou chceme upravit.
```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof LevelsLayer) {
        LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
        // Další manipulace půjde sem...
    }
}
```
 V této smyčce`instanceof LevelsLayer` zkontroluje, zda je aktuální vrstva vrstvou úprav úrovní. Pokud ano, můžeme přistoupit k úpravě jeho vlastností.
## Krok 4: Upravte nastavení úrovně kanálu
Jakmile identifikujeme správnou vrstvu, můžeme upravit její vstupní a výstupní úrovně. Tady se děje kouzlo! Upravte různé parametry, abyste viděli, jak ovlivňují obraz.
```java
LevelChannel channel = levelsLayer.getChannel(0);
channel.setInputMidtoneLevel(2.0f);
channel.setInputShadowLevel((short) 10);
channel.setInputHighlightLevel((short) 230);
channel.setOutputShadowLevel((short) 20);
channel.setOutputHighlightLevel((short) 200);
```
Každý parametr dělá toto:
- Input Midtone Level: Upravuje střední tóny.
- Úroveň vstupního stínu: Vyladí tmavší oblasti obrazu.
- Vstupní úroveň zvýraznění: Mění světlé oblasti obrazu.
- Úroveň výstupních stínů: Nastavuje, jak se budou zobrazovat tmavé stíny.
- Output Highlight Level: Nastavuje, jak budou vypadat světlá světla.
Nebojte se experimentovat s různými hodnotami!
## Krok 5: Uložte upravený soubor PSD
Nyní, když jsme provedli naše úpravy, je čas uložit upravený soubor PSD. Tento krok je zásadní pro zajištění použití a uložení vašich změn.
```java
im.save(psdPathAfterChange);
```
 Nyní můžete svůj upravený soubor PSD najít na zadané adrese`psdPathAfterChange`. 
## Závěr
Právě jste se naučili, jak přidat vrstvu úpravy úrovně do souboru PSD pomocí Aspose.PSD for Java! Podle tohoto průvodce můžete bez námahy upravit tonální kvalitu svých obrázků a připravit tak cestu pro živější a vizuálně přitažlivější výstup. Pamatujte, že cvičení dělá mistra, takže neváhejte vyladit úpravy a prozkoumejte různé soubory PSD, abyste viděli účinky svých změn.
## FAQ
### Co je to vrstva úpravy úrovně?
Vrstva nastavení úrovně vám umožňuje opravit tónový rozsah v obrázcích, vyvážit stíny, střední tóny a světla.
### Mohu používat Aspose.PSD bez nákupu?
Ano! Aspose nabízí bezplatnou zkušební verzi k otestování knihovny před jejím zakoupením.
### Kde najdu dokumentaci k Aspose.PSD?
 Dokumentaci najdete[zde](https://reference.aspose.com/psd/java/).
### Existuje nějaká podpora komunity pro produkty Aspose?
 Absolutně! Můžete klást otázky a získat podporu v[Aspose fórum](https://forum.aspose.com/c/psd/34).
### Jak mohu získat dočasnou licenci pro Aspose.PSD?
 Můžete požádat o dočasnou licenci[zde](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
