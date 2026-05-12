---
date: 2026-02-22
description: Naučte se, jak vytvořit vektorovou masku v Javě pomocí Aspose.PSD pro
  Javu, přidat vektorovou masku do PSD a programově manipulovat se zdroji Vmsk.
linktitle: Create Vector Mask Java – Vmsk Resource in PSD Files
second_title: Aspose.PSD Java API
title: Vytvořit vektorovou masku v Javě – Vmsk zdroj v souborech PSD
url: /cs/java/advanced-psd-layer-features-effects/support-vmsk-resource-psd-files/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Vytvoření vektorové masky Java – Vmsk zdroj v souborech PSD

## Úvod
Pokud potřebujete **create vector mask** (Vmsk) zdroje uvnitř souborů Photoshop (PSD), Aspose.PSD pro Java vám poskytuje čistý programový způsob, jak to provést. Ať už budujete nástroj pro automatizaci designu nebo přidáváte podporu vlastních masek do existující grafické pipeline, tento tutoriál vás provede každým krokem – načtením PSD, čtením Vmsk zdroje, úpravou jeho vlastností a uložením výsledku. Na konci budete pohodlně pracovat s vektorovými maskami, převádět PSD na PNG a rozšiřovat soubor o další vektorová data – vše pomocí technik **create vector mask java**.

## Rychlé odpovědi
- **Co je Vmsk zdroj?** Jedná se o data vektorové masky uložená uvnitř souboru PSD, definující komplexní vektorové tvary pro vrstvu.  
- **Která knihovna to podporuje?** Aspose.PSD pro Java poskytuje plný přístup ke čtení/zápisu Vmsk zdrojů.  
- **Potřebuji licenci?** K dispozici je bezplatná zkušební verze; pro produkční použití je vyžadována komerční licence.  
- **Mohu upravený PSD převést na PNG?** Ano – po uložení můžete načíst PSD a exportovat do PNG pomocí stejného API.  
- **Je k dispozici podpora Maven?** Rozhodně; Aspose.PSD lze přidat jako Maven závislost (viz klíčové slovo “aspose psd maven”).

## Co je vektorová maska (Vmsk zdroj)?
Vektorová maska (Vmsk) je maska nezávislá na pixelech, která používá Bézierovy křivky a záznamy cest k definování průhledných a neprůhledných oblastí na vrstvě. Protože je vektorová, mění velikost bez ztráty kvality – ideální pro grafiku ve vysokém rozlišení.

## Proč vytvořit vektorovou masku pomocí Aspose.PSD?
- **Automatizace:** Programově přidávat nebo upravovat masky bez otevírání Photoshopu.  
- **Konzistence:** Zajistit, že každý generovaný PSD dodržuje stejné maskové pravidla.  
- **Cross‑platform:** Funguje na jakémkoli OS, který podporuje Javu.  
- **Integrace:** Kombinovat s dalšími Aspose API (např. převod PSD → PNG) pro end‑to‑end workflow.  
- **Škálovatelnost:** Vektorové masky zůstávají ostré při jakékoli velikosti, což je činí ideálními pro responzivní designy.

## Proč je to důležité pro vývojáře Java
Používání technik **create vector mask java** vám umožní vložit pokročilou grafickou logiku přímo do back‑end služeb, CI pipeline nebo desktopových utilit. Už nebudete potřebovat designéra k ručnímu přidávání masek; váš kód může masky generovat nebo upravovat za běhu, čímž ušetří čas a sníží lidské chyby.

## Předpoklady
Než se ponoříme do kódu, ujistěte se, že máte následující:

### Co potřebujete
- Java Development Kit (JDK): Ujistěte se, že máte nainstalovaný JDK na svém počítači. Pokud ne, můžete jej stáhnout z [Oracle webu](https://www.oracle.com/java/technologies/javase-downloads.html).
- Aspose.PSD pro Java knihovna: Jedná se o výkonnou knihovnu pro správu souborů PSD. Můžete ji stáhnout ze [stránky vydání Aspose](https://releases.aspose.com/psd/java/). Pro ty, kteří chtějí vyzkoušet před koupí, můžete také začít s [bezplatnou zkušební verzí](https://releases.aspose.com/).
- IDE: Jakékoli IDE pro Javu (např. IntelliJ IDEA, Eclipse atd.) bude pro tento projekt fungovat.

### Nastavení pracovního prostoru
1. **Vytvořte nový Java projekt** – Otevřete své preferované IDE a založte nový projekt.  
2. **Přidejte knihovnu Aspose** – Po stažení Aspose JAR ji přidejte do cesty sestavení vašeho projektu, aby byly dostupné všechny třídy související s PSD.

S připraveným prostředím přejděme k vlastní implementaci.

## Jak vytvořit vektorovou masku v souborech PSD pomocí Javy
Níže je průvodce krok za krokem. Kódové bloky zůstávají nezměněny oproti originálnímu tutoriálu; pouze jsme přidali vysvětlující text, aby byl každý krok naprosto jasný.

### Import balíčků
Před tím, než budeme pracovat se soubory PSD, musíme importovat potřebné třídy z knihovny Aspose.PSD.

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

### Krok 1: Načtěte svůj PSD soubor
První věc, kterou chcete udělat, je načíst svůj PSD soubor. Zde začíná veškerá magie.

```java
String dataDir = "Your Document Directory"; // Update this path
String sourceFileName = dataDir + "Rectangle.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

- Nastavujeme `dataDir` na adresář vašeho PSD souboru.  
- Vytváříme řetězec pro `sourceFileName`, který kombinuje adresář s názvem PSD souboru.  
- Nakonec načteme PSD soubor do objektu `PsdImage` pomocí `Image.load()`.

### Krok 2: Získejte Vmsk zdroj
Teď, když máme načtený PSD obrázek, načteme Vmsk zdroj.

```java
VmskResource resource = getVmskResource(im);
```

- Voláme metodu `getVmskResource()`, která provádí vyhledávání a získání Vmsk zdroje z obrázku.

### Krok 3: Ověřte vlastnosti Vmsk zdroje
Než budeme pokračovat s úpravami, je důležité ověřit, že náš Vmsk zdroj je ve očekávaném stavu.

```java
if (resource.isDisabled() != false ||
	resource.isInverted() != false ||
	resource.isNotLinked() != false ||
	resource.getPaths().length != 7) {
	throw new RuntimeException("VmskResource was read wrong");
}
```

- Zde kontrolujeme různé vlastnosti Vmsk zdroje. Chceme se ujistit, že není zakázán, invertován ani nepropojen, a že má správný počet cest.

### Krok 4: Přístup k jednotlivým cestám a ověření
Podívejme se trochu hlouběji a prozkoumejme cesty uvnitř Vmsk zdroje.

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

### Krok 5: Upravit Vmsk zdroj
Nyní přecházíme k části úprav! Můžete podle potřeby upravit vlastnosti Vmsk zdroje.

```java
resource.setDisabled(true);
resource.setInverted(true);
resource.setNotLinked(true);
```

- V tomto bloku přepínáme různé vlastnosti Vmsk zdroje. Nastavením na `true` můžeme ovládat, jak maska funguje v PSD souboru.

### Krok 6: Upravit body Bézierových uzlů
Bezierovy uzly jsou klíčové pro vektorové cesty. Změníme zde některé hodnoty.

```java
BezierKnotRecord bezierKnot = (BezierKnotRecord) resource.getPaths()[3];
bezierKnot.getPoints()[0] = new Point(0, 0);
bezierKnot = (BezierKnotRecord) resource.getPaths()[4];
bezierKnot.getPoints()[0] = new Point(8039797, 10905190);
```

- Přistupujeme k konkrétním cestám `BezierKnotRecord` a měníme jejich body, abychom případně přetvořili vektorovou masku.

### Krok 7: Uložit upravený PSD soubor
Jakmile jsou všechny úpravy dokončeny, je čas uložit upravený PSD soubor.

```java
String exportPath = dataDir + "Rectangle_changed.psd";
im.save(exportPath);
```

- Nastavíme cestu pro exportovaný PSD soubor a poté zavoláme `im.save()`, aby se změny zapsaly do nového souboru.

### Krok 8: Vyčistit zdroje
Nakonec musíme zajistit, že správně uvolníme obrázek, aby se uvolnily zdroje.

```java
im.dispose();
```

- Vždy je dobré po dokončení uvolnit všechny zdroje. Pomáhá to předcházet únikům paměti ve vašich aplikacích.

## Časté problémy a řešení
| Problém | Proč se vyskytuje | Jak opravit |
|---------|-------------------|-------------|
| **`VmskResource` not found** | PSD neobsahuje vrstvu s vektorovou maskou. | Ověřte, že zdrojový PSD má vektorovou masku, nebo ji přidejte ručně ve Photoshopu před spuštěním kódu. |
| **`ArrayIndexOutOfBoundsException` při přístupu k cestě** | Očekávaný počet záznamů cest se liší. | Prozkoumejte `resource.getPaths().length` a podle toho upravte použití indexů. |
| **License exception** | Spuštění bez platné licence Aspose.PSD. | Použijte zkušební nebo zakoupenou licenci pomocí `License license = new License(); license.setLicense("Aspose.PSD.lic");`. |
| **Memory leak** | Obrázek není uvolněn v dlouho běžících procesech. | Vždy zavolejte `im.dispose()` v `finally` bloku nebo použijte try‑with‑resources, pokud je podporováno. |

## Často kladené otázky

**Q: Jak přidám novou vektorovou masku k existující vrstvě?**  
A: Vytvořte `VmskResource`, naplňte jej požadovanými záznamy cest (např. `BezierKnotRecord`) a připojte jej ke kolekci zdrojů vrstvy.

**Q: Můžu upravený PSD přímo převést na PNG bez otevření Photoshopu?**  
A: Ano – po uložení PSD jej znovu načtěte pomocí `Image.load()` a zavolejte `im.save("output.png")` s určením formátu PNG.

**Q: Existuje způsob, jak to automatizovat v CI/CD pipeline?**  
A: Rozhodně. Protože proces je čistě v Javě, můžete jej vložit do Maven/Gradle buildů, Docker kontejnerů nebo jakéhokoli CI systému, který podporuje Javu.

**Q: Které verze Aspose.PSD jsou kompatibilní s Java 11+?**  
A: Všechny nedávné vydání (2024‑2025) podporují Java 8 a vyšší, včetně Java 11, 17 a novějších LTS verzí.

**Q: Potřebuji licenci pro vývojové sestavení?**  
A: Bezplatná evaluační licence funguje pro vývoj a testování. Pro produkční nasazení je vyžadována komerční licence.

---

**Poslední aktualizace:** 2026-02-22  
**Testováno s:** Aspose.PSD 24.11 for Java  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}