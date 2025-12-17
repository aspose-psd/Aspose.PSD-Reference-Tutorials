---
date: 2025-12-17
description: Naučte se, jak upravovat vektorové tvary PSD podporou vlastností datových
  záznamů délky pomocí Aspose.PSD pro Javu. Praktický průvodce krok za krokem s ukázkami
  kódu.
linktitle: Support Length Record Data Properties in PSD - Java
second_title: Aspose.PSD Java API
title: Jak upravit vektorové tvary PSD – podpora vlastností dat záznamu délky v Javě
url: /cs/java/advanced-psd-layer-features-effects/support-length-record-data-properties-psd/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Podpora vlastností datových záznamů délky v PSD - Java

## Úvod
Pokud potřebujete **programově upravovat vektorové tvary v PSD**, knihovna Aspose.PSD pro Java vám poskytne plnou kontrolu nad soubory Photoshopu přímo z vašeho Java kódu. V tomto tutoriálu projdeme vše, co potřebujete vědět k podpoře vlastností datových záznamů délky — nezbytný krok, když chcete editovat vrstvy s vektorovými tvary. Na konci budete schopni otevřít PSD, upravit jeho vlastnosti vektorových tvarů a uložit aktualizovaný soubor, aniž byste opustili své IDE. Pojďme na to!

## Rychlé odpovědi
- **Co znamená „modify PSD vector shapes“?** Úprava geometrie, operací cesty nebo jiných vlastností vrstev založených na vektorech uvnitř souboru PSD.  
- **Která knihovna to řeší?** Aspose.PSD pro Java.  
- **Potřebuji licenci?** Bezplatná zkušební verze stačí pro hodnocení; pro produkční nasazení je vyžadována komerční licence.  
- **Jak dlouho trvá implementace?** Přibližně 10‑15 minut pro základní skript úpravy tvarů.  
- **Jaké jsou hlavní předpoklady?** Java JDK, Aspose.PSD pro Java a ukázkový soubor PSD.

## Co znamená „modify PSD vector shapes“?
Úprava vektorových tvarů v PSD zahrnuje změnu podkladových dat vektorové cesty — například záznamů délky a operací cesty — tak, aby se vizuální vzhled tvarů podle toho aktualizoval. To je zvláště užitečné pro automatizované grafické pipeline, dávkové zpracování nebo vlastní nástroje pro design.

## Proč použít Aspose.PSD pro Java k úpravě vektorových tvarů v PSD?
- **Bez Photoshopu** — práce přímo se soubory PSD na jakémkoli serveru.  
- **Bohaté API** — přístup k vrstvám, zdrojům a vektorovým datům pomocí silně typovaných tříd.  
- **Cross‑platform** — běží na Windows, Linuxu i macOS s libovolným JDK.  
- **Výkonnostně orientované** — efektivní správa paměti a rychlé ukládání.

## Požadavky
1. **Java Development Kit (JDK)** — stáhněte z [Oracle's website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) nebo použijte svůj oblíbený správce balíčků.  
2. **Aspose.PSD pro Java** — získejte nejnovější JAR ze [Aspose releases page](https://releases.aspose.com/psd/java/).  
3. **IDE** — IntelliJ IDEA, Eclipse nebo jakýkoli editor kompatibilní s Javou.  
4. **Soubor PSD** — vytvořte jej v Photoshopu nebo si pořiďte ukázkový PSD pro experimentování.  
5. **Základní znalost Javy** — znalost tříd, objektů a zpracování výjimek.

## Import balíčků
Nejprve importujte třídy, které budete potřebovat pro práci se soubory PSD a zdroji vektorových tvarů.

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.LayerResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.VsmsResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.LengthRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.PathOperations;
```

## Krok 1: Nastavte své vstupní a výstupní adresáře
Definujte, kde se nachází původní PSD a kam chcete uložit upravený soubor.

```java
String sourceDir = "Your Source Directory";
String outputDir = "Your Document Directory";
String inPsdFilePath = sourceDir + "PathOperationsShape.psd";
String outPsdFilePath = outputDir + "out_PathOperationsShape.psd";
```

## Krok 2: Načtěte soubor PSD
Použijte `Image.load` k otevření souboru a přetypujte jej na `PsdImage` pro funkce specifické pro PSD.

```java
PsdImage psdImage = (PsdImage) Image.load(inPsdFilePath);
```

## Krok 3: Najděte zdroj Vsms ve vrstvě
Data vektorových tvarů jsou uložena uvnitř `VsmsResource`. Projděte prostředky druhé vrstvy a najděte jej.

```java
VsmsResource resource = null;
for (LayerResource layerResource : psdImage.getLayers()[1].getResources()) {
    if (layerResource instanceof VsmsResource) {
        resource = (VsmsResource) layerResource;
        break;
    }
}
```

## Krok 4: Přístup k záznamům délky
Každý `LengthRecord` představuje samostatnou vektorovou cestu. Získejte ty, které chcete upravit.

```java
LengthRecord lengthRecord0 = (LengthRecord) resource.getPaths()[2];
LengthRecord lengthRecord1 = (LengthRecord) resource.getPaths()[7];
LengthRecord lengthRecord2 = (LengthRecord) resource.getPaths()[11];
```

## Krok 5: Úprava vlastností operací cesty
Nyní můžete **upravit vektorové tvary v PSD** změnou jejich `PathOperations`. To určuje, jak se tvary navzájem ovlivňují (např. vyloučení, průnik, odečtení).

```java
lengthRecord0.setPathOperations(PathOperations.ExcludeOverlappingShapes);
lengthRecord1.setPathOperations(PathOperations.IntersectShapeAreas);
lengthRecord2.setPathOperations(PathOperations.SubtractFrontShape);
```

## Krok 6: Uložte upravený soubor PSD
Uložte své změny do nového souboru.

```java
psdImage.save(outPsdFilePath);
```

## Krok 7: Vyčistěte zdroje
Uvolněte `PsdImage`, aby se uvolnila paměť.

```java
psdImage.dispose();
```

## Časté úskalí a tipy
- **Kontrola null** — vždy ověřte, že `resource` není `null`, než začnete přistupovat k cestám.  
- **Rozsahy indexů cesty** — ujistěte se, že použité indexy (`[2]`, `[7]`, `[11]`) existují v konkrétním PSD, který upravujete.  
- **Licence** — běh bez platné licence vloží vodoznak do uloženého PSD.

## Závěr
Nyní máte kompletní příklad od začátku do konce, jak **upravit vektorové tvary v PSD** podporou vlastností datových záznamů délky pomocí Aspose.PSD pro Java. Ať už automatizujete pipeline aktiv nebo budujete vlastní nástroj pro design, tato API vám poskytují flexibilitu manipulovat s vektorovými vrstvami bez ruční práce ve Photoshopu. Prozkoumejte dál experimentováním s dalšími `PathOperations` nebo kombinací úprav více `LengthRecord` pro složité tvary.

## Často kladené otázky
### Co je Aspose.PSD pro Java?
Aspose.PSD pro Java je knihovna, která vývojářům umožňuje programově manipulovat a pracovat se soubory Photoshop PSD pomocí Javy.

### Mohu použít Aspose.PSD ve volném projektu?
Ano, knihovnu můžete vyzkoušet zdarma pomocí zkušební verze dostupné na webu Aspose.

### Jaké typy úprav mohu provádět v souborech PSD?
Můžete manipulovat s vrstvami, tvary, texty, operacemi cesty a mnoha dalšími aspekty souborů PSD.

### Je Aspose.PSD kompatibilní s jinými programovacími jazyky?
Ano, Aspose nabízí různé knihovny pro různé programovací jazyky, včetně .NET a Pythonu.

### Kde najdu dokumentaci k Aspose.PSD?
Kompletní dokumentaci můžete získat [zde](https://reference.aspose.com/psd/java/).

## Často kladené otázky

**Q: Jak zacházet s PSD, který neobsahuje žádné vrstvy s vektorovými tvary?**  
A: `VsmsResource` bude chybět, takže `resource` zůstane `null`. Přidejte kontrolu a přeskočte krok úpravy nebo uživatele informujte.

**Q: Mohu změnit i jiné vlastnosti, jako barvu výplně nebo šířku tahu?**  
A: Ano, `LengthRecord` poskytuje další settery pro výplň, tah a neprůhlednost. Podívejte se do API dokumentace pro podrobnosti.

**Q: Je možné dávkově zpracovávat více souborů PSD?**  
A: Rozhodně. Zabalte kód do smyčky, která iteruje přes adresář s PSD soubory, a při každém průchodu upravte vstupní a výstupní cesty.

**Q: Musím ručně zavírat streamy při načítání ze souborové cesty?**  
A: Metoda `Image.load` interně spravuje souborové streamy, ale pokud načítáte z `InputStream`, nezapomeňte jej po použití zavřít.

**Q: Jaká verze Aspose.PSD je pro tyto API vyžadována?**  
A: Třídy `LengthRecord` a `PathOperations` jsou k dispozici od Aspose.PSD 20.10. Doporučujeme použít nejnovější verzi.

**Poslední aktualizace:** 2025-12-17  
**Testováno s:** Aspose.PSD pro Java 24.11  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}