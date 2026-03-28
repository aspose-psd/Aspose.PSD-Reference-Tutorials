---
date: 2026-03-28
description: Naučte se, jak vytvořit novou vrstvu PSD a spravovat datum a čas jejího
  vytvoření pomocí Aspose.PSD pro Javu. Tento krok za krokem průvodce pokrývá načítání,
  čtení, ověřování a přidávání vrstev.
linktitle: Create New PSD Layer and Manage Creation DateTime in Java
second_title: Aspose.PSD Java API
title: Vytvořit novou vrstvu PSD a spravovat datum a čas vytvoření v Javě
url: /cs/java/psd-image-modification-conversion/manage-layer-creation-datetime-psd/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Vytvoření nového vrstvy PSD a správa data a času vytvoření v Javě

## Úvod
Když pracujete s soubory Photoshop (PSD) programově, schopnost **create new PSD layer** objektů a sledovat jejich časová razítka vytvoření je skutečným průlomem. Ať už budujete systém pro správu verzí designových aktiv, automatizujete hromadné úpravy, nebo jen potřebujete auditní stopu pro kolaborativní projekty, znalost toho, jak číst a nastavit datum vytvoření vrstvy, vám umožní udržet úplný původ každé změny. V tomto tutoriálu projdeme celý proces pomocí Aspose.PSD pro Javu – od načtení PSD, získání data vytvoření vrstvy, jeho ověření až po přidání zcela nové úpravové vrstvy.

## Rychlé odpovědi
- **Jaká knihovna zpracovává PSD soubory v Javě?** Aspose.PSD for Java  
- **Mohu přečíst datum vytvoření vrstvy?** Ano, pomocí `layer.getLayerCreationDateTime()`  
- **Je možné přidat novou úpravovou vrstvu?** Rozhodně – `im.addLevelsAdjustmentLayer()` ji vytvoří  
- **Potřebuji licenci pro produkční použití?** Komerční licence je vyžadována pro nasazení mimo zkušební verzi  
- **Která verze Javy je podporována?** JDK 8 nebo novější  

## Co je „create new PSD layer“?
Vytvoření nového vrstvy PSD znamená programově vložit čerstvý objekt vrstvy – například úpravovou, textovou nebo pixelovou vrstvu – do existujícího PSD dokumentu. Tato operace vám umožní rozšířit nebo upravit obrázek bez ručního otevírání Photoshopu.

## Proč spravovat datum a čas vytvoření vrstvy?
Sledování data a času vytvoření každé vrstvy vám pomáhá:
- **Audit revizí** – přesně vědět, kdy byla vrstva přidána.  
- **Synchronizovat aktiva** mezi týmy porovnáním časových razítek.  
- **Automatizovat pracovní postupy**, které závisí na časových pravidlech (např. skrýt vrstvy starší než měsíc).  

## Požadavky
Předtím, než se ponoříte dál, ujistěte se, že máte připraveno:

1. **Java Development Kit (JDK)** – verze 8 nebo novější.  
2. **IDE** – IntelliJ IDEA, Eclipse, NetBeans nebo jakýkoli editor, který preferujete.  
3. **Aspose.PSD for Java** – můžete si jej [stáhnout zde](https://releases.aspose.com/psd/java/) pro instalaci.  
4. **Základní znalost Javy** – pokud jste v Javě noví, nebojte se; kód je plně okomentován.

Máte vše připravené? Skvělé! Pojďme se pustit do zábavné části kódování.

## Import balíčků
Nejprve importujte třídy Aspose.PSD a Java utility, které budete potřebovat. Tyto importy vám poskytují přístup k manipulaci s obrázky, vrstvami a formátování dat.

```java
import com.aspose.psd.Image;
import com.aspose.psd.examples.Utils.Assert;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import java.text.DateFormat;
import java.text.SimpleDateFormat;
import java.util.Date;
```

## Krok 1: Nastavte adresář dokumentu
Určete složku, která obsahuje PSD, se kterým chcete pracovat. Nahraďte zástupný text absolutní cestou na vašem počítači.

```java
String dataDir = "Your Document Directory";
```

## Krok 2: Načtěte soubor PSD
Vytvořte instanci `PsdImage` načtením cílového souboru. Tento objekt je vstupním bodem pro všechny operace s vrstvami.

```java
String sourceName = dataDir + "OneLayer.psd";
PsdImage im = (PsdImage) Image.load(sourceName);
```

## Krok 3: Přístup k vrstvě a jejímu datu vytvoření
Získejte první vrstvu (index 0) a načtěte její časové razítko vytvoření. Toto je datum, které později porovnáte nebo zaznamenáte.

```java
Layer layer = im.getLayers()[0];
Date creationDateTime = layer.getLayerCreationDateTime();
```

## Krok 4: Formátování data vytvoření
Převeďte surový objekt `Date` na lidsky čitelný řetězec. Pokud preferujete jiný formát, upravte vzor.

```java
DateFormat dateFormat = new SimpleDateFormat("yyyy/MM/dd HH:mm:ss");
```

## Krok 5: Ověření data vytvoření
Pro demonstraci porovnáme získané datum s očekávanou hodnotou. Ve skutečných projektech můžete porovnávat s databázovým záznamem nebo konfiguračním souborem.

```java
Date expectedDateTime = new Date("2018/7/17 8:57:24");
Assert.areEqual(expectedDateTime, creationDateTime);
```

## Krok 6: Vytvořte novou vrstvu
Nyní skutečně **create new PSD layer** objekty. Zde přidáváme úpravovou vrstvu Levels, která vám umožní upravit tónové rozsahy bez změny původních pixelů.

```java
Date now = new Date();
Layer createdLayer = im.addLevelsAdjustmentLayer();
```

> **Pro tip:** Proměnná `now` zachycuje okamžik, kdy vrstvu přidáte, což můžete později uložit jako metadata, pokud potřebujete vlastní časové razítko.

## Časté problémy a řešení
| Problém | Proč se vyskytuje | Oprava |
|-------|----------------|-----|
| `NullPointerException` při volání `layer.getLayerCreationDateTime()` | PSD neobsahuje žádné vrstvy nebo je index vrstvy mimo rozsah. | Ověřte, že `im.getLayers().length > 0` před přístupem. |
| Neshoda data při validaci | Konstruktor `Date` parsuje řetězce závisle na locale. | Použijte `SimpleDateFormat.parse("2018/07/17 08:57:24")` pro spolehlivé parsování. |
| Nová vrstva není viditelná ve Photoshopu | Úpravová vrstva může být ve výchozím nastavení skrytá. | Po vytvoření zavolejte `createdLayer.setVisible(true);`. |

## Závěr
Nyní víte, jak **create new PSD layer** objekty, číst jejich časová razítka vytvoření, ověřovat tato razítka a přidávat úpravové vrstvy – vše pomocí Aspose.PSD pro Java. Tato schopnost otevírá dveře k sofistikované automatizaci, auditním stopám a kolaborativním pracovním postupům v jakémkoli Java‑založeném pipeline pro zpracování obrázků.

Pokud se vám tento tutoriál líbil, prozkoumejte další funkce Aspose.PSD, jako je slučování vrstev, aplikace filtrů nebo export do různých formátů. Možnosti jsou neomezené!

## Často kladené otázky
### Co je Aspose.PSD?  
Aspose.PSD je výkonná knihovna pro programovou práci se soubory Photoshop (PSD).

### Mohu používat Aspose.PSD zdarma?  
Ano! Můžete začít s bezplatnou zkušební verzí dostupnou [zde](https://releases.aspose.com/).

### Potřebuji zakoupit licenci pro dlouhodobé používání?  
Ano, licenci můžete získat [zde](https://purchase.aspose.com/buy), jakmile budete připraveni.

### Kde najdu více informací o Aspose.PSD?  
Podrobné návody a reference API najdete v [dokumentaci](https://reference.aspose.com/psd/java/).

### Jak mohu získat podporu, pokud narazím na problémy s Aspose.PSD?  
Neváhejte navštívit [fórum podpory](https://forum.aspose.com/c/psd/34) pro pomoc od komunity.

---

**Poslední aktualizace:** 2026-03-28  
**Testováno s:** Aspose.PSD for Java 24.10  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}