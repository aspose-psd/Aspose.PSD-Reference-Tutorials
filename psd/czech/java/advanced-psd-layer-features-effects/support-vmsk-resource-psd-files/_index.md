---
title: Podpora Vmsk Resource v souborech PSD s Java
linktitle: Podpora Vmsk Resource v souborech PSD s Java
second_title: Aspose.PSD Java API
description: Bez námahy spravujte prostředky Vmsk v souborech PSD pomocí Aspose.PSD for Java. Komplexní výukový program krok za krokem ideální pro vývojáře i designéry.
type: docs
weight: 23
url: /cs/java/advanced-psd-layer-features-effects/support-vmsk-resource-psd-files/
---
## Zavedení
Pokud jde o práci se soubory PSD (Photoshop Document), správa zdrojů je zásadní, zejména při integraci speciálních funkcí, jako je zdroj Vmsk (vektorová maska). Zdroje Vmsk mohou návrhářům pomoci přidáním složitých vektorových tvarů, což jim umožní bez námahy vytvářet úžasnou grafiku. V této příručce se podíváme na praktický přístup, abychom vám ukázali, jak podporovat prostředky Vmsk v souborech PSD pomocí Aspose.PSD for Java. Ať už jste vývojář, který chce vylepšit svou aplikaci, nebo návrhář, který hledá automatizaci, tento výukový program vás provede procesem krok za krokem, takže jej budete snadno sledovat a implementovat.
## Předpoklady
Než se ponoříme do šťavnatých detailů zacházení se zdroji Vmsk, ujistěte se, že máte vše připraveno pro bezproblémový zážitek.
### Co potřebujete
-  Java Development Kit (JDK): Ujistěte se, že máte na svém počítači nainstalovaný JDK. Pokud ne, můžete si jej stáhnout z[Web společnosti Oracle](https://www.oracle.com/java/technologies/javase-downloads.html).
- Aspose.PSD for Java Library: Toto je výkonná knihovna pro správu souborů PSD. Můžete si jej stáhnout z[Aspose release page](https://releases.aspose.com/psd/java/) . Pro ty, kteří chtějí před nákupem vyzkoušet, můžete také začít s[zkušební verze zdarma](https://releases.aspose.com/).
- IDE: Pro tento projekt bude fungovat jakékoli IDE pro Javu (jako IntelliJ IDEA, Eclipse atd.).
### Nastavení vašeho pracovního prostoru
1. Vytvoření nového projektu Java: Spusťte preferované IDE a vytvořte nový projekt Java. Toto je vaše hřiště pro práci s kódem.
2. Přidejte knihovnu Aspose: Po stažení knihovny Aspose přidejte soubor jar do knihoven svého projektu. Tento krok je zásadní, protože nám umožňuje využít všechny ty sladké funkce Aspose.PSD.
S těmito předpoklady jste připraveni začít vytvářet, upravovat a spravovat soubory PSD pomocí prostředků Vmsk. Pojďme rovnou do programování!
## Importujte balíčky
Než budeme moci pracovat na souborech PSD, musíme naimportovat potřebné balíčky. Toto je páteř našeho kódu, která nám umožňuje přístup k různým třídám a metodám, které knihovna Aspose.PSD nabízí.
```java
import com.aspose.psd.Image;
import com.aspose.psd.Point;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.fileformats.psd.layers.LayerResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.VmskResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.BezierKnotRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.InitialFillRuleRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.LengthRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.PathFillRuleRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathType;
```
Nyní, když jsme připravili půdu, je čas na akci! V této části rozdělíme kód do zvládnutelných kroků. Tyto kroky vás provedou čtením souboru PSD, zpracováním prostředku Vmsk a dokonce jeho úpravou.
## Krok 1: Načtěte soubor PSD
První věc, kterou chcete udělat, je načíst soubor PSD. Tady začíná veškerá magie.
```java
String dataDir = "Your Document Directory"; // Aktualizujte tuto cestu
String sourceFileName = dataDir + "Rectangle.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

-  Nastavili jsme`dataDir` do adresáře vašeho PSD souboru. 
-  Vytvoříme řetězec pro`sourceFileName`, který kombinuje adresář s názvem souboru PSD.
-  Nakonec načteme soubor PSD do a`PsdImage` pomocí objektu`Image.load()`.
## Krok 2: Načtěte prostředek Vmsk
Nyní, když máme načtený náš PSD obraz, pojďme načíst prostředek Vmsk.
```java
VmskResource resource = getVmskResource(im);
```

-  Zavoláme na`getVmskResource()` metoda, která zpracovává vyhledávání a načítání prostředku Vmsk z obrázku.
## Krok 3: Ověřte vlastnosti prostředku Vmsk
Než budete pokračovat v úpravách, je nezbytné ověřit, zda je náš zdroj Vmsk v očekávaném stavu.
```java
if (resource.isDisabled() != false ||
	resource.isInverted() != false ||
	resource.isNotLinked() != false ||
	resource.getPaths().length != 7) {
	throw new RuntimeException("VmskResource was read wrong");
}
```

- Zde kontrolujeme různé vlastnosti prostředku Vmsk. Chceme zajistit, aby nebyl deaktivován, převrácen nebo nepropojen a aby měl správný počet cest.
## Krok 4: Přístup ke každé cestě a ověření
Pojďme se ponořit trochu hlouběji a prozkoumat cesty v rámci zdroje Vmsk.
```java
PathFillRuleRecord pathFillRule = (PathFillRuleRecord) resource.getPaths()[0];
InitialFillRuleRecord initialFillRule = (InitialFillRuleRecord) resource.getPaths()[1];
LengthRecord subpathLength = (LengthRecord) resource.getPaths()[2];
if (pathFillRule.getType() != VectorPathType.PathFillRuleRecord ||
	initialFillRule.getType() != VectorPathType.InitialFillRuleRecord ||
	initialFillRule.isFillStartsWithAllPixels() != false ||
	subpathLength.getType() != VectorPathType.ClosedSubpathLengthRecord ||
	subpathLength.isClosed() != true) {
	throw new RuntimeException("VmskResource paths were read wrong");
}
```

- Extrahujeme tři konkrétní záznamy cest a ověřujeme jejich typy a vlastnosti, abychom zajistili, že splňují naše kritéria.
## Krok 5: Upravte zdroj Vmsk
Nyní se dostáváme do části modifikace! Vlastnosti prostředku Vmsk můžete upravit podle potřeby.
```java
resource.setDisabled(true);
resource.setInverted(true);
resource.setNotLinked(true);
```

- V tomto bloku přepínáme různé vlastnosti prostředku Vmsk. Jejich nastavením na hodnotu true můžeme ovládat, jak se maska chová v souboru PSD.
## Krok 6: Upravte body Bezierových uzlů
Bézierovy uzly jsou rozhodující pro vektorové cesty. Pojďme zde změnit některé hodnoty.
```java
BezierKnotRecord bezierKnot = (BezierKnotRecord) resource.getPaths()[3];
bezierKnot.getPoints()[0] = new Point(0, 0);
bezierKnot = (BezierKnotRecord) resource.getPaths()[4];
bezierKnot.getPoints()[0] = new Point(8039797, 10905190);
```

-  Přistupujeme ke konkrétním`BezierKnotRecord` cesty a změnou jejich bodů potenciálně přetvořit vektorovou masku.
## Krok 7: Uložte upravený soubor PSD
Po dokončení všech úprav je čas uložit upravený soubor PSD. 
```java
String exportPath = dataDir + "Rectangle_changed.psd";
im.save(exportPath);
```

-  Nastavíme cestu pro exportovaný soubor PSD a poté zavoláme`im.save()` zapsat změny do tohoto nového souboru.
## Krok 8: Vyčistěte zdroje
Nakonec se musíme ujistit, že obraz řádně zlikvidujeme, abychom uvolnili zdroje.
```java
im.dispose();
```

- Vždy je dobrým zvykem zbavit se všech zdrojů, jakmile skončíte. To pomáhá vyhnout se únikům paměti ve vašich aplikacích.
## Závěr
Gratuluji! Právě jste prošli podrobným procesem podpory zdrojů Vmsk v souborech PSD pomocí Aspose.PSD for Java. Od načtení obrázku, načtení a ověření prostředku Vmsk, úpravy jeho vlastností a následného uložení upraveného PSD jste pokryli základy. S těmito dovednostmi můžete efektivně spravovat a využívat různé zdroje v souborech PSD a vylepšovat tak své projekty grafického designu nebo automatizační skripty.
## FAQ
### Co je zdroj Vmsk?
Prostředek Vmsk je vektorová maska v souboru PSD, která umožňuje složité vektorové tvary a funkce úprav.
### Mohu použít Aspose.PSD v projektu Maven?
Ano, můžete zahrnout Aspose.PSD jako závislost do vašeho projektu Maven pomocí jeho souřadnic z úložiště.
### V jakém formátu mohu uložit své upravené soubory PSD?
Můžete je uložit zpět jako soubory PSD nebo je exportovat do jiných formátů, jako je PNG, JPEG atd.
### Je k dispozici bezplatná zkušební verze pro Aspose.PSD?
 Ano, máte přístup k bezplatné zkušební verzi Aspose.PSD a otestujte její funkce. Navštivte[odkaz na bezplatnou zkušební verzi](https://releases.aspose.com/).
### Jak mohu získat podporu pro Aspose.PSD?
 Můžete se připojit k[Aspose fórum](https://forum.aspose.com/c/psd/34)pro podporu a pomoc při odstraňování problémů.