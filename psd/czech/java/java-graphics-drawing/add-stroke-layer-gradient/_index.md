---
date: 2026-01-14
description: Naučte se, jak vytvořit vrstvu s gradientním obrysem a přizpůsobit gradienty
  obrysu v souborech PSD pomocí Aspose.PSD pro Javu v tomto krok‑za‑krokem tutoriálu.
linktitle: How to Create Gradient Stroke Layer in Java
second_title: Aspose.PSD Java API
title: Jak vytvořit vrstvu s gradientním obrysem v Javě
url: /cs/java/java-graphics-drawing/add-stroke-layer-gradient/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak vytvořit vrstvu gradientního tahu v Java

## Úvod
Už jste se někdy zamýšleli, jak **vytvořit gradientní vrstvu tahu** ve svých souborech PSD pomocí Javy? Jste na správném místě! Dnes se ponoříme do Aspose.PSD pro Java – výkonné knihovny, která vám umožní snadno manipulovat se soubory PSD. Ať už jste nováčkem v programování grafiky nebo chcete doladit existující návrhy, tento průvodce vás krok za krokem provede přidáním a úpravou gradientních tahů.

## Rychlé odpovědi
- **Jaký je hlavní cíl?** Vytvořit vrstvu gradientního tahu v souboru PSD.  
- **Která knihovna je vyžadována?** Aspose.PSD pro Java.  
- **Potřebuji licenci?** Ano, pro produkční použití je vyžadována platná (nebo dočasná) licence.  
- **Jaká verze Javy funguje?** Java 8 nebo vyšší.  
- **Jak dlouho trvá implementace?** Přibližně 10‑15 minut pro základní gradientní tah.

## Co je vrstva gradientního tahu?
Vrstva gradientního tahu je vektorový obrys kolem tvaru nebo textu, který plynule přechází mezi barvami. Pomocí Aspose.PSD můžete programově definovat barvy, neprůhlednost, úhel a typ (lineární, radiální atd.) tahu.

## Proč použít Aspose.PSD pro Java?
- **Kompletní podpora PSD** – čtení, úprava a zápis souborů PSD bez Photoshopu.  
- **Bohaté API efektů** – přístup k tahům, stínům, záři a mnoha dalším efektům vrstev.  
- **Cross‑platform** – funguje na jakémkoli OS, který podporuje Javu.  
- **Žádné nativní závislosti** – čistá Java, snadná integrace do CI pipeline.

## Předpoklady
1. **Java Development Kit (JDK)** – Nainstalujte nejnovější JDK z [webu Oracle](https://www.oracle.com/java/technologies/javase-downloads.html).  
2. **Aspose.PSD pro Java** – Stáhněte knihovnu ze [stránky ke stažení Aspose.PSD](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse nebo NetBeans.  
4. **Licence** – Získejte [dočasnou licenci](https://purchase.aspose.com/temporary-license/), pokud nemáte plnou.

## Import balíčků
Nejprve importujte třídy, které budeme potřebovat pro načtení PSD, přístup k efektům a konfiguraci gradientních výplní.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.examples.Utils.Assert;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.IGradientColorPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientColorPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientTransparencyPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientTransparencyPoint;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
```

Nyní rozdělíme proces do jasných kroků.

## Krok 1: Načtení souboru PSD
Načteme zdrojový PSD a povolíme zdroje efektů, aby byl tah dostupný.

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
String exportPath = dataDir + "StrokeGradientChanged.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```

## Krok 2: Přístup k efektu tahu
Předpokládáme, že tah, který chceme upravit, patří třetí vrstvě (index 2), a získáme její `StrokeEffect`.

```java
StrokeEffect gradientStroke = (StrokeEffect) im.getLayers()[2].getBlendingOptions().getEffects()[0];
```

## Krok 3: Ověření vlastností efektu tahu
Před provedením změn si ověříme existující nastavení, abychom přesně věděli, co aktualizujeme.

```java
Assert.areEqual(BlendMode.Normal, gradientStroke.getBlendMode());
Assert.areEqual(255, gradientStroke.getOpacity());
Assert.areEqual(true, gradientStroke.isVisible());
GradientFillSettings fillSettings = (GradientFillSettings) gradientStroke.getFillSettings();
Assert.areEqual(Color.getBlack(), fillSettings.getColor());
Assert.areEqual(FillType.Gradient, fillSettings.getFillType());
Assert.areEqual(true, fillSettings.getAlignWithLayer());
Assert.areEqual(GradientType.Linear, fillSettings.getGradientType());
Assert.isTrue(Math.abs(90 - fillSettings.getAngle()) < 0.001, "Angle is incorrect");
Assert.areEqual(false, fillSettings.getDither());
Assert.isTrue(Math.abs(0 - fillSettings.getHorizontalOffset()) < 0.001, "Horizontal offset is incorrect");
Assert.isTrue(Math.abs(0 - fillSettings.getVerticalOffset()) < 0.001, "Vertical offset is incorrect");
Assert.areEqual(false, fillSettings.getReverse());
```

## Krok 4: Úprava nastavení gradientní výplně
Zde změníme barvu, neprůhlednost, režim prolnutí a další vlastnosti, aby výsledek odpovídal požadovanému vzhledu.

```java
fillSettings.setColor(Color.getGreen());
gradientStroke.setOpacity((byte) 127);
gradientStroke.setBlendMode(BlendMode.Color);
fillSettings.setAlignWithLayer(false);
fillSettings.setGradientType(GradientType.Radial);
fillSettings.setAngle(45);
fillSettings.setDither(true);
fillSettings.setHorizontalOffset(15);
fillSettings.setVerticalOffset(11);
fillSettings.setReverse(true);
```

## Krok 5: Přidání a úprava bodů barvy a průhlednosti
Přidáme nové body barvy a průhlednosti a upravíme stávající, abychom tvarovali gradient.

```java
// Add new color point
GradientColorPoint colorPoint = fillSettings.addColorPoint();
colorPoint.setColor(Color.getGreen());
colorPoint.setLocation(4096);
colorPoint.setMedianPointLocation(75);
// Change location of previous point
fillSettings.getColorPoints()[1].setLocation(1899);
// Add new transparency point
GradientTransparencyPoint transparencyPoint = fillSettings.addTransparencyPoint();
transparencyPoint.setOpacity(25);
transparencyPoint.setMedianPointLocation(25);
transparencyPoint.setLocation(4096);
// Change location of previous transparency point
fillSettings.getTransparencyPoints()[1].setLocation(2411);
```

## Krok 6: Uložení upraveného souboru PSD
Po všech úpravách zapíšeme aktualizovaný soubor zpět na disk.

```java
im.save(exportPath);
```

## Krok 7: Ověření úprav
Načteme uložený soubor a ověříme, že každá vlastnost odráží provedené změny.

```java
PsdImage img = (PsdImage) Image.load(exportPath, loadOptions);
StrokeEffect gradientStrokeEffect = (StrokeEffect) img.getLayers()[2].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Color, gradientStrokeEffect.getBlendMode());
Assert.areEqual(127, gradientStrokeEffect.getOpacity());
Assert.areEqual(true, gradientStrokeEffect.isVisible());
GradientFillSettings fillSetting = (GradientFillSettings) gradientStrokeEffect.getFillSettings();
Assert.areEqual(Color.getGreen(), fillSetting.getColor());
Assert.areEqual(FillType.Gradient, fillSetting.getFillType());
// Check color points
Assert.areEqual(3, fillSetting.getColorPoints().length);
IGradientColorPoint point = fillSetting.getColorPoints()[0];
Assert.areEqual(50, point.getMedianPointLocation());
Assert.areEqual(Color.getBlack(), point.getColor());
Assert.areEqual(0, point.getLocation());
point = fillSettings.getColorPoints()[1];
Assert.areEqual(50, point.getMedianPointLocation());
Assert.areEqual(Color.getWhite(), point.getColor());
Assert.areEqual(1899, point.getLocation());
point = fillSettings.getColorPoints()[2];
Assert.areEqual(75, point.getMedianPointLocation());
Assert.areEqual(Color.getGreen(), point.getColor());
Assert.areEqual(4096, point.getLocation());
// Check transparency points
Assert.areEqual(3, fillSettings.getTransparencyPoints().length);
IGradientTransparencyPoint transparencyPoint1 = fillSettings.getTransparencyPoints()[0];
Assert.areEqual(50, transparencyPoint1.getMedianPointLocation());
Assert.areEqual(100, transparencyPoint1.getOpacity());
Assert.areEqual(0, transparencyPoint1.getLocation());
transparencyPoint1 = fillSettings.getTransparencyPoints()[1];
Assert.areEqual(50, transparencyPoint.getMedianPointLocation());
Assert.areEqual(100, transparencyPoint.getOpacity());
Assert.areEqual(2411, transparencyPoint.getLocation());
transparencyPoint1 = fillSettings.getTransparencyPoints()[2];
Assert.areEqual(25, transparencyPoint.getMedianPointLocation());
Assert.areEqual(25, transparencyPoint.getOpacity());
Assert.areEqual(4096, transparencyPoint.getLocation());
```

## Závěr
Nyní víte, jak **vytvořit vrstvu gradientního tahu** v souborech PSD pomocí Aspose.PSD pro Java. Načtením PSD, přístupem k efektu tahu, úpravou nastavení gradientní výplně a uložením výsledku můžete programově vytvářet profesionální grafiku, aniž byste kdykoli otevřeli Photoshop.

## Často kladené otázky
### Co je Aspose.PSD pro Java?
Aspose.PSD pro Java je knihovna, která vývojářům umožňuje pracovat se soubory PSD v Java aplikacích a poskytuje funkce pro vytváření, manipulaci a konverzi souborů PSD.

### Potřebuji licenci k použití Aspose.PSD pro Java?
Ano, k použití Aspose.PSD pro Java potřebujete platnou licenci. Pro evaluační účely můžete získat [dočasnou licenci](https://purchase.aspose.com/temporary-license/).

### Můžu pomocí Aspose.PSD pro Java vytvářet soubory PSD od nuly?
Určitě! Aspose.PSD pro Java poskytuje komplexní API pro programové vytváření a manipulaci souborů PSD.

### Je možné pomocí Aspose.PSD pro Java aplikovat i jiné efekty?
Ano, můžete aplikovat různé efekty jako stín, záři a další pomocí Aspose.PSD pro Java.

### Kde najdu dokumentaci k Aspose.PSD pro Java?
Dokumentaci najdete [zde](https://reference.aspose.com/psd/java/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Poslední aktualizace:** 2026-01-14  
**Testováno s:** Aspose.PSD pro Java 24.11  
**Autor:** Aspose