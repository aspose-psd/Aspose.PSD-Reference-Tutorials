---
date: 2026-02-27
description: Dowiedz się, jak dostosować gamma w przetwarzaniu obrazów w Javie przy
  użyciu Aspose.PSD, konwertować pliki PSD na TIFF oraz naprawić wyblakłe obrazy w
  zwięzłym samouczku.
linktitle: Adjust Gamma of an Image
second_title: Aspose.PSD Java API
title: Jak dostosować gamma w przetwarzaniu obrazów w Javie przy użyciu Aspose.PSD
url: /pl/java/advanced-techniques/adjust-gamma/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak dostosować gamma w przetwarzaniu obrazów Java z Aspose.PSD

## Wprowadzenie

Jeśli pracujesz nad **przetwarzaniem obrazów w Javie**, nauka **jak dostosować gamma** jest podstawową techniką poprawiającą jasność i kontrast bez utraty szczegółów. W tym samouczku pokażemy, jak używać **Aspose.PSD for Java** do zastosowania korekcji gamma w pliku PSD, **konwersji PSD do TIFF**, oraz uniknięcia **przepalonego obrazu**. Zobaczysz, dlaczego to podejście jest szybkie, niezawodne i idealne dla serwerowych potoków obrazowych.

## Szybkie odpowiedzi
- **Co robi korekcja gamma?** Przekształca wartości luminancji, aby ciemne obszary stały się jaśniejsze, a jasne ciemniejsze, zachowując przy tym szczegóły.  
- **Która biblioteka obsługuje przetwarzanie?** Aspose.PSD for Java udostępnia dedykowaną metodę `adjustGamma` dla obrazów rastrowych.  
- **Czy mogę konwertować PSD do TIFF w tym samym przepływie?** Tak – po korekcji gamma możesz zapisać obraz bezpośrednio do TIFF używając `TiffOptions`.  
- **Czy potrzebna jest licencja do rozwoju?** Darmowa wersja próbna wystarczy do testów; licencja komercyjna jest wymagana w środowisku produkcyjnym.  
- **Jaką wersję Javy obsługuje?** Aspose.PSD wspiera Javę 8 i nowsze.

## Jak dostosować gamma w przetwarzaniu obrazów Java
Dostosowywanie gamma jest kluczowym elementem każdego **samouczka przetwarzania obrazów w Javie**, który dotyczy jasności lub kontrastu. Poniżej rozbijamy kroki, wyjaśniamy, dlaczego każda linia ma znaczenie, i pokazujemy, jak włączyć ten proces do istniejącego kodu.

## Co to jest korekcja gamma w Javie?
Korekcja gamma zmienia nieliniowy związek między zakodowanymi wartościami pikseli a wyświetlaną jasnością. Poprzez regulację krzywej gamma możesz **naprawić problemy z przepalonym obrazem** lub wydobyć szczegóły w cieniach bez prześwietlania jasnych partii.

## Dlaczego używać Aspose.PSD do korekcji gamma?
Aspose.PSD działa jako potężna **biblioteka przetwarzania obrazów w Javie**, ukrywająca złożoność formatu PSD. Obsługuje profile kolorów, buforowanie i oferuje prostą metodę `adjustGamma`, co czyni ją idealną do **korekcji gamma w Javie** oraz **konwersji PSD do TIFF**.

## Wymagania wstępne

1. **Środowisko programistyczne Java** – zainstalowana Java 8 lub nowsza.  
2. **Biblioteka Aspose.PSD** – pobierz i dodaj plik JAR do projektu. Zobacz oficjalną [dokumentację](https://reference.aspose.com/psd/java/).  
3. **Przykładowy obraz** – plik PSD, który chcesz przetworzyć (np. `sample.psd`).  

## Import pakietów

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## Krok 1: Załaduj obraz

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);

// Cast object of Image to RasterImage
RasterImage rasterImage = (RasterImage)image;

// Check if RasterImage is cached for better performance
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

**Wskazówka:** Buforowanie danych rastrowych jednorazowo zmniejsza obciążenie pamięci przy wielokrotnym stosowaniu poprawek.

## Krok 2: Dostosuj gamma

```java
// Adjust the gamma
rasterImage.adjustGamma(2.2f, 2.2f, 2.2f);
```

Możesz podać różne wartości dla kanałów czerwonego, zielonego i niebieskiego, jeśli potrzebujesz korekt specyficznych dla kanałów.

## Krok 3: Utwórz TiffOptions

```java
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

Ustawienie 8‑bitowego próbki (`{8,8,8}`) utrzymuje rozmiar pliku TIFF w rozsądnych granicach, zachowując jednocześnie wierność kolorów.

## Krok 4: Zapisz wynikowy obraz

```java
// Save the resultant image to TIFF format
String destName = dataDir + "AdjustGamma_out.tiff";
rasterImage.save(destName, tiffOptions);
```

Po zapisaniu możesz przekazać plik TIFF do kolejnych systemów, takich jak usługi drukowania czy API internetowe.

## Typowe przypadki użycia

- **Zautomatyzowane potoki graficzne** – Dostosuj gamma w locie przed generowaniem miniatur.  
- **Narzędzia do konwersji wsadowej** – Konwertuj duże archiwa PSD do TIFF, jednocześnie normalizując jasność.  
- **Usługi internetowe** – Udostępnij endpoint, który przyjmuje PSD, stosuje korekcję gamma i zwraca TIFF dla klienta.

## Typowe problemy i rozwiązania

| Problem | Dlaczego się pojawia | Jak naprawić |
|-------|----------------|------------|
| **Obraz wygląda na przepalony** | Zbyt wysoka wartość gamma (np. > 2,5) | Obniż współczynnik gamma do wartości między 1,8 a 2,2. |
| **`rasterImage.isCached()` zwraca false** | Obraz nie został jeszcze załadowany do pamięci | Wywołaj `rasterImage.cacheData()` przed dostosowaniem gamma. |
| **Rozmiar pliku TIFF jest duży** | Próbka ustawiona na 16‑bitową | Użyj 8‑bitowej próbki (`{8,8,8}`) jak w przykładzie. |

## Najczęściej zadawane pytania

**P: Czy mogę zastosować różne wartości gamma dla każdego kanału kolorów?**  
O: Tak – metoda `adjustGamma` przyjmuje osobne wartości typu float dla kanałów czerwonego, zielonego i niebieskiego.

**P: Czy można łączyć wiele poprawek obrazu przed zapisem?**  
O: Oczywiście. Możesz kolejno wykonywać zmianę rozmiaru, przycinanie lub korekcje kolorów na tym samym obiekcie `RasterImage`.

**P: Czy Aspose.PSD obsługuje pliki PSD wielostronicowe?**  
O: Tak, każdy warstwa może być dostępna i przetwarzana indywidualnie.

**P: Na jakie formaty mogę eksportować oprócz TIFF?**  
O: Aspose.PSD obsługuje PNG, JPEG, BMP i wiele innych formatów poprzez ich klasy opcji.

**P: Jak uniknąć przepalonego obrazu po korekcji gamma?**  
O: Zacznij od umiarkowanej wartości gamma (około 2,0) i podglądaj wynik; zmniejszaj wartość, jeśli obraz wydaje się zbyt jasny.

## Zakończenie

Gratulacje! Pomyślnie nauczyłeś się **jak dostosować gamma** w **przepływie przetwarzania obrazów w Javie**, skonwertowałeś PSD do TIFF i uniknąłeś typowych pułapek, takich jak **przepalony obraz**. Ten wzorzec daje precyzyjną kontrolę nad jasnością i kontrastem, co czyni go idealnym dla zautomatyzowanych potoków graficznych, usług internetowych lub aplikacji desktopowych.

---

**Ostatnia aktualizacja:** 2026-02-27  
**Testowano z:** Aspose.PSD 24.11 for Java  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}