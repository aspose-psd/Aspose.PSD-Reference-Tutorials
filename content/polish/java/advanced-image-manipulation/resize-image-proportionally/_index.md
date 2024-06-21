---
title: Zmień rozmiar obrazu proporcjonalnie za pomocą Aspose.PSD dla Java
linktitle: Zmień rozmiar obrazu proporcjonalnie
second_title: Aspose.PSD API Java
description: Ulepsz swoje aplikacje Java za pomocą Aspose.PSD. Postępuj zgodnie z naszym przewodnikiem, aby bez wysiłku zmieniać rozmiar obrazów proporcjonalnie. Już dziś zwiększ swoje możliwości w zakresie obsługi obrazów.
type: docs
weight: 17
url: /pl/java/advanced-image-manipulation/resize-image-proportionally/
---
## Wstęp

Witamy w naszym przewodniku krok po kroku dotyczącym proporcjonalnej zmiany rozmiaru obrazów przy użyciu Aspose.PSD dla Java. Jeśli chcesz ulepszyć swoje aplikacje Java dzięki wydajnym możliwościom zmiany rozmiaru obrazu, trafiłeś we właściwe miejsce. W tym samouczku przeprowadzimy Cię przez ten proces, stosując jasne i zwięzłe kroki.

## Warunki wstępne

Zanim przejdziesz do samouczka, upewnij się, że spełniasz następujące wymagania wstępne:

1. Środowisko Java: Upewnij się, że masz zainstalowaną Javę w swoim systemie.
2.  Biblioteka Aspose.PSD: Pobierz i zainstaluj bibliotekę Aspose.PSD. Możesz znaleźć niezbędne zasoby[Tutaj](https://releases.aspose.com/psd/java/).

## Importuj pakiety

Po uporządkowaniu wymagań wstępnych zaimportuj wymagane pakiety do projektu Java. Upewnij się, że w Twoim projekcie poprawnie odniesiono się do biblioteki Aspose.PSD.

```java
import com.aspose.psd.Image;

import com.aspose.psd.imageoptions.PngOptions;
```

## Krok 1: Załaduj obraz

Rozpocznij od załadowania obrazu, którego rozmiar chcesz zmienić, do aplikacji Java.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

Image image = Image.load(sourceFile);

if (!image.isCached()) {
    image.cacheData();
}
```

## Krok 2: Określ szerokość i wysokość

Określ nową szerokość i wysokość obrazu o zmienionym rozmiarze. W tym przykładzie zmienimy rozmiar obrazu do połowy jego oryginalnych wymiarów.

```java
int newWidth = image.getWidth() / 2;
image.resizeWidthProportionally(newWidth);

int newHeight = image.getHeight() / 2;
image.resizeHeightProportionally(newHeight);
```

## Krok 3: Zapisz obraz o zmienionym rozmiarze

Zapisz obraz o zmienionym rozmiarze w wybranej lokalizacji, określając opcje formatu (w tym przypadku PNG).

```java
String destName = dataDir + "SimpleResizeImageProportionally_out.png";
image.save(destName, new PngOptions());
```

I masz to! Pomyślnie zmieniłeś rozmiar obrazu proporcjonalnie przy użyciu Aspose.PSD dla Java.

## Wniosek

W tym samouczku omówiliśmy podstawowe kroki proporcjonalnej zmiany rozmiaru obrazów przy użyciu biblioteki Aspose.PSD dla Java. Teraz możesz bez wysiłku zintegrować tę funkcjonalność z aplikacjami Java, aby usprawnić obsługę obrazów.

## Często zadawane pytania

### P1: Czy Aspose.PSD jest kompatybilny ze wszystkimi formatami obrazów?

 O1: Aspose.PSD obsługuje różne formaty obrazów, w tym PSD, PNG, JPEG i inne. Sprawdź[dokumentacja](https://reference.aspose.com/psd/java/) dla pełnej listy.

### P2: Czy mogę używać Aspose.PSD do projektów komercyjnych?

 A2: Tak, możesz. Odwiedzić[strona zakupu](https://purchase.aspose.com/buy) w celu uzyskania szczegółów licencji.

### P3: Czy dostępne są licencje tymczasowe do celów testowych?

 Odpowiedź 3: Tak, możesz uzyskać licencję tymczasową.[Tutaj](https://purchase.aspose.com/temporary-license/) dla ewolucji.

### P4: Gdzie mogę znaleźć wsparcie dla Aspose.PSD?

 A4: Odwiedź[Forum Aspose.PSD](https://forum.aspose.com/c/psd/34) za wsparcie i pomoc społeczną.

### P5: Jak mogę uzyskać dostęp do dokumentacji Aspose.PSD?

 Odpowiedź 5: Zapoznaj się ze szczegółową dokumentacją[Tutaj](https://reference.aspose.com/psd/java/).
`