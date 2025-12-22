---
date: 2025-12-21
description: Dowiedz się, jak regulować kontrast obrazów przy użyciu Aspose.PSD dla
  Javy, wiodącej biblioteki do manipulacji obrazami w Javie, oraz jak efektywnie konwertować
  pliki PSD na TIFF.
linktitle: Adjust Contrast of an Image
second_title: Aspose.PSD Java API
title: Jak dostosować kontrast obrazu przy użyciu Aspose.PSD dla Javy
url: /pl/java/advanced-techniques/adjust-contrast/
weight: 22
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak dostosować kontrast obrazu przy użyciu Aspose.PSD dla Javy

## Wprowadzenie

Jeśli szukasz **sposobu na dostosowanie kontrastu** w swoich projektach Java, trafiłeś we właściwe miejsce. Aspose.PSD dla Javy to potężna **biblioteka do manipulacji obrazami w Javie**, która pozwala precyzyjnie regulować właściwości obrazu, takie jak kontrast, jasność i wiele innych. W tym samouczku przeprowadzimy Cię krok po kroku przez proces zwiększenia kontrastu pliku PSD, a następnie **konwersji PSD do TIFF** w celu dalszych przepływów pracy.

## Szybkie odpowiedzi
- **Co oznacza „dostosowanie kontrastu”?** Zmienia różnicę między najciemniejszymi a najjaśniejszymi pikselami, podkreślając szczegóły.
- **Która biblioteka to obsługuje?** Aspose.PSD dla Javy – kompletny zestaw narzędzi do przetwarzania obrazów.
- **Czy potrzebna jest licencja?** Licencja tymczasowa wystarczy do testów; pełna licencja jest wymagana w środowisku produkcyjnym.
- **Czy mogę zapisać wynik jako TIFF?** Tak, użyjemy `TiffOptions`, aby wyeksportować przetworzony obraz.
- **Jak długo trwa wykonanie kodu?** Zazwyczaj poniżej sekundy dla standardowych plików PSD.

## Co to jest regulacja kontrastu?
Regulacja kontrastu modyfikuje zakres tonalny obrazu, wzmacniając różnicę między jasnymi a ciemnymi obszarami. Jest to szczególnie przydatne, gdy obrazy po skanowaniu wyglądają płasko lub gdy przygotowujemy grafikę do druku.

## Dlaczego warto używać Aspose.PSD dla Javy?
- **Bogate wsparcie formatów** – otwieraj, edytuj i zapisuj PSD, TIFF, PNG, JPEG i wiele innych.
- **Wysoka wydajność** – buforowanie i optymalizacje obrazu rastrowego zmniejszają zużycie pamięci.
- **Proste API** – jednowierszowe wywołania, takie jak `adjustContrast`, sprawiają, że kod jest czytelny.

## Wymagania wstępne

Zanim przejdziesz dalej, upewnij się, że masz:

- Podstawową znajomość programowania w Javie.
- Zainstalowaną bibliotekę Aspose.PSD dla Javy. Możesz ją pobrać [tutaj](https://releases.aspose.com/psd/java/).

## Importowanie pakietów

Dodaj wymagane importy do swojej klasy Java:

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
```

Ładujemy źródłowy plik PSD (`sample.psd`) do obiektu `Image`, który jest punktem wyjścia dla dalszego przetwarzania.

## Krok 2: Rzutuj na RasterImage i buforuj dane

```java
// Cast object of Image to RasterImage
RasterImage rasterImage = (RasterImage)image;

// Check if RasterImage is cached and Cache RasterImage for better performance
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

Rzutowanie na `RasterImage` daje dostęp do operacji na poziomie pikseli. Buforowanie poprawia wydajność, szczególnie przy dużych plikach.

## Jak dostosować kontrast obrazu

```java
// Adjust the contrast
rasterImage.adjustContrast(50);
```

Metoda `adjustContrast` przyjmuje liczbę całkowitą reprezentującą procentową zmianę. W tym przykładzie zwiększamy kontrast o **50 %**.

## Konwersja PSD do TIFF przy użyciu Aspose.PSD

```java
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);

// Save the resultant image to TIFF format
String destName = dataDir + "AdjustContrast_out.tiff";
rasterImage.save(destName, tiffOptions);
```

Tutaj konfigurujemy `TiffOptions` (liczba bitów na próbkę, interpretacja fotometryczna) i zapisujemy obraz z podwyższonym kontrastem do pliku TIFF.

## Typowe problemy i rozwiązania
- **Obraz nie został buforowany:** Zawsze wywołuj `cacheData()` dla dużych plików PSD, aby uniknąć `OutOfMemoryError`.
- **Nieoczekiwane przesunięcie kolorów:** Upewnij się, że `setPhotometric` odpowiada docelowemu przestrzeni kolorów (RGB vs. CMYK).
- **Plik nie został znaleziony:** Sprawdź, czy `dataDir` wskazuje na właściwy folder i czy nazwa pliku jest poprawna.

## Najczęściej zadawane pytania

### Q1: Czy Aspose.PSD jest kompatybilny z różnymi formatami obrazów?

A1: Tak, Aspose.PSD obsługuje różne formaty obrazów, zapewniając elastyczność w Twoich projektach.

### Q2: Jak mogę uzyskać tymczasową licencję dla Aspose.PSD?

A2: Tymczasową licencję możesz uzyskać [tutaj](https://purchase.aspose.com/temporary-license/).

### Q3: Gdzie mogę znaleźć dokumentację Aspose.PSD?

A3: Dokumentacja jest dostępna [tutaj](https://reference.aspose.com/psd/java/).

### Q4: Jakie opcje wsparcia są dostępne dla Aspose.PSD?

A4: W sprawach wsparcia odwiedź [forum Aspose.PSD](https://forum.aspose.com/c/psd/34).

### Q5: Czy mogę kupić Aspose.PSD?

A5: Tak, możesz zakupić Aspose.PSD [tutaj](https://purchase.aspose.com/buy).

## Zakończenie

Teraz wiesz, **jak dostosować kontrast** obrazu PSD przy użyciu Aspose.PSD dla Javy oraz **jak skonwertować PSD do TIFF** w celu dalszego przetwarzania. Te kroki dają Ci precyzyjną kontrolę nad jakością obrazu, jednocześnie utrzymując kod przejrzystym i łatwym w utrzymaniu. Śmiało eksperymentuj z innymi metodami regulacji obrazu, takimi jak `adjustBrightness` czy `adjustGamma`, aby dopasować je do swoich konkretnych potrzeb.

---

**Ostatnia aktualizacja:** 2025-12-21  
**Testowane z:** Aspose.PSD dla Javy 24.12  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}