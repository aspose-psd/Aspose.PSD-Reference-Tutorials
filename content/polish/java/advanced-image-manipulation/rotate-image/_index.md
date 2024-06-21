---
title: Obróć obraz w Aspose.PSD dla Java
linktitle: Obróć obraz
second_title: Aspose.PSD API Java
description: Przeglądaj rotację obrazu w Javie bez wysiłku dzięki Aspose.PSD. Z łatwością obracaj, odwracaj i zapisuj pliki PSD.
type: docs
weight: 19
url: /pl/java/advanced-image-manipulation/rotate-image/
---
## Wstęp

Aspose.PSD dla Java zapewnia potężny zestaw funkcji do pracy z obrazami, umożliwiając programistom efektywne manipulowanie i przetwarzanie plików PSD. W tym samouczku skupimy się na jednym konkretnym zadaniu: obracaniu obrazu. Niezależnie od tego, czy tworzysz aplikację do edycji zdjęć, czy po prostu chcesz dostosować orientację obrazu, Aspose.PSD sprawia, że proces jest prosty.

## Warunki wstępne

Zanim przejdziesz do samouczka, upewnij się, że spełniasz następujące wymagania wstępne:

-  Biblioteka Aspose.PSD dla Java: Upewnij się, że pobrałeś i zainstalowałeś bibliotekę Aspose.PSD dla Java. Można znaleźć bibliotekę i szczegółową dokumentację[Tutaj](https://reference.aspose.com/psd/java/).

- Środowisko programistyczne Java: Upewnij się, że na komputerze jest skonfigurowane środowisko programistyczne Java.

-  Przykładowy plik PSD: Przygotuj przykładowy plik PSD, który chcesz obrócić. Poprawić`sourceFile` zmienną w przykładowym kodzie ze ścieżką do pliku PSD.

## Importuj pakiety

Zacznij od zaimportowania niezbędnych pakietów, aby wykorzystać możliwości Aspose.PSD:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RotateFlipType;

import com.aspose.psd.imageoptions.JpegOptions;
```

## Krok 1: Załaduj obraz

 Załaduj istniejący obraz do instancji pliku`Image` klasa:

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
Image image = Image.load(sourceFile);
```

## Krok 2: Obróć obraz

 Obróć obraz za pomocą`rotateFlip` metoda. W tym przykładzie obracamy obraz o 270 stopni:

```java
image.rotateFlip(RotateFlipType.Rotate270FlipNone);
```

## Krok 3: Zapisz obrócony obraz

 Zapisz obrócony obraz za pomocą`save` metodę i określenie formatu wyjściowego (w tym przypadku JPEG):

```java
String destName = dataDir + "RotatedImage_out.jpg";
image.save(destName, new JpegOptions());
```

## Wniosek

Gratulacje! Pomyślnie obróciłeś obraz za pomocą Aspose.PSD dla Java. Ta prosta, ale potężna biblioteka otwiera świat możliwości manipulacji obrazami w aplikacjach Java.

## Często zadawane pytania

### P1: Czy Aspose.PSD jest kompatybilny z różnymi formatami obrazów?

O1: Tak, Aspose.PSD obsługuje różne formaty obrazów, w tym PSD, JPEG, PNG i inne.

### P2: Czy mogę zastosować niestandardowe obroty, a nie tylko predefiniowane przewroty?

A2: Absolutnie! Aspose.PSD zapewnia elastyczność stosowania niestandardowych rotacji w celu spełnienia określonych wymagań.

### P3: Gdzie mogę znaleźć dodatkowe wsparcie lub pomoc?

 O3: W przypadku jakichkolwiek pytań lub problemów odwiedź stronę[Forum Aspose.PSD](https://forum.aspose.com/c/psd/34) za wsparcie społeczne.

### P4: Czy dostępny jest bezpłatny okres próbny?

 O4: Tak, możesz eksplorować Aspose.PSD za pomocą[bezpłatna wersja próbna](https://releases.aspose.com/).

### P5: Jak uzyskać licencję tymczasową?

 Odpowiedź 5: Jeśli potrzebujesz licencji tymczasowej, możesz ją uzyskać.[Tutaj](https://purchase.aspose.com/temporary-license/).