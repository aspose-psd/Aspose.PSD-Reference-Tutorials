---
date: 2025-12-19
description: Dowiedz się, jak dostosować jasność obrazu przy użyciu Aspose.PSD dla
  Javy. Ten samouczek manipulacji obrazem w Javie zapewnia przewodnik krok po kroku.
linktitle: Adjust Brightness of an Image
second_title: Aspose.PSD Java API
title: Jak dostosować jasność obrazu przy użyciu Aspose.PSD dla Javy
url: /pl/java/advanced-techniques/adjust-brightness/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Regulacja jasności obrazu przy użyciu Aspose.PSD dla Javy

## Wprowadzenie

Jeśli potrzebujesz **nauczyć się, jak regulować jasność** obrazu bezpośrednio w kodzie Java, jesteś we właściwym miejscu. Dostosowywanie jasności to częste zadanie dla grafików, fotografów i każdego, kto buduje potoki przetwarzania obrazów. W tym **tutorialu manipulacji obrazami w Javie** przeprowadzimy Cię przez pełny przepływ pracy — ładowanie pliku PSD/TIFF, zastosowanie przesunięcia jasności i zapisanie wyniku — przy użyciu biblioteki Aspose.PSD for Java.

## Szybkie odpowiedzi
- **Jaką bibliotekę obsługuje jasność?** Aspose.PSD for Java  
- **Która metoda zmienia jasność?** `RasterImage.adjustBrightness()`  
- **Czy mogę pracować z plikami PSD i TIFF?** Tak, API obsługuje oba formaty.  
- **Czy potrzebna jest licencja do produkcji?** Wymagana jest licencja komercyjna do użytku nie‑ewaluacyjnego.  
- **Jak długo trwa implementacja?** Zazwyczaj poniżej 10 minut dla podstawowej regulacji.

## Czym jest regulacja jasności obrazu?

Regulacja jasności obrazu zmienia ogólną jasność każdego piksela w obrazie. Zwiększenie jasności rozjaśnia ciemne obszary, natomiast zmniejszenie przyciemnia cały obraz. Operacja ta jest przydatna do korekcji niedoświetlonych zdjęć, przygotowywania zasobów do druku lub tworzenia efektów wizualnych w aplikacjach.

## Dlaczego używać Aspose.PSD dla Javy?

- **Pełne wsparcie formatów** – PSD, TIFF, JPEG, PNG i inne.  
- **Brak zewnętrznych zależności natywnych** – czysta Java, łatwa integracja.  
- **Wysokowydajne buforowanie** – dane rastrowe mogą być buforowane dla szybszych powtarzających się operacji.  
- **Bogate API** – metody korekcji kolorów, warstw, masek i innych zaawansowanych edycji.

## Prerequisites

Zanim zanurzysz się w tutorial, upewnij się, że masz następujące wymagania wstępne:

- Biblioteka Aspose.PSD for Java: Pobierz i zainstaluj bibliotekę z [dokumentacji Aspose.PSD for Java](https://reference.aspose.com/psd/java/).

## Importowanie pakietów

Na początek zaimportuj niezbędne pakiety do swojego projektu Java. W tym przykładzie użyjemy następujących:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

Teraz rozbijmy proces regulacji jasności obrazu na proste kroki:

## Jak regulować jasność przy użyciu Aspose.PSD

### Krok 1: Załaduj obraz

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "AdjustBrightness_out.tiff";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);
// Cast object of Image to RasterImage
RasterImage rasterImage = (RasterImage) image;

// Check if RasterImage is cached and Cache RasterImage for better performance
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

W tym kroku ładujemy docelowy obraz i rzutujemy go na `RasterImage` w celu dalszego przetwarzania.

### Krok 2: Regulacja jasności

```java
// Adjust the brightness
rasterImage.adjustBrightness(-50);
```

Tutaj używamy metody `adjustBrightness`, aby zmodyfikować jasność obrazu. W tym przykładzie zmniejszamy jasność o 50 jednostek, ale możesz dostosować tę wartość według własnych wymagań.

### Krok 3: Ustaw TiffOptions

```java
int[] ushort = {8, 8, 8};
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

Skonfiguruj `TiffOptions` do zapisu zmodyfikowanego obrazu. Dostosuj właściwości `bitsPerSample` i `photometric` zgodnie z konkretnymi potrzebami.

### Krok 4: Zapisz wynikowy obraz

```java
// Save the resultant image
rasterImage.save(destName, tiffOptions);
```

Na koniec zapisz zmodyfikowany obraz używając określonych `TiffOptions`.

## Częste problemy i rozwiązania

| Problem | Powód | Rozwiązanie |
|---------|-------|-------------|
| **`ClassCastException` przy rzutowaniu Image** | Plik nie jest obrazem rastrowym (np. wektorowy PSD). | Zweryfikuj format pliku źródłowego lub użyj `image instanceof RasterImage` przed rzutowaniem. |
| **Zmiana jasności nie ma efektu** | Obraz nie został zbuforowany przed regulacją. | Wywołaj `rasterImage.cacheData()` jak pokazano w Kroku 1. |
| **Zapisany plik wydaje się uszkodzony** | Nieprawidłowa konfiguracja `TiffOptions`. | Upewnij się, że `bitsPerSample` odpowiada głębokości obrazu źródłowego (zwykle 8‑bit na kanał). |

## Najczęściej zadawane pytania

### P1: Czy mogę regulować jasność w innych formatach obrazów poza PSD?

**Odp1:** Tak, Aspose.PSD for Java obsługuje różne formaty obrazów, takie jak JPEG, PNG i TIFF.

### P2: Jak mogę obsłużyć błędy podczas procesu regulacji obrazu?

**Odp2:** Możesz zaimplementować obsługę błędów przy użyciu bloków try‑catch, aby zarządzać ewentualnymi wyjątkami.

### P3: Czy istnieje limit zakresu regulacji jasności?

**Odp3:** Zakres regulacji zależy od zawartości i formatu obrazu, ale Aspose.PSD zapewnia elastyczność w dostosowywaniu.

### P4: Czy mogę używać Aspose.PSD for Java w projektach komercyjnych?

**Odp4:** Tak, Aspose.PSD for Java jest biblioteką komercyjną i możesz uzyskać licencję [tutaj](https://purchase.aspose.com/buy).

### P5: Czy dostępna jest darmowa wersja próbna Aspose.PSD for Java?

**Odp5:** Tak, możesz przetestować bibliotekę w wersji próbnej [tutaj](https://releases.aspose.com/).

### P6: Czy metoda `adjustBrightness` wpływa na widoczność warstw?

**Odp6:** Metoda działa na zrastrzowanym obrazie kompozytowym, więc widoczność warstw jest respektowana podczas rasteryzacji.

### P7: Czy mogę łączyć wiele regulacji (np. kontrast, nasycenie) razem?

**Odp7:** Oczywiście. Po regulacji jasności możesz wywołać `adjustContrast`, `adjustSaturation` itp. na tej samej instancji `RasterImage`.

**Ostatnia aktualizacja:** 2025-12-19  
**Testowano z:** Aspose.PSD for Java 24.12 (najnowsza w momencie pisania)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}