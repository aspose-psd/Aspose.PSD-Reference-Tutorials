---
date: 2025-12-02
description: Naučte se, jak v Javě pomocí Aspose.PSD nakreslit obrázek na plátno a
  překrýt jej podpisem. Postupujte podle tohoto krok‑za‑krokem tutoriálu pro zpracování
  obrázků v Javě a výsledek uložte jako PNG.
linktitle: Add a Signature to an Image
second_title: Aspose.PSD Java API
title: Vykreslit obrázek na plátno – Přidat podpis pomocí Aspose.PSD pro Javu
url: /cs/java/advanced-image-effects/add-signature-to-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Nakreslit obrázek na plátno – Přidat podpis pomocí Aspose.PSD for Java

## Úvod

Přidání ručně psaného nebo digitálního podpisu k obrázku je častý požadavek u smluv, faktur nebo jakéhokoli dokumentu, který potřebuje důkaz pravosti. S **Aspose.PSD for Java** můžete **draw image on canvas** a zacházet s podpisem jako s dalším překryvným vrstvou. V tomto **java image processing tutorial** projdeme celý postup – od načtení základního obrázku a souboru s podpisem, přes inicializaci grafiky, kreslení překryvu a nakonec **save image png java**‑styl.

## Rychlé odpovědi
- **Co znamená “draw image on canvas”?** Jedná se o vykreslení jednoho obrázku na druhý pomocí třídy `Graphics`.  
- **Jak přidat podpis v Javě?** Načtěte soubor s podpisem jako `Image` a použijte `Graphics.drawImage`.  
- **Která verze Aspose.PSD je vyžadována?** Jakákoli aktuální verze 24.x; kód funguje s nejnovější knihovnou.  
- **Mohu překrýt více obrázků?** Ano – opakujte volání `drawImage` s různými zdroji.  
- **Potřebuji licenci?** Zkušební verze funguje pro vývoj; pro produkci je vyžadována komerční licence.

## Co je “Draw Image on Canvas”?
V terminologii Aspose.PSD znamená kreslení obrázku na plátno natření jednoho objektu `Image` na jiný pomocí kontextu `Graphics`. Tato operace je základem technik **overlay images java**, jako je přidávání vodoznaků, log nebo podpisů.

## Proč použít Aspose.PSD pro překrytí podpisu?
- **Kompletní podpora PSD** – funguje s vrstvami, maskami a průhledností.  
- **Žádné nativní závislosti na OS** – čistá Java, ideální pro server‑side zpracování.  
- **Vysoce výkonné vykreslování** – optimalizováno pro velké soubory a složité kompozice.  

## Požadavky
- Java Development Kit (JDK) 8 nebo vyšší.  
- JAR Aspose.PSD for Java přidaný do classpath vašeho projektu.  
- Dva soubory obrázků: základní obrázek (např. `layers.psd`) a grafika podpisu (`sample.psd`).  

## Importovat balíčky

```java
import com.aspose.psd.Graphics;
import static com.aspose.psd.GraphicsUnit.Point;
import com.aspose.psd.Image;
import com.aspose.psd.Point;

import com.aspose.psd.imageoptions.PngOptions;
```

## Krok 1: Načíst primární a sekundární obrázky

```java
//ExStart:LoadImages
String dataDir = "Your Document Directory";

// Load the primary image (the canvas)
Image canvas = Image.load(dataDir + "layers.psd");

// Load the secondary image containing the signature graphics
Image signature = Image.load(dataDir + "sample.psd");
//ExEnd:LoadImages
```

> **Tip:** Uchovávejte oba obrázky ve stejném barevném režimu (RGB), aby nedocházelo k neočekávaným posunům barev při kreslení.

## Krok 2: Inicializovat grafiku (initialize graphics java)

```java
//ExStart:InitializeGraphics
Graphics graphics = new Graphics(canvas);
//ExEnd:InitializeGraphics
```

Objekt `Graphics` funguje jako štětec, který vám umožňuje **draw image on canvas**. Jeho inicializace s primárním `Image` sváže všechny následné kreslicí příkazy k tomuto plátnu.

## Krok 3: Přidat podpis k obrázku (how to add signature)

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
| Symptom | Příčina | Řešení |
|---------|----------|--------|
| Podpis je zkreslený | Nesoulad DPI mezi plátnem a podpisem | Použijte `signature.resize` před kreslením nebo zajistěte, aby oba soubory měly stejné DPI. |
| Výstupní soubor je obrovský | Ukládání bez komprese | Předávejte nakonfigurovaný `PngOptions` s vyšší hodnotou `CompressionLevel`. |
| Nic se nevykreslí | Grafika nebyla uvolněna | Po kreslení zavolejte `graphics.dispose()` (volitelné, ale dobrá praxe). |

## Závěr

Podle těchto kroků jste se naučili **how to draw image on canvas** a bez problémů **add a signature** pomocí Aspose.PSD for Java. Tuto techniku lze rozšířit na vodoznaky, loga nebo jakékoli překryvné grafiky, což vašim Java aplikacím poskytne výkonné možnosti **java image processing**.

## Často kladené otázky

### Q1: Mohu přidat více podpisů k obrázku?

Ano, můžete přidat více podpisů opakováním kroků s různými obrázky podpisů.

### Q2: Podporuje Aspose.PSD jiné formáty obrázků?

Ano, Aspose.PSD podporuje širokou škálu formátů obrázků, což zajišťuje flexibilitu při zpracování obrázků.

### Q3: Je licence vyžadována pro používání Aspose.PSD pro Java?

Ano, potřebujete platnou licenci pro používání Aspose.PSD. Navštivte [Purchase Aspose.PSD](https://purchase.aspose.com/buy) pro podrobnosti o licencování.

### Q4: Jak mohu získat podporu pro Aspose.PSD?

Navštivte [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34) pro komunitní podporu a diskuse.

### Q5: Můžu vyzkoušet Aspose.PSD pro Java před zakoupením?

Ano, můžete získat [free trial](https://releases.aspose.com/) a prozkoumat funkce před nákupem.

## Další často kladené otázky

**Q: Jak změním neprůhlednost podpisu?**  
A: Použijte `graphics.setOpacity(float opacity)` před voláním `drawImage`. Hodnoty se pohybují od 0.0 (průhledné) do 1.0 (neprůhledné).

**Q: Je možné podpis otočit?**  
A: Ano – použijte transformační matici pomocí `graphics.rotateTransform(angle)` před kreslením.

**Q: Můžu kreslit podpis na JPEG místo PNG?**  
A: Samozřejmě. Nahraďte `PngOptions` za `JpegOptions` a uveďte požadovanou úroveň kvality.

---

**Poslední aktualizace:** 2025-12-02  
**Testováno s:** Aspose.PSD for Java 24.11  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}