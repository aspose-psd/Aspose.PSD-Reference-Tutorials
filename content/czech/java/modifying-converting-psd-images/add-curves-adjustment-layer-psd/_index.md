---
title: Přidejte vrstvu úprav křivek v PSD pomocí Java
linktitle: Přidejte vrstvu úprav křivek v PSD pomocí Java
second_title: Aspose.PSD Java API
description: V tomto podrobném návodu se dozvíte, jak přidat vrstvu Úprava křivek do souboru PSD pomocí Aspose.PSD for Java. Vylepšete své obrázky snadno.
type: docs
weight: 11
url: /cs/java/modifying-converting-psd-images/add-curves-adjustment-layer-psd/
---
## Zavedení
Stalo se vám někdy, že jste se zasekli při pokusu o manipulaci s obrázky ve formátu PSD? Ať už jste začínající grafik nebo ostřílený profík, práce se soubory Photoshopu vám někdy může připadat jako navigace v labyrintu. Naštěstí existuje nástroj, který tento proces zjednodušuje – Aspose.PSD for Java. V tomto tutoriálu se ponoříme do toho, jak přidat vrstvu Úprava křivek do souboru PSD pomocí Aspose.PSD, což vám usnadní a zefektivní úpravy obrázků. S podrobným vedením budete moci vylepšovat své snímky jako profesionál, aniž byste se zabředli do složitostí tradičně spojených s manipulací s obrázky.
## Předpoklady
Než se ponoříme do kódu, ujistěte se, že máte vše připraveno. Zde jsou předpoklady, které budete potřebovat:
1. Java Development Kit (JDK): V počítači musíte mít nainstalovaný JDK. Ujistěte se, že se jedná o nejnovější verzi pro nejlepší kompatibilitu.
2. Aspose.PSD for Java Library: Chcete-li manipulovat se soubory PSD, budete si muset stáhnout a zahrnout knihovnu Aspose.PSD do svého projektu. Můžeš to chytit[zde](https://releases.aspose.com/psd/java/).
3. IDE: K napsání kódu použijte jakékoli Java IDE, jako je IntelliJ IDEA, Eclipse nebo dokonce jednoduchý textový editor.
4. Základní porozumění Javě: Znalost programování v Javě vám pomůže hladce pokračovat.
Máš všechno? Děsivý! Pojďme k zábavné části.
## Import balíčků
Nejprve musíte importovat požadované balíčky. Postupujte takto:
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.CurvesLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.CurvesContinuousManager;
import com.aspose.psd.fileformats.psd.layers.layerresources.CurvesDiscreteManager;
```
Importováním těchto balíčků sdělujete své Java aplikaci o třídách, které potřebuje pro manipulaci se soubory PSD a pro specifickou práci s vrstvami úprav křivek.
Nyní, když máme vše nastaveno, pojďme si kód rozebrat a podívat se, jak přidat vrstvu Úprava křivek krok za krokem.
## Krok 1: Definujte svůj datový adresář
Prvním krokem je určit, kde budou vaše soubory PSD uloženy. Nastavte si adresář, abyste měli vše uspořádané.
```java
String dataDir = "Your Document Directory"; // Aktualizujte tuto cestu
```
 Myslete na to`dataDir`jako váš pracovní prostor; tam se odehrává všechna ta kouzla! Nezapomeňte vyměnit`Your Document Directory` se skutečnou cestou, kde jsou nebo budou umístěny vaše soubory PSD.
## Krok 2: Načtěte soubor PSD
Dále budete muset načíst soubor PSD, který chcete upravit. To se provádí pomocí následujícího kódu:
```java
String sourceFileName = dataDir + "CurvesAdjustmentLayer";
String psdPathAfterChange = dataDir + "CurvesAdjustmentLayerChanged";
```
 V tomto fragmentu kódu`sourceFileName` ukazuje na původní soubor PSD, zatímco`psdPathAfterChange` je místo, kam uložíte upravený soubor. Nezapomeňte přiložit`.psd` dále v kódu.
## Krok 3: Iterujte přes vrstvy
Nyní je čas ponořit se do vrstev vašeho souboru PSD. Budeme procházet každou vrstvou a hledat vrstvy úprav křivek.
```java
for (int j = 1; j < 2; j++) {
    String fileName = sourceFileName + ".psd";
    PsdImage im = (PsdImage) Image.load(fileName);
    
    for(int k = 0; k < im.getLayers().length; k++) {
        if (im.getLayers()[k] instanceof CurvesLayer) {
            // Zpracování vrstev křivek půjde sem
        }
    }
}
```
Zde je rozpis toho, co se děje:
-  Začneme načtením souboru PSD do a`PsdImage` objekt pojmenovaný`im`.
-  Dále projdeme všechny vrstvy v obrázku pomocí`im.getLayers().length` . To nám umožňuje přístup ke každé vrstvě, což nám umožňuje zkontrolovat, zda se jedná o a`CurvesLayer`.
## Krok 4: Upravte vrstvu křivek
 Uvnitř smyčky, která kontroluje`CurvesLayer`přidáte logiku pro úpravu křivek. Uděláte to takto:
```java
if (curvesLayer.isDiscreteManagerUsed()) {
    CurvesDiscreteManager manager = (CurvesDiscreteManager) curvesLayer.getCurvesManager();
    for (int i = 10; i < 50; i++) {
        manager.setValueInPosition(0, (byte) i, (byte) (15 + (i * 2)));
    }
} else {
    CurvesContinuousManager manager = (CurvesContinuousManager) curvesLayer.getCurvesManager();
    manager.addCurvePoint((byte) 0, (byte) 50, (byte) 100);
    manager.addCurvePoint((byte) 0, (byte) 150, (byte) 130);
}
```
V tomto segmentu:
- Zkontrolujeme, zda vrstva křivek používá diskrétní manažer nebo spojitý manažer.
- Pokud se jedná o diskrétního manažera, nastavíme pro každou pozici nové hodnoty od 10 do 49.
- Naopak u průběžného správce přidáváme body křivky, abychom křivky upravili podle potřeby.
## Krok 5: Uložte upravené PSD
Po provedení úprav je posledním krokem uložení upraveného souboru PSD.
```java
im.save(psdPathAfterChange + Integer.toString(j) + ".psd");
```
 Tento řádek uloží upravené PSD do cesty, kterou jste definovali dříve. Při každé úpravě se vytvoří nový soubor s jinou příponou na základě čítače smyček`j`.
## Závěr
Gratuluji! Úspěšně jste se naučili, jak přidat vrstvu Úprava křivek do souboru PSD pomocí Aspose.PSD for Java. Pomocí několika kroků můžete své obrázky vylepšit a manipulovat s nimi podle svých potřeb. Flexibilita, kterou tato knihovna poskytuje, z ní dělá neocenitelný nástroj pro každého, kdo pracuje se soubory PSD. Nyní pokračujte a experimentujte s různými křivkami a nechte svou kreativitu plynout.
## FAQ
### Co je Aspose.PSD?
Aspose.PSD je knihovna pro zpracování souborů Photoshop PSD v různých programovacích jazycích, včetně Javy.
### Mohu používat Aspose.PSD zdarma?
 Ano, Aspose nabízí bezplatnou zkušební verzi, kterou si můžete před nákupem prozkoumat. Zkontrolujte[zkušební verze zdarma ke stažení](https://releases.aspose.com/) odkaz.
### Je nutné mít nainstalovaný Photoshop?
Ne, pro práci s Aspose.PSD nepotřebujete na svém počítači nainstalovaný Photoshop.
### Mohu manipulovat s jinými vrstvami než s vrstvami úprav křivek?
Absolutně! Aspose.PSD umožňuje manipulaci s různými typy vrstev v souborech PSD.
### Kde najdu další dokumentaci?
 Pro podrobnou dokumentaci navštivte[Aspose.PSD pro dokumenty Java](https://reference.aspose.com/psd/java/).