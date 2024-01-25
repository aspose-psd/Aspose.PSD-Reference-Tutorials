---
title: Implementowanie regulacji kontrastu w Aspose.PSD dla .NET
linktitle: Wdrażanie regulacji kontrastu
second_title: Aspose.PSD API .NET
description: Dowiedz się, jak wdrożyć regulację kontrastu w Aspose.PSD dla .NET, korzystając z tego przewodnika krok po kroku.
type: docs
weight: 11
url: /pl/net/image-adjustment/contrast-adjustment/
---
## Wstęp

Witamy w tym kompleksowym przewodniku na temat wdrażania regulacji kontrastu w Aspose.PSD dla .NET! W tym samouczku omówimy proces zwiększania kontrastu obrazu przy użyciu Aspose.PSD, potężnej biblioteki obrazowania .NET. Pod koniec tego przewodnika będziesz mieć solidną wiedzę na temat płynnego stosowania korekcji kontrastu w obrazach.

## Warunki wstępne

Zanim przejdziemy do procesu krok po kroku, upewnij się, że spełnione są następujące wymagania wstępne:

1.  Biblioteka Aspose.PSD dla .NET: Pobierz i zainstaluj bibliotekę Aspose.PSD dla .NET. Możesz znaleźć link do pobrania[Tutaj](https://releases.aspose.com/psd/net/).

2. Katalog dokumentów: skonfiguruj katalog, w którym będą przechowywane pliki źródłowe i docelowe. Zastąp „Twój katalog dokumentów” w dostarczonym kodzie ścieżką do tego katalogu.

Skoro mamy już przygotowane wymagania wstępne, możemy przystąpić do wdrażania.

## Importuj przestrzenie nazw

W tym kroku zaimportujemy niezbędne przestrzenie nazw, aby uzyskać dostęp do funkcjonalności udostępnianych przez bibliotekę Aspose.PSD.

```csharp
using Aspose.PSD.FileFormats.Tiff.Enums;
using Aspose.PSD.ImageOptions;
```

## Krok 1: Załaduj obraz

 Załaduj obraz źródłowy do instancji pliku`RasterImage` klasa.

```csharp
//ExStart: Załaduj obraz
string sourceFile = dataDir + @"sample.psd";
using (var image = Image.Load(sourceFile))
{
    RasterImage rasterImage = (RasterImage)image;
    if (!rasterImage.IsCached)
    {
        rasterImage.CacheData();
    }
    // Przejdź do następnego kroku...
}
//Rozwiń: Załaduj obraz
```

## Krok 2: Dostosuj kontrast

W tym kroku dopasujemy kontrast załadowanego obrazu.

```csharp
//ExStart: Dostosuj kontrast
rasterImage.AdjustContrast(50); // Dostosuj kontrast o 50%
// Przejdź do następnego kroku...
//ExEnd:Dostosuj kontrast
```

## Krok 3: Utwórz opcje TIFF

 Utwórz instancję`TiffOptions` dla powstałego obrazu ustaw różne właściwości i zapisz obraz w formacie TIFF.

```csharp
//ExStart:Utwórz opcjeTiff
string destName = dataDir + @"AdjustContrast_out.tiff";
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.BitsPerSample = new ushort[] { 8, 8, 8 };
tiffOptions.Photometric = TiffPhotometrics.Rgb;
rasterImage.Save(destName, tiffOptions);
//ExEnd: CreateTiffOptions
```

Gratulacje! Pomyślnie zaimplementowałeś regulację kontrastu przy użyciu Aspose.PSD dla .NET.

## Wniosek

tym samouczku zbadaliśmy proces zwiększania kontrastu obrazu za pomocą Aspose.PSD dla .NET. Biblioteka zapewnia prosty sposób manipulowania właściwościami obrazu, umożliwiając programistom łatwe tworzenie atrakcyjnych wizualnie obrazów.

## Często zadawane pytania

### P1: Czy Aspose.PSD dla .NET jest odpowiedni dla początkujących?

O1: Aspose.PSD dla .NET został zaprojektowany tak, aby był przyjazny dla programistów, dzięki czemu jest odpowiedni zarówno dla początkujących, jak i doświadczonych programistów.

### P2: Czy mogę używać Aspose.PSD do projektów komercyjnych?

 O2: Tak, Aspose.PSD dla .NET może być używany w projektach komercyjnych. Aby uzyskać szczegółowe informacje na temat licencji, odwiedź stronę[Tutaj](https://purchase.aspose.com/buy).

### P3: Czy dostępny jest bezpłatny okres próbny?

 O3: Tak, możesz skorzystać z bezpłatnej wersji próbnej Aspose.PSD dla .NET[Tutaj](https://releases.aspose.com/).

### P4: Gdzie mogę znaleźć wsparcie dla Aspose.PSD dla .NET?

 A4: Odwiedź forum wsparcia Aspose.PSD dla .NET[Tutaj](https://forum.aspose.com/c/psd/34) do pomocy.

### P5: Jak mogę uzyskać licencję tymczasową?

 Odpowiedź 5: W razie potrzeby możesz uzyskać licencję tymczasową[Tutaj](https://purchase.aspose.com/temporary-license/).