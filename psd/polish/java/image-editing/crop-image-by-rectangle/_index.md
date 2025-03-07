---
title: Przytnij obraz według prostokąta w Aspose.PSD dla Java
linktitle: Przytnij obraz według prostokąta
second_title: Aspose.PSD API Java
description: Poznaj możliwości płynnego przycinania obrazów w Javie za pomocą Aspose.PSD. Postępuj zgodnie z naszym przewodnikiem krok po kroku, aby bez wysiłku przycinać obrazy za pomocą Aspose.PSD dla Java.
weight: 15
url: /pl/java/image-editing/crop-image-by-rectangle/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Przytnij obraz według prostokąta w Aspose.PSD dla Java

## Wstęp

W świecie programowania w języku Java manipulowanie obrazami jest częstym zadaniem, a Aspose.PSD dla Java zapewnia potężne rozwiązanie do przetwarzania obrazów. W tym samouczku przeprowadzimy Cię przez proces przycinania obrazu przez prostokąt przy użyciu Aspose.PSD dla Java. Aby to osiągnąć z łatwością, wykonaj poniższe czynności.

## Warunki wstępne

Zanim zagłębisz się w samouczek, upewnij się, że spełniasz następujące wymagania wstępne:

- Zestaw Java Development Kit (JDK) zainstalowany na komputerze.
- Aspose.PSD dla biblioteki Java. Można go pobrać z[strona internetowa](https://releases.aspose.com/psd/java/).

## Importuj pakiety

Pamiętaj o dołączeniu niezbędnych pakietów do swojego projektu Java, aby wykorzystać możliwości Aspose.PSD dla Java. Dodaj następujące instrukcje importu na początku pliku Java:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;

import com.aspose.psd.imageoptions.JpegOptions;
```

Teraz podzielmy proces na wiele kroków, które poprowadzą Cię przez przycięcie obrazu przez prostokąt za pomocą Aspose.PSD dla Java.

## Krok 1: Skonfiguruj katalog dokumentów

```java
String dataDir = "Your Document Directory";
```

 Zastępować`"Your Document Directory"` z rzeczywistą ścieżką, w której znajduje się plik PSD.

## Krok 2: Określ pliki źródłowe i docelowe

```java
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "CroppingByRectangle_out.jpg";
```

Zdefiniuj ścieżki źródłowego pliku PSD i docelowego pliku JPEG.

## Krok 3: Załaduj i buforuj obraz

```java
RasterImage rasterImage = (RasterImage)Image.load(sourceFile);

if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

 Załaduj obraz PSD do pliku`RasterImage` instancję i buforować jej dane.

## Krok 4: Utwórz i zdefiniuj prostokąt przycięcia

```java
Rectangle rectangle = new Rectangle(20, 20, 20, 20);
```

 Utwórz instancję`Rectangle` klasę o żądanym rozmiarze do przycięcia.

## Krok 5: Przytnij i zapisz obraz

```java
rasterImage.crop(rectangle);
rasterImage.save(destName, new JpegOptions());
```

Wykonaj operację przycinania, używając określonego prostokąta i zapisz wyniki jako plik JPEG.

W razie potrzeby powtórz te kroki, dostosowując parametry zgodnie ze swoimi specyficznymi wymaganiami.

## Wniosek

W tym samouczku przeszliśmy przez proces przycinania obrazu przez prostokąt przy użyciu Aspose.PSD dla Java. Wykonując poniższe kroki, możesz łatwo zintegrować zaawansowane możliwości manipulacji obrazami z aplikacjami Java.

## Często zadawane pytania

### P1: Czy mogę używać Aspose.PSD for Java z innymi frameworkami Java?

Odpowiedź 1: Tak, Aspose.PSD for Java można zintegrować z różnymi frameworkami Java, zapewniając elastyczność w projektach programistycznych.

### P2: Czy dostępna jest bezpłatna wersja próbna Aspose.PSD dla Java?

 Odpowiedź 2: Tak, możesz uzyskać dostęp do bezpłatnej wersji próbnej[Tutaj](https://releases.aspose.com/).

### P3: Gdzie mogę znaleźć dodatkowe wsparcie lub pomoc?

 A3: Odwiedź[Forum Aspose.PSD](https://forum.aspose.com/c/psd/34) za wsparcie społeczności i dyskusje.

### P4: Jak uzyskać tymczasową licencję na Aspose.PSD dla Java?

 Odpowiedź 4: Możesz nabyć licencję tymczasową[Tutaj](https://purchase.aspose.com/temporary-license/).

### P5: Jakie są obsługiwane formaty obrazów do kadrowania w Aspose.PSD dla Java?

O5: Aspose.PSD dla Java obsługuje różne formaty obrazów, w tym PSD, PNG, JPEG i inne.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
