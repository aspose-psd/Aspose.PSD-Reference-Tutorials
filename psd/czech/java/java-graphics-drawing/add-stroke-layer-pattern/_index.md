---
title: Jak přidat vzor vrstvy tahu v Javě
linktitle: Jak přidat vzor vrstvy tahu v Javě
second_title: Aspose.PSD Java API
description: Naučte se, jak přidat vzor vrstvy tahu do souborů PSD pomocí Aspose.PSD for Java. Chcete-li své obrázky snadno vylepšit, postupujte podle tohoto podrobného průvodce.
type: docs
weight: 11
url: /cs/java/java-graphics-drawing/add-stroke-layer-pattern/
---
## Zavedení
Přidání vzoru vrstvy tahu do obrázku v Javě může znít jako skličující úkol, ale s Aspose.PSD pro Javu je to jednodušší, než si myslíte. Ať už navrhujete grafiku nebo pracujete na aplikacích pro úpravu fotografií, tato příručka vás provede procesem krok za krokem. Jste připraveni začít? Pojďme se ponořit!
## Předpoklady
Než začnete, budete potřebovat několik věcí:
- Java Development Kit (JDK): Ujistěte se, že máte v systému nainstalovaný JDK.
-  Aspose.PSD pro Java: Stáhněte si knihovnu z[zde](https://releases.aspose.com/psd/java/) a zahrnout jej do svého projektu.
- IDE: Použijte své oblíbené integrované vývojové prostředí (IDE), jako je IntelliJ IDEA nebo Eclipse.
## Importujte balíčky
Nejprve musíte do svého projektu Java importovat potřebné balíčky. Tyto balíčky jsou nezbytné pro práci s Aspose.PSD.
```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;
import com.aspose.psd.examples.Utils.Assert;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.PatternFillSettings;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.fileformats.psd.layers.layerresources.PattResource;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import java.util.UUID;
```
## Krok 1: Načtěte soubor PSD
Prvním krokem při přidávání vzorku vrstvy tahu je načtení souboru PSD, který chcete upravit.
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```
Načtením souboru PSD nyní můžete přistupovat k jeho vrstvám a efektům a manipulovat s nimi.
## Krok 2: Připravte data nového vzoru
Dále je třeba připravit data nového vzoru, která použijete na vrstvu tahu.
```java
int[] newPattern = new int[]
{
    Color.getAqua().toArgb(), Color.getRed().toArgb(), Color.getRed().toArgb(), Color.getAqua().toArgb(),
    Color.getAqua().toArgb(), Color.getWhite().toArgb(), Color.getWhite().toArgb(), Color.getAqua().toArgb(),
    Color.getAqua().toArgb(), Color.getWhite().toArgb(), Color.getWhite().toArgb(), Color.getAqua().toArgb(),
    Color.getAqua().toArgb(), Color.getRed().toArgb(), Color.getRed().toArgb(), Color.getAqua().toArgb(),
};
Rectangle newPatternBounds = new Rectangle(0, 0, 4, 4);
UUID guid = UUID.randomUUID();
```
Tato data vzoru budou použita k vytvoření nového efektu tahu.
## Krok 3: Přístup k efektu tahu
Chcete-li upravit efekt tahu, musíte otevřít konkrétní vrstvu a její možnosti prolnutí.
```java
StrokeEffect patternStroke = (StrokeEffect)im.getLayers()[3].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Normal, patternStroke.getBlendMode());
Assert.areEqual(255, patternStroke.getOpacity());
Assert.areEqual(true, patternStroke.isVisible());
PatternFillSettings fillSettings = (PatternFillSettings)patternStroke.getFillSettings();
Assert.areEqual(FillType.Pattern, fillSettings.getFillType());
```
To zajišťuje, že pracujete se správnou vrstvou a efektem.
## Krok 4: Upravte efekt tahu
Nyní upravme efekt tahu pomocí nových dat vzoru.
### Aktualizujte vlastnosti efektu tahu
```java
patternStroke.setOpacity((byte)127);
patternStroke.setBlendMode(BlendMode.Color);
```
### Aktualizujte prostředek vzoru
```java
PattResource resource;
for (int i = 0; i < im.getGlobalLayerResources().length; i++)
{
    if (im.getGlobalLayerResources()[i] instanceof PattResource)
    {
        resource = (PattResource)im.getGlobalLayerResources()[i];
        resource.setPatternId(guid.toString());
        resource.setName("$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0");
        resource.setPattern(newPattern, newPatternBounds);
    }
}
```
Tento fragment kódu aktualizuje zdroj vzoru novými daty vzoru.
## Krok 5: Použijte nový vzor
Nakonec použijte nový vzor na efekt tahu a uložte změny.
```java
((PatternFillSettings)patternStroke.getFillSettings()).setPatternName("$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0");
((PatternFillSettings)patternStroke.getFillSettings()).setPatternId(guid.toString() + "\0");
im.save(exportPath);
```
Tím zajistíte, že se nový vzor použije správně a soubor se uloží se změnami.
## Krok 6: Ověřte změny
Abyste se ujistili, že vše fungovalo správně, načtěte soubor znovu a ověřte změny.
```java
PsdImage img = (PsdImage)Image.load(sourceFileName, loadOptions);
StrokeEffect patternStrokeEffect = (StrokeEffect)img.getLayers()[3].getBlendingOptions().getEffects()[0];
PattResource resource1 = null;
for (int i = 0; i < img.getGlobalLayerResources().length; i++)
{
    if (img.getGlobalLayerResources()[i] instanceof PattResource)
    {
        resource1 = (PattResource)img.getGlobalLayerResources()[i];
    }
}
try
{
    Assert.areEqual(newPattern, resource1.getPatternData());
    Assert.areEqual(newPatternBounds, new Rectangle(0, 0, resource1.getWidth(), resource1.getHeight()));
    Assert.areEqual(guid.toString(), resource1.getPatternId());
    Assert.areEqual(BlendMode.Color, patternStrokeEffect.getBlendMode());
    Assert.areEqual(127, patternStrokeEffect.getOpacity());
    Assert.areEqual(true, patternStrokeEffect.isVisible());
    PatternFillSettings fillSettings1 = (PatternFillSettings)patternStrokeEffect.getFillSettings();
    Assert.areEqual(FillType.Pattern, fillSettings1.getFillType());
}
catch (Exception e)
{
    System.out.println(e.getMessage());
}
```
Tento krok ověří, že data vzoru byla správně aplikována na efekt tahu.
## Závěr
A tady to máte! Úspěšně jste přidali vzor vrstvy tahu do souboru PSD pomocí Aspose.PSD for Java. Podle těchto kroků můžete své obrázky snadno přizpůsobit a vylepšit. Šťastné kódování!
## FAQ
### Co je Aspose.PSD for Java?
Aspose.PSD for Java je knihovna, která umožňuje vývojářům vytvářet, upravovat a převádět soubory PSD (Photoshop Document) programově.
### Mohu použít Aspose.PSD pro Javu v komerčním projektu?
 Ano, můžete jej použít v komerčních projektech. Licenci si můžete zakoupit od[zde](https://purchase.aspose.com/buy).
### Je k dispozici bezplatná zkušební verze pro Aspose.PSD pro Javu?
 Ano, můžete si stáhnout bezplatnou zkušební verzi z[zde](https://releases.aspose.com/).
### Jak mohu získat podporu pro Aspose.PSD pro Java?
 Podporu můžete získat na fórech komunity Aspose[zde](https://forum.aspose.com/c/psd/34).
### Jaké jsou systémové požadavky pro Aspose.PSD pro Java?
Pro vývoj potřebujete nainstalovaný JDK a IDE. Knihovna podporuje více operačních systémů včetně Windows, Linux a macOS.