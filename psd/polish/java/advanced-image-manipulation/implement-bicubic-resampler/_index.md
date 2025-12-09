---
date: 2025-12-01
description: Dowiedz się, jak uzyskać wysokiej jakości skalowanie obrazu w Javie przy
  użyciu Bicubic Resampler firmy Aspose.PSD. Skorzystaj z naszego przewodnika krok
  po kroku, aby uzyskać doskonałe wyniki.
linktitle: Implement Bicubic Resampler
second_title: Aspose.PSD Java API
title: Skalowanie obrazu wysokiej jakości z użyciem resamplera bikubicznego w Aspose.PSD
  dla Javy
url: /pl/java/advanced-image-manipulation/implement-bicubic-resampler/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Skalowanie obrazu wysokiej jakości przy użyciu resamplera bikubicznego w Aspose.PSD dla Javy

## Wprowadzenie

Skalowanie obrazu wysokiej jakości jest częstym wymaganiem, gdy trzeba zmienić rozmiar grafiki bez utraty wierności wizualnej. Aspose.PSD dla Javy oferuje **Bicubic Resampler**, który zapewnia płynne, wyraźne wyniki dla plików PSD i innych obsługiwanych formatów. W tym samouczku dowiesz się dokładnie, jak zaimplementować resampler bikubiczny, krok po kroku, abyś mógł wprowadzić skalowanie obrazu wysokiej jakości do swoich aplikacji Java już dziś.

## Szybkie odpowiedzi
- **Co robi Bicubic Resampler?** Stosuje zaawansowany algorytm interpolacji, który zachowuje szczegóły przy zmianie rozmiaru obrazów.  
- **Jakie wartości ResizeType są dostępne?** `CubicConvolution` i `Bell` to dwie opcje bikubiczne udostępnione przez Aspose.PSD.  
- **Czy potrzebna jest licencja do uruchomienia kodu?** Tymczasowa licencja działa w trybie ewaluacyjnym; pełna licencja jest wymagana w produkcji.  
- **Jakiej wersji Javy wymaga?** Każde środowisko Java 8+ jest kompatybilne z najnowszą biblioteką Aspose.PSD.  
- **Czy mogę zmieniać rozmiar innych formatów (PNG, JPEG) przy użyciu tego samego API?** Tak, Aspose.PSD obsługuje wiele typów obrazów, choć przykłady koncentrują się na PSD.

## Czym jest skalowanie obrazu wysokiej jakości?

Skalowanie obrazu wysokiej jakości odnosi się do zmiany rozmiaru obrazu przy zachowaniu ostrych krawędzi, płynnych gradientów i dokładnej reprodukcji kolorów. Bicubic Resampler osiąga to, biorąc pod uwagę wartości otaczających pikseli (przy użyciu konwolucji sześciennej lub algorytmu Bell) w celu obliczenia każdego nowego piksela, co daje bardziej naturalny wygląd w porównaniu z metodami najbliższego sąsiada lub dwuliniowej interpolacji.

## Dlaczego używać Bicubic Resampler do skalowania obrazu wysokiej jakości?

- **Zachowuje szczegóły:** Drobne tekstury i linie pozostają wyraźne nawet po znaczących zmianach rozmiaru.  
- **Redukuje artefakty:** Minimalizuje zjawiska ringing i rozmycia, które często pojawiają się przy prostszych algorytmach.  
- **Łatwa integracja:** Jednolinijkowe wywołanie metody (`image.resize`) pozwala przełączać algorytmy bez przepisywania kodu.  

## Wymagania wstępne

Przed rozpoczęciem upewnij się, że masz:

- **Aspose.PSD for Java** – pobierz najnowszy plik JAR z [dokumentacji Aspose.PSD for Java](https://reference.aspose.com/psd/java/).  
- **Java Development Kit** – zainstalowany i skonfigurowany JDK 8 lub nowszy.  
- **Przykładowy plik PSD** – obraz testowy (np. `sample_bicubic.psd`) umieszczony w znanym katalogu.

## Importowanie pakietów

Dodaj wymagane importy do swojej klasy Java. Dzięki nim zostaną zaimportowane podstawowe klasy Aspose.PSD oraz wyliczenie `ResizeType`.

```java
import com.aspose.psd.Image;
import com.aspose.psd.ResizeType;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PsdOptions;
```

## Krok 1: Załaduj obraz

Najpierw załaduj źródłowy plik PSD, który chcesz przeskalować. Zastąp `Your Document Directory` rzeczywistą ścieżką na swoim komputerze.

```java
String dataDir = "Your Document Directory";
String filePath = dataDir + "sample_bicubic.psd";
PsdImage image = (PsdImage)Image.load(filePath);
```

## Krok 2: Skalowanie przy użyciu Cubic Convolution (wysoka jakość)

Teraz zastosuj algorytm **Cubic Convolution**, jedną z dwóch opcji bikubicznych zapewniających wysokiej jakości skalowanie obrazu. Przykład przeskalowuje obraz do 300 × 300 pikseli.

```java
String destNameCubicConvolution = dataDir + "ResamplerCubicConvolutionStripes_after.psd";
image.resize(300, 300, ResizeType.CubicConvolution);
image.save(destNameCubicConvolution, new PsdOptions(image));
```

## Krok 3: Skalowanie przy użyciu algorytmu Bell (alternatywna wysoka jakość)

Jeśli wolisz algorytm **Bell**, który oferuje nieco inny efekt wygładzania, możesz go użyć w ten sam sposób. Zauważ, że ponownie ładujemy oryginalny obraz, aby zachować uczciwe porównanie.

```java
String destNameBell = dataDir + "ResamplerBellStripes_after.psd";
PsdImage imageBellStripes = (PsdImage)Image.load(filePath);
imageBellStripes.resize(300, 300, ResizeType.Bell);
imageBellStripes.save(destNameBell, new PsdOptions(imageBellStripes));
```

Śmiało eksperymentuj z innymi wymiarami lub formatami plików — po prostu dostosuj odpowiednio parametry.

## Typowe pułapki i wskazówki

- **Nieprawidłowa ścieżka:** Upewnij się, że `dataDir` kończy się separatorem plików (`/` lub `\`) odpowiednim dla Twojego systemu operacyjnego.  
- **Wyjątki licencyjne:** Uruchomienie bez ważnej licencji może dodać znak wodny do obrazu wyjściowego.  
- **Zużycie pamięci:** Duże pliki PSD mogą zużywać znaczną ilość pamięci; rozważ zwolnienie obrazów (`image.dispose()`) po zapisaniu.  

## Najczęściej zadawane pytania

**Q: Czy mogę używać Aspose.PSD for Java z innymi formatami obrazów?**  
A: Tak, biblioteka obsługuje PSD, PNG, JPEG, TIFF, BMP i wiele innych.

**Q: Czy dostępna jest tymczasowa licencja dla Aspose.PSD for Java?**  
A: Tak, tymczasową licencję można uzyskać [tutaj](https://purchase.aspose.com/temporary-license/).

**Q: Gdzie mogę znaleźć wsparcie dla Aspose.PSD for Java?**  
A: Odwiedź forum Aspose.PSD [tutaj](https://forum.aspose.com/c/psd/34) w celu uzyskania pomocy.

**Q: Czy mogę pobrać bibliotekę Aspose.PSD for Java?**  
A: Tak, pobierz bibliotekę ze strony wydań [tutaj](https://releases.aspose.com/psd/java/).

**Q: Jak mogę kupić Aspose.PSD for Java?**  
A: Możesz zakupić Aspose.PSD for Java na stronie zakupu [tutaj](https://purchase.aspose.com/buy).

---

**Ostatnia aktualizacja:** 2025-12-01  
**Testowano z:** Aspose.PSD for Java 24.11 (latest at time of writing)  
**Autor:** Aspose

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}