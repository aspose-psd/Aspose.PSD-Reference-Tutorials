---
title: Implementowanie regulacji jasności w Aspose.PSD dla .NET
linktitle: Wdrażanie regulacji jasności
second_title: Aspose.PSD API .NET
description: Poznaj moc Aspose.PSD dla .NET w dostosowywaniu jasności obrazu. Postępuj zgodnie z naszym przewodnikiem krok po kroku, aby zapewnić bezproblemową implementację.
type: docs
weight: 10
url: /pl/net/image-adjustment/brightness-adjustment/
---
## Wstęp

Poprawianie i dostosowywanie atrybutów obrazu jest powszechnym wymaganiem w różnych aplikacjach, a Aspose.PSD dla .NET zapewnia potężne rozwiązanie do płynnego manipulowania plikami PSD. Jedną z takich manipulacji jest regulacja jasności, która pozwala na łatwą modyfikację jasności obrazu.

W tym samouczku omówimy proces wdrażania regulacji jasności za pomocą Aspose.PSD dla .NET. Wykonaj poniższe kroki, aby uzyskać pełną wiedzę na temat włączania regulacji jasności do plików PSD.

## Warunki wstępne

Zanim przejdziesz do samouczka, upewnij się, że spełniasz następujące wymagania wstępne:

-  Biblioteka Aspose.PSD dla .NET: Pobierz i zainstaluj bibliotekę Aspose.PSD dla .NET z[link do pobrania](https://releases.aspose.com/psd/net/).

-  Katalog dokumentów: skonfiguruj katalog do przechowywania plików PSD i aktualizacji`dataDir` zmienną w podanym fragmencie kodu ze ścieżką do katalogu dokumentów.

## Importuj przestrzenie nazw

swoim projekcie .NET uwzględnij niezbędne przestrzenie nazw, aby uzyskać dostęp do funkcjonalności Aspose.PSD. Dodaj następujące przestrzenie nazw do swojego kodu:

```csharp
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Tiff.Enums;
using Aspose.PSD.ImageOptions;
```

Podzielmy teraz przykład na kilka kroków:

## Krok 1: Załaduj plik PSD

```csharp
// Ścieżka do katalogu dokumentów.
string dataDir = "Your Document Directory";
string sourceFile = dataDir + @"sample.psd";

// Załaduj plik PSD za pomocą Aspose.PSD
using (var image = (PsdImage)Image.Load(sourceFile))
{
    // Twój kod dalszych kroków znajduje się tutaj
}
```

## Krok 2: Uzyskaj obraz rastrowy

```csharp
// Uzyskaj obraz rastrowy z załadowanego pliku PSD
RasterCachedImage rasterImage = image;
```

## Krok 3: Dostosuj jasność

```csharp
// Ustaw wartość jasności. Przyjmowane wartości jasności mieszczą się w przedziale [-255, 255].
rasterImage.AdjustBrightness(-50);
```

## Krok 4: Zapisz zmodyfikowany obraz

```csharp
// Zapisz zmodyfikowany obraz z dostosowaną jasnością
string destName = dataDir + @"AdjustBrightness_out.tiff";
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
rasterImage.Save(destName, tiffOptions);
```

Teraz, gdy podzieliliśmy przykład na łatwe do wykonania kroki, możesz bezproblemowo zintegrować regulację jasności z projektem .NET za pomocą Aspose.PSD.

## Wniosek

Aspose.PSD dla .NET upraszcza proces wdrażania regulacji jasności w plikach PSD. Postępując zgodnie z powyższym przewodnikiem krok po kroku, możesz bez wysiłku poprawić atrakcyjność wizualną swoich obrazów. Eksperymentuj z różnymi wartościami jasności, aby osiągnąć pożądane rezultaty.

## Często zadawane pytania

### P1: Gdzie mogę znaleźć dokumentację Aspose.PSD dla .NET?

 Odpowiedź 1: Dokumentacja jest dostępna.[Tutaj](https://reference.aspose.com/psd/net/).

### P2: Jak mogę pobrać bibliotekę Aspose.PSD dla .NET?

 O2: Możesz pobrać bibliotekę z[strona wydania](https://releases.aspose.com/psd/net/).

### P3: Czy dostępna jest bezpłatna wersja próbna Aspose.PSD dla .NET?

 Odpowiedź 3: Tak, możesz uzyskać dostęp do bezpłatnego okresu próbnego.[Tutaj](https://releases.aspose.com/).

### P4: Gdzie mogę uzyskać wsparcie dla Aspose.PSD dla .NET?

 A4: Aby uzyskać pomoc, odwiedź stronę[Forum Aspose.PSD](https://forum.aspose.com/c/psd/34).

### P5: Jak uzyskać tymczasową licencję na Aspose.PSD dla .NET?

 Odpowiedź 5: Możesz nabyć licencję tymczasową.[Tutaj](https://purchase.aspose.com/temporary-license/).