---
date: 2025-12-30
description: Naučte se, jak změnit barvu stínu a přizpůsobit efekty stínu pomocí Aspose.PSD
  pro Javu. Postupujte podle tohoto krok‑za‑krokem tutoriálu o efektech stínu.
linktitle: Support Shadow Effect
second_title: Aspose.PSD Java API
title: Jak změnit barvu stínu pomocí Aspose.PSD pro Javu
url: /cs/java/basic-image-operations/support-shadow-effect/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Změna barvy stínu pomocí Aspose.PSD pro Java

## Úvod

Přidání hloubky do vašich grafických prvků často znamená **změnu barvy stínu**, aby odpovídala náladě návrhu. S Aspose.PSD pro Java můžete snadno přidávat nebo upravovat efekty vrženého stínu, řídit neprůhlednost a jemně ladit další parametry – vše z Java kódu. V tomto **návodu na efekty stínu** vás provedeme načtením PSD, čtením existujícího stínu, přizpůsobením jeho barvy, neprůhlednosti, vzdálenosti a nakonec uložením aktualizovaného souboru.

## Rychlé odpovědi
- **Co znamená „změna barvy stínu“?** Aktualizuje vlastnost barvy DropShadowEffect aplikovaného na vrstvu PSD.  
- **Která knihovna to podporuje?** Aspose.PSD pro Java poskytuje plnou podporu efektů stínů.  
- **Potřebuji licenci?** Zkušební verze funguje pro vývoj; pro produkci je vyžadována komerční licence.  
- **Mohu nastavit neprůhlednost stínu?** Ano – použijte `setOpacity(byte)` k definování průhlednosti (0‑255).  
- **Je kód kompatibilní s Java 8+?** Naprosto, API cílí na Java 8 a novější.

## Co je „změna barvy stínu“ v souborech PSD?

Změna barvy stínu upravuje vizuální odstín vrženého stínu, který se zobrazuje za vrstvou. To je užitečné pro vytvoření realistického osvětlení, sladění s barvami značky nebo prostě pro přidání uměleckého nádechu.

## Proč použít Aspose.PSD pro Java k přizpůsobení efektů stínů?

- **Plná věrnost PSD** – všechny efekty vrstev, včetně stínů, jsou zachovány.  
- **Není vyžadován Photoshop** – manipulujte se soubory programově na jakémkoli serveru.  
- **Jemná kontrola** – upravujte barvu, neprůhlednost, vzdálenost, úhel, rozptyl a šum.  
- **Cross‑platform** – funguje na Windows, Linux a macOS JVM.

## Požadavky

- Základní znalost programování v Java.  
- Aspose.PSD pro Java nainstalováno. Můžete jej stáhnout [zde](https://releases.aspose.com/psd/java/).  

## Import balíčků

Před začátkem importujte požadované třídy, abyste mohli pracovat s obrázky a efekty stínů:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;


import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.layereffects.DropShadowEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
```

## Postupný návod

### Krok 1: Načtení PSD obrázku

Nejprve načtěte zdrojový PSD a povolte načítání zdrojů efektů:

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Shadow.psd";
String psdPathAfterChange = dataDir + "ShadowChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

### Krok 2: Získání existujícího efektu vrženého stínu

Najděte efekt stínu na požadované vrstvě (v tomto příkladu druhá vrstva):

```java
DropShadowEffect shadowEffect = (DropShadowEffect)(im.getLayers()[1].getBlendingOptions().getEffects()[0]);
```

### Krok 3: Ověření výchozích nastavení (volitelné)

Spuštění těchto asercí vám pomůže pochopit původní hodnoty před jejich úpravou:

```java
Assert.areEqual(Color.getBlack(), shadowEffect.getColor());
Assert.areEqual(255, shadowEffect.getOpacity());
Assert.areEqual(3, shadowEffect.getDistance());
Assert.areEqual(7, shadowEffect.getSize());
Assert.areEqual(true, shadowEffect.getUseGlobalLight());
Assert.areEqual(90, shadowEffect.getAngle());
Assert.areEqual(0, shadowEffect.getSpread());
Assert.areEqual(0, shadowEffect.getNoise());
```

### Krok 4: **Změna barvy stínu** a přizpůsobení dalších vlastností

Nyní skutečně **změníme barvu stínu** na zelenou, upravíme neprůhlednost, vzdálenost, velikost a další atributy. Toto demonstruje možnosti **přizpůsobení efektu stínu** v Aspose.PSD:

```java
shadowEffect.setColor(Color.getGreen());          // change shadow color
shadowEffect.setOpacity((byte)128);               // set shadow opacity (50% transparent)
shadowEffect.setDistance(11);                     // move shadow farther from the object
shadowEffect.setUseGlobalLight(false);            // use local lighting
shadowEffect.setSize(9);                          // adjust blur radius
shadowEffect.setAngle(45);                        // rotate light source
shadowEffect.setSpread(3);                        // increase spread
shadowEffect.setNoise(50);                        // add texture noise
```

### Krok 5: Uložení upraveného obrázku

Nakonec zapište aktualizovaný PSD zpět na disk:

```java
im.save(psdPathAfterChange);
```

## Časté problémy a tipy

- **NullPointerException při získávání efektů** – ujistěte se, že je zavoláno `setLoadEffectsResource(true)`; jinak se efekty nenačtou.  
- **Barva se nemění** – ověřte, že upravujete správný index vrstvy (`im.getLayers()[1]` v tomto příkladu).  
- **Neprůhlednost vypadá nezměněně** – pamatujte, že neprůhlednost je byte (0‑255). Je nutné přetypovat na `(byte)`.

## Závěr

Podle těchto kroků můžete **změnit barvu stínu**, **nastavit neprůhlednost stínu** a plně **přizpůsobit parametry efektu stínu** v libovolném souboru PSD pomocí Aspose.PSD pro Java. To vám umožní programově vytvářet bohatší grafiku bez ruční práce ve Photoshopu.

## Často kladené otázky

**Q: Je Aspose.PSD pro Java vhodný pro profesionální projekty grafického designu?**  
A: Naprosto! Aspose.PSD pro Java je výkonná knihovna navržená pro profesionální úkoly grafického designu.

**Q: Mohu použít Aspose.PSD pro Java v komerčních aplikacích?**  
A: Ano, Aspose.PSD pro Java je komerční produkt. Můžete jej zakoupit [zde](https://purchase.aspose.com/buy).

**Q: Je k dispozici bezplatná zkušební verze?**  
A: Ano, můžete si vyzkoušet bezplatnou verzi [zde](https://releases.aspose.com/).

**Q: Kde najdu podrobnou dokumentaci?**  
A: Odkazujte na komplexní dokumentaci [zde](https://reference.aspose.com/psd/java/).

**Q: Jak mohu získat podporu pro Aspose.PSD pro Java?**  
A: Připojte se ke komunitnímu fóru [zde](https://forum.aspose.com/c/psd/34) pro jakékoli dotazy ohledně podpory.

---

**Poslední aktualizace:** 2025-12-30  
**Testováno s:** Aspose.PSD for Java 24.10  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}