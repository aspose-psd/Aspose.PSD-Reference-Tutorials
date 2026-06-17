---
date: 2026-06-03
description: Zjistěte, jak převést PSD na PNG a vytvořit vektorovou masku v Java pomocí
  Aspose.PSD for Java, přidat vektorovou masku do PSD a programově manipulovat se
  zdroji Vmsk.
keywords:
- convert psd to png
- add vector mask psd
- psd vector mask tutorial
- aspose psd maven
linktitle: Převod PSD na PNG a vytvoření vektorové masky v Java – Vmsk zdroj v souborech
  PSD
schemas:
- author: Aspose
  dateModified: '2026-06-03'
  description: Learn how to convert PSD to PNG and create vector mask Java using Aspose.PSD
    for Java, add vector mask PSD, and manipulate Vmsk resources programmatically.
  headline: Convert PSD to PNG and Create Vector Mask Java – Vmsk Resource in PSD
    Files
  type: TechArticle
- questions:
  - answer: Create a `VmskResource`, populate it with the required path records (e.g.,
      `BezierKnotRecord`), and attach it to the layer’s resources collection.
    question: How do I add a new vector mask to an existing layer?
  - answer: Yes—after saving the PSD, load it again with `Image.load()` and call `im.save("output.png")`
      specifying the PNG format.
    question: Can I convert the edited PSD directly to PNG without opening Photoshop?
  - answer: Absolutely. Since the process is pure Java, you can embed it in Maven/Gradle
      builds, Docker containers, or any CI system that supports Java.
    question: Is there a way to automate this in a CI/CD pipeline?
  - answer: All recent releases (2024‑2025) support Java 8 and above, including Java
      11, 17, and newer LTS versions.
    question: What versions of Aspose.PSD are compatible with Java 11+?
  - answer: A free evaluation license works for development and testing. For production
      deployments, a commercial license is required.
    question: Do I need a license for development builds?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Převod PSD na PNG a vytvoření vektorové masky v Java – Vmsk zdroj v souborech
  PSD
url: /cs/java/advanced-psd-layer-features-effects/support-vmsk-resource-psd-files/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Převod PSD na PNG a vytvoření vektorové masky Java – Vmsk zdroj v souborech PSD

## Úvod
Pokud potřebujete **convert PSD to PNG** a zároveň **create vector mask** (Vmsk) zdroje uvnitř souborů Photoshopu, Aspose.PSD pro Java vám poskytuje čistý, programový způsob, jak to provést. Ať už budujete nástroj pro automatizaci designu, CI pipeline, který validuje aktiva, nebo rozšiřujete grafický workflow o vlastní masky, tento tutoriál vás provede každým krokem – načtením PSD, čtením Vmsk zdroje, úpravou jeho vlastností, exportem výsledku do PNG a uložením upraveného souboru. Na konci budete pohodlně pracovat s vektorovými maskami, převádět PSD → PNG a rozšiřovat soubor o další vektorová data – vše pomocí technik **convert PSD to PNG**.

## Rychlé odpovědi
- **Co je Vmsk zdroj?** Jedná se o data vektorové masky uložená uvnitř souboru PSD, definující komplexní vektorové tvary pro vrstvu.  
- **Která knihovna to podporuje?** Aspose.PSD pro Java poskytuje plný přístup ke čtení/zápisu Vmsk zdrojů.  
- **Potřebuji licenci?** K dispozici je bezplatná zkušební verze; pro produkční použití je vyžadována komerční licence.  
- **Mohu upravený PSD převést na PNG?** Ano – po uložení můžete PSD načíst a exportovat do PNG pomocí stejného API.  
- **Je podpora Maven k dispozici?** Rozhodně; Aspose.PSD lze přidat jako Maven závislost (viz klíčové slovo „aspose psd maven“).

## Co je vektorová maska (Vmsk zdroj)?
Vektorová maska (Vmsk) je maska ne‑pixelová, která používá Bézierovy křivky a záznamy cest k definování průhledných a neprůhledných oblastí na vrstvě. Protože je vektorová, škáluje se bez ztráty kvality – ideální pro grafiku ve vysokém rozlišení. Může obsahovat více cest, z nichž každá se skládá z Bézierových uzlů, a podporuje atributy masky jako neprůhlednost, výplň a propojení s maskami vrstev.

## Proč vytvořit vektorovou masku pomocí Aspose.PSD?
Programové vytváření vektorových masek eliminuje potřebu ruční úpravy ve Photoshopu, zajišťuje konzistenci napříč velkými dávkami souborů a umožňuje integraci do automatizovaných build nebo deployment pipeline. S Aspose.PSD můžete generovat přesnou geometrii masky, aplikovat ji na libovolnou vrstvu a zachovat plnou editovatelnost, což je nezbytné pro dynamické generování grafiky a workflow responzivního designu.

- **Automatizace:** Programově přidávejte nebo upravujte masky bez otevírání Photoshopu.  
- **Konzistence:** Zajistěte, aby každý vygenerovaný PSD dodržoval stejné maskové pravidla.  
- **Cross‑platform:** Funguje na jakémkoli OS, který podporuje Java.  
- **Integrace:** Kombinujte s dalšími Aspose API (např. convert PSD → PNG) pro end‑to‑end workflow.  
- **Škálovatelnost:** Vektorové masky zůstávají ostré při jakékoli velikosti, což je ideální pro responzivní designy.

## Proč je to důležité pro vývojáře Java
Používání technik **create vector mask java** vám umožní vložit sofistikovanou grafickou logiku přímo do backendových služeb, CI pipeline nebo desktopových utilit. Už nepotřebujete designéra, který ručně přidává masky; váš kód může masky generovat nebo upravovat za běhu, šetří čas a snižuje lidské chyby.

## Předpoklady
Než se ponoříme do kódu, ujistěte se, že máte následující:

### Co potřebujete
- **Java Development Kit (JDK):** Nainstalujte JDK 8 nebo novější. Můžete jej stáhnout z [Oracle website](https://www.oracle.com/java/technologies/javase-downloads.html).  
- **Aspose.PSD for Java Library:** Tato výkonná knihovna spravuje PSD soubory. Stáhněte ji ze [Aspose release page](https://releases.aspose.com/psd/java/). Pro rychlý start si stáhněte bezplatnou zkušební verzi ze stejné stránky nebo z [free trial](https://releases.aspose.com/).  
- **IDE:** Jakékoli Java IDE (IntelliJ IDEA, Eclipse, NetBeans) bude fungovat.

### Nastavení pracovního prostoru
1. **Vytvořte nový Java projekt** – Otevřete preferované IDE a založte nový projekt.  
2. **Přidejte Aspose knihovnu** – Po stažení Aspose JAR souboru jej přidejte do cesty sestavení projektu, aby byly k dispozici všechny třídy související s PSD.

S připraveným prostředím projděme skutečnou implementaci.

## Jak převést PSD na PNG pomocí Aspose.PSD pro Java?
Načtěte svůj zdrojový PSD pomocí `PsdImage.load()`, volitelně upravte jeho vektorovou masku a poté zavolejte `save()` s parametrem `ExportFormat.Png`. Aspose.PSD automaticky zpracuje všechny barevné profily, vrstvy a data masky a vytvoří pixel‑perfektní PNG, který odpovídá původnímu vizuálnímu vzhledu. Tento dvoukrokový tok funguje pro jakýkoli PSD, bez ohledu na velikost, a běží na jakékoli platformě kompatibilní s Java.

## Import balíčků
Balíček `com.aspose.psd` poskytuje základní třídy pro práci se soubory PSD, včetně načítání obrázků, manipulace se zdroji a exportních možností.

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

Nyní, když jsme připravili scénu, projděme jednotlivé operace.

## Krok 1: Načtěte svůj PSD soubor
Načtení souboru vám poskytne objekt `PsdImage`, který představuje celý dokument v paměti.

```java
String dataDir = "Your Document Directory"; // Update this path
String sourceFileName = dataDir + "Rectangle.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

- Nastavíme `dataDir` na adresář vašeho PSD souboru.  
- Vytvoříme řetězec pro `sourceFileName`, který kombinuje adresář s názvem PSD souboru.  
- Nakonec načteme PSD soubor do objektu `PsdImage` pomocí `Image.load()`.

## Krok 2: Získejte Vmsk zdroj
Třída `VmskResource` zapouzdřuje data vektorové masky uložená uvnitř vrstvy PSD. Získání jí vám umožní prohlížet nebo upravovat cesty masky.

```java
VmskResource resource = getVmskResource(im);
```

- Voláme metodu `getVmskResource()`, která vyhledá a načte Vmsk zdroj z obrázku.

## Krok 3: Ověřte vlastnosti Vmsk zdroje
Před provedením změn ověřte, že maska je povolena, správně orientována a obsahuje očekávaný počet cest.

```java
if (resource.isDisabled() != false ||
	resource.isInverted() != false ||
	resource.isNotLinked() != false ||
	resource.getPaths().length != 7) {
	throw new RuntimeException("VmskResource was read wrong");
}
```

- Zde kontrolujeme různé vlastnosti Vmsk zdroje. Chceme se ujistit, že není zakázána, invertovaná ani nepropojená a že má správný počet cest.

## Krok 4: Přístup ke každé cestě a ověření
Každý záznam cesty popisuje část vektorového tvaru. Kontrola jejich správnosti zajišťuje, že pracujete s požadovanou geometrií.

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

## Krok 5: Upravit Vmsk zdroj
Nyní přecházíme k úpravě! Můžete přepínat příznaky chování masky podle potřeby vašeho workflow.

```java
resource.setDisabled(true);
resource.setInverted(true);
resource.setNotLinked(true);
```

- V tomto bloku přepínáme různé vlastnosti Vmsk zdroje. Nastavením na `true` můžeme řídit, jak se maska chová v souboru PSD.

## Krok 6: Upravit body Bézierových uzlů
Bézierovy uzly definují zakřivení každého vektorového segmentu. Úpravou jejich bodů můžete přetvořit masku bez rasterizace.

```java
BezierKnotRecord bezierKnot = (BezierKnotRecord) resource.getPaths()[3];
bezierKnot.getPoints()[0] = new Point(0, 0);
bezierKnot = (BezierKnotRecord) resource.getPaths()[4];
bezierKnot.getPoints()[0] = new Point(8039797, 10905190);
```

- Přistupujeme ke konkrétním `BezierKnotRecord` cestám a měníme jejich body, abychom potenciálně přetvořili vektorovou masku.

## Krok 7: Uložit upravený PSD soubor
Po dokončení všech úprav uložte změny do nového PSD souboru.

```java
String exportPath = dataDir + "Rectangle_changed.psd";
im.save(exportPath);
```

- Nastavíme cestu pro exportovaný PSD soubor a poté zavoláme `im.save()` k zápisu změn do tohoto nového souboru.

## Krok 8: Exportovat PSD jako PNG
Nyní, když PSD obsahuje aktualizovanou masku, exportujte jej přímo do PNG. Tento krok demonstruje workflow **convert PSD to PNG**.

```java
im.dispose();
```

- Použijte `im.save("output.png", ExportFormat.Png)` k vytvoření vysoce kvalitního PNG, který odráží upravenou vektorovou masku.

## Vyčištění zdrojů
Nakonec musíme zajistit, že obrázek řádně uvolníme, aby se uvolnily prostředky.

CODE_BLOCK_PLACEHOLDER_9_END

- Vždy je dobré po dokončení uvolnit všechny zdroje. Pomáhá to předcházet únikům paměti ve vašich aplikacích.

## Časté problémy a řešení
| Problém | Proč se stane | Jak opravit |
|---------|----------------|-------------|
| **`VmskResource` not found** | PSD neobsahuje vrstvu s vektorovou maskou. | Ověřte, že zdrojový PSD má vektorovou masku, nebo ji přidejte ručně ve Photoshopu před spuštěním kódu. |
| **`ArrayIndexOutOfBoundsException` on path access** | Počet očekávaných záznamů cest se liší. | Prozkoumejte `resource.getPaths().length` a podle toho upravte indexy. |
| **License exception** | Spuštění bez platné Aspose.PSD licence. | Použijte zkušební nebo zakoupenou licenci pomocí `License license = new License(); license.setLicense("Aspose.PSD.lic");`. |
| **Memory leak** | Obrázek není uvolněn v dlouho běžících procesech. | Vždy zavolejte `im.dispose()` v `finally` bloku nebo použijte try‑with‑resources, pokud je podporováno. |

## Často kladené otázky

**Q: Jak přidám novou vektorovou masku k existující vrstvě?**  
A: Vytvořte `VmskResource`, naplňte jej požadovanými záznamy cest (např. `BezierKnotRecord`) a připojte jej ke kolekci zdrojů vrstvy.

**Q: Mohu upravený PSD přímo převést na PNG bez otevírání Photoshopu?**  
A: Ano – po uložení PSD jej znovu načtěte pomocí `Image.load()` a zavolejte `im.save("output.png")` s určením formátu PNG.

**Q: Existuje způsob, jak to automatizovat v CI/CD pipeline?**  
A: Rozhodně. Protože proces je čistě v Javě, můžete jej začlenit do Maven/Gradle buildů, Docker kontejnerů nebo jakéhokoli CI systému podporujícího Java.

**Q: Jaké verze Aspose.PSD jsou kompatibilní s Java 11+?**  
A: Všechny nedávné verze (2024‑2025) podporují Java 8 a vyšší, včetně Java 11, 17 a novějších LTS verzí.

**Q: Potřebuji licenci pro vývojové buildy?**  
A: Bezplatná evaluační licence funguje pro vývoj a testování. Pro produkční nasazení je vyžadována komerční licence.

**Last Updated:** 2026-06-03  
**Tested With:** Aspose.PSD 24.11 for Java  
**Author:** Aspose

## Související tutoriály

- [Export PSD to PNG with Layer Mask Support in Java](/psd/java/advanced-psd-layer-features-effects/support-layer-mask-psd-files/)
- [How to Convert PSD to PNG and Resize Proportionally with Aspose.PSD for Java](/psd/java/advanced-image-manipulation/resize-image-proportionally/)
- [Convert PSD to PNG with Color Overlay – Aspose.PSD for Java](/psd/java/advanced-image-manipulation/rendering-color-effect/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}