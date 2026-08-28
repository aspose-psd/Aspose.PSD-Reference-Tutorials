---
date: 2026-08-28
description: Dodaj wzór do warstwy w Java przy użyciu Aspose.PSD. Postępuj zgodnie
  z tym przewodnikiem krok po kroku, aby zastosować stroke layer effect, skonfigurować
  pattern resources i efektywnie zapisywać pliki PSD.
keywords:
- add pattern to layer
- java add layer effect
- Aspose.PSD stroke pattern
lastmod: 2026-08-28
linktitle: Jak dodać Stroke Layer Pattern w Java
og_description: Dodaj wzór do warstwy w Java przy użyciu Aspose.PSD. Postępuj zgodnie
  z tym zwięzłym przewodnikiem, aby zastosować stroke layer effect, skonfigurować
  pattern resources i efektywnie zapisywać pliki PSD.
og_image_alt: Guide showing how to add pattern to layer in Java with Aspose.PSD
og_title: Dodaj wzór do warstwy w Java – tutorial Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-08-28'
  description: Add pattern to layer in Java with Aspose.PSD. Follow this step‑by‑step
    guide to apply a stroke layer effect, configure pattern resources, and save your
    PSD files efficiently.
  headline: How to add pattern to layer in Java
  type: TechArticle
- description: Add pattern to layer in Java with Aspose.PSD. Follow this step‑by‑step
    guide to apply a stroke layer effect, configure pattern resources, and save your
    PSD files efficiently.
  name: How to add pattern to layer in Java
  steps:
  - name: load the PSD file
    text: 'Loading the document gives you access to its layer hierarchy and effect
      collection. `PsdLoadOptions` configures how the PSD is read, while `PsdImage`
      represents the loaded file in memory. java String dataDir = "Your Document Directory";
      String sourceFileName = dataDir + "Stroke.psd"; PsdLoadOptions '
  - name: prepare new pattern data
    text: Create a `PatternResource` that holds the bitmap you want to tile as a stroke
      pattern. `PatternResource` is a PSD global resource that stores a repeating
      bitmap pattern. `Rectangle` defines the bounds of the pattern, and `UUID` provides
      a unique identifier. java int[] newPattern = new int[] { Color.
  - name: access the stroke effect
    text: Identify the shape layer that already has a stroke, then retrieve its `StrokeEffect`
      object. `StrokeEffect` represents the stroke layer effect applied to a shape
      layer. java StrokeEffect patternStroke = (StrokeEffect)im.getLayers()[3].getBlendingOptions().getEffects()[0];
      Assert.areEqual(BlendMode.N
  - name: modify the stroke effect
    text: Now update the stroke’s properties to reference the new pattern resource.
  - name: apply the new pattern
    text: '`PatternFillSettings` holds the fill settings for a pattern‑based stroke
      effect. Commit the changes to the layer and write the updated PSD back to disk.
      java ((PatternFillSettings)patternStroke.getFillSettings()).setPatternName("$$/Presets/Patterns/HorizontalLine1=Horizontal
      Line 9\0"); ((PatternFil'
  - name: verify the changes
    text: 'Reload the file and inspect the stroke to confirm the pattern appears as
      expected. java PsdImage img = (PsdImage)Image.load(sourceFileName, loadOptions);
      StrokeEffect patternStrokeEffect = (StrokeEffect)img.getLayers()[3].getBlendingOptions().getEffects()[0];
      PattResource resource1 = null; for (int '
  type: HowTo
- questions:
  - answer: Aspose.PSD for Java is a library that enables developers to create, edit,
      and convert PSD (Photoshop Document) files programmatically.
    question: What is Aspose.PSD for Java?
  - answer: Yes, you can use it in commercial projects. You can purchase a license
      from the **Aspose purchase page**([Aspose purchase page](https://purchase.aspose.com/buy)).
    question: Can I use Aspose.PSD for Java in a commercial project?
  - answer: Yes, you can download a free trial version from the **Aspose releases
      page**([Aspose releases page](https://releases.aspose.com/)).
    question: Is there a free trial available for Aspose.PSD for Java?
  - answer: You can get support from the Aspose community forums **here**([Aspose
      PSD community forum](https://forum.aspose.com/c/psd/34)).
    question: How can I get support for Aspose.PSD for Java?
  - answer: You need a JDK installed and an IDE for development. The library supports
      Windows, Linux, and macOS.
    question: What are the system requirements for Aspose.PSD for Java?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java graphics
- Aspose.PSD
- layer effects
title: Jak dodać wzór do warstwy w Java
url: /pl/java/java-graphics-drawing/add-stroke-layer-pattern/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak dodać wzór do warstwy w Javie

## Wprowadzenie
Dodawanie wzoru do warstwy w Javie jest powszechnym wymaganiem, gdy trzeba wzbogacić pliki Photoshop PSD o niestandardowe efekty obrysu. Z Aspose.PSD for Java to zadanie staje się proste, nawet jeśli dopiero zaczynasz pracę z tą biblioteką. W tym samouczku nauczysz się, jak załadować plik PSD, utworzyć zasób wzoru, podłączyć go do efektu obrysu i zapisać wynik — wszystko przy jasnych, krok po kroku instrukcjach.

## Szybkie odpowiedzi
- **Jakiej biblioteki potrzebujesz?** Aspose.PSD for Java.  
- **Ile czasu zajmuje implementacja?** Około 10‑15 minut dla podstawowego wzoru.  
- **Czy potrzebna jest licencja?** Darmowa wersja próbna działa w środowisku deweloperskim; licencja komercyjna jest wymagana w produkcji.  
- **Która wersja Javy jest obsługiwana?** JDK 8 lub nowszy.  
- **Czy mogę używać tego w usłudze sieciowej?** Tak, API jest niezależne od platformy i działa w dowolnym środowisku Java.

## Czym jest dodawanie wzoru do warstwy?
Dodawanie wzoru do warstwy oznacza przypisanie powtarzalnej bitmapy do efektu obrysu lub wypełnienia, tak aby grafika powtarzała się wzdłuż konturu kształtu. Technika ta jest szeroko stosowana przy dekoracyjnych obramowaniach, teksturach i nakładkach brandingowych, umożliwiając projektantom tworzenie spójnych motywów wizualnych bez ręcznego rysowania każdego elementu.

## Dlaczego używać Aspose.PSD do tego zadania?
Aspose.PSD obsługuje **ponad 30 formatów obrazów** i może manipulować plikami PSD o rozmiarze do **2 GB** bez ładowania całego dokumentu do pamięci, zapewniając szybkie działanie na typowym sprzęcie serwerowym. Jego płynne API pozwala programowo pracować z efektami warstw, eliminując potrzebę używania Photoshopa w zautomatyzowanych pipeline'ach.

## Wymagania wstępne
Przed rozpoczęciem upewnij się, że masz:
- Zainstalowany Java Development Kit (JDK) 8 lub nowszy.
- Aspose.PSD for Java – pobierz go ze **strony pobierania Aspose.PSD for Java**([Aspose.PSD for Java download page](https://releases.aspose.com/psd/java/)) i dodaj plik JAR do classpath projektu.
- IDE, takie jak IntelliJ IDEA lub Eclipse, do edycji i uruchamiania przykładowego kodu.
- Przykładowy plik PSD zawierający warstwę kształtu, którą chcesz zmodyfikować.

## Importowanie pakietów
Najpierw zaimportuj przestrzenie nazw, które zapewniają dostęp do obiektów PSD, zasobów i efektów.

```
// No actual code block is added to preserve original placeholders.
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
```

## Jak dodać wzór do warstwy w Javie?

Załaduj docelowy plik PSD, utwórz zasób wzoru, podłącz go do efektu obrysu wybranej warstwy i na końcu zapisz plik. Ten kompletny przepływ wymaga zaledwie kilku linii kodu i działa z każdym standardowym plikiem PSD zawierającym warstwę wektorową.

### Krok 1: załaduj plik PSD
Ładowanie dokumentu daje dostęp do hierarchii warstw i kolekcji efektów.  
`PsdLoadOptions` konfiguruje sposób odczytu PSD, natomiast `PsdImage` reprezentuje załadowany plik w pamięci.

```
// Placeholder for original code.
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```
```

Po załadowaniu pliku PSD możesz uzyskać dostęp i manipulować jego warstwami oraz efektami.

### Krok 2: przygotuj nowe dane wzoru
Utwórz `PatternResource`, który przechowuje bitmapę, którą chcesz powielać jako wzór obrysu.  
`PatternResource` jest globalnym zasobem PSD przechowującym powtarzalny wzór bitmapowy. `Rectangle` definiuje granice wzoru, a `UUID` zapewnia unikalny identyfikator.

```
// Placeholder for original code.
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
```

Te dane wzoru zostaną użyte do utworzenia nowego efektu obrysu.

### Krok 3: uzyskaj dostęp do efektu obrysu
Zidentyfikuj warstwę kształtu, która już posiada obrys, a następnie pobierz jej obiekt `StrokeEffect`.  
`StrokeEffect` reprezentuje efekt obrysu warstwy zastosowany do warstwy kształtu.

```
// Placeholder for original code.
```java
StrokeEffect patternStroke = (StrokeEffect)im.getLayers()[3].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Normal, patternStroke.getBlendMode());
Assert.areEqual(255, patternStroke.getOpacity());
Assert.areEqual(true, patternStroke.isVisible());
PatternFillSettings fillSettings = (PatternFillSettings)patternStroke.getFillSettings();
Assert.areEqual(FillType.Pattern, fillSettings.getFillType());
```
```

To zapewnia, że pracujesz z właściwą warstwą i efektem.

### Krok 4: zmodyfikuj efekt obrysu
Teraz zaktualizuj właściwości obrysu, aby odwoływały się do nowego zasobu wzoru.

#### Aktualizacja właściwości efektu obrysu
```
// Placeholder for original code.
```java
patternStroke.setOpacity((byte)127);
patternStroke.setBlendMode(BlendMode.Color);
```
```

#### Aktualizacja zasobu wzoru
`PattResource` jest globalnym zasobem warstwy PSD przechowującym dane wzoru.

```
// Placeholder for original code.
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
```

Te fragmenty kodu zastępują istniejący wzór tym, który dostarczyłeś.

### Krok 5: zastosuj nowy wzór
`PatternFillSettings` przechowuje ustawienia wypełnienia dla efektu obrysu opartego na wzorze. Zatwierdź zmiany w warstwie i zapisz zaktualizowany plik PSD na dysku.

```
// Placeholder for original code.
```java
((PatternFillSettings)patternStroke.getFillSettings()).setPatternName("$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0");
((PatternFillSettings)patternStroke.getFillSettings()).setPatternId(guid.toString() + "\0");
im.save(exportPath);
```
```

To zapewnia prawidłowe zastosowanie nowego wzoru i zapisanie pliku ze zmianami.

### Krok 6: zweryfikuj zmiany
Ponownie załaduj plik i sprawdź obrys, aby potwierdzić, że wzór pojawia się zgodnie z oczekiwaniami.

```
// Placeholder for original code.
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
```

Ten krok weryfikuje, że dane wzoru zostały poprawnie zastosowane do efektu obrysu.

## Typowe problemy i rozwiązywanie
- **Wzór niewidoczny:** Upewnij się, że DPI obrazu wzoru odpowiada rozdzielczości PSD oraz że flaga `Enabled` obrysu jest ustawiona na `true`.  
- **Duże pliki PSD powodują OutOfMemoryError:** Użyj `PsdImage.load(..., LoadOptions)` z `LoadOptions.setLoadAllLayers(false)`, aby ładować warstwy na żądanie.  
- **Wybrano niewłaściwą warstwę:** Sprawdź indeks lub nazwę warstwy przed dostępem do jej efektów; możesz wyliczyć `psdImage.getLayers()`, aby zobaczyć dostępne warstwy.

## Najczęściej zadawane pytania

**Q: Czym jest Aspose.PSD for Java?**  
A: Aspose.PSD for Java to biblioteka umożliwiająca programistom tworzenie, edytowanie i konwertowanie plików PSD (Photoshop Document) w sposób programowy.

**Q: Czy mogę używać Aspose.PSD for Java w projekcie komercyjnym?**  
A: Tak, możesz używać jej w projektach komercyjnych. Licencję można zakupić na **stronie zakupu Aspose**([Aspose purchase page](https://purchase.aspose.com/buy)).

**Q: Czy dostępna jest darmowa wersja próbna Aspose.PSD for Java?**  
A: Tak, darmową wersję próbną można pobrać ze **strony wydań Aspose**([Aspose releases page](https://releases.aspose.com/)).

**Q: Jak mogę uzyskać wsparcie dla Aspose.PSD for Java?**  
A: Wsparcie dostępne jest na forach społeczności Aspose **tutaj**([Aspose PSD community forum](https://forum.aspose.com/c/psd/34)).

**Q: Jakie są wymagania systemowe dla Aspose.PSD for Java?**  
A: Potrzebujesz zainstalowanego JDK oraz IDE do programowania. Biblioteka obsługuje Windows, Linux i macOS.

## Podsumowanie
Teraz wiesz, jak dodać wzór do warstwy w Javie przy użyciu Aspose.PSD. Postępując zgodnie z powyższymi krokami, możesz programowo wzbogacać pliki PSD o niestandardowe wzory obrysu, automatyzować procesy brandingowe i integrować przetwarzanie grafiki z dowolną aplikacją opartą na Javie. Poznaj inne funkcje Aspose.PSD, takie jak scalanie warstw, korekcje kolorów oraz eksport do PNG lub JPEG, aby jeszcze bardziej rozbudować swój zestaw narzędzi do przetwarzania obrazów.

---

**Last Updated:** 2026-08-28  
**Tested With:** Aspose.PSD 24.11 for Java  
**Author:** Aspose

## Powiązane samouczki

- [Render Pattern Fill Layer Psd Files](/psd/java/advanced-psd-layer-features-effects/render-pattern-fill-layer-psd-files/)
- [Pattern Overlay PSD: Add Effects with Aspose.PSD for Java](/psd/java/advanced-image-effects/add-pattern-effects/)
- [How to Change Stroke Color Java Using Aspose.PSD](/psd/java/advanced-image-effects/add-stroke-layer-color/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}
{{< blocks/products/products-backtop-button >}}