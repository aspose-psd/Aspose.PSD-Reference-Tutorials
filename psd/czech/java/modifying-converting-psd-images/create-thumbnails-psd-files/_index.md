---
date: 2026-03-13
description: Naučte se, jak vytvořit miniaturu PSD v Javě pomocí Aspose.PSD. Postupujte
  podle našeho krok‑za‑krokem průvodce a rychle generujte miniatury z PSD souborů.
linktitle: Create Thumbnails from PSD Files using Java
second_title: Aspose.PSD Java API
title: Vytvořit miniaturu PSD v Javě – Generovat miniatury z PSD
url: /cs/java/modifying-converting-psd-images/create-thumbnails-psd-files/
weight: 24
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Vytvořit náhled PSD v Javě – Generovat náhledy z PSD

## Úvod
Pokud potřebujete **create PSD thumbnail Java** kód, který extrahuje náhledové obrázky ze souborů Photoshopu, jste na správném místě. Ať už budujete správce digitálních aktiv, webovou galerii nebo automatizovanou pipeline pro dávkové zpracování, generování náhledů ze souborů PSD může dramaticky zlepšit výkon a uživatelský zážitek. V tomto tutoriálu projdeme celý proces s Aspose.PSD for Java, ukážeme vám, jak načíst PSD, najít jeho vložené zdroje náhledů a uložit je jako samostatné obrazové soubory.

## Rychlé odpovědi
- **Jaká knihovna je nejlepší pro extrakci náhledů PSD?** Aspose.PSD for Java.  
- **Jak dlouho trvá implementace?** Přibližně 10‑15 minut pro základní nastavení.  
- **Potřebuji mít nainstalovaný Photoshop?** Ne, Aspose.PSD funguje nezávisle.  
- **Do jakých formátů mohu exportovat náhled?** Jakýkoli formát podporovaný Aspose.PSD (např. BMP, PNG, JPEG).  
- **Je licence vyžadována pro produkční použití?** Ano, pro produkční nasazení je potřeba komerční licence.

## Co je „create PSD thumbnail Java“?
Vytvoření náhledu PSD v Javě znamená programově přečíst náhled uložený uvnitř dokumentu Photoshopu (PSD) a zapsat jej jako samostatný obrazový soubor. To je užitečné pro rychlé náhledy bez načítání celého, často velkého, obsahu PSD.

## Proč použít Aspose.PSD pro tento úkol?
- **Žádná závislost na Photoshopu:** Funguje na jakékoli platformě s JDK.  
- **Kompletní podpora PSD:** Zpracovává všechny verze a zdroje PSD, včetně náhledů.  
- **Jednoduché API:** Několik řádků kódu pro extrakci a uložení náhledů.  
- **Optimalizovaný výkon:** Efektivní správa paměti pro velké soubory.

## Požadavky
Než se ponoříme do detailů tvorby náhledů, podívejme se, co budete potřebovat.

### Vývojové prostředí Java
- **Java JDK:** Ujistěte se, že máte nainstalovaný Java Development Kit (JDK). Můžete jej stáhnout [zde](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
- **IDE:** Integrované vývojové prostředí (IDE) jako IntelliJ IDEA, Eclipse nebo NetBeans vám usnadní psaní kódu.

### Knihovna Aspose.PSD
- Musíte zahrnout knihovnu Aspose.PSD do svého projektu. Můžete [stáhnout nejnovější verzi zde](https://releases.aspose.com/psd/java/).

### Základní znalosti Javy
- Znalost základů Javy vám pomůže lépe se orientovat v ukázkovém kódu. Koncepty jako třídy, objekty a smyčky budou často používány.

## Import balíčků
Začněte importováním potřebných tříd z knihovny Aspose.PSD. Tento krok je zásadní, protože vám umožní využít funkce knihovny ve vašem kódu.

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.ThumbnailFormat;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```

S požadavky za sebou přejděme k hlavnímu tématu! Vytváření náhledů ze souborů PSD zahrnuje několik jednoduchých kroků, které vám podrobně popíšu.

## Jak vytvořit PSD thumbnail Java – Průvodce krok za krokem

### Krok 1: Nastavte své prostředí
Zde je návod, jak zahájit projekt a připravit se na generování náhledů.

1. **Vytvořte Java projekt**  
   - Otevřete své IDE a vytvořte nový Java projekt.  
   - Pojmenujte jej například `"PsdThumbnailGenerator"`.

2. **Zahrňte knihovnu Aspose.PSD**  
   - Přidejte soubor Aspose.PSD JAR do cesty sestavení projektu.  
   - Pokud používáte Maven, zahrňte jej do svého `pom.xml`:

```xml
<dependency>
    <groupId>com.aspose</groupId>
    <artifactId>aspose-psd</artifactId>
    <version>your_version_here</version>
</dependency>
```

### Krok 2: Načtěte soubor PSD
Dále musíme načíst PSD soubor, ze kterého chceme vytvořit náhledy.

1. **Určete adresář dokumentu**  
   Definujte adresář, kde se nachází váš soubor PSD.

```java
String dataDir = "Your Document Directory"; // Replace with your path
```

2. **Načtěte soubor PSD**  
   Použijte třídu `PsdImage` k načtení vašeho PSD souboru.

```java
PsdImage image = (PsdImage) Image.load(dataDir + "sample.psd");
```

> **Pro tip:** Ukládejte své PSD soubory do vyhrazené složky (např. `src/main/resources`), abyste se vyhnuli problémům s cestami.

### Krok 3: Procházejte zdroje PSD
Nyní, když máme načtený obrázek PSD, dalším krokem je prozkoumat jeho zdroje.

1. **Získejte počet zdrojů**  
   Projdeme všechny zdroje v souboru PSD.

```java
for (int i = 0; i < image.getImageResources().length; i++) {
    // Processing resources
}
```

2. **Identifikujte zdroje náhledů**  
   V cyklu zkontrolujte, zda je zdroj náhledem.

```java
if (image.getImageResources()[i] instanceof ThumbnailResource) {
    // Process the thumbnail
}
```

### Krok 4: Zpracujte náhled
Jakmile identifikujeme zdroj náhledu, musíme jej adekvátně zpracovat.

1. **Získejte a ověřte formát náhledu**  
   Pokud je zdroj skutečně náhledem, načtěte jej a ověřte jeho formát.

```java
ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
if (thumbnail.getFormat() == ThumbnailFormat.KJpegRgb) {
    // Create and save the thumbnail
}
```

### Krok 5: Vytvořte a uložte náhled
Zde se děje kouzlo! Vytvoříme nový obrázek z dat náhledu a uložíme jej.

1. **Vytvořte nový obrázek**  
   Použijeme šířku a výšku náhledového zdroje k vytvoření nového bitmapového obrázku.

```java
PsdImage thumbnailImage = new PsdImage(thumbnail.getWidth(), thumbnail.getHeight());
```

2. **Uložte pixely do nového obrázku**  
   Přeneste data náhledu do nově vytvořeného obrázku.

```java
thumbnailImage.savePixels(thumbnailImage.getBounds(), thumbnail.getThumbnailData());
```

3. **Uložte obrázek náhledu**  
   Nakonec uložte obrázek náhledu do vašeho adresáře dokumentu s unikátním názvem.

```java
thumbnailImage.save(dataDir + "CreateThumbnailsFromPSDFiles_out_" + i + ".bmp");
```

> **Častý úskalí:** Zapomenutí uzavřít objekty `PsdImage` může vést k únikům paměti. Zabalte kód pro práci s obrázkem do bloku try‑with‑resources, pokud používáte Java 7+.

## Závěr
Po provedení těchto kroků máte nyní solidní, znovupoužitelný způsob, jak **create PSD thumbnail Java** implementace, které extrahují náhledové obrázky z libovolného souboru Photoshopu. Tuto techniku lze integrovat do dávkových procesorů, webových služeb nebo desktopových utilit pro zrychlení katalogizace obrázků a zlepšení odezvy UI. Vyzkoušejte ji na své vlastní kolekci PSD a uvidíte, jak rychle můžete generovat lehké náhledy!

## Často kladené otázky
### Co je Aspose.PSD?
Aspose.PSD je Java knihovna, která umožňuje vývojářům pracovat se soubory Photoshopu, usnadňuje manipulaci a správu PSD souborů programově.

### Můžu použít Aspose.PSD zdarma?
Ano, Aspose nabízí bezplatnou zkušební verzi, kterou můžete použít k otestování knihovny před zakoupením licence.

### Do jakých formátů mohu uložit náhledy?
V tomto příkladu jsme uložili náhledy ve formátu BMP, ale Aspose.PSD podporuje také různé další formáty.

### Potřebuji mít nainstalovaný Photoshop pro použití Aspose.PSD?
Ne, Aspose.PSD funguje nezávisle na Photoshopu.

### Kde najdu více informací o Aspose.PSD?
Podrobnosti, tutoriály a další zdroje najdete v [dokumentaci Aspose.PSD](https://reference.aspose.com/psd/java/).

## Často kladené otázky

**Q: Jak mohu extrahovat náhledy z PSD chráněného heslem?**  
A: Načtěte PSD pomocí příslušného přetížení `Image.load`, které přijímá parametr hesla.

**Q: Mohu generovat náhledy ve formátu PNG místo BMP?**  
A: Rozhodně. Změňte příponu souboru v metodě `save` a Aspose.PSD provede konverzi.

**Q: Existuje způsob, jak hromadně zpracovat více souborů PSD?**  
A: Zabalte kód do smyčky, která iteruje přes adresář se soubory PSD, a opakujte stejnou logiku extrakce pro každý soubor.

**Q: Jaká verze Javy je vyžadována?**  
A: Aspose.PSD podporuje Java 8 a novější. Doporučuje se používat nejnovější JDK pro lepší výkon a bezpečnost.

**Q: Zvládá knihovna velké soubory PSD efektivně?**  
A: Ano, Aspose.PSD používá lazy loading a optimalizovanou správu paměti, aby pracovala s velkými soubory bez vyčerpání haldy.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Poslední aktualizace:** 2026-03-13  
**Testováno s:** Aspose.PSD 24.11 for Java (nejnovější v době psaní)  
**Autor:** Aspose  

---