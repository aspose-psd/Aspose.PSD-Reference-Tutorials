---
date: 2025-12-18
description: Naučte se, jak vytvořit vektorovou masku (zdroj Vmsk) v souborech PSD
  pomocí Aspose.PSD pro Javu. Tento krok‑za‑krokem návod vám ukáže, jak přidat vektorovou
  masku, převést PSD na PNG a další.
linktitle: Create Vector Mask (Vmsk Resource) in PSD Files with Java
second_title: Aspose.PSD Java API
title: Vytvořit vektorovou masku (zdroj Vmsk) v souborech PSD pomocí Javy
url: /cs/java/advanced-psd-layer-features-effects/support-vmsk-resource-psd-files/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Vytvoření vektorové masky (Vmsk Resource) v souborech PSD pomocí Javy

## Úvod
Pokud potřebujete **vytvořit vektorovou masku** (Vmsk) v souborech Photoshop (PSD), Aspose.PSD pro Javu vám poskytuje čistý programový způsob, jak to provést. Ať už budujete nástroj pro automatizaci designu nebo přidáváte podporu vlastních masek do existující grafické pipeline, tento tutoriál vás provede každým krokem – načtením PSD, načtením Vmsk resource, úpravou jejích vlastností a uložením výsledku. Na konci budete pohodlně pracovat s vektorovými maskami, převádět PSD na PNG a rozšiřovat soubor o další vektorová data.

## Rychlé odpovědi
- **Co je Vmsk resource?** Jedná se o data vektorové masky uložená uvnitř souboru PSD, definující komplexní vektorové tvary pro vrstvu.  
- **Která knihovna to podporuje?** Aspose.PSD pro Javu poskytuje plný přístup čtení/zápisu k Vmsk resource.  
- **Potřebuji licenci?** K dispozici je bezplatná zkušební verze; pro produkční použití je vyžadována komerční licence.  
- **Mohu upravený PSD převést na PNG?** Ano – po uložení můžete načíst PSD a exportovat do PNG pomocí stejného API.  
- **Je k dispozici podpora Maven?** Rozhodně; Aspose.PSD lze přidat jako Maven závislost (viz klíčové slovo “aspose psd maven”).

## Co je vektorová maska (Vmsk Resource)?
Vektorová maska (Vmsk) je maska založená na vektorech, která používá Bézierovy křivky a záznamy cest k definování průhledných a neprůhledných oblastí na vrstvě. Protože je vektorová, mění velikost bez ztráty kvality – ideální pro grafiku ve vysokém rozlišení.

## Proč vytvořit vektorovou masku pomocí Aspose.PSD?
- **Automatizace:** Programově přidávat nebo upravovat masky bez otevření Photoshopu.  
- **Konzistence:** Zajistit, aby každý generovaný PSD dodržoval stejné maskové pravidla.  
- **Cross‑platform:** Funguje na jakémkoli OS, který podporuje Javu.  
- **Integrace:** Kombinovat s dalšími Aspose API (např. převod PSD → PNG) pro kompletní workflow.

## Předpoklady
Než se ponoříme do kódu, ujistěte se, že máte následující:

### Co potřebujete
- Java Development Kit (JDK): Ujistěte se, že máte na svém počítači nainstalovaný JDK. Pokud ne, můžete jej stáhnout z [Oracle website](https://www.oracle.com/java/technologies/javase-downloads.html).
- Aspose.PSD pro Java knihovna: Jedná se o výkonnou knihovnu pro správu souborů PSD. Můžete ji stáhnout ze [Aspose release page](https://releases.aspose.com/psd/java/). Pro ty, kteří chtějí vyzkoušet před zakoupením, můžete také začít s [free trial](https://releases.aspose.com/).
- IDE: Jakékoli IDE pro Javu (např. IntelliJ IDEA, Eclipse atd.) bude pro tento projekt fungovat.

### Nastavení pracovního prostoru
1. **Vytvořte nový Java projekt** – Otevřete své preferované IDE a založte nový projekt.  
2. **Přidejte knihovnu Aspose** – Po stažení Aspose JAR ji přidejte do cesty sestavení vašeho projektu, aby byly dostupné všechny třídy související s PSD.

S připraveným prostředím přejděme k samotné implementaci.

## Jak vytvořit vektorovou masku v souborech PSD pomocí Javy
Níže je krok za krokem průvodce. Kódové bloky jsou nezměněny oproti originálnímu tutoriálu; přidali jsme pouze vysvětlující text, aby byl každý krok naprosto jasný.

## Import balíčků
Než budeme moci pracovat se soubory PSD, musíme importovat potřebné třídy z knihovny Aspose.PSD.

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

Nyní, když jsme připravili scénu, projděme si každou operaci.

## Krok 1: Načtěte svůj PSD soubor
První věc, kterou chcete udělat, je načíst svůj PSD soubor. Zde začíná veškerá magie.

```java
String dataDir = "Your Document Directory"; // Update this path
String sourceFileName = dataDir + "Rectangle.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

- Nastavíme `dataDir` na adresář vašeho PSD souboru.  
- Vytvoříme řetězec pro `sourceFileName`, který kombinuje adresář s názvem PSD souboru.  
- Nakonec načteme PSD soubor do objektu `PsdImage` pomocí `Image.load()`.

## Krok 2: Získejte Vmsk resource
Nyní, když máme načtený PSD obrázek, načteme Vmsk resource.

```java
VmskResource resource = getVmskResource(im);
```

- Zavoláme metodu `getVmskResource()`, která provádí vyhledávání a získání Vmsk resource z obrázku.

## Krok 3: Ověřte vlastnosti Vmsk resource
Před pokračováním v úpravách je nutné ověřit, že náš Vmsk resource je v očekávaném stavu.

```java
if (resource.isDisabled() != false ||
	resource.isInverted() != false ||
	resource.isNotLinked() != false ||
	resource.getPaths().length != 7) {
	throw new RuntimeException("VmskResource was read wrong");
}
```

- Zde kontrolujeme různé vlastnosti Vmsk resource. Chceme zajistit, že není zakázán, invertován ani nepropojen, a že má správný počet cest.

## Krok 4: Přístup ke každé cestě a ověření
Ponořme se trochu hlouběji a prozkoumejme cesty uvnitř Vmsk resource.

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

- Extrahujeme tři konkrétní záznamy cest a ověřujeme jejich typy a vlastnosti, aby splňovaly naše kritéria.

## Krok 5: Upravit Vmsk resource
Nyní přicházíme k části úprav! Můžete podle potřeby upravit vlastnosti Vmsk resource.

```java
resource.setDisabled(true);
resource.setInverted(true);
resource.setNotLinked(true);
```

- V tomto bloku přepínáme různé vlastnosti Vmsk resource. Nastavením na `true` můžeme řídit, jak maska funguje v PSD souboru.

## Krok 6: Upravit body Bézierových uzlů
Bézierové uzly jsou klíčové pro vektorové cesty. Změníme zde některé hodnoty.

```java
BezierKnotRecord bezierKnot = (BezierKnotRecord) resource.getPaths()[3];
bezierKnot.getPoints()[0] = new Point(0, 0);
bezierKnot = (BezierKnotRecord) resource.getPaths()[4];
bezierKnot.getPoints()[0] = new Point(8039797, 10905190);
```

- Přistupujeme ke konkrétním `BezierKnotRecord` cestám a měníme jejich body, abychom případně přetvořili vektorovou masku.

## Krok 7: Uložit upravený PSD soubor
Po dokončení všech úprav je čas uložit upravený PSD soubor.

```java
String exportPath = dataDir + "Rectangle_changed.psd";
im.save(exportPath);
```

- Nastavíme cestu pro exportovaný PSD soubor a poté zavoláme `im.save()`, aby se změny zapsaly do nového souboru.

## Krok 8: Vyčistit zdroje
Nakonec musíme zajistit, aby byl obrázek řádně uvolněn a uvolnily se zdroje.

```java
im.dispose();
```

- Vždy je dobré po dokončení uvolnit všechny zdroje. Pomáhá to předcházet únikům paměti ve vašich aplikacích.

## Závěr
Gratulujeme! Právě jste prošli podrobným procesem **vytváření vektorové masky** (Vmsk) v souborech PSD pomocí Aspose.PSD pro Javu. Od načtení obrázku, získání a ověření Vmsk resource, úpravy jejích vlastností až po uložení upraveného PSD, nyní máte pevný základ pro automatizaci workflow vektorových masek. Použijte tyto techniky k obohacení vašich designových pipeline, integraci s dalšími Aspose API (např. převod PSD na PNG) nebo k vytvoření vlastních grafických nástrojů.

## Často kladené otázky
**Q: Jak přidám novou vektorovou masku k existující vrstvě?**  
A: Vytvořte `VmskResource`, naplňte jej požadovanými záznamy cest (např. `BezierKnotRecord`) a připojte jej ke kolekci zdrojů vrstvy.

**Q: Mohu upravený PSD přímo převést na PNG bez otevření Photoshopu?**  
A: Ano – po uložení PSD jej znovu načtěte pomocí `Image.load()` a zavolejte `im.save("output.png")` s určením formátu PNG.

**Q: Existuje způsob, jak to automatizovat v CI/CD pipeline?**  
A: Rozhodně. Protože proces je čistě v Javě, můžete jej vložit do Maven/Gradle buildů, Docker kontejnerů nebo jakéhokoli CI systému podporujícího Javu.

**Q: Jaké verze Aspose.PSD jsou kompatibilní s Java 11+?**  
A: Všechny nedávné verze (2024‑2025) podporují Java 8 a vyšší, včetně Java 11, 17 a novějších LTS verzí.

**Q: Potřebuji licenci pro vývojové sestavení?**  
A: Bezplatná evaluační licence funguje pro vývoj a testování. Pro produkční nasazení je vyžadována komerční licence.

---

**Poslední aktualizace:** 2025-12-18  
**Testováno s:** Aspose.PSD 24.11 for Java  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
