---
date: 2025-12-21
description: Dowiedz się, jak wykonywać przetwarzanie obrazów w języku Java, regulując
  gamma obrazu za pomocą Aspose.PSD. Przewodnik krok po kroku, jak konwertować pliki
  PSD na TIFF i zastosować korekcję gamma.
linktitle: Adjust Gamma of an Image
second_title: Aspose.PSD Java API
title: Przetwarzanie obrazów w Javie – regulacja gamma przy użyciu Aspose.PSD
url: /pl/java/advanced-techniques/adjust-gamma/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Przetwarzanie obrazów w Javie – Regulacja gamma przy użyciu Aspose.PSD

## Wprowadzenie

Jeśli pracujesz nad **java image processing**, regulacja gamma obrazu jest podstawową techniką poprawy jasności i kontrastu bez utraty szczegółów. W tym samouczku pokażemy, jak używać **Aspose.PSD for Java**, aby zastosować korekcję gamma do pliku PSD, a następnie wyeksportować wynik jako obraz TIFF. Zobaczysz, dlaczego to podejście jest szybkie, niezawodne i idealne dla serwerowych potoków przetwarzania obrazów.

## Szybkie odpowiedzi
- **Co robi korekcja gamma?** Przekształca wartości luminancji, aby ciemne obszary stały się jaśniejsze, a jasne ciemniejsze, zachowując ogólne szczegóły.  
- **Która biblioteka obsługuje przetwarzanie?** Aspose.PSD for Java udostępnia dedykowaną metodę `adjustGamma` dla obrazów rastrowych.  
- **Czy mogę przekonwertować PSD na TIFF w tym samym procesie?** Tak – po regulacji gamma możesz zapisać obraz bezpośrednio jako TIFF używając `TiffOptions`.  
- **Czy potrzebuję licencji do rozwoju?** Darmowa wersja próbna wystarcza do testów; licencja komercyjna jest wymagana w środowisku produkcyjnym.  
- **Jaką wersję Javy obsługuje?** Aspose.PSD obsługuje Javę 8 i nowsze.

## Czym jest java image processing?

Java image processing odnosi się do manipulacji, analizy i przekształcania danych wizualnych przy użyciu bibliotek Java. Zadania obejmują zmianę rozmiaru, filtrowanie, korekcję kolorów i konwersję formatów — wszystko to może być zautomatyzowane w aplikacjach desktopowych lub webowych.

## Dlaczego używać Aspose.PSD do korekcji gamma?

Aspose.PSD oferuje API wysokiego poziomu, które ukrywa złożoność formatu PSD, pozwalając skupić się na rzeczywistych korektach obrazu. Obsługuje buforowanie, profile kolorów i udostępnia prostą metodę `adjustGamma`, co czyni go idealnym dla **image gamma correction** oraz **convert psd to tiff** w przepływach pracy.

## Wymagania wstępne

Zanim zanurzysz się w samouczek, upewnij się, że masz przygotowane następujące wymagania wstępne:

1. **Java Development Environment** – Upewnij się, że masz zainstalowane środowisko programistyczne Java na swoim systemie.  
2. **Aspose.PSD Library** – Pobierz i zintegrować bibliotekę Aspose.PSD w swoim projekcie Java. Niezbędne zasoby znajdziesz w [documentation](https://reference.aspose.com/psd/java/).  
3. **Sample Image** – Przygotuj przykładowy obraz PSD, którego użyjesz do zastosowania regulacji gamma.

## Importowanie pakietów

Aby rozpocząć proces, zaimportuj wymagane pakiety w swoim projekcie Java. To przygotuje środowisko do płynnego korzystania z funkcjonalności Aspose.PSD.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## Krok 1: Załaduj obraz

Zacznij od załadowania przykładowego obrazu PSD do instancji klasy `RasterImage`. To podstawa dla kolejnych regulacji gamma.

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

## Krok 2: Regulacja gamma

Teraz, dostosuj gamma załadowanego obrazu przy użyciu metody `adjustGamma`. Dostosuj wartości gamma zgodnie z wymaganiami.

```java
// Adjust the gamma
rasterImage.adjustGamma(2.2f, 2.2f, 2.2f);
```

## Krok 3: Utwórz TiffOptions

Utwórz instancję `TiffOptions` dla wynikowego obrazu. Ustaw różne właściwości, takie jak liczba bitów na próbkę oraz opcje fotometryczne, aby dopasować wyjście do swoich specyfikacji.

```java
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

## Krok 4: Zapisz wynikowy obraz

Zapisz zmodyfikowany obraz w formacie TIFF, używając wcześniej zdefiniowanego `TiffOptions`.

```java
// Save the resultant image to TIFF format
String destName = dataDir + "AdjustGamma_out.tiff";
rasterImage.save(destName, tiffOptions);
```

## Częste problemy i rozwiązania

| Problem | Dlaczego się pojawia | Jak naprawić |
|---------|----------------------|--------------|
| **Obraz jest wyblakły** | Wartość gamma jest za wysoka (np. > 2,5) | Obniż współczynnik gamma do wartości pomiędzy 1,8 a 2,2. |
| **`rasterImage.isCached()` zwraca false** | Obraz nie został jeszcze załadowany do pamięci | Wywołaj `rasterImage.cacheData()` przed regulacją gamma. |
| **Rozmiar pliku TIFF jest duży** | Liczba bitów na próbkę ustawiona na 16‑bit | Użyj 8‑bitowej próbki (`{8,8,8}`) jak pokazano w przykładzie. |

## Najczęściej zadawane pytania

**Q: Czy mogę zastosować różne wartości gamma dla każdego kanału kolorów?**  
A: Tak – metoda `adjustGamma` przyjmuje oddzielne wartości typu float dla kanałów czerwonego, zielonego i niebieskiego.

**Q: Czy można łączyć wiele korekt obrazu przed zapisem?**  
A: Oczywiście. Możesz kolejno wykonywać zmianę rozmiaru, przycinanie lub korekcje kolorów na tej samej instancji `RasterImage`.

**Q: Czy Aspose.PSD obsługuje wielostronicowe pliki PSD?**  
A: Tak, każda warstwa może być dostępna i przetwarzana indywidualnie.

**Q: Do jakich formatów mogę eksportować oprócz TIFF?**  
A: Aspose.PSD obsługuje PNG, JPEG, BMP i wiele innych formatów poprzez odpowiednie klasy opcji.

## Zakończenie

Gratulacje! Pomyślnie wykonałeś **java image processing**, regulując gamma pliku PSD i eksportując go jako obraz TIFF przy użyciu Aspose.PSD for Java. Ten przepływ pracy daje precyzyjną kontrolę nad jasnością i kontrastem obrazu, co czyni go idealnym dla zautomatyzowanych potoków graficznych, usług webowych lub aplikacji desktopowych.

---

**Last Updated:** 2025-12-21  
**Tested With:** Aspose.PSD 24.11 for Java  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
