---
date: 2026-03-28
description: Naučte se, jak upravit jas v souboru PSD pomocí Aspose.PSD pro Javu,
  včetně toho, jak změnit jas a kontrast vrstvy PSD. Ideální pro vývojáře a grafické
  designéry.
linktitle: Adjust Brightness PSD Java – Manage Brightness & Contrast
second_title: Aspose.PSD Java API
title: Upravit jas PSD Java – Spravovat jas a kontrast
url: /cs/java/psd-image-modification-conversion/manage-brightness-contrast-psd-layers/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Upravit jas PSD Java – Správa jasu a kontrastu

## Úvod

Jste grafický designér nebo vývojář, který často pracuje se soubory PSD (Photoshop Document)? Potřebujete **adjust brightness psd java** rychle a spolehlivě, aniž byste opustili své Java prostředí? V tomto tutoriálu vám přesně ukážeme, jak změnit jas a kontrast vrstev PSD pomocí knihovny Aspose.PSD pro Java. Získáte znovupoužitelný úryvek kódu, který lze integrovat do jakéhokoli automatizovaného pipeline pro zpracování obrázků. Pojďme si zapřát rukávy a začít!

## Rychlé odpovědi
- **Jaká knihovna je potřeba?** Aspose.PSD for Java  
- **Mohu změnit více vrstev najednou?** Ano – iterujte přes všechny objekty `BrightnessContrastLayer`.  
- **Jaká verze Javy je vyžadována?** JDK 8 nebo vyšší.  
- **Potřebuji licenci pro produkci?** Ano, pro ne‑evaluační použití je vyžadována komerční licence.  
- **Je kód kompatibilní s projekty Maven/Gradle?** Naprosto – stačí přidat závislost Aspose.PSD.

## Co je „adjust brightness psd java“?

Úprava jasu v souboru PSD pomocí Javy znamená programové měnění hodnot `BrightnessContrastLayer`, což vám umožní automatizovat vizuální úpravy, které by jinak vyžadovaly ruční práci ve Photoshopu.

## Proč upravovat jas a kontrast ve vrstvách PSD?

- **Zrychlit dávkové zpracování** – ideální pro rozsáhlé knihovny designů.  
- **Zachovat strukturu vrstev** – mění se pouze cílené vrstvy úprav, zachovávají se masky a efekty.  
- **Integrovat do CI/CD pipeline** – automaticky generovat náhledové obrázky nebo miniatury.

## Požadavky

Než se vydáme na tuto vzrušující cestu manipulace se soubory PSD pomocí Javy, je nezbytné zajistit, že máte vše potřebné správně nastavené. Zde je, co budete potřebovat k úspěšnému dokončení tohoto tutoriálu:

1. **Java Development Kit (JDK)** – Ujistěte se, že máte na svém počítači nainstalovaný JDK 8 nebo novější. Můžete jej stáhnout z [Oracle's website](https://www.oracle.com/java/technologies/javase-jdk8-downloads.html).
2. **Aspose.PSD for Java Library** – Pro práci se soubory PSD budete potřebovat knihovnu Aspose.PSD. Nejnovější verzi můžete stáhnout ze [release page](https://releases.aspose.com/psd/java/).
3. **IDE podle vašeho výběru** – Integrované vývojové prostředí (IDE) jako IntelliJ IDEA, Eclipse nebo NetBeans je preferováno pro psaní a spouštění vašeho Java kódu.
4. **Základní znalost Javy** – Znalost programování v Javě vám pomůže pochopit úryvky kódu, se kterými budeme pracovat.

Jakmile budete mít tyto požadavky splněny, můžeme pokračovat. Vezměte si svůj oblíbený editor kódu a pojďme programovat!

## Import balíčků

Prvním krokem na naší programovací cestě je importovat potřebné balíčky. Než budete moci využívat funkce poskytované knihovnou Aspose.PSD, musíte zajistit, aby byla knihovna ve vašem classpath. Zde je návod, jak to provést:

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.BrightnessContrastLayer;
```

Dokončením těchto kroků připravujete prostředí pro efektivní práci se soubory PSD!

Nyní, když máme vše nastavené, je čas se pustit do hlavní části tutoriálu: úpravy jasu a kontrastu ve vrstvách PSD. Rozdělíme tento proces do jasných kroků, abyste jej mohli snadno sledovat.

## Krok 1: Definujte adresář dokumentů

Začněte definováním adresáře, kde se nacházejí vaše soubory PSD. Tento krok pomáhá efektivně organizovat soubory.

```java
String dataDir = "Your Document Directory";
```

Nahraďte `"Your Document Directory"` skutečnou cestou k adresáři s vašimi soubory PSD.

## Krok 2: Zadejte názvy zdrojového a cílového souboru

Dále musíte zadat název zdrojového souboru vašeho PSD a cílový soubor, kam bude upravený PSD uložen.

```java
String sourceFileName = dataDir + "BrightnessContrastModern.psd";
String psdPathAfterChange = dataDir + "BrightnessContrastModernChanged.psd";
```

V tomto příkladu předpokládáme, že ve vašem adresáři máte soubor PSD s názvem `BrightnessContrastModern.psd`.

## Krok 3: Načtěte soubor PSD

Nyní je čas načíst soubor PSD do vaší aplikace, abyste s ním mohli manipulovat.

```java
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

Tento řádek kódu vytvoří instanci `PsdImage`, která představuje váš soubor PSD. Nyní můžete přistupovat ke všem vrstvám PSD.

## Krok 4: Procházejte vrstvy

Dalším krokem je iterovat přes každou vrstvu vašeho souboru PSD, abyste našli a upravili nastavení jasu a kontrastu.

```java
for(int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof BrightnessContrastLayer) {
        BrightnessContrastLayer brightnessContrastLayer = (BrightnessContrastLayer)im.getLayers()[i];
```

Cyklus `for` prochází každou vrstvu PSD. Kontrolujeme, zda je vrstva instancí `BrightnessContrastLayer`. To je nezbytné pro zajištění, že se pokoušíte změnit jas vrstvy PSD pouze na správných vrstvách.

## Krok 5: Upravit jas a kontrast

Uvnitř smyčky můžete nyní nastavit jas a kontrast pro každou `BrightnessContrastLayer`. 

```java
        brightnessContrastLayer.setBrightness(50);
        brightnessContrastLayer.setContrast(50);
    }
}
```

V tomto příkladu nastavujeme jas a kontrast na `50`. Tyto hodnoty můžete upravit podle svých požadavků. Vyšší číslo zvyšuje jas/kontrast, nižší číslo jej snižuje.

## Krok 6: Uložit změny

Posledním krokem je uložit vaše změny do souboru PSD. Budete chtít zapsat upravený obrázek zpět do určeného cíle.

```java
im.save(psdPathAfterChange);
```

Tento řádek kódu uloží upravený soubor PSD s vašimi novými nastaveními jasu a kontrastu.

## Časté problémy a řešení

| Problém | Proč k tomu dochází | Řešení |
|-------|----------------|-----|
| **No `BrightnessContrastLayer` found** | PSD může používat jiný typ úpravy (např. Levels). | Ověřte typ vrstvy nebo převěďte úpravu na `BrightnessContrastLayer`. |
| **Saved file looks corrupted** | Chybějící licence nebo použití zastaralé verze Aspose.PSD. | Použijte platnou licenci a ujistěte se, že používáte nejnovější verzi knihovny. |
| **Values out of range** | Hodnoty jasu/kontrastu musí být mezi -100 a 100. | Omezte hodnoty před voláním `setBrightness`/`setContrast`. |

## Často kladené otázky

**Q: Co je Aspose.PSD for Java?**  
A: Aspose.PSD for Java je knihovna, která umožňuje vývojářům programově manipulovat se soubory PSD, což umožňuje automatizaci úkolů souvisejících s Photoshopem.

**Q: Mohu najednou upravit jas a kontrast více vrstev?**  
A: Ano, přístup použitý v tomto tutoriálu iteruje přes všechny vrstvy v PSD, což vám umožní upravit více instancí `BrightnessContrastLayer`.

**Q: Jak získám dočasnou licenci pro Aspose.PSD?**  
A: Dočasnou licenci můžete získat návštěvou [temporary license page](https://purchase.aspose.com/temporary-license/).

**Q: Je k dispozici bezplatná zkušební verze Aspose.PSD?**  
A: Ano, můžete si stáhnout bezplatnou zkušební verzi Aspose.PSD ze [release page](https://releases.aspose.com/).

**Q: Kde mohu najít další podporu pro Aspose.PSD?**  
A: Podporu pro Aspose.PSD můžete získat na jejich [support forum](https://forum.aspose.com/c/psd/34).

---

**Poslední aktualizace:** 2026-03-28  
**Testováno s:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}