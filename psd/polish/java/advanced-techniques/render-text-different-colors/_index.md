---
date: 2026-05-29
description: Dowiedz się, jak zapisać plik PSD jako PNG z kolorowym tekstem przy użyciu
  Aspose.PSD for Java. Ten przewodnik krok po kroku pokazuje, jak efektywnie konwertować
  PSD na PNG.
keywords:
- save psd as png
- convert psd to png
- Aspose.PSD Java
linktitle: Renderowanie tekstu w różnych kolorach w warstwie tekstowej
schemas:
- author: Aspose
  dateModified: '2026-05-29'
  description: Learn how to save PSD as PNG with colored text using Aspose.PSD for
    Java. This step‑by‑step guide shows how to convert PSD to PNG efficiently.
  headline: Save PSD as PNG with Colored Text using Aspose.PSD for Java
  type: TechArticle
- questions:
  - answer: Aspose.PSD is primarily designed for Java, but Aspose provides similar
      libraries for various programming languages.
    question: Can I use Aspose.PSD for Java with other programming languages?
  - answer: Yes, you can obtain a free trial version from [Aspose.PSD](https://releases.aspose.com/).
    question: Is there a trial version available for Aspose.PSD for Java?
  - answer: Visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) for community
      support and discussions.
    question: Where can I find additional support or assistance?
  - answer: You can request a temporary license from [Aspose.PSD](https://purchase.aspose.com/temporary-license/).
    question: How can I obtain a temporary license for Aspose.PSD for Java?
  - answer: Yes, explore the [Aspose.PSD documentation](https://reference.aspose.com/psd/java/)
      for more tutorials and examples.
    question: Are there other tutorials available for Aspose.PSD?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Zapisz plik PSD jako PNG z kolorowym tekstem przy użyciu Aspose.PSD for Java
url: /pl/java/advanced-techniques/render-text-different-colors/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Zapisz PSD jako PNG z kolorowym tekstem przy użyciu Aspose.PSD dla Javy

Witamy w naszym przewodniku krok po kroku, jak **zapisz PSD jako PNG** z tekstem w różnych kolorach przy użyciu Aspose.PSD dla Javy. Aspose.PSD to potężna biblioteka Java, która umożliwia programowe manipulowanie plikami Photoshop, zapewniając rozbudowane możliwości pracy z formatami plików PSD i PSB.

W tym samouczku przeprowadzimy Cię przez proces renderowania tekstu w różnych kolorach w warstwie tekstowej przy użyciu Aspose.PSD. Po zakończeniu tego przewodnika będziesz mieć jasne zrozumienie, jak bezproblemowo wykonać to zadanie.

## Szybkie odpowiedzi
- **Jak zapisać PSD jako PNG?** Użyj klasy `PsdImage` z Aspose.PSD, aby załadować plik PSD i wywołać `save` z `PngOptions`.
- **Czy mogę renderować wiele kolorów w jednej warstwie tekstowej?** Tak, przypisz różne obiekty `Color` do każdej `Portion` tekstu.
- **Jaka wersja Javy jest wymagana?** Obsługiwana jest Java 8 lub nowsza.
- **Czy potrzebna jest licencja do produkcji?** Wymagana jest licencja komercyjna; dostępna jest darmowa wersja próbna.
- **Czy biblioteka jest efektywna pamięciowo przy dużych plikach?** Może obsługiwać pliki do 2 GB bez pełnego ładowania do pamięci.

## Jak zapisać PSD jako PNG z kolorowym tekstem?

Załaduj plik PSD, zmodyfikuj fragmenty warstwy tekstowej, aby przypisać różne kolory, a następnie zapisz obraz jako PNG — cały ten przepływ pracy odbywa się w kilku linijkach kodu Java. Aspose.PSD automatycznie rasteryzuje edytowaną warstwę, zachowując przezroczystość i wierność kolorów, dzięki czemu powstały PNG odpowiada pierwotnemu projektowi.

## Czym jest Aspose.PSD dla Javy?

Aspose.PSD dla Javy to biblioteka umożliwiająca programowe tworzenie, edycję i konwersję plików Photoshop (PSD/PSB). Obsługuje **ponad 50 formatów obrazów** i może przetwarzać dokumenty liczące setki stron bez ładowania całego pliku do pamięci, zapewniając wysoką wydajność automatyzacji po stronie serwera.

## Wymagania wstępne

- Podstawowa znajomość programowania w Javie.
- Zainstalowana biblioteka Aspose.PSD dla Javy. Możesz ją pobrać z [Aspose.PSD for Java documentation](https://reference.aspose.com/psd/java/).

## Importowanie pakietów

`Image` jest klasą bazową do ładowania i zapisywania plików obrazów. `PsdImage` reprezentuje dokument Photoshop, natomiast `TextLayer` zapewnia dostęp do właściwości warstwy tekstowej. `PngOptions` definiuje ustawienia eksportu PNG.  
```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.TextLayer;
import com.aspose.psd.imageoptions.PngOptions;
```

## Krok 1: Skonfiguruj swój projekt

Utwórz nowy projekt Java i dołącz bibliotekę Aspose.PSD. Upewnij się, że masz niezbędne uprawnienia do dostępu i modyfikacji plików w katalogu projektu.

## Krok 2: Zdefiniuj katalogi źródłowy i wyjściowy

Określ katalogi źródłowy i wyjściowy, w których znajdują się pliki PSD oraz gdzie zostaną zapisane powstałe obrazy. Zaktualizuj zmienne `sourceDir` i `outputDir` odpowiednio.  
```java
String sourceDir = "Your Document Directory";
String outputDir = "Your Document Directory";
```

## Krok 3: Załaduj plik PSD i uzyskaj dostęp do warstwy tekstowej

`PsdImage` ładuje plik PSD do pamięci, a `TextLayer` umożliwia manipulację treścią tekstu w tej warstwie.  
```java
String targetFilePath = sourceDir + "text_ethalon_different_colors.psd";
String resultFilePath = outputDir + "RenderTextWithDifferentColorsInTextLayer_out.png";

PsdImage psdImage = null;
try
{
    psdImage = (PsdImage) Image.load(targetFilePath);
    TextLayer txtLayer = (TextLayer)psdImage.getLayers()[1];
    txtLayer.getTextData().updateLayerData();
```

## Krok 4: Ustaw opcje PNG i zapisz powstały obraz

`PngOptions` konfiguruje parametry wyjściowe PNG, takie jak typ koloru i kompresja.  
```java
    PngOptions pngOptions = new PngOptions();
    pngOptions.setColorType(PngColorType.TruecolorWithAlpha);
    psdImage.save(resultFilePath, pngOptions);
}
finally
{
    if (psdImage != null) psdImage.dispose();
}
```

## Typowe problemy i rozwiązania

- **Brak licencji (exception):** Upewnij się, że zastosowano prawidłowy plik licencji przed wywołaniem jakiejkolwiek operacji zapisu.  
- **Kolor nie zastosowany:** Sprawdź, czy każda `Portion` w warstwie tekstowej ma poprawnie ustawioną właściwość `Color`.  
- **Użycie pamięci przy dużych plikach:** Użyj przeciążenia `load` klasy `PsdImage` z `loadOptions`, aby strumieniowo przetwarzać duże pliki.

## Najczęściej zadawane pytania

**Q: Czy mogę używać Aspose.PSD dla Javy z innymi językami programowania?**  
A: Aspose.PSD jest głównie przeznaczony dla Javy, ale Aspose udostępnia podobne biblioteki dla różnych języków programowania.

**Q: Czy dostępna jest wersja próbna Aspose.PSD dla Javy?**  
A: Tak, możesz uzyskać darmową wersję próbną z [Aspose.PSD](https://releases.aspose.com/).

**Q: Gdzie mogę znaleźć dodatkowe wsparcie lub pomoc?**  
A: Odwiedź [forum Aspose.PSD](https://forum.aspose.com/c/psd/34) w celu uzyskania wsparcia społeczności i dyskusji.

**Q: Jak mogę uzyskać tymczasową licencję dla Aspose.PSD dla Javy?**  
A: Możesz poprosić o tymczasową licencję na [Aspose.PSD](https://purchase.aspose.com/temporary-license/).

**Q: Czy dostępne są inne samouczki dotyczące Aspose.PSD?**  
A: Tak, zapoznaj się z [dokumentacją Aspose.PSD](https://reference.aspose.com/psd/java/) aby znaleźć więcej samouczków i przykładów.

**Q: Czy biblioteka obsługuje konwersję wsadową wielu plików PSD do PNG?**  
A: Tak, możesz iterować po folderze z plikami PSD, zastosować tę samą logikę kolorów tekstu i zapisać każdy jako PNG przy użyciu pętli.

**Q: Czy wyjściowy PNG jest bezstratny?**  
A: PNG zapisany przy użyciu Aspose.PSD zachowuje pełną jakość bezstratną, utrzymując wszystkie informacje o kolorze i przezroczystości.

---

**Ostatnia aktualizacja:** 2026-05-29  
**Testowano z:** Aspose.PSD 24.12 for Java  
**Autor:** Aspose

{{< blocks/products/products-backtop-button >}}

## Powiązane samouczki

- [Eksportuj PSD do PNG i dodaj nową warstwę zwykłą przy użyciu Aspose.PSD dla Javy](/psd/java/advanced-image-effects/add-new-regular-layer/)
- [Zapisz PSD jako PNG i zastosuj renderowanie cienia padającego w Aspose.PSD dla Javy](/psd/java/advanced-image-manipulation/rendering-drop-shadow/)
- [Konwertuj PSD do PNG z nakładką kolorystyczną – Aspose.PSD dla Javy](/psd/java/advanced-image-manipulation/rendering-color-effect/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}