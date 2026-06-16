---
date: 2026-03-02
description: Naučte se, jak přidat výplň vytvořením vrstvy s barevnou výplní v souborech
  PSD pomocí Javy a Aspose.PSD. Postupujte podle našeho krok za krokem průvodce a
  rychle nastavte barvu výplňové vrstvy.
linktitle: Add Color Fill Layer to PSD Files using Java
second_title: Aspose.PSD Java API
title: 'Jak přidat výplň: Přidat vrstvu barevné výplně do souborů PSD pomocí Javy'
url: /cs/java/modifying-converting-psd-images/add-color-fill-layer-psd-files/
weight: 20
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Přidání vrstvy výplně barvou do souborů PSD pomocí Javy

## Úvod
Už jste někdy potřebovali programově manipulovat se soubory Photoshopu, třeba přidat špetku barvy do návrhu? Pokud se ptáte **jak přidat výplň** do PSD, jste na správném místě. V tomto tutoriálu vás provedeme, jak pomocí Javy a knihovny Aspose.PSD přidat vrstvu výplně barvou do souborů PSD (Photoshop Document). Představte si svůj PSD jako digitální plátno – na konci budete vědět, jak vytvořit vrstvu výplně barvou, nastavit barvu vrstvy výplně a uložit aktualizovaný soubor během několika řádků kódu.

## Rychlé odpovědi
- **Jaká knihovna je potřeba?** Aspose.PSD pro Javu  
- **Hlavní případ použití?** Programově přidávat nebo měnit barvy výplně v PSD  
- **Jak dlouho trvá implementace?** Přibližně 10‑15 minut pro základní scénář  
- **Potřebuji licenci?** Bezplatná zkušební verze stačí pro hodnocení; pro produkční nasazení je vyžadována komerční licence  
- **Podporovaná verze Javy?** Java 8 a novější  

## Co je vrstva výplně barvou?
Vrstva výplně barvou je jednobarevná překrytí, která leží nad ostatními vrstvami v dokumentu Photoshopu. Často se používá k přidání barvy pozadí, vytvoření masek nebo rychlé změně vizuálního tématu návrhu bez úpravy jednotlivých pixelů.

## Proč přidávat vrstvu výplně barvou pomocí kódu?
- **Automatizace:** Generovat konzistentní značkové materiály napříč mnoha soubory.  
- **Dávkové zpracování:** Aktualizovat desítky PSD během několika sekund místo ruční práce.  
- **Dynamické návrhy:** Měnit barvy za běhu na základě vstupu uživatele nebo datových zdrojů.  

## Požadavky
1. **Java Development Kit (JDK)** – Nainstalovaný JDK 8 nebo novější.  
2. **Knihovna Aspose.PSD** – Stáhněte nejnovější JAR ze [stránky Aspose Releases](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse, NetBeans nebo jakýkoli editor dle vaší preference.  
4. **Základní znalost Javy** – Znalost objektů, smyček a zpracování výjimek.  

## Import balíčků
Nyní, když máme základy pokryté, importujme potřebné třídy. Tyto importy nám poskytují přístup k manipulaci s PSD a vrstvami výplně.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.filllayers.FillLayer;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.IColorFillSettings;
```

## Jak přidat výplň – krok za krokem průvodce

### Krok 1: Nastavte své prostředí
Definujte, kde se nachází váš zdrojový PSD a kam bude upravený soubor uložen, poté načtěte dokument.

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "ColorFillLayer.psd";
String exportPath     = dataDir + "ColorFillLayer_output.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

- `dataDir` ukazuje na složku obsahující váš PSD.  
- `sourceFileName` je původní soubor, který budete upravovat.  
- `exportPath` je cesta, kam bude zapsán nový soubor s **přidanou vrstvou výplně barvou**.  

### Krok 2: Procházejte vrstvy
Musíme najít všechny existující vrstvy výplně, abychom je mohli buď upravit, nebo vytvořit novou.

```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof FillLayer) {
        FillLayer fillLayer = (FillLayer) im.getLayers()[i];
```

- `for` smyčka iteruje přes každou vrstvu v PSD.  
- Kontrola `instanceof FillLayer` zajišťuje, že pracujeme jen s vrstvami výplně.  

### Krok 3: Ověřte typ výplně
Ujistěte se, že nalezená vrstva je **vrstva výplně barvou**, než se pokusíte změnit její barvu.

```java
if (fillLayer.getFillSettings().getFillType() != FillType.Color) {
    throw new Exception("Wrong Fill Layer");
}
```

Pokud typ výplně není `FillType.Color`, operaci přerušíme, abychom nechtěně neovlivnili gradientní nebo vzorové výplně.

### Krok 4: Nastavte barvu výplně
Zde **nastavujeme barvu vrstvy výplně**. Příklad mění vrstvu na červenou, ale můžete nahradit `Color.getRed()` libovolnou jinou `Color`, kterou potřebujete (např. `Color.getBlue()`, `new Color(255, 165, 0)` pro oranžovou).

```java
IColorFillSettings settings = (IColorFillSettings) fillLayer.getFillSettings();
settings.setColor(Color.getRed());
fillLayer.update();
```

- `settings.setColor(...)` mění skutečnou barvu výplně.  
- `fillLayer.update()` obnoví vrstvu, aby se nová barva aplikovala.  

### Krok 5: Uložte změny
Nakonec zapište upravený PSD zpět na disk.

```java
im.save(exportPath);
break;
```

- `break` ukončí smyčku po aktualizaci první odpovídající vrstvy výplně, což je obvykle požadováno, když potřebujete **jednou změnit barvu výplně v PSD**.

## Časté problémy a tipy
- **Nebyla nalezena žádná vrstva výplně:** Pokud váš PSD neobsahuje vrstvu výplně, musíte ji vytvořit pomocí `new FillLayer(im)` a přidat ji do `im.getLayers()`.  
- **Barva se neaktualizuje:** Ujistěte se, že po nastavení barvy zavoláte `fillLayer.update()`.  
- **Soubor se neuložil:** Ověřte, že `exportPath` ukazuje na zapisovatelný adresář a že máte oprávnění zapisovat soubory tam.  

## Často kladené otázky

**Q: Co je Aspose.PSD?**  
A: Aspose.PSD je výkonná knihovna pro Javu, která vám umožní vytvářet, upravovat a konvertovat soubory Photoshop PSD bez potřeby Adobe Photoshopu.

**Q: Mohu používat Aspose.PSD zdarma?**  
A: Ano, bezplatná zkušební verze je k dispozici na [stránce Aspose Releases](https://releases.aspose.com/).

**Q: S jakými formáty souborů mohu pracovat kromě PSD?**  
A: Aspose.PSD podporuje PSD, PSB, BMP, JPEG, PNG, GIF, TIFF a další.

**Q: Jak získám podporu, pokud narazím na problémy?**  
A: Otázky můžete klást na [fóru podpory Aspose](https://forum.aspose.com/c/psd/34).

**Q: Kde mohu zakoupit plnou licenci?**  
A: Licence se prodávají přes [stránku nákupu Aspose](https://purchase.aspose.com/buy).

## Závěr
Nyní už víte **jak přidat výplň** do Photoshop dokumentu programově pomocí Javy. Vytvořením nebo nalezením vrstvy výplně barvou, nastavením její barvy a uložením výsledku můžete automatizovat opakující se úkoly v designu, generovat dynamické materiály nebo integrovat manipulaci s PSD do větších Java aplikací. Vyzkoušejte to – experimentujte s různými barvami, přidejte více vrstev výplně nebo zkombinujte tuto techniku s dalšími funkcemi Aspose.PSD pro výkonné pipeline zpracování obrázků.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Poslední aktualizace:** 2026-03-02  
**Testováno s:** Aspose.PSD for Java 24.11 (latest at time of writing)  
**Autor:** Aspose