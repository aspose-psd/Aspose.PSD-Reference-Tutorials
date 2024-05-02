---
title: Przycinanie plików PSD podczas konwersji do formatu PNG w Aspose.PSD dla .NET
linktitle: Przycinanie plików PSD podczas konwersji do formatu PNG
second_title: Aspose.PSD API .NET
description: Dowiedz się, jak bez wysiłku przycinać pliki PSD za pomocą Aspose.PSD dla .NET. Postępuj zgodnie z naszym przewodnikiem krok po kroku, aby uzyskać płynną konwersję do formatu PNG.
type: docs
weight: 18
url: /pl/net/psd-file-manipulation/crop-psd-conversion-png/
---
## Wstęp
W dziedzinie programowania .NET manipulowanie i konwertowanie obrazów jest częstym zadaniem. Aspose.PSD dla .NET zapewnia potężny zestaw narzędzi usprawniających ten proces. Częstym wymaganiem jest przycięcie plików PSD przed ich konwersją do formatu PNG. W tym samouczku krok po kroku zagłębimy się w proces korzystania z Aspose.PSD dla .NET.
## Warunki wstępne
Zanim wyruszymy w tę podróż, upewnijmy się, że posiadamy:
-  Biblioteka Aspose.PSD dla .NET: Pobierz i zainstaluj bibliotekę z[Aspose.PSD dla dokumentacji .NET](https://reference.aspose.com/psd/net/).
- Przykładowy plik PSD: Przygotuj plik PSD do eksperymentowania. Jeśli go nie masz, możesz skorzystać z próbki podanej w samouczku.
- Środowisko .NET: Upewnij się, że masz skonfigurowane działające środowisko programistyczne .NET.
- Katalog dokumentów: Określ ścieżkę do katalogu dokumentów w kodzie.
## Importuj przestrzenie nazw
W projekcie .NET uwzględnij niezbędne przestrzenie nazw dla Aspose.PSD dla .NET:
```csharp
using Aspose.PSD.ImageOptions;
```
## Krok 1: Załaduj obraz PSD
```csharp
// Ścieżka do katalogu dokumentów.
string dataDir = "Your Document Directory";
string srcPath = dataDir + @"sample.psd";
// Załaduj istniejący obraz PSD
using (RasterImage image = (RasterImage)Image.Load(srcPath))
{
    // Twój kod dalszych kroków będzie tutaj
}
```
## Krok 2: Zdefiniuj prostokąt przycinania
```csharp
// Utwórz instancję klasy Rectangle, przekazując x, y, szerokość i wysokość
Rectangle cropRectangle = new Rectangle(0, 0, 350, 450);
```
## Krok 3: Przytnij obraz
```csharp
// Wywołaj metodę kadrowania klasy Image i przekaż instancję klasy prostokąta
image.Crop(cropRectangle);
```
## Krok 4: Określ opcje PNG
```csharp
// Utwórz instancję klasy PngOptions
PngOptions pngOptions = new PngOptions();
```
## Krok 5: Zapisz przycięty obraz jako PNG
```csharp
// Wywołaj metodę save, podaj ścieżkę wyjściową i PngOptions, aby przekonwertować plik PSD na PNG i zapisać wynik
string destName = dataDir + @"export.png";
image.Save(destName, pngOptions);
```
## Wniosek

Gratulacje! Pomyślnie nauczyłeś się, jak przycinać pliki PSD podczas konwertowania ich do formatu PNG za pomocą Aspose.PSD dla .NET. Ta funkcja może być nieoceniona w różnych scenariuszach przetwarzania obrazu.

## Często zadawane pytania

### P1: Czy mogę używać tej biblioteki w projekcie komercyjnym?

 O1: Tak, Aspose.PSD dla .NET jest dostępny do użytku komercyjnego. Odnosić się do[Licencja Aspose.PSD](https://purchase.aspose.com/buy) dla szczegółów.

### P2: Czy dostępny jest bezpłatny okres próbny?

 A2: Absolutnie! Możesz skorzystać z bezpłatnej wersji próbnej[Tutaj](https://releases.aspose.com/).

### P3: Gdzie mogę znaleźć wsparcie dla Aspose.PSD dla .NET?

 A3: Odwiedź[Forum Aspose.PSD](https://forum.aspose.com/c/psd/34) w celu uzyskania pomocy lub pytań.

### P4: Jak uzyskać licencję tymczasową?

 Odpowiedź 4: Jeśli potrzebujesz licencji tymczasowej, możesz ją uzyskać[Tutaj](https://purchase.aspose.com/temporary-license/).

### P5: Czy w dokumentacji dostępne są jakieś przykłady lub samouczki?

 Odpowiedź 5: Tak, można znaleźć obszerną dokumentację i przykłady[Tutaj](https://reference.aspose.com/psd/net/).