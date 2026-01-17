---
date: 2026-01-17
description: Dowiedz się, jak dodać wzór obrysu w Javie przy użyciu Aspose.PSD for
  Java. Postępuj zgodnie z tym przewodnikiem krok po kroku, aby szybko ulepszyć swoje
  obrazy PSD.
linktitle: How to Add Stroke Layer Pattern in Java
second_title: Aspose.PSD Java API
title: Jak dodać wzór obrysu w Javie przy użyciu Aspose.PSD
url: /pl/java/java-graphics-drawing/add-stroke-layer-pattern/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak dodać wzór obramowania w Javie przy użyciu Aspose.PSD

## Wprowadzenie
Jeśli potrzebujesz **dodać wzór obramowania w Javie** do pliku Photoshop, Aspose.PSD for Java czyni to zadanie zaskakująco prostym. Niezależnie od tego, czy tworzysz narzędzie do projektowania graficznego, automatyzujesz masowe edycje, czy po prostu eksperymentujesz z efektami warstw, ten samouczek przeprowadzi Cię przez każdy krok — od załadowania pliku PSD po weryfikację nowego wzoru. Zanurzmy się i zobaczmy, jak szybko możesz wzbogacić swoje obrazy.

## Szybkie odpowiedzi
- **Jakiej biblioteki potrzebuję?** Aspose.PSD for Java  
- **Która wersja Javy jest obsługiwana?** JDK 8 lub nowszy  
- **Czy potrzebna jest licencja do testów?** Darmowa wersja próbna wystarczy do rozwoju; licencja jest wymagana w produkcji  
- **Jak długo trwa implementacja?** Około 10‑15 minut dla podstawowego wzoru obramowania  
- **Czy mogę ponownie użyć wzoru na wielu warstwach?** Tak, wystarczy przypisać ten sam `PattResource` do innych warstw  

## Co to jest dodawanie wzoru obramowania w Javie?
Dodanie wzoru obramowania w Javie oznacza zastosowanie niestandardowego wypełnienia (często powtarzającego się bitmapu) do efektu obramowania warstwy. Technika ta pozwala tworzyć stylizowane kontury — myśl o przerywanej linii, fakturze cegieł lub własnej ramce graficznej — bezpośrednio w pliku PSD, bez otwierania Photoshopa.

## Dlaczego używać Aspose.PSD do dodawania wzoru obramowania w Javie?
- **Pełna wierność PSD** – Wszystkie efekty warstw, zasoby i tryby mieszania są zachowane.  
- **Brak wymogu natywnego Photoshopa** – Działa na każdym systemie operacyjnym z JDK.  
- **Kontrola programistyczna** – Automatyzuj przetwarzanie wsadowe lub integruj z usługami po stronie serwera.  
- **Bogate API** – Dostęp do zasobów globalnych, wypełnień wzorami i trybów mieszania w jednej spójnej interfejsie.

## Wymagania wstępne
- **Java Development Kit (JDK)** – Upewnij się, że masz zainstalowany JDK 8 lub nowszy.  
- **Aspose.PSD for Java** – Pobierz bibliotekę z [here](https://releases.aspose.com/psd/java/) i dodaj plik JAR do classpathu projektu.  
- **IDE** – IntelliJ IDEA, Eclipse lub dowolny edytor, którego używasz.

## Importowanie pakietów
Najpierw zaimportuj klasy potrzebne do obsługi plików PSD, kolorów, prostokątów i efektów obramowania.

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
Załaduj źródłowy plik PSD, aby móc pracować z jego warstwami i zasobami.

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

## Krok 2: Przygotuj nowe dane wzoru
Utwórz prosty wzór 4 × 4 piksele, który zostanie użyty do obramowania.

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

## Krok 3: Uzyskaj dostęp do efektu obramowania
Zlokalizuj efekt obramowania na docelowej warstwie (w tym przykładzie na czwartej warstwie).

```java
StrokeEffect patternStroke = (StrokeEffect)im.getLayers()[3].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Normal, patternStroke.getBlendMode());
Assert.areEqual(255, patternStroke.getOpacity());
Assert.areEqual(true, patternStroke.isVisible());
PatternFillSettings fillSettings = (PatternFillSettings)patternStroke.getFillSettings();
Assert.areEqual(FillType.Pattern, fillSettings.getFillType());
```

## Krok 4: Zmodyfikuj efekt obramowania
### Aktualizacja właściwości efektu obramowania
Dostosuj krycie i tryb mieszania, aby zobaczyć wizualny wpływ nowego wzoru.

```java
patternStroke.setOpacity((byte)127);
patternStroke.setBlendMode(BlendMode.Color);
```

### Aktualizacja zasobu wzoru
Zastąp istniejący globalny zasób wzoru tym, który właśnie utworzyłeś.

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

## Krok 5: Zastosuj nowy wzór
Połącz zaktualizowany zasób wzoru z efektem obramowania i zapisz plik PSD.

```java
((PatternFillSettings)patternStroke.getFillSettings()).setPatternName("$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0");
((PatternFillSettings)patternStroke.getFillSettings()).setPatternId(guid.toString() + "\0");
im.save(exportPath);
```

## Krok 6: Zweryfikuj zmiany
Wczytaj ponownie plik i potwierdź, że nowy wzór, krycie i tryb mieszania zostały poprawnie zastosowane.

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

## Typowe problemy i rozwiązania
| Problem | Przyczyna | Rozwiązanie |
|---------|-----------|-------------|
| Wzór nie pojawia się | Nieprawidłowe odwołanie `PatternId` | Upewnij się, że `PatternId` ustawiony w `PattResource` odpowiada temu używanemu w `PatternFillSettings`. |
| Obramowanie znika po zapisaniu | Krycie ustawione na 0 lub efekt ukryty | Sprawdź, czy `setOpacity` ma wartość od 0‑255 oraz czy `isVisible()` zwraca `true`. |
| Nieoczekiwane kolory | Niepasujący tryb mieszania | Użyj `BlendMode.Color` (lub innego trybu), który odpowiada zamierzonemu efektowi. |

## FAQ
### Co to jest Aspose.PSD dla Javy?
Aspose.PSD for Java to biblioteka umożliwiająca programistom tworzenie, edytowanie i konwertowanie plików PSD (Photoshop Document) w sposób programowy.

### Czy mogę używać Aspose.PSD dla Javy w projekcie komercyjnym?
Tak, możesz używać jej w projektach komercyjnych. Licencję można zakupić [here](https://purchase.aspose.com/buy).

### Czy dostępna jest darmowa wersja próbna Aspose.PSD dla Javy?
Tak, darmową wersję próbną można pobrać [here](https://releases.aspose.com/).

### Jak mogę uzyskać wsparcie dla Aspose.PSD dla Javy?
Wsparcie dostępne jest na forach społeczności Aspose [here](https://forum.aspose.com/c/psd/34).

### Jakie są wymagania systemowe dla Aspose.PSD dla Javy?
Potrzebujesz zainstalowanego JDK oraz IDE do programowania. Biblioteka obsługuje wiele systemów operacyjnych, w tym Windows, Linux i macOS.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Ostatnia aktualizacja:** 2026-01-17  
**Testowano z:** Aspose.PSD for Java 24.12 (najnowsza w momencie pisania)  
**Autor:** Aspose