---
title: Rozmycie obrazu w Aspose.PSD dla .NET
linktitle: Zamazanie obrazu
second_title: Aspose.PSD API .NET
description: Dowiedz się, jak bez wysiłku rozmyć obrazy za pomocą Aspose.PSD dla .NET. Przewodnik krok po kroku dotyczący płynnej manipulacji obrazami w projektach C#.
type: docs
weight: 13
url: /pl/net/image-adjustment/blur-image/
---
## Wstęp

W dziedzinie rozwoju .NET Aspose.PSD okazuje się potężnym sojusznikiem w manipulacji obrazami. Ten samouczek skupia się na konkretnym zadaniu: rozmyciu obrazu przy użyciu Aspose.PSD dla .NET. Jeśli chcesz udoskonalić swoje umiejętności przetwarzania obrazu lub po prostu szukasz skutecznego sposobu na programowe rozmycie obrazów, jesteś we właściwym miejscu.

## Warunki wstępne

Zanim przejdziesz do samouczka, upewnij się, że spełniasz następujące wymagania wstępne:

-  Aspose.PSD dla .NET: Upewnij się, że masz zainstalowaną bibliotekę Aspose.PSD. Można go pobrać z[Tutaj](https://releases.aspose.com/psd/net/).

- Środowisko programistyczne: skonfiguruj środowisko programistyczne .NET i poznaj podstawową wiedzę na temat języka C#.

- Przykładowy obraz: Przygotuj przykładowy obraz w formacie PSD. Możesz użyć własnego lub pobrać go do testów.

## Importuj przestrzenie nazw

Zacznij od zaimportowania niezbędnych przestrzeni nazw do kodu C#:

```csharp
using Aspose.PSD.ImageFilters.FilterOptions;
using Aspose.PSD.ImageOptions;
```

## Krok 1: Zdefiniuj katalog dokumentów

```csharp
// Ścieżka do katalogu dokumentów.
string dataDir = "Your Document Directory";
```

## Krok 2: Załaduj obraz

```csharp
//ExStart: BluranImage

string sourceFile = dataDir + @"sample.psd";

// Załaduj istniejący obraz do instancji klasy RasterImage
using (var image = Image.Load(sourceFile))
{
    // Przejdź do kolejnych kroków w ramach tego bloku
}
```

## Krok 3: Konwertuj obraz na RasterImage

```csharp
RasterImage rasterImage = (RasterImage)image;
```

## Krok 4: Zastosuj filtr rozmycia gaussowskiego.

```csharp
rasterImage.Filter(rasterImage.Bounds, new GaussianBlurFilterOptions(15, 15));
```

 Tutaj`GaussianBlurFilterOptions` class jest używana z określonym promieniem 15 zarówno w przypadku rozmycia w poziomie, jak i w pionie.

## Krok 5: Zapisz zamazany obraz

```csharp
string destName = dataDir + @"BlurAnImage_out.gif";
rasterImage.Save(destName, new GifOptions());
```

## Wniosek

Gratulacje! Pomyślnie zamazałeś obraz za pomocą Aspose.PSD dla .NET. Ten samouczek daje wgląd w możliwości Aspose.PSD i otwiera drzwi do wielu możliwości manipulacji obrazami w aplikacjach .NET.

## Często zadawane pytania

### P1: Czy mogę zastosować różną intensywność rozmycia do różnych części obrazu?

Odpowiedź 1: Tak, Aspose.PSD pozwala na zastosowanie filtrów o różnych parametrach do określonych obszarów obrazu, zapewniając szczegółową kontrolę nad procesem rozmycia.

### P2: Czy Aspose.PSD jest kompatybilny ze wszystkimi formatami obrazów?

Odpowiedź 2: Chociaż Aspose.PSD obsługuje szeroką gamę formatów obrazów, zaleca się sprawdzenie dokumentacji pod kątem pełnej listy i wszelkich uwag specyficznych dla formatu.

### P3: Jak mogę uzyskać tymczasową licencję na Aspose.PSD?

 Odpowiedź 3: Możesz nabyć licencję tymczasową od[Tutaj](https://purchase.aspose.com/temporary-license/) do celów testowania i oceny.

### P4: Czy w Aspose.PSD dostępne są inne funkcje manipulacji obrazami?

A4: Absolutnie! Aspose.PSD oferuje kompleksowy zestaw funkcji, w tym zmianę rozmiaru, przycinanie i regulację kolorów. Pełną listę znajdziesz w dokumentacji.

### P5: Gdzie mogę szukać pomocy lub nawiązać kontakt ze społecznością Aspose.PSD?

 Odpowiedź 5: W przypadku jakichkolwiek pytań lub dyskusji przejdź do[Forum Aspose.PSD](https://forum.aspose.com/c/psd/34).