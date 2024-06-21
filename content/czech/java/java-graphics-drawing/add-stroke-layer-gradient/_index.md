---
title: Jak přidat přechod vrstvy tahu v Javě
linktitle: Jak přidat přechod vrstvy tahu v Javě
second_title: Aspose.PSD Java API
description: Naučte se přidávat a přizpůsobovat přechody vrstvy tahu v souborech PSD pomocí Aspose.PSD for Java s tímto komplexním výukovým programem krok za krokem.
type: docs
weight: 10
url: /cs/java/java-graphics-drawing/add-stroke-layer-gradient/
---
## Úvod
Přemýšleli jste někdy, jak přidat přechod vrstvy tahu k vašim obrázkům pomocí Java? Tak to jste na správném místě! Dnes se ponoříme do světa Aspose.PSD for Java, výkonné knihovny, která vám pomůže snadno manipulovat se soubory PSD. Ať už jste začátečník nebo zkušený vývojář, tento podrobný průvodce vás provede procesem přidávání přechodu vrstvy tahu do vašich souborů PSD. Takže se připoutejte a připravte se zlepšit své dovednosti v oblasti grafických úprav!
## Předpoklady
Než začneme, je pár věcí, které musíte mít na svém místě. Ujistěte se, že máte následující:
1.  Java Development Kit (JDK): Ujistěte se, že máte v systému nainstalovaný JDK. Můžete si jej stáhnout z[Web společnosti Oracle](https://www.oracle.com/java/technologies/javase-downloads.html).
2.  Aspose.PSD for Java Library: Můžete si ji stáhnout z[Stránka ke stažení Aspose.PSD](https://releases.aspose.com/psd/java/).
3. Integrované vývojové prostředí (IDE): Bude fungovat jakékoli IDE jako IntelliJ IDEA, Eclipse nebo NetBeans.
4.  Platná licence: Můžete získat a[dočasná licence](https://purchase.aspose.com/temporary-license/) pokud ji nemáte plnou.
## Importujte balíčky
Nejprve naimportujme potřebné balíčky. Ty nám umožní používat třídy a metody potřebné pro manipulaci se souborem PSD.
```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.examples.Utils.Assert;
import com.aspose.psd.examples.Utils.Utils;
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
Nyní si pro lepší pochopení rozdělíme příklad do několika kroků.
## Krok 1: Načtěte soubor PSD
 Nejprve musíme načíst soubor PSD, který chceme upravit. Použijeme`PsdLoadOptions` k určení, že chceme načíst prostředky efektů.
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
String exportPath = dataDir + "StrokeGradientChanged.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```
## Krok 2: Přístup k efektu tahu
Dále musíme získat přístup k efektu tahu vrstvy, která nás zajímá. Zde předpokládáme, že se jedná o třetí vrstvu (index 2) v souboru PSD.
```java
StrokeEffect gradientStroke = (StrokeEffect) im.getLayers()[2].getBlendingOptions().getEffects()[0];
```
## Krok 3: Ověřte vlastnosti efektu tahu
Než provedete jakékoli změny, ověřte vlastnosti efektu tahu, abyste se ujistili, že upravujeme správná nastavení.
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
## Krok 4: Upravte nastavení přechodové výplně
Nyní je čas upravit nastavení přechodové výplně podle našich požadavků. Změníme barvu, krytí, režim prolnutí a další vlastnosti.
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
## Krok 5: Přidejte a upravte body barev a průhlednosti
Pojďme přidat nové barevné a průhledné body a upravit ty stávající, abychom dosáhli požadovaného efektu přechodu.
```java
// Přidat nový barevný bod
GradientColorPoint colorPoint = fillSettings.addColorPoint();
colorPoint.setColor(Color.getGreen());
colorPoint.setLocation(4096);
colorPoint.setMedianPointLocation(75);
// Změnit umístění předchozího bodu
fillSettings.getColorPoints()[1].setLocation(1899);
// Přidejte nový bod průhlednosti
GradientTransparencyPoint transparencyPoint = fillSettings.addTransparencyPoint();
transparencyPoint.setOpacity(25);
transparencyPoint.setMedianPointLocation(25);
transparencyPoint.setLocation(4096);
// Změnit umístění předchozího bodu průhlednosti
fillSettings.getTransparencyPoints()[1].setLocation(2411);
```
## Krok 6: Uložte upravený soubor PSD
Po provedení všech nezbytných úprav musíme soubor PSD uložit.
```java
im.save(exportPath);
```
## Krok 7: Ověřte úpravy
Nakonec načteme uložený soubor PSD a ověříme, že naše změny byly správně použity.
```java
PsdImage img = (PsdImage) Image.load(exportPath, loadOptions);
StrokeEffect gradientStrokeEffect = (StrokeEffect) img.getLayers()[2].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Color, gradientStrokeEffect.getBlendMode());
Assert.areEqual(127, gradientStrokeEffect.getOpacity());
Assert.areEqual(true, gradientStrokeEffect.isVisible());
GradientFillSettings fillSetting = (GradientFillSettings) gradientStrokeEffect.getFillSettings();
Assert.areEqual(Color.getGreen(), fillSetting.getColor());
Assert.areEqual(FillType.Gradient, fillSetting.getFillType());
// Zkontrolujte barevné body
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
// Zkontrolujte body průhlednosti
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
A tady to máte! Nyní víte, jak přidávat a manipulovat s přechody vrstvy tahu v souborech PSD pomocí Aspose.PSD pro Java. Tento výukový program se zabýval načítáním souboru PSD, přístupem a úpravou efektů tahu a uložením změn. S těmito dovednostmi můžete vytvářet vizuálně přitažlivé přechody a upravovat své soubory PSD tak, aby vyhovovaly vašim potřebám.
## FAQ
### Co je Aspose.PSD for Java?
Aspose.PSD for Java je knihovna, která umožňuje vývojářům pracovat se soubory PSD v aplikacích Java a poskytuje funkce pro vytváření, manipulaci a konverzi souborů PSD.
### Potřebuji licenci k používání Aspose.PSD pro Javu?
 Ano, k používání Aspose.PSD pro Javu potřebujete platnou licenci. Můžete získat a[dočasná licence](https://purchase.aspose.com/temporary-license/) pro účely hodnocení.
### Mohu použít Aspose.PSD for Java k vytvoření souborů PSD od začátku?
Absolutně! Aspose.PSD for Java poskytuje komplexní rozhraní API pro vytváření a manipulaci se soubory PSD programově.
### Je možné použít jiné efekty pomocí Aspose.PSD pro Javu?
Ano, pomocí Aspose.PSD pro Java můžete použít různé efekty, jako je stín, záře a další.
### Kde najdu dokumentaci k Aspose.PSD pro Javu?
 Dokumentaci najdete[tady](https://reference.aspose.com/psd/java/).