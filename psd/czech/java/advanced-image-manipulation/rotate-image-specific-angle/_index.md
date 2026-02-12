---
date: 2026-02-12
description: Naučte se, jak v Javě pomocí Aspose.PSD otočit obrázek o konkrétní úhel.
  Tento průvodce ukazuje, jak obrázek otočit, jak jej otočit o určitý počet stupňů
  a jak pracovat s barvami pozadí.
linktitle: How to Rotate Image on a Specific Angle
second_title: Aspose.PSD Java API
title: Jak otočit obrázek o konkrétní úhel pomocí Aspose.PSD pro Javu
url: /cs/java/advanced-image-manipulation/rotate-image-specific-angle/
weight: 20
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak otočit obrázek o konkrétní úhel pomocí Aspose.PSD pro Java

## Úvod

Pokud potřebujete **jak otočit obrázek** programově v Java aplikaci, Aspose.PSD pro Java nabízí čisté, vysoce výkonné API, které se postará o těžkou práci. Ať už vytváříte fotoeditor, generujete náhledy nebo připravujete zdroje pro webovou službu, otáčení obrázku o přesný stupeň je běžná potřeba. V tomto tutoriálu projdeme kompletním procesem – od načtení PSD souboru po uložení otočeného výsledku – a zdůrazníme osvědčené postupy, jako je cachování a řízení pozadí.

## Rychlé odpovědi
- **Jaká knihovna je nejlepší pro otáčení obrázků v Javě?** Aspose.PSD pro Java.  
- **Mohu otáčet o libovolný stupeň?** Ano, metoda `rotate` přijímá `float` úhel (kladný nebo záporný).  
- **Potřebuji licenci pro vývoj?** Bezplatná zkušební verze funguje pro testování; licence je vyžadována pro produkci.  
- **Jaké formáty obrázků jsou podporovány?** PSD, JPEG, PNG, TIFF, GIF, BMP a mnoho dalších.  
- **Jak nastavit barvu pozadí pro prázdný prostor?** Předávejte instanci `Color` metodě `rotate`.

## Co je otáčení obrázku v Javě?

Otáčení obrázku znamená otočit matici pixelů kolem pivotního bodu (obvykle středu) o zadaný úhel. V Javě to můžete provést ručně pomocí `Graphics2D`, ale Aspose.PSD abstrahuje matematiku, zpracovává různé barevné hloubky a zachovává informace o vrstvách při práci s PSD soubory.

## Proč použít Aspose.PSD pro otáčení obrázků?

- **Přesnost:** Otočte o libovolný zlomkový stupeň bez ztráty kvality.  
- **Výkon:** Vestavěné cachování (`image.cacheData()`) urychluje práci s velkými soubory.  
- **Řízení pozadí:** Zadejte barvu pozadí pro vyplnění mezer vzniklých otáčením.  
- **Flexibilita formátů:** Načtěte PSD, výstup jako JPEG, PNG nebo jakýkoli podporovaný formát.

## Předpoklady

Než začneme, ujistěte se, že máte následující:

1. **Java Development Kit (JDK 8 nebo novější)** – funkční Java IDE nebo nastavení příkazové řádky.  
2. **Aspose.PSD pro Java** – stáhněte nejnovější JAR ze stránky [Aspose.PSD Java page](https://reference.aspose.com/psd/java/).  
3. **Ukázkový soubor PSD** – např. `sample.psd` umístěný ve složce, na kterou můžete odkazovat z kódu.

## Import balíčků

Nejprve importujte třídy, které budeme potřebovat. Tyto importy zůstávají stejné bez ohledu na zvolený úhel otáčení.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imageoptions.JpegOptions;
```

## Postupný průvodce

### Krok 1: Definujte adresář dokumentu

Nastavte složku, která obsahuje zdrojový PSD a kam bude zapsán výstup.

```java
String dataDir = "Your Document Directory";
```

> **Pro tip:** Použijte absolutní cestu nebo `System.getProperty("user.dir")`, abyste se vyhnuli překvapením s relativními cestami.

### Krok 2: Zadejte cesty ke zdrojovému a cílovému souboru

```java
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "RotatingImageOnSpecificAngle_out.jpg";
```

Můžete změnit `destName` na libovolnou podporovanou příponu (`.png`, `.tiff`, atd.) podle vašich výstupních potřeb.

### Krok 3: Načtěte obrázek

```java
RasterImage image = (RasterImage)Image.load(sourceFile);
```

`Image.load` automaticky detekuje formát souboru a vrací konkrétní `RasterImage` pro operace založené na rastru.

### Krok 4: Cacheujte data obrázku (volitelné, ale doporučené)

```java
if (!image.isCached())
{
    image.cacheData();
}
```

Cachování ukládá pixely obrázku do paměti, což urychluje následné transformace – zvláště užitečné u velkých PSD souborů.

### Krok 5: Otočte obrázek

```java
image.rotate(20f, true, Color.getRed());
```

- **20f** – úhel otáčení ve stupních (float). Změňte tuto hodnotu pro otáčení o libovolný úhel, např. `-45f` pro proti směru hodinových ručiček.  
- **true** – zachovat původní poměr stran při rozšíření plátna tak, aby se vešel otočený obrázek.  
- **Color.getRed()** – barva pozadí, která vyplní prázdné rohy vzniklé otáčením. Nahraďte `Color.getWhite()` nebo libovolnou vlastní barvou podle potřeby.

#### Otočení obrázku o stupně v Javě

`rotate` metoda přijímá libovolnou hodnotu s plovoucí desetinnou čárkou, takže můžete **otočit obrázek o stupně** jako `30f`, `90f` nebo `-15f`. Kladné hodnoty otáčejí po směru hodinových ručiček, záporné proti směru.

#### Otočení obrázku o konkrétní úhel pomocí Aspose.PSD

Protože metoda pracuje s `float`, můžete zadat **otočení obrázku o konkrétní úhel** jako `22.5f` pro přesnou kontrolu v grafickém designu.

#### Shrnutí příkladu otáčení obrázku v Javě

Všechny výše uvedené kroky ukazují kompletní workflow **rotate image java** – od načtení souboru po uložení otočeného výstupu.

### Krok 6: Uložte výsledek

```java
image.save(destName, new JpegOptions());
```

`JpegOptions` vám umožňuje řídit kvalitu, kompresi a další nastavení specifická pro JPEG. Pro bezztrátový výstup použijte `PngOptions`.

## Časté problémy a řešení

| Problém | Příčina | Řešení |
|---------|---------|--------|
| **Prázdné rohy po otáčení** | Nebyla zadána barva pozadí | Předávejte `Color` (např. `Color.getWhite()`) metodě `rotate`. |
| **Chyba nedostatku paměti u velkých PSD** | Obrázek nebyl cachován | Zavolejte `image.cacheData()` před zpracováním. |
| **Nesprávný směr úhlu** | Záměna záporných a kladných úhlů | Používejte záporné hodnoty pro otáčení po směru hodinových ručiček (nebo opačně podle vašeho souřadnicového systému). |
| **Neuložené změny** | Zapomenuté volání `save` | Ujistěte se, že `image.save(...)` je provedeno po otáčení. |

## Často kladené otázky

**Q: Mohu otáčet obrázky s průhledností pomocí Aspose.PSD pro Java?**  
A: Ano. Knihovna zachovává alfa kanály; stačí se vyhnout zadání neprůhledné barvy pozadí, pokud chcete průhledné rohy.

**Q: Existují nějaká omezení formátů souborů podporovaných pro otáčení?**  
A: Ne. Aspose.PSD podporuje PSD, JPEG, PNG, TIFF, GIF, BMP, JPEG2000, WMF, EMF a mnoho dalších.

**Q: Mohu otáčet obrázky o záporný úhel?**  
A: Rozhodně. Předávejte záporný float metodě `rotate` (např. `-30f`) pro otáčení po směru hodinových ručiček.

**Q: Poskytuje Aspose.PSD náhled v reálném čase během otáčení?**  
A: API je pouze na straně serveru. Pro živé náhledy integrujte otočený bitmap do UI frameworku (Swing, JavaFX) a obnovte zobrazení.

**Q: Existuje komunitní fórum pro Aspose.PSD, kde mohu požádat o pomoc?**  
A: Ano, navštivte [Aspose.PSD forum](https://forum.aspose.com/c/psd/34), kde můžete klást otázky a sdílet zkušenosti.

## Závěr

Nyní víte **jak otočit obrázek** soubory o konkrétní úhel pomocí Aspose.PSD pro Java. Využitím cachování, řízení barvy pozadí a flexibilních výstupních možností můžete integrovat přesnou funkci otáčení do libovolného Java‑založeného workflow pro práci s obrázky.

---

**Poslední aktualizace:** 2026-02-12  
**Testováno s:** Aspose.PSD pro Java 24.11 (nejnovější v době psaní)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}