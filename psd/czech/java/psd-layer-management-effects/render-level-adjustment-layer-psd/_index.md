---
title: Vrstva úprav úrovně vykreslení v souborech PSD - Java
linktitle: Vrstva úprav úrovně vykreslení v souborech PSD - Java
second_title: Aspose.PSD Java API
description: Naučte se, jak snadno zlepšit kontrast a živost obrazu pomocí Aspose.PSD pro Java. Master Levels Adjustment Layers s tímto průvodcem krok za krokem.
weight: 17
url: /cs/java/psd-layer-management-effects/render-level-adjustment-layer-psd/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Vrstva úprav úrovně vykreslení v souborech PSD - Java

## Zavedení

Už jste někdy otevřeli soubor PSD, abyste našli obrázek postrádající kontrast nebo živost? Nebojte se, bojovníci za úpravu obrázků! Aspose.PSD for Java přichází k záchraně se svými výkonnými možnostmi manipulace s vrstvami úprav úrovní. Tato příručka vás vybaví znalostmi pro jemné doladění obrázků pomocí Úrovně v vánku. 

## Předpoklady

- Java Development Kit (JDK): Ujistěte se, že máte v systému nainstalovanou nejnovější verzi JDK. Můžete si jej stáhnout z webu Oracle ([https://www.oracle.com/java/technologies/javase-downloads.html](https://www.oracle.com/java/technologies/javase-downloads.html)).
- Aspose.PSD for Java Library: Stáhněte si knihovnu Aspose.PSD for Java ze stránky stahování ([https://releases.aspose.com/psd/java/](https://releases.aspose.com/psd/java/)). K používání všech funkcí budete potřebovat platnou licenci, ale pro začátek je k dispozici bezplatná zkušební verze ([https://releases.aspose.com/](https://releases.aspose.com/)).

## Importujte balíčky

Než se ponoříme do kódu, musíme importovat potřebné třídy Aspose.PSD pro interakci se soubory PSD. Zde je to, co budete potřebovat:

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.LevelsLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.LevelChannel;
import com.aspose.psd.imageoptions.PngOptions;
```

 The`com.aspose.psd` balíček poskytuje přístup k funkcím manipulace s PSD, zatímco`com.aspose.psd.imaging.PngOptions` nám umožňuje definovat možnosti při ukládání obrázku jako PNG.

Nyní se pojďme pustit do našeho dobrodružství s úpravou úrovní:

## Krok 1: Nastavení cest souborů:

- Definujte proměnné pro svůj adresář dokumentů (`dataDir`), název zdrojového souboru PSD (`sourceFileName`), název cílového souboru PSD po úpravě (`psdPathAfterChange`) a konečná cesta exportu PNG (`pngExportPath`). Zvažte použití popisných názvů ke zlepšení čitelnosti kódu.

```java
String dataDir = "Your Document Directory";

String sourceFileName = dataDir + "LevelsAdjustmentLayer.psd";
String psdPathAfterChange = dataDir + "LevelsAdjustmentLayerChanged.psd";
String pngExportPath = dataDir + "LevelsAdjustmentLayerChanged.png";
```

## Krok 2: Načtení obrázku PSD:

-  Použijte`Image.load` způsob, jak otevřít zdrojový soubor PSD a uložit jej do a`PsdImage`objekt (`im`). Aspose.PSD automaticky detekuje formát souboru.

```java
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

## Krok 3: Iterace přes vrstvy:

- Potřebujeme najít vrstvu pro úpravu úrovní ve vašem PSD. Aspose poskytuje pohodlný způsob, jak iterovat všemi vrstvami pomocí smyčky.

```java
for (int i = 0; i < im.getLayers().length; i++) {
   // ... (zde bude přidán kód pro kontrolu vrstvy úrovní)
}
```

## Krok 4: Identifikace vrstvy úrovní:

- Uvnitř smyčky zkontrolujte, zda aktuální vrstva (`im.getLayers()[i]` ) je příkladem`LevelsLayer` třídy pomocí`instanceof` operátor. 
-  Pokud ano, přeneste vrstvu na a`LevelsLayer` objekt pro další manipulaci.

```java
for (int i = 0; i < im.getLayers().length; i++) {
   if (im.getLayers()[i] instanceof LevelsLayer) {
	   LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
	   // ... (zde bude přidán kód pro úpravu úrovní)
   }
}
```
## Krok 5: Jemné doladění úrovní (pokračování):

-  Upravte výstupní úrovně pomocí`setOutputShadowLevel` a`setOutputHighlightLevel` ovládat tmavost a světlost výsledného obrazu. Tyto hodnoty určují rozsah vstupních úrovní, které budou mapovány do výstupního rozsahu.

```java
for (int i = 0; i < im.getLayers().length; i++) {
   if (im.getLayers()[i] instanceof LevelsLayer) {
	   LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
	   LevelChannel channel = levelsLayer.getChannel(0);

	   // Upravit vstupní úrovně (0-255):
	   channel.setInputShadowLevel((short) 10); // Stíny mírně ztmavte
	   channel.setInputMidtoneLevel(2.0f);     // Zvyšte střední tóny
	   channel.setInputHighlightLevel((short) 230); // Omezte odlesky

	   // Upravit výstupní úrovně (0-255):
	   channel.setOutputShadowLevel((short) 20); // Dále ztmavte stíny
	   channel.setOutputHighlightLevel((short) 200); //Rozjasněte odlesky
   }
}
```

## Krok 6: Uložení upraveného PSD:

-  Použijte`save` metoda`PsdImage` objekt pro uložení upraveného obrázku do zadané cesty (`psdPathAfterChange`).

```java
im.save(psdPathAfterChange);
```

## Krok 7: Export jako PNG (volitelné):

-  Pokud potřebujete verzi PNG upraveného obrázku, vytvořte a`PngOptions` objekt a nastavte typ barvy na`TruecolorWithAlpha` . Poté použijte`save` znovu s cestou exportu PNG a možnostmi.

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
im.save(pngExportPath, saveOptions);
```

A tady to máte! Úspěšně jste upravili vrstvu úprav úrovní v souboru PSD pomocí Aspose.PSD for Java. Pochopením těchto kroků a experimentováním s různými hodnotami můžete zlepšit kontrast a celkový vzhled svých obrázků.

## Závěr

Aspose.PSD for Java vám umožňuje převzít kontrolu nad procesem úprav obrázků. Zvládnutím vrstvy úprav úrovní můžete svým fotografiím a návrhům vdechnout nový život. Pamatujte, že praxe dělá mistra, takže neváhejte experimentovat a prozkoumat plný potenciál tohoto mocného nástroje.
 
## FAQ

### Mohu upravit jednotlivé barevné kanály (RGB) samostatně? 
Ano, ke každému barevnému kanálu můžete přistupovat pomocí`getChannel` metoda`LevelsLayer` objekt a nezávisle upravovat jeho úrovně.

### Jak zpracuji více vrstev úprav úrovní v PSD?
Kód prochází všemi vrstvami, takže automaticky zpracuje všechny další vrstvy úrovní nalezené v obrázku.

### Existují jiné způsoby, jak upravit kontrast obrazu kromě Úrovně?
Absolutně! Aspose.PSD nabízí různé nástroje pro úpravu obrazu, jako jsou křivky, jas/kontrast a další.

### Mohu tento proces automatizovat pro více obrázků? 
Ano, tento kód můžete začlenit do smyčky nebo skriptu pro dávkové zpracování pro efektivní zpracování více souborů PSD.

### Kde najdu další informace a podporu?
Aspose poskytuje rozsáhlou dokumentaci ([https://reference.aspose.com/psd/java/](https://reference.aspose.com/psd/java/)) a fórum podpory ([https://forum.aspose.com/c/psd/34](https://forum.aspose.com/c/psd/34)) pro jakékoli dotazy nebo problémy, se kterými se můžete setkat.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
