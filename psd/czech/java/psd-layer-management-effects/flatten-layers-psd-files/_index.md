---
date: 2026-04-03
description: Naučte se, jak snížit velikost souboru PSD zploštěním vrstev pomocí Aspose.PSD
  pro Javu. Tento krok‑za‑krokem průvodce ukazuje, jak rychle zploštit soubory PSD.
keywords:
- reduce psd file size
- how to flatten psd
- flatten visible layers psd
linktitle: Zmenšete velikost souboru PSD sloučením vrstev – Aspose.PSD Java
second_title: Aspose.PSD Java API
title: Zmenšete velikost souboru PSD zploštěním vrstev – Aspose.PSD Java
url: /cs/java/psd-layer-management-effects/flatten-layers-psd-files/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Zmenšení velikosti souboru PSD zploštěním vrstev – Aspose.PSD Java

## Úvod

Pokud jste někdy otevřeli dokument Photoshopu a přemýšleli, jak **reduce PSD file size**, zploštění vrstev je jeden z nejúčinnějších triků. S Aspose.PSD pro Java můžete programově zploštit celý PSD nebo sloučit jen vrstvy, které si vyberete, což vám poskytuje jemnou kontrolu nad velikostí souboru bez ztráty vizuální kvality. V tomto tutoriálu projdeme oba přístupy – zploštění celého obrázku a sloučení konkrétních vrstev – abyste mohli rychle zmenšit své PSD soubory a udržet plynulý pracovní postup.

## Rychlé odpovědi
- **Co dělá flattening?** Spojuje viditelné vrstvy do jedné vrstvy pozadí, odstraňuje informace o vrstvách a často snižuje velikost souboru.  
- **Mohu zploštit jen vybrané vrstvy?** Ano, můžete sloučit konkrétní vrstvy a ostatní nechat nedotčené.  
- **Potřebuji licenci?** Ano, pro vývoj stačí bezplatná zkušební verze; pro produkci je vyžadována komerční licence.  
- **Jaká verze Javy je požadována?** JDK 8 nebo vyšší.  
- **Ovlivní flattening kvalitu obrazu?** Ne, vizuální vzhled zůstává stejný; mění se pouze struktura vrstev.

## Co je „reduce PSD file size“?

Zmenšení velikosti souboru PSD znamená odstranění zbytečných dat – jako jsou nadbytečné vrstvy, skryté kanály nebo nadměrná metadata – aby se soubor stal lehčím a rychleji se načítal, sdílel nebo zpracovával. Zploštění vrstev je běžná technika, protože odstraňuje samostatné objekty vrstev a zachovává finální kompozitní obrázek.

## Proč zploštit vrstvy pomocí Aspose.PSD pro Java?

- **Automatizace:** Není nutné ručně otevírat Photoshop; integrujte přímo do svých Java aplikací.  
- **Přesnost:** Zvolte, zda zploštit celý dokument nebo jen viditelné vrstvy (`flattenImage`) nebo sloučit vybrané vrstvy (`mergeLayers`).  
- **Výkon:** Menší soubory se načítají rychleji a spotřebovávají méně paměti v následných procesech.  
- **Cross‑platform:** Funguje na jakémkoli OS, který podporuje Javu.

## Požadavky

1. **Java Development Kit (JDK):** Nainstalovaný JDK 8 nebo novější.  
2. **Aspose.PSD pro Java:** Stáhněte knihovnu z [here](https://releases.aspose.com/psd/java/).  
3. **IDE:** IntelliJ IDEA, Eclipse nebo jakékoli Java‑kompatibilní IDE.  
4. **Základní znalost Javy:** Užitečná, ale není povinná pro sledování kroků.  
5. **Ukázkový PSD:** Soubor s více vrstvami (použijeme `ThreeRegularLayersSemiTransparent.psd`).

Nyní, když máme vše připravené, ponořme se do kódu.

## Import balíčků

Nejprve importujte základní třídy Aspose.PSD:

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
```

Tyto importy nám umožňují načíst PSD soubory, pracovat s jejich vrstvami a uložit výsledky.

## Krok 1: Zploštění celého PSD obrázku

Zploštění celého obrázku je nejrychlejší způsob, jak **reduce PSD file size**, protože odstraňuje všechna jednotlivá data vrstev.

### 1.1 Načtení PSD souboru

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "ThreeRegularLayersSemiTransparent.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

### 1.2 Zploštění obrázku

```java
im.flattenImage();
```

### 1.3 Uložení zploštěného obrázku

```java
String exportPath = dataDir + "ThreeRegularLayersSemiTransparentFlattened.psd";
im.save(exportPath);
```

Váš nový soubor nyní obsahuje jedinou vrstvu pozadí, což obvykle vede k menší velikosti PSD.

## Krok 2: Sloučení konkrétních vrstev (Jak selektivně zploštit PSD)

Někdy chcete **flatten visible layers** nebo sloučit podmnožinu vrstev a přitom nechat ostatní editovatelné.

### 2.1 Znovu načíst PSD soubor

```java
PsdImage img = (PsdImage) Image.load(sourceFileName);
```

### 2.2 Identifikace a výběr vrstev

```java
Layer bottomLayer = img.getLayers()[0];
Layer middleLayer = img.getLayers()[1];
Layer topLayer = img.getLayers()[2];
```

### 2.3 Sloučení vrstev

```java
Layer layer1 = img.mergeLayers(bottomLayer, middleLayer);
Layer layer2 = img.mergeLayers(layer1, topLayer);
```

### 2.4 Nahrazení existujících vrstev sloučenou vrstvou

```java
img.setLayers(new Layer[]{layer2});
```

### 2.5 Uložení aktualizovaného PSD souboru

```java
exportPath = dataDir + "ThreeRegularLayersSemiTransparentFlattenedLayerByLayer.psd";
img.save(exportPath);
```

Nyní PSD obsahuje pouze sloučenou vrstvu, čímž dosáhne zmenšené velikosti souboru při zachování vrstev, které jste chtěli ponechat.

## Časté problémy a tipy

- **Záloha před zploštěním:** Jakmile jsou vrstvy zploštěny, operaci nelze vrátit zpět. Uchovejte si kopii původního PSD.  
- **Viditelnost má význam:** `flattenImage()` sloučí pouze *viditelné* vrstvy. Skryjte vrstvy, které nechcete zahrnout.  
- **Spotřeba paměti:** Velké PSD mohou spotřebovat značnou RAM; zvažte zpracování na stroji s dostatečnou pamětí.  
- **Režimy prolnutí:** Sloučení respektuje režim prolnutí každé vrstvy, takže vizuální výsledek odpovídá tomu, co byste viděli ve Photoshopu.

## Často kladené otázky

**Q: Mohu vrátit zploštění vrstev v Aspose.PSD?**  
A: Ne, zploštění je nevratné. Vždy si uchovávejte zálohu původního souboru.

**Q: Je možné zploštit pouze viditelné vrstvy?**  
A: Ano. `flattenImage()` respektuje viditelnost vrstev, takže před voláním metody skryjte vrstvy, které nechcete zploštit.

**Q: Snižuje zploštění vrstev velikost souboru?**  
A: Obecně ano. Odstranění dat vrstev a metadat často vede k menšímu PSD, i když přesná úspora závisí na obsahu.

**Q: Mohu sloučit vrstvy s různými režimy prolnutí?**  
A: Ano. Aspose.PSD sloučí vrstvy a zachová vizuální vzhled vytvořený jejich režimy prolnutí.

**Q: Co se stane, když se pokusím sloučit nesousedící vrstvy?**  
A: Aspose.PSD umožňuje sloučit libovolné vrstvy bez ohledu na jejich pořadí v zásobníku; výsledek odráží kombinovaný vzhled.

---

**Poslední aktualizace:** 2026-04-03  
**Testováno s:** Aspose.PSD 24.11 for Java  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}
{{< blocks/products/products-backtop-button >}}