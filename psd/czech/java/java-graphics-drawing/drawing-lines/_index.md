---
date: 2026-01-19
description: Naučte se kreslit čáry v souborech PSD pomocí ASP a Aspose.PSD pro Javu.
  Zvyšte své dovednosti vývoje v Javě s tímto krok‑za‑krokem průvodcem.
linktitle: Drawing Lines in Java
second_title: Aspose.PSD Java API
title: asp kreslení čar v Javě
url: /cs/java/java-graphics-drawing/drawing-lines/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# asp Kreslení čar v Javě

## Úvod
V moderním vývoji v Javě umožňuje programová práce se soubory Photoshop Document (PSD) otevřít svět automatizačních možností. **asp** (knihovna Aspose.PSD) vám poskytuje plnou kontrolu pro vytváření, úpravu a vykreslování PSD souborů přímo z Java kódu. V tomto tutoriálu se naučíte **jak kreslit čáry v Javě** pomocí Aspose.PSD for Java, krok za krokem.

## Rychlé odpovědi
- **Jaká knihovna vám umožní upravovat PSD soubory v Javě?** asp (Aspose.PSD for Java)  
- **Mohu kreslit jak tečkované, tak plné čáry?** Ano, pomocí různých nastavení Pen.  
- **Potřebuji licenci pro vývoj?**šební verze funguje pro testování; licence?** Obvykle méně než 15 minut pro základní kreslení čar.

## Co je asp?
**asp. sadu API pro čtení, úpravu a zápis PSD souborů bez potřeby Adobe Photoshopu. Ať už potřebujete překrýt grafiku, extrahovat vrstvy nebo kreslit tvary, asp se postará o těžkou práci.

## Proč použít asp pro kreslení čar v Javě?
- **Výkon:** Optimalizovaný nativní kód zajišťuje rychlé vykreslování i pro velké PSD soubory.  
- **Flexibilita:** Podporuje širokou škálu kreslicích primitiv—čáry, obdélníky, elipsy a vlastní cesty.  
- **Cross‑platform:** Funguje na jakémkoli operačním systému, který spouští Javu.  
- **Není potřeba Photoshop:** Veškeré operace jsou prováděny programově.

## Předpoklady
- Základní znalost programování v Javě.  
- Nainstalovaný JDK (Java Development Kit).  
- Knihovna **asp** (Aspose.PSD for Java) stažená a přidaná do závislostí vašehonu můžete získat z oficiální stránky ke stažení:

- [Stáhnout Aspose.PSD pro Java](https://releases.aspose.com/psd/java/)

## Import balíčků
Nejprve importujte požadované asp třídy do vašeho Java projektu:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import static com.aspose.psd.GraphicsUnit.Point;
import com.aspose.psd.Image;
import com.aspose.psd.Pen;
import com.aspose.psd.Point;
import com.aspose.psd.brushes.SolidBrush;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.BmpOptions;
```

## Krok 1: Nastavení projektu
Vytvořte nový Java projekt ve svém IDE a přidejte soubory asp JAR do cesty sestavení. To vám poskytne přístup ke všem kreslicím API demonstrovaným níže.

## Krok 2: Inicializace PSD obrázku
Vytvořte prázdné PSD plátno s požadovanými rozměry:

```java
String dataDir = "Your Document Directory";
String outpath = dataDir + "Lines.psd";
Image image = new PsdImage(100, 100);
```

## Krok 3: Inicializace objektu Graphics
Objekt Graphics funguje jako kreslicí plocha. Před kreslením jej vymažte barvou pozadí:

```java
Graphics graphic = new Graphics(image);
graphic.clear(Color.getYellow());
```

## Krok 4: Kreslení úhlopříčných tečkovaných čar
Použijte Pen s výchozím stylem pro nakreslení dvou úhlopříčných tečkovaných čar:

```java
graphic.drawLine(new Pen(Color.getBlue()), 9, 9, 90, 90);
graphic.drawLine(new Pen(Color.getBlue()), 9, 90, 90, 9);
```

## Krok 5: Kreslení spojitých čar
Pro plné čáry s vlastními barvami vytvořte instance Pen podporované objekty SolidBrush:

```java
graphic.drawLine(new Pen(new SolidBrush(Color.getRed())), new Point(9, 9), new Point(9, 90));
graphic.drawLine(new Pen(new SolidBrush(Color.getAqua())), new Point(9, 90), new Point(90, 90));
graphic.drawLine(new Pen(new SolidBrush(Color.getBlack())), new Point(90, 90), new Point(90, 9));
graphic.drawLine(new Pen(new SolidBrush(Color.getWhite())), new Point(90, 9), new Point(9, 9));
```

## Krok 6: Uložení obrázku
Uložte upravený PSD na disk:

```java
image.save(outpath);
```

## Závěr
Po provedení těchto kroků jste úspěšně použili **asp** k nakreslení čar uvnitř PSD souboru pomocí Javy. Nyní víte, jak nastavit plátno, vymazat jej, kreslit jak tečkované, tak plné čáry a výsledek uložit. Tento základ vám umožní vytvářet složitější grafiku, přidávat textové vrstvy nebo integrovat manipulaci s PSD do větších Java aplikací.

## Často kladené otázky

**Q: Co je Aspose.PSD for Java?**  
A: Aspose.PSD for Java je výkonná Java knihovna pro programovou práci se soubory PSD.

**Q: Kde mohu najít dokumentaci pro Aspose.PSD for Java?**  
A: Můžete najít dokumentaci [zde](https://reference.aspose.com/psd/java/).

**Q: Mohu vyzkoušet Aspose.PSD for Java před zakoupením?**  
A: Ano, můžete získat bezplatnou zkušební verzi [zde](https://releases.aspose.com/).

**Q: Jak získám technickou podporu pro Aspose.PSD for Java?**  
A: Pro technickou podporu navštivte [forum Aspose.PSD](https://forum.aspose.com/c/psd/34).

**Q: Kde mohu získat dočasnou licenci pro Aspose.PSD for Java?**  
A: Dočasnou licenci můžete získat [zde](https://purchase.aspose.com/temporary-license/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Poslední aktualizace:** 2026-01-19  
**Testováno s:** Aspose.PSD for Java 24.12 (nejnovější v době psaní)  
**Autor:** Aspose  

---