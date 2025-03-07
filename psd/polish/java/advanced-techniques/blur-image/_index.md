---
title: Rozmycie obrazu za pomocą Aspose.PSD dla Java
linktitle: Rozmycie obrazu
second_title: Aspose.PSD API Java
description: Naucz się rozmazywać obrazy w Javie za pomocą Aspose.PSD. Postępuj zgodnie z naszym przewodnikiem krok po kroku, aby uzyskać profesjonalne rezultaty.
weight: 24
url: /pl/java/advanced-techniques/blur-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Rozmycie obrazu za pomocą Aspose.PSD dla Java

## Wstęp

W świecie programowania w języku Java ulepszanie obrazów i manipulowanie nimi jest powszechnym wymogiem. Jeśli chcesz programowo dodać efekt rozmycia do swoich obrazów, Aspose.PSD dla Java to potężne narzędzie, które upraszcza ten proces. Ten samouczek poprowadzi Cię przez etapy rozmycia obrazu za pomocą Aspose.PSD, zapewniając bezproblemowe osiągnięcie profesjonalnych rezultatów.

## Warunki wstępne

Zanim przejdziesz do samouczka, upewnij się, że spełniasz następujące wymagania wstępne:

- Zestaw Java Development Kit (JDK) zainstalowany w systemie.
-  Aspose.PSD dla biblioteki Java. Możesz go pobrać[Tutaj](https://releases.aspose.com/psd/java/).
- Podstawowa znajomość programowania w języku Java.

## Importuj pakiety

Zacznij od zaimportowania niezbędnych pakietów do projektu Java. Należą do nich klasy Aspose.PSD do przetwarzania obrazu.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imagefilters.filteroptions.GaussianBlurFilterOptions;
import com.aspose.psd.imageoptions.GifOptions;
```

Podzielmy teraz proces rozmycia obrazu na kilka etapów.

## Krok 1: Zdefiniuj ścieżki plików

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "BlurAnImage_out.gif";
```

## Krok 2: Załaduj obraz

```java
// Załaduj istniejący obraz do instancji klasy RasterImage
Image image = Image.load(sourceFile);
```

## Krok 3: Konwertuj na obraz rastrowy

```java
// Konwertuj obraz na RasterImage
RasterImage rasterImage = (RasterImage)image;
```

## Krok 4: Zastosuj filtr rozmycia

```java
//Przekaż Bounds[rectangle] obrazu i instancję GaussianBlurFilterOptions do metody Filter
rasterImage.filter(rasterImage.getBounds(), new GaussianBlurFilterOptions(15, 15));
```

## Krok 5: Zapisz wynik

```java
// Zapisz wyniki w formacie GIF
rasterImage.save(destName, new GifOptions());
```

Wykonując poniższe kroki, udało Ci się zastosować efekt rozmycia do swojego obrazu przy użyciu Aspose.PSD dla Java.

## Wniosek

Aspose.PSD dla Java upraszcza zadania przetwarzania obrazu, ułatwiając programistom osiągnięcie profesjonalnych wyników. Programowe rozmycie obrazów to tylko jeden z przykładów potężnych funkcji, jakie zapewnia ta biblioteka.

## Często zadawane pytania

### P1: Czy Aspose.PSD dla Java jest odpowiedni dla początkujących programistów?

A1: Absolutnie! Aspose.PSD zawiera obszerną dokumentację, która pomoże programistom na wszystkich poziomach umiejętności.

### P2: Czy mogę używać Aspose.PSD do projektów komercyjnych?

 A2: Tak, możesz. Odwiedzać[Tutaj](https://purchase.aspose.com/buy) aby poznać opcje licencjonowania.

### P3: Czy dostępny jest bezpłatny okres próbny?

 A3: Tak, możesz uzyskać bezpłatną wersję próbną[Tutaj](https://releases.aspose.com/).

### P4: Gdzie mogę znaleźć wsparcie dla Aspose.PSD dla Java?

 A4: Odwiedź[Forum Aspose.PSD](https://forum.aspose.com/c/psd/34) w przypadku jakichkolwiek pytań związanych ze wsparciem.

### P5: Jak uzyskać tymczasową licencję na Aspose.PSD?

 Odpowiedź 5: Możesz uzyskać licencję tymczasową[Tutaj](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
