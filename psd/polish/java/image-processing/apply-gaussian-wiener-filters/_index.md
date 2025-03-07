---
title: Zastosuj filtry Gaussa i Wienera w Aspose.PSD dla Java
linktitle: Zastosuj filtry Gaussa i Wienera
second_title: Aspose.PSD API Java
description: Ulepsz przetwarzanie obrazu Java za pomocą Aspose.PSD. Naucz się krok po kroku stosować filtry Gaussa i Wienera, aby uzyskać oszałamiające rezultaty wizualne.
weight: 10
url: /pl/java/image-processing/apply-gaussian-wiener-filters/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Zastosuj filtry Gaussa i Wienera w Aspose.PSD dla Java

## Wstęp

Witamy w naszym obszernym samouczku na temat stosowania filtrów Gaussa i Wienera w Aspose.PSD dla Java! W tym przewodniku przeprowadzimy Cię przez proces ulepszania zdjęć przy użyciu tych potężnych filtrów. Aspose.PSD dla Java zapewnia solidny zestaw funkcji do przetwarzania obrazu, a dzięki zastosowaniu filtrów Gaussa i Wienera można uzyskać gładsze i bardziej wyrafinowane obrazy.

## Warunki wstępne

Zanim przejdziemy do samouczka, upewnij się, że spełniasz następujące wymagania wstępne:

- Środowisko programistyczne Java: Upewnij się, że na komputerze skonfigurowano środowisko programistyczne Java.

- Biblioteka Aspose.PSD dla Java: Pobierz i zainstaluj bibliotekę Aspose.PSD dla Java. Możesz znaleźć link do pobrania[Tutaj](https://releases.aspose.com/psd/java/).

## Importuj pakiety

W swoim projekcie Java zaimportuj niezbędne pakiety dla Aspose.PSD. Oto przykładowa instrukcja importu, od której możesz zacząć:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imagefilters.filteroptions.GaussWienerFilterOptions;
import com.aspose.psd.imageoptions.GifOptions;
```

Podzielmy teraz przykład na wiele kroków, aby zastosować filtry Gaussa i Wienera.

## Krok 1: Załaduj obraz

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

Image image = Image.load(sourceFile);
RasterImage rasterImage = (RasterImage)image;
```

W tym kroku ładujemy plik obrazu PSD z określonego katalogu.

## Krok 2: Sprawdź RasterImage

```java
if (rasterImage == null) {
    return;
}
```

Upewnij się, że załadowany obraz jest prawidłowym obrazem RasterImage; w przeciwnym razie proces zostaje zakończony.

## Krok 3: Skonfiguruj opcje filtra

```java
GaussWienerFilterOptions options = new GaussWienerFilterOptions(12, 3);
options.setGrayscale(true);
```

Utwórz instancję GaussWienerFilterOptions, ustaw rozmiar promienia, wartość wygładzenia i określ, czy chcesz zastosować filtr w skali szarości.

## Krok 4: Zastosuj filtr i zapisz

```java
rasterImage.filter(image.getBounds(), options);
String destName = dataDir + "gauss_wiener_out.gif";
image.save(destName, new GifOptions());
```

Na koniec zastosuj skonfigurowane filtry Gaussa i Wienera do RasterImage i zapisz wynikowy obraz w formacie GIF.

## Wniosek

Gratulacje! Pomyślnie nauczyłeś się, jak stosować filtry Gaussa i Wienera przy użyciu Aspose.PSD dla Java. Eksperymentuj z różnymi parametrami, aby uzyskać pożądane ulepszenia obrazu.

## Często zadawane pytania

### P1: Czy mogę zastosować te filtry do obrazów w formatach innych niż PSD?

Odpowiedź 1: Tak, Aspose.PSD dla Java obsługuje różne formaty obrazów poza PSD.

### P2: Czy są jakieś ograniczenia w wersji próbnej Aspose.PSD dla Java?

Odpowiedź 2: Wersja próbna ma ograniczenia i możesz poznać pełne możliwości, uzyskując ważną licencję.

### P3: Jak mogę uzyskać wsparcie dla Aspose.PSD dla Java?

 A3: Odwiedź[Forum Aspose.PSD](https://forum.aspose.com/c/psd/34) za wsparcie społeczności i dyskusje.

### P4: Czy dostępna jest licencja tymczasowa do celów testowych?

 Odpowiedź 4: Tak, możesz uzyskać licencję tymczasową[Tutaj](https://purchase.aspose.com/temporary-license/).

### P5: Gdzie mogę znaleźć szczegółową dokumentację Aspose.PSD dla Java?

 Odpowiedź 5: Patrz[dokumentacja](https://reference.aspose.com/psd/java/) w celu uzyskania szczegółowych informacji.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
