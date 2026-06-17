---
date: 2026-03-04
description: Naučte se, jak programově upravovat vrstvy PSD přidáváním výplňových
  vrstev pomocí Aspose.PSD pro Javu. Postupujte podle tohoto krok‑za‑krokem průvodce
  a rychle vylepšete své návrhy.
linktitle: Modify PSD Layers Programmatically – Add Fill Layers (Java)
second_title: Aspose.PSD Java API
title: Programaticky upravovat vrstvy PSD – Přidat výplňové vrstvy (Java)
url: /cs/java/modifying-converting-psd-images/add-fill-layers-psd-files/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Programatická úprava vrstev PSD – Přidání výplňových vrstev (Java)

Pokud chcete **programaticky upravovat vrstvy PSD**, přidání výplňových vrstev je jedním z nejrychlejších způsobů, jak obohatit své Photoshop dokumenty, aniž byste museli Photoshop vůbec otevřít. V tomto tutoriálu projdeme přesně kroky, které potřebujete k vytvoření nového PSD, vložení barevných, gradientových a vzorových výplňových vrstev a následnému uložení výsledku – vše pomocí Aspose.PSD for Java.

## Rychlé odpovědi
- **Co mohu dosáhnout?** Přidat barevné, gradientové a vzorové výplňové vrstvy do souboru PSD programaticky.  
- **Která knihovna je vyžadována?** Aspose.PSD for Java (nejnovější verze).  
- **Potřebuji licenci?** Pro testování stačí bezplatná zkušební verze; pro produkční nasazení je vyžadována komerční licence.  
- **Jak dlouho trvá implementace?** Přibližně 10‑15 minut pro základní příklad.  
- **Jaká verze Javy je podporována?** JDK 11 nebo novější.

## Co znamená „programatická úprava vrstev PSD“?
Programatická úprava vrstev PSD znamená použití kódu k vytvoření, úpravě nebo odstranění vrstev uvnitř Photoshop dokumentu, což vám poskytuje plnou kontrolu nad pracovním postupem designu bez nutnosti ruční interakce s uživatelským rozhraním.

## Proč přidávat výplňové vrstvy pomocí Aspose.PSD?
- **Automatizace** – Generujte desítky PSD souborů v dávkovém úkolu.  
- **Konzistence** – Použijte naprosto stejnou barvu, gradient nebo vzor napříč více soubory.  
- **Rychlost** – Přeskočte časově náročné ruční kroky v Photoshopu.  
- **Cross‑platform** – Funguje na jakémkoli OS, který podporuje Javu.

## Předpoklady
Než se pustíme do kódu, ujistěte se, že máte následující:

1. **Java Development Kit (JDK)** – Nainstalujte JDK 11 nebo novější. Stáhnout jej můžete z [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. **Aspose.PSD for Java** – Získejte nejnovější knihovnu z oficiální stránky ke stažení [here](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse nebo jakýkoli editor, který preferujete.  
4. **Základní znalosti Javy** – Znalost tříd a metod vám pomůže, ale tutoriál vše vysvětlí krok za krokem.

## Import balíčků
Pro práci se soubory PSD musíte importovat příslušné třídy Aspose.PSD:

```java
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.filllayers.FillLayer;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
```

Tyto importy vám poskytují přístup k objektu `PsdImage` (samotnému dokumentu) a různým typům `FillLayer`, které budeme používat.

## Jak programaticky upravit vrstvy PSD – Průvodce krok za krokem

### Krok 1: Nastavte výstupní adresář
Definujte, kam se má výsledný PSD uložit, abyste jej mohli později najít.

```java
String outputDir = "Your Document Directory";
String outPsdFilePath = outputDir + "output.psd";
```

Nahraďte `"Your Document Directory"` absolutní nebo relativní cestou na vašem počítači.

### Krok 2: Vytvořte nový Photoshop dokument
Instancujte prázdné plátno, které bude hostit výplňové vrstvy.

```java
PsdImage psdImage = new PsdImage(100, 100);
```

Parametry `100, 100` představují šířku a výšku v pixelech. Upravit je můžete podle požadavků vašeho designu.

### Krok 3: Přidejte barevnou výplňovou vrstvu
Vytvořte výplňovou vrstvu s plnou barvou a dejte jí přátelský název.

```java
FillLayer colorFillLayer = FillLayer.createInstance(FillType.Color);
colorFillLayer.setDisplayName("Color Fill Layer");
psdImage.addLayer(colorFillLayer);
```

Později můžete změnit skutečnou barvu přístupem k nastavení výplně vrstvy (není zde ukázáno pro stručnost).

### Krok 4: Přidejte gradientovou výplňovou vrstvu
Gradientové výplně přidávají hloubku a vizuální zajímavost.

```java
FillLayer gradientFillLayer = FillLayer.createInstance(FillType.Gradient);
gradientFillLayer.setDisplayName("Gradient Fill Layer");
psdImage.addLayer(gradientFillLayer);
```

Klidně experimentujte s lineárními nebo radiálními gradienty pomocí nastavení vrstvy.

### Krok 5: Přidejte vzorovou výplňovou vrstvu
Vzorové výplně vám umožní dlaždicovat obrázky nebo textury napříč vrstvou.

```java
FillLayer patternFillLayer = FillLayer.createInstance(FillType.Pattern);
patternFillLayer.setDisplayName("Pattern Fill Layer");
patternFillLayer.setOpacity((byte)50);
psdImage.addLayer(patternFillLayer);
```

Nastavení opacity na 50 % způsobí, že se vzor hezky sloučí s vrstvami pod ním.

### Krok 6: Uložte svůj PSD soubor
Uložte změny na disk.

```java
psdImage.save(outPsdFilePath);
```

Otevřete uložený soubor ve Photoshopu nebo jakémkoli prohlížeči PSD a uvidíte tři nové výplňové vrstvy.

### Krok 7: Uvolněte prostředky
Vždy uvolněte objekt `PsdImage`, aby se uvolnila nativní paměť.

```java
psdImage.dispose();
```

## Časté problémy a tipy
- **Neplatná výstupní cesta** – Ujistěte se, že adresář existuje a máte práva k zápisu.  
- **Spotřeba paměti** – U velkých pláten volejte `psdImage.dispose()` hned, jakmile s obrázkem skončíte.  
- **Pořadí vrstev** – Vrstvy se standardně přidávají na vrchol zásobníku; pokud potřebujete konkrétní pořadí, použijte `psdImage.insertLayer(layer, index)`.

## Často kladené otázky

**Q: Jaké typy výplňových vrstev mohu přidat pomocí Aspose.PSD for Java?**  
A: Můžete přidat barevné, gradientové a vzorové výplňové vrstvy.

**Q: Podporuje Aspose.PSD i jiné formáty obrázků?**  
A: Ano, funguje s BMP, JPEG, PNG a mnoha dalšími formáty.

**Q: Můžu Aspose.PSD používat zdarma?**  
A: Vyzkoušet si můžete bezplatnou zkušební verzi Aspose.PSD for Java [here](https://releases.aspose.com/).

**Q: Kde najdu další dokumentaci k Aspose.PSD?**  
A: Kompletní dokumentaci získáte [here](https://reference.aspose.com/psd/java/).

**Q: Existuje komunita podpory pro Aspose.PSD?**  
A: Ano, pomoc získáte na fóru Aspose [here](https://forum.aspose.com/c/psd/34).

## Závěr
Nyní jste se naučili, jak **programaticky upravovat vrstvy PSD** přidáním různých výplňových vrstev pomocí Aspose.PSD for Java. Tento přístup vám ušetří čas, zajistí konzistenci napříč projekty a otevře dveře k výkonným scénářům dávkového zpracování. Experimentujte s různými barvami, gradienty a vzory a zjistěte, kam vás může automatizace designu zavést.

---

**Poslední aktualizace:** 2026-03-04  
**Testováno s:** Aspose.PSD for Java (nejnovější verze)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}