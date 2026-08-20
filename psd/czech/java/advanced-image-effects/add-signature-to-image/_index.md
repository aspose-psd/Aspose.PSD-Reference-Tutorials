---
date: 2026-04-28
description: Naučte se, jak přidat podpis k obrázku kreslením obrázku na plátno pomocí
  Aspose.PSD pro Javu. Tento tutoriál pro zpracování obrázků v Javě ukazuje, jak uložit
  obrázek jako PNG a překrýt grafiku.
keywords:
- add signature to image
- draw image on canvas
- save image as png
- java image processing
- add watermark java
linktitle: Přidat podpis k obrázku
second_title: Aspose.PSD Java API
title: Přidat podpis k obrázku – Vykreslit obrázek na plátno pomocí Aspose.PSD pro
  Javu
url: /cs/java/advanced-image-effects/add-signature-to-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Přidání podpisu k obrázku – Kreslení obrázku na plátno pomocí Aspose.PSD pro Java

## Úvod

Přidání ručně psaného nebo digitálního **add signature to image** je běžná požadavek pro smlouvy, faktury nebo jakýkoli dokument, který potřebuje důkaz pravosti. V tomto tutoriálu uvidíte, jak Aspose.PSD pro Java umožňuje **draw image on canvas** a zacházet s podpisem jako s dalším překryvným vrstvou. Provedeme načtení základního obrázku, načtení souboru s podpisem, inicializaci grafického kontextu, kreslení překryvu a nakonec **save image as PNG**. Na konci budete mít znovupoužitelný vzor pro jakýkoli scénář **java image processing**, ať už jde o podpis, vodoznak nebo logo.

## Rychlé odpovědi
- **Co znamená „draw image on canvas“?** Jedná se o vykreslení jednoho obrázku na druhý pomocí třídy `Graphics`.  
- **Jak přidat podpis v Javě?** Načtěte soubor s podpisem jako `Image` a použijte `Graphics.drawImage`.  
- **Která verze Aspose.PSD je vyžadována?** Jakákoli aktuální verze 24.x; kód funguje s nejnovější knihovnou.  
- **Mohu překrýt více obrázků?** Ano — opakujte volání `drawImage` s různými zdroji.  
- **Potřebuji licenci?** Zkušební verze funguje pro vývoj; pro produkci je vyžadována komerční licence.

## Co je „draw image on canvas“?

V terminologii Aspose.PSD znamená kreslení obrázku na plátno malování jednoho objektu `Image` na jiný pomocí kontextu `Graphics`. Tato operace je základem technik **overlay images java**, jako je přidávání vodoznaků, log nebo podpisů.

## Proč použít Aspose.PSD pro překrytí podpisu?

- **Full PSD support** – funguje s vrstvami, maskami a průhledností.  
- **No native OS dependencies** – čistá Java, ideální pro server‑side zpracování.  
- **High‑performance rendering** – optimalizováno pro velké soubory a složité kompozice.  

## Požadavky
- Java Development Kit (JDK) 8 nebo vyšší.  
- JAR Aspose.PSD pro Java přidaný do classpath vašeho projektu.  
- Dva soubory obrázků: základní obrázek (např. `layers.psd`) a grafika podpisu (`sample.psd`).  

## Import balíčků

```java
import com.aspose.psd.Graphics;
import static com.aspose.psd.GraphicsUnit.Point;
import com.aspose.psd.Image;
import com.aspose.psd.Point;

import com.aspose.psd.imageoptions.PngOptions;
```

## Krok 1: Načtení primárního a sekundárního obrázku

```java
//ExStart:LoadImages
String dataDir = "Your Document Directory";

// Load the primary image (the canvas)
Image canvas = Image.load(dataDir + "layers.psd");

// Load the secondary image containing the signature graphics
Image signature = Image.load(dataDir + "sample.psd");
//ExEnd:LoadImages
```

> **Pro tip:** Uchovávejte oba obrázky ve stejném barevném režimu (RGB), aby nedocházelo k neočekávaným posunům barev při kreslení.

## Krok 2: Inicializace grafiky (initialize graphics java)

```java
//ExStart:InitializeGraphics
Graphics graphics = new Graphics(canvas);
//ExEnd:InitializeGraphics
```

`Graphics` objekt funguje jako štětec, který vám umožňuje **draw image on canvas**. Jeho inicializace s primárním `Image` propojí všechny následné kreslicí příkazy s tímto plátnem.

## Krok 3: Přidání podpisu k obrázku (how to add signature)

```java
//ExStart:AddSignatureToImage
graphics.drawImage(
    signature,
    new Point(
        canvas.getHeight() - signature.getHeight(),   // X‑coordinate (bottom)
        canvas.getWidth() - signature.getWidth()      // Y‑coordinate (right)
    )
);
canvas.save(dataDir + "AddSignatureToImage_out.png", new PngOptions());
//ExEnd:AddSignatureToImage
```

V tomto úryvku **overlay images java** umisťujeme podpis do pravého dolního rohu. Pokud potřebujete jiné umístění, upravte hodnoty `Point`.

## Časté problémy a řešení
| Problém | Příčina | Řešení |
|---------|----------|--------|
| Podpis se zobrazuje deformovaně | Nesoulad DPI mezi plátnem a podpisem | Použijte `signature.resize` před kreslením nebo zajistěte, aby oba soubory měly stejné DPI. |
| Výstupní soubor je velký | Ukládání bez komprese | Předávejte nakonfigurovaný `PngOptions` s nastaveným `CompressionLevel` na vyšší hodnotu. |
| Nic se nevykreslí | Graphics nebyl uvolněn | Zavolejte `graphics.dispose()` po kreslení (volitelné, ale dobrá praxe). |

## Další tipy pro reálné použití

- **Multiple signatures:** Volajte `graphics.drawImage` opakovaně s různými objekty `Image` a souřadnicemi.  
- **Opacity control:** Použijte `graphics.setOpacity(float opacity)` před kreslením, aby byl podpis poloprůhledný.  
- **Rotating the signature:** Použijte `graphics.rotateTransform(angle)`, pokud potřebujete šikmý podpis.  
- **Saving to other formats:** Nahraďte `PngOptions` za `JpegOptions` nebo `BmpOptions` pro výstup ve formátu JPEG, BMP atd.

## Často kladené otázky

### Q1: Mohu přidat více podpisů k obrázku?

A1: Ano, můžete přidat více podpisů opakováním kroků s různými soubory podpisů.

### Q2: Podporuje Aspose.PSD jiné formáty obrázků?

A2: Ano, Aspose.PSD podporuje širokou škálu formátů obrázků, což zajišťuje flexibilitu při zpracování obrázků.

### Q3: Je licence vyžadována pro používání Aspose.PSD pro Java?

A3: Ano, potřebujete platnou licenci pro používání Aspose.PSD. Navštivte [Purchase Aspose.PSD](https://purchase.aspose.com/buy) pro podrobnosti o licencování.

### Q4: Jak mohu získat podporu pro Aspose.PSD?

A4: Navštivte [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34) pro komunitní podporu a diskuse.

### Q5: Můžu vyzkoušet Aspose.PSD pro Java před zakoupením?

A5: Ano, můžete získat [free trial](https://releases.aspose.com/) a prozkoumat funkce před zakoupením.

**Další časté otázky**

**Q: Jak změním průhlednost podpisu?**  
A: Použijte `graphics.setOpacity(float opacity)` před voláním `drawImage`. Hodnoty se pohybují od 0.0 (průhledné) do 1.0 (neprůhledné).

**Q: Je možné podpis otočit?**  
A: Ano — použijte transformační matici pomocí `graphics.rotateTransform(angle)` před kreslením.

**Q: Mohu kreslit podpis do JPEG místo PNG?**  
A: Rozhodně. Nahraďte `PngOptions` za `JpegOptions` a zadejte požadovanou úroveň kvality.

## Závěr

Po provedení těchto kroků jste se naučili **how to add signature to image** pomocí **drawing an image on canvas** s Aspose.PSD pro Java. Stejný vzor lze rozšířit na vodoznaky, loga nebo jakékoli překryvné grafiky, což vašim Java aplikacím poskytuje výkonné schopnosti **java image processing**.

---

**Poslední aktualizace:** 2026-04-28  
**Testováno s:** Aspose.PSD for Java 24.11  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}