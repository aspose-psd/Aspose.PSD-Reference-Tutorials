---
date: 2026-03-07
description: Naučte se, jak upravit úrovně přidáním vrstvy úpravy úrovní v souborech
  PSD pomocí Aspose.PSD pro Javu. Rychle si osvojte tónové úpravy.
linktitle: Add Level Adjustment Layer in PSD
second_title: Aspose.PSD Java API
title: Jak upravit úrovně – Přidat vrstvu úpravy úrovní v PSD
url: /cs/java/modifying-converting-psd-images/add-level-adjustment-layer-psd/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Přidání vrstvy úpravy úrovní v PSD

## Úvod
Pokud hledáte **jak upravit úrovně** ve svých dokumentech Photoshopu, vrstva úpravy úrovní je ideální nástroj. Umožňuje vám jemně doladit stíny, střední tóny a světla, aniž byste trvale změnili původní pixely. V tomto tutoriálu vás provedeme přidáním vrstvy úpravy úrovní do souboru PSD pomocí Aspose.PSD pro Java, abyste dosáhli profesionálního tónového řízení během několika kroků.

## Rychlé odpovědi
- **Co dělá vrstva úpravy úrovní?** Modifikuje tónový rozsah obrázku nedestruktivně.  
- **Která knihovna se používá?** Aspose.PSD pro Java.  
- **Potřebuji licenci?** Bezplatná zkušební verze funguje pro vývoj; licence je vyžadována pro produkci.  
- **Jak dlouho trvá implementace?** Přibližně 10‑15 minut pro základní úpravu.  
- **Mohu upravit více kanálů?** Ano, můžete nastavit vstupní/výstupní úrovně pro každý barevný kanál samostatně.

## Co je vrstva úpravy úrovní?
Vrstva úpravy úrovní vám umožňuje opravit tónovou rovnováhu obrázku úpravou vstupních stínů, středních tónů a světel stejně jako výstupních úrovní. Protože existuje na vlastní vrstvě, můžete přepínat její viditelnost nebo ji smazat, aniž byste ovlivnili podkladovou grafiku.

## Proč přidat vrstvu úpravy úrovní pomocí Aspose.PSD?
- **Automatizace:** Integrujte úpravy úrovní do dávkových zpracovatelských pipeline.  
- **Cross‑platform:** Funguje na jakémkoli OS, který podporuje Java.  
- **Přesnost:** Přistupujte k nastavením každého kanálu programově pro přesné výsledky.  

## Požadavky
1. Java Development Kit (JDK). Pokud jej nemáte, stáhněte jej z [webu Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) nebo použijte OpenJDK.  
2. Knihovna Aspose.PSD pro Java – stáhněte nejnovější JAR z tohoto [odkazu ke stažení](https://releases.aspose.com/psd/java/).  
3. Základní znalost programování v Javě.  
4. IDE, jako je IntelliJ IDEA, Eclipse nebo NetBeans, s přidaným Aspose.PSD JAR do classpath projektu.

## Import balíčků
Než začneme psát kód, musíme importovat potřebné balíčky z knihovny Aspose.PSD. Zde je návod, jak na to:
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.LevelsLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.LevelChannel;
```
Tyto importy nám poskytují přístup ke třídám pro načítání souborů PSD, práci s vrstvami úpravy úrovní a manipulaci s nastavením jednotlivých kanálů.

## Jak upravit úrovně v souboru PSD
Níže je krok za krokem průvodce, který vám přesně ukáže **jak upravit úrovně** programově.

### Krok 1: Nastavte cesty k souborům
Definujte, kde se nachází zdrojový PSD a kam bude upravený soubor uložen.
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "LevelsAdjustmentLayer.psd";
String psdPathAfterChange = dataDir + "LevelsAdjustmentLayerChanged.psd";
```
Nahraďte `"Your Document Directory"` skutečnou složkou ve vašem počítači.

### Krok 2: Načtěte soubor PSD
Vytvořte instanci `PsdImage` ze zdrojového souboru.
```java
PsdImage im = (PsdImage) Image.load(sourceFileName);
```
Nyní máte plný přístup ke všem vrstvám uvnitř PSD.

### Krok 3: Procházejte vrstvy
Najděte vrstvu úpravy úrovní, kterou chcete upravit.
```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof LevelsLayer) {
        LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
        // Further manipulation will go here...
    }
}
```
Kontrola `instanceof LevelsLayer` zajišťuje, že pracujeme pouze s vrstvami úpravy úrovní.

### Krok 4: Upravit nastavení kanálu úrovní
Upravte vstupní a výstupní hodnoty pro vybraný kanál.
```java
LevelChannel channel = levelsLayer.getChannel(0);
channel.setInputMidtoneLevel(2.0f);
channel.setInputShadowLevel((short) 10);
channel.setInputHighlightLevel((short) 230);
channel.setOutputShadowLevel((short) 20);
channel.setOutputHighlightLevel((short) 200);
```
- **Úroveň vstupního středního tónu:** Posouvá rozsah středních tónů.  
- **Úroveň vstupního stínu:** Ztmavuje nebo zesvětluje stíny.  
- **Úroveň vstupního světla:** Řídí nejjasnější části.  
- **Výstupní úrovně stínu/světla:** Definují konečný výstupní rozsah.  

Neváhejte experimentovat s různými hodnotami a sledovat, jak ovlivňují obrázek.

### Krok 5: Uložte upravený soubor PSD
Uložte své změny do nového souboru.
```java
im.save(psdPathAfterChange);
```
Aktualizovaný PSD najdete na místě, které jste zadali v `psdPathAfterChange`.

## Časté problémy a řešení
- **Soubor nenalezen:** Ověřte, že `dataDir` ukazuje na správnou složku a že zdrojový PSD existuje.  
- **ClassCastException:** Ujistěte se, že načítaný soubor je skutečně PSD; jiné formáty vyžadují jiné třídy.  
- **Chyby licence:** Použijte platnou licenci Aspose.PSD pro produkční sestavení; zkušební verze funguje pro vývoj.

## Závěr
Nyní víte **jak upravit úrovně** přidáním a konfigurací vrstvy úpravy úrovní v souboru PSD pomocí Aspose.PSD pro Java. Tato technika vám poskytuje přesnou kontrolu nad tónovou rovnováhou a zároveň udržuje váš pracovní postup plně automatizovaný. Pokračujte v experimentování s různými hodnotami kanálů a prozkoumejte dávkové zpracování, abyste aplikovali stejné úpravy na více obrázků.

## Často kladené otázky

**Q: Co je vrstva úpravy úrovní?**  
A: Je to nedestruktivní vrstva, která vám umožňuje měnit tónový rozsah (stíny, střední tóny, světla) obrázku.

**Q: Mohu používat Aspose.PSD bez zakoupení licence?**  
A: Ano, můžete knihovnu vyzkoušet pomocí bezplatné zkušební verze, ale licence je vyžadována pro komerční nasazení.

**Q: Kde najdu dokumentaci k Aspose.PSD?**  
A: Dokumentaci najdete [zde](https://reference.aspose.com/psd/java/).

**Q: Existuje komunita podpory pro produkty Aspose?**  
A: Rozhodně! Můžete klást otázky a získat pomoc na [fóru Aspose](https://forum.aspose.com/c/psd/34).

**Q: Jak získat dočasnou licenci pro Aspose.PSD?**  
A: Dočasnou licenci můžete požádat [zde](https://purchase.aspose.com/temporary-license/).

---

**Poslední aktualizace:** 2026-03-07  
**Testováno s:** Aspose.PSD nejnovější verze (Java)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}