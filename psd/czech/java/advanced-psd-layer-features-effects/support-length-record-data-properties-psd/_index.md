---
date: 2026-02-20
description: Naučte se, jak podporovat vlastnosti délky záznamu a hromadně zpracovávat
  soubory PSD pomocí Aspose.PSD pro Javu. Průvodce krok za krokem s ukázkami kódu.
linktitle: Support Length Record Data Properties in PSD - Java
second_title: Aspose.PSD Java API
title: Podpora vlastností záznamu délky – upravit vektorové tvary PSD (Java)
url: /cs/java/advanced-psd-layer-features-effects/support-length-record-data-properties-psd/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Podpora vlastností záznamu délky – Úprava vektorových tvarů PSD (Java)

## Úvod
Pokud potřebujete **upravit vektorové tvary PSD** programově, knihovna Aspose.PSD pro Java vám poskytuje plnou kontrolu nad soubory Photoshopu přímo z vašeho Java kódu. V tomto tutoriálu projdeme vše, co potřebujete vědět k **podpoře vlastností záznamu délky** — nezbytný krok, když chcete editovat vrstvy s vektorovými tvary. Na konci budete schopni otevřít PSD, upravit jeho vlastnosti vektorových tvarů a uložit aktualizovaný soubor, aniž byste opustili své IDE. Pojďme na to!

## Rychlé odpovědi
- **Co znamená „upravit vektorové tvary PSD“?** Úprava geometrie, operací cesty nebo jiných vlastností vrstev založených na vektorech uvnitř souboru PSD.  
- **Která knihovna to řeší?** Aspose.PSD pro Java.  
- **Potřebuji licenci?** Bezplatná zkušební verze stačí pro hodnocení; pro produkční nasazení je vyžadována komerční licence.  
- **Jak dlouho trvá implementace?** Přibližně 10‑15 minut pro základní skript úpravy tvaru.  
- **Jaké jsou hlavní předpoklady?** Java JDK, Aspose.PSD pro Java a ukázkový soubor PSD.

## Co znamená „podpora vlastností záznamu délky“?
Podpora vlastností záznamu délky znamená přístup k objektům `LengthRecord`, které popisují každou vektorovou cestu uvnitř PSD. Změnou těchto záznamů můžete řídit, jak se tvary kombinují, protínají nebo odečítají od sebe navzájem.

## Proč použít Aspose.PSD pro Java k podpoře vlastností záznamu délky?
- **Žádný Photoshop není potřeba** — pracujte přímo se soubory PSD na jakémkoli serveru.  
- **Bohaté API** — přístup k vrstvám, zdrojům a vektorovým datům pomocí silně typovaných tříd.  
- **Cross‑platform** — běží na Windows, Linuxu i macOS s libovolným JDK.  
- **Zaměřeno na výkon** — efektivní správa paměti a rychlé ukládání.

## Předpoklady
1. **Java Development Kit (JDK)** — stáhněte z [Oracle's website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) nebo použijte svůj oblíbený správce balíčků.  
2. **Aspose.PSD for Java** — získejte nejnovější JAR ze [Aspose releases page](https://releases.aspose.com/psd/java/).  
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

## Krok 1: Nastavte zdrojové a výstupní adresáře
Definujte, kde se nachází původní PSD, a kam chcete uložit upravený soubor.

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
Data vektorových tvarů jsou uložena uvnitř `VsmsResource`. Projděte zdroje druhé vrstvy, abyste jej našli.

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

## Krok 5: Upravit vlastnosti operací cesty
Nyní můžete **upravit vektorové tvary PSD** změnou jejich `PathOperations`. To určuje, jak se tvary navzájem ovlivňují (např. vyloučení, průnik, odečtení).

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
Uvolněte paměť voláním `dispose` na objektu `PsdImage`.

```java
psdImage.dispose();
```

## Jak dávkově zpracovat soubory PSD s podporou vlastností záznamu délky
Pokud potřebujete aplikovat stejné úpravy vektorových tvarů na mnoho PSD, zabalte výše uvedený kód do smyčky, která prochází adresář souborů. Aktualizujte `inPsdFilePath` a `outPsdFilePath` pro každou iteraci a budete moci **dávkově zpracovávat soubory PSD** efektivně.

## Časté úskalí a tipy
- **Kontroly na null** — vždy ověřte, že `resource` není `null`, než přistoupíte k cestám.  
- **Omezení indexů cest** — ujistěte se, že použité indexy (`[2]`, `[7]`, `[11]`) existují v konkrétním PSD, který upravujete.  
- **Licence** — běh bez platné licence vloží vodoznak do uloženého PSD.

## Závěr
Nyní máte kompletní, end‑to‑end příklad, jak **upravit vektorové tvary PSD** podporou vlastností záznamu délky pomocí Aspose.PSD pro Java. Ať už automatizujete pipeline assetů nebo budujete vlastní designový nástroj, tato API vám poskytují flexibilitu manipulovat s vektorovými vrstvami bez ruční práce ve Photoshopu. Prozkoumejte dál experimentováním s dalšími `PathOperations` nebo kombinováním více úprav `LengthRecord` pro složité tvary.

## Často kladené otázky

**Q: Jak zacházet s PSD, který neobsahuje žádné vrstvy s vektorovými tvary?**  
A: `VsmsResource` bude chybět, takže `resource` zůstane `null`. Přidejte kontrolu a přeskočte krok úpravy nebo uživatele informujte.

**Q: Můžu změnit i jiné vlastnosti, jako barvu výplně nebo šířku tahu?**  
A: Ano, `LengthRecord` poskytuje další settery pro výplň, tah a neprůhlednost. Podívejte se do dokumentace API pro podrobnosti.

**Q: Je možné dávkově zpracovat více souborů PSD?**  
A: Rozhodně. Zabalte kód do smyčky, která prochází adresář souborů PSD, a při každém průchodu upravte vstupní a výstupní cesty.

**Q: Musím ručně zavírat streamy při načítání ze souborové cesty?**  
A: Metoda `Image.load` interně spravuje souborové streamy, ale pokud načítáte z `InputStream`, nezapomeňte jej po použití zavřít.

**Q: Jaká verze Aspose.PSD je pro tyto API vyžadována?**  
A: Třídy `LengthRecord` a `PathOperations` jsou k dispozici od Aspose.PSD 20.10. Doporučujeme používat nejnovější verzi.

---

**Poslední aktualizace:** 2026-02-20  
**Testováno s:** Aspose.PSD for Java 24.11  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}