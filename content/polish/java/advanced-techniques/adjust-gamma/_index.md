---
title: Dostosuj gamma obrazu za pomocą Aspose.PSD dla Java
linktitle: Dostosuj gamma obrazu
second_title: Aspose.PSD API Java
description: Naucz się bez wysiłku dostosowywać gamma obrazu za pomocą Aspose.PSD dla Java. Postępuj zgodnie z naszym przewodnikiem krok po kroku, aby uzyskać optymalne rezultaty.
type: docs
weight: 23
url: /pl/java/advanced-techniques/adjust-gamma/
---
## Wstęp

W dziedzinie przetwarzania obrazu dostosowanie gamma obrazu jest kluczowym krokiem w celu poprawy jego atrakcyjności wizualnej. Aspose.PSD dla Java oferuje potężne rozwiązanie dla programistów Java, umożliwiające łatwe manipulowanie gamma obrazu. W tym samouczku przyjrzymy się, jak dostosować gamma za pomocą Aspose.PSD, dzieląc każdy krok, aby zapewnić bezproblemową implementację.

## Warunki wstępne

Zanim przejdziesz do samouczka, upewnij się, że masz skonfigurowane następujące wymagania wstępne:

1. Środowisko programistyczne Java: Upewnij się, że w systemie jest zainstalowane środowisko programistyczne Java.
2.  Biblioteka Aspose.PSD: Pobierz i zintegruj bibliotekę Aspose.PSD ze swoim projektem Java. Niezbędne zasoby znajdziesz w[dokumentacja](https://reference.aspose.com/psd/java/).
3. Przykładowy obraz: Przygotuj przykładowy obraz PSD, którego użyjesz do zastosowania korekty gamma.

## Importuj pakiety

Aby rozpocząć proces, zaimportuj wymagane pakiety do projektu Java. To przygotowuje grunt pod bezproblemowe wykorzystanie funkcjonalności Aspose.PSD.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## Krok 1: Załaduj obraz

 Zacznij od załadowania przykładowego obrazu PSD do instancji pliku`RasterImage` klasa. Jest to podstawa do późniejszych korekt gamma.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Załaduj istniejący obraz do instancji klasy RasterImage
Image image = Image.load(sourceFile);

// Rzuć obiekt obrazu na RasterImage
RasterImage rasterImage = (RasterImage)image;

// Sprawdź, czy RasterImage jest buforowany, aby uzyskać lepszą wydajność
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

## Krok 2: Dostosuj gamma

 Teraz dostosuj gamma załadowanego obrazu za pomocą`adjustGamma` metoda. Dostosuj wartości gamma zgodnie ze swoimi wymaganiami.

```java
// Dostosuj gammę
rasterImage.adjustGamma(2.2f, 2.2f, 2.2f);
```

## Krok 3: Utwórz opcje Tiff

 Utwórz instancję`TiffOptions` dla powstałego obrazu. Ustaw różne właściwości, takie jak liczba bitów na próbkę i opcje fotometryczne, aby dostosować wydruk do swoich specyfikacji.

```java
// Utwórz instancję TiffOptions dla wynikowego obrazu
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

## Krok 4: Zapisz wynikowy obraz

 Zapisz zmanipulowany obraz w formacie TIFF, korzystając z wcześniej zdefiniowanego`TiffOptions`.

```java
// Zapisz wynikowy obraz w formacie TIFF
String destName = dataDir + "AdjustGamma_out.tiff";
rasterImage.save(destName, tiffOptions);
```

## Wniosek

Gratulacje! Pomyślnie dostosowałeś gamma obrazu za pomocą Aspose.PSD dla Java. Proces ten umożliwia programistom bezproblemową poprawę jakości obrazu, przyczyniając się do atrakcyjnego wizualnie doświadczenia użytkownika.

## Często zadawane pytania

### P1: Gdzie mogę znaleźć dokumentację Aspose.PSD?

 Odpowiedź 1: Dostęp do dokumentacji można uzyskać pod adresem[https://reference.aspose.com/psd/java/](https://reference.aspose.com/psd/java/).

### P2: Jak pobrać Aspose.PSD dla Java?

 A2: Pobierz bibliotekę z[https://releases.aspose.com/psd/java/](https://releases.aspose.com/psd/java/).

### P3: Gdzie mogę kupić Aspose.PSD?

 A3: Odwiedź[https://purchase.aspose.com/buy](https://purchase.aspose.com/buy) kupić Aspose.PSD.

### P4: Czy dostępny jest bezpłatny okres próbny?

 Odpowiedź 4: Tak, możesz skorzystać z bezpłatnego okresu próbnego pod adresem[https://releases.aspose.com/](https://releases.aspose.com/).

### P5: Gdzie mogę szukać wsparcia dla Aspose.PSD?

 O5: Aby uzyskać pomoc, odwiedź forum Aspose.PSD pod adresem[https://forum.aspose.com/c/psd/34](https://forum.aspose.com/c/psd/34).