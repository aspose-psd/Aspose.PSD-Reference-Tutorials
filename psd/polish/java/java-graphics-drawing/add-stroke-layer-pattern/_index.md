---
title: Jak dodać wzór warstwy obrysu w Javie
linktitle: Jak dodać wzór warstwy obrysu w Javie
second_title: Aspose.PSD API Java
description: Dowiedz się, jak dodać wzór warstwy obrysu do plików PSD przy użyciu Aspose.PSD dla Java. Postępuj zgodnie z tym przewodnikiem krok po kroku, aby łatwo ulepszać swoje obrazy.
type: docs
weight: 11
url: /pl/java/java-graphics-drawing/add-stroke-layer-pattern/
---
## Wstęp
Dodanie wzorca warstwy obrysu do obrazu w Javie może wydawać się trudnym zadaniem, ale dzięki Aspose.PSD dla Java jest to łatwiejsze niż myślisz. Niezależnie od tego, czy projektujesz grafikę, czy pracujesz nad aplikacjami do edycji zdjęć, ten przewodnik przeprowadzi Cię krok po kroku przez ten proces. Gotowy, aby zacząć? Zanurzmy się!
## Warunki wstępne
Zanim zaczniesz, będziesz potrzebować kilku rzeczy:
- Zestaw Java Development Kit (JDK): Upewnij się, że masz zainstalowany pakiet JDK w swoim systemie.
-  Aspose.PSD dla Java: Pobierz bibliotekę z[Tutaj](https://releases.aspose.com/psd/java/) i umieść go w swoim projekcie.
- IDE: Użyj swojego ulubionego zintegrowanego środowiska programistycznego (IDE), takiego jak IntelliJ IDEA lub Eclipse.
## Importuj pakiety
Po pierwsze, musisz zaimportować niezbędne pakiety do swojego projektu Java. Pakiety te są niezbędne do pracy z Aspose.PSD.
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
## Krok 1: Załaduj plik PSD
Pierwszym krokiem podczas dodawania wzoru warstwy obrysu jest załadowanie pliku PSD, który chcesz edytować.
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```
Po załadowaniu pliku PSD możesz teraz uzyskać dostęp do jego warstw i efektów oraz manipulować nimi.
## Krok 2: Przygotuj nowe dane wzorca
Następnie musisz przygotować nowe dane wzoru, które zastosujesz do warstwy obrysu.
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
Dane wzoru zostaną użyte do stworzenia nowego efektu obrysu.
## Krok 3: Uzyskaj dostęp do efektu obrysu
Aby zmodyfikować efekt obrysu, musisz uzyskać dostęp do określonej warstwy i jej opcji mieszania.
```java
StrokeEffect patternStroke = (StrokeEffect)im.getLayers()[3].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Normal, patternStroke.getBlendMode());
Assert.areEqual(255, patternStroke.getOpacity());
Assert.areEqual(true, patternStroke.isVisible());
PatternFillSettings fillSettings = (PatternFillSettings)patternStroke.getFillSettings();
Assert.areEqual(FillType.Pattern, fillSettings.getFillType());
```
Dzięki temu masz pewność, że pracujesz z właściwą warstwą i efektem.
## Krok 4: Zmodyfikuj efekt obrysu
Teraz zmodyfikujmy efekt obrysu za pomocą nowych danych wzoru.
### Zaktualizuj właściwości efektu obrysu
```java
patternStroke.setOpacity((byte)127);
patternStroke.setBlendMode(BlendMode.Color);
```
### Zaktualizuj zasób wzorca
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
Ten fragment kodu aktualizuje zasób wzorca przy użyciu nowych danych wzorca.
## Krok 5: Zastosuj nowy wzór
Na koniec zastosuj nowy wzór do efektu obrysu i zapisz zmiany.
```java
((PatternFillSettings)patternStroke.getFillSettings()).setPatternName("$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0");
((PatternFillSettings)patternStroke.getFillSettings()).setPatternId(guid.toString() + "\0");
im.save(exportPath);
```
Dzięki temu nowy wzór zostanie zastosowany poprawnie, a plik zostanie zapisany ze zmianami.
## Krok 6: Sprawdź zmiany
Aby upewnić się, że wszystko działa poprawnie, załaduj plik ponownie i sprawdź zmiany.
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
Ten krok sprawdza, czy dane wzoru zostały prawidłowo zastosowane do efektu obrysu.
## Wniosek
I masz to! Pomyślnie dodałeś wzór warstwy obrysu do pliku PSD przy użyciu Aspose.PSD dla Java. Wykonując poniższe kroki, możesz z łatwością dostosowywać i ulepszać swoje obrazy. Miłego kodowania!
## Często zadawane pytania
### Co to jest Aspose.PSD dla Java?
Aspose.PSD dla Java to biblioteka, która umożliwia programistom programowe tworzenie, edytowanie i konwertowanie plików PSD (dokument programu Photoshop).
### Czy mogę używać Aspose.PSD dla Java w projekcie komercyjnym?
 Tak, możesz go używać w projektach komercyjnych. Możesz kupić licencję od[Tutaj](https://purchase.aspose.com/buy).
### Czy dostępna jest bezpłatna wersja próbna Aspose.PSD dla Java?
 Tak, możesz pobrać bezpłatną wersję próbną ze strony[Tutaj](https://releases.aspose.com/).
### Jak mogę uzyskać wsparcie dla Aspose.PSD dla Java?
 Możesz uzyskać wsparcie na forach społeczności Aspose[Tutaj](https://forum.aspose.com/c/psd/34).
### Jakie są wymagania systemowe dla Aspose.PSD dla Java?
Potrzebujesz zainstalowanego JDK i IDE do programowania. Biblioteka obsługuje wiele systemów operacyjnych, w tym Windows, Linux i macOS.