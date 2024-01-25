---
title: Zmiana rozmiaru za pomocą wyliczenia typu zmiany rozmiaru w Aspose.PSD dla Java
linktitle: Zmiana rozmiaru za pomocą wyliczenia typu zmiany rozmiaru
second_title: Aspose.PSD API Java
description: Opanuj zmianę rozmiaru obrazu w Javie za pomocą Aspose.PSD. Przewodnik krok po kroku dotyczący wyliczania typu zmiany rozmiaru.
type: docs
weight: 18
url: /pl/java/advanced-image-manipulation/resizing-with-resize-type-enumeration/
---
## Wstęp

W stale zmieniającym się środowisku programowania w języku Java wydajne przetwarzanie obrazu jest kluczowym aspektem, z którym często borykają się programiści. Aspose.PSD dla Java jawi się jako potężne rozwiązanie, zapewniające płynną zmianę rozmiaru obrazów z dodatkową zaletą wyliczania typu zmiany rozmiaru. W tym samouczku zagłębimy się w zawiłości zmiany rozmiaru obrazów przy użyciu Aspose.PSD dla Java, dzieląc każdy krok, aby zapewnić wszechstronne zrozumienie.

## Warunki wstępne

Przed rozpoczęciem korzystania z tego samouczka upewnij się, że spełnione są następujące wymagania wstępne:

1. Środowisko programistyczne Java: Upewnij się, że na komputerze jest skonfigurowane środowisko programistyczne Java.

2. Biblioteka Aspose.PSD: Pobierz i zainstaluj bibliotekę Aspose.PSD z[strona internetowa](https://releases.aspose.com/psd/java/).

3.  Przykładowy plik PSD: Przygotuj przykładowy plik PSD do eksperymentów. Możesz skorzystać z[sample.psd](Twój katalog dokumentów/sample.psd) na potrzeby tego samouczka.

## Importuj pakiety

Aby rozpocząć, zaimportuj niezbędne pakiety do swojego projektu Java:

```java
import com.aspose.psd.Image;
import com.aspose.psd.ResizeType;

import com.aspose.psd.imageoptions.JpegOptions;
```

## Krok 1: Załaduj obraz

 Zacznij od załadowania istniejącego obrazu do instancji pliku`RasterImage` klasa. Użyj następującego fragmentu kodu:

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Załaduj istniejący obraz do instancji klasy RasterImage
Image image = Image.load(sourceFile);
```

## Krok 2: Zmień rozmiar obrazu

Teraz zmień rozmiar załadowanego obrazu, korzystając z wyliczenia typu zmiany rozmiaru. W tym przykładzie używamy metody Lanczos Resample:

```java
image.resize(300, 300, ResizeType.LanczosResample);
```

## Krok 3: Zapisz obraz o zmienionym rozmiarze

Po zmianie rozmiaru zapisz obraz z określonymi wymiarami i wybranym typem zmiany rozmiaru. Tutaj zapisujemy go jako plik JPEG:

```java
String destName = dataDir + "ResizingwithResizeTypeEnumeration_out.jpg";
image.save(destName, new JpegOptions());
```

I masz to! Pomyślnie zmieniłeś rozmiar obrazu za pomocą wyliczenia typu zmiany rozmiaru w Aspose.PSD dla Java.

Podsumowując, Aspose.PSD dla Java zapewnia solidną platformę do manipulacji obrazami, a wyliczenie typu zmiany rozmiaru dodaje warstwę elastyczności do tego procesu. Niezależnie od tego, czy pracujesz nad małym projektem, czy aplikacją na dużą skalę, opanowanie tych kroków umożliwi Ci płynną zmianę rozmiaru obrazu.

## Często zadawane pytania

### P1: Czy Aspose.PSD dla Java nadaje się zarówno do projektów na małą, jak i dużą skalę?

A1: Absolutnie! Aspose.PSD dla Java został zaprojektowany z myślą o projektach dowolnej wielkości, zapewniając skalowalność i wydajność.

### P2: Czy mogę użyć innego typu zmiany rozmiaru niż Lanczos Resample?

O2: Tak, Aspose.PSD dla Java oferuje różne typy zmiany rozmiaru, takie jak Najbliższy sąsiad, Bicubic i inne. Zapoznaj się z dokumentacją, aby uzyskać obszerną listę.

### P3: Gdzie mogę znaleźć dodatkowe wsparcie dla Aspose.PSD dla Java?

 O3: W razie jakichkolwiek pytań lub pomocy odwiedź stronę[Forum Aspose.PSD](https://forum.aspose.com/c/psd/34).

### P4: Czy dostępna jest bezpłatna wersja próbna Aspose.PSD dla Java?

 Odpowiedź 4: Tak, możesz uzyskać dostęp do bezpłatnej wersji próbnej[Tutaj](https://releases.aspose.com/).

### P5: Jak mogę uzyskać tymczasową licencję na Aspose.PSD dla Java?

 A5: Aby uzyskać tymczasową licencję, odwiedź stronę[ten link](https://purchase.aspose.com/temporary-license/).