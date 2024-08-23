---
title: Implementowanie regulacji gamma w Aspose.PSD dla .NET
linktitle: Wdrażanie regulacji gamma
second_title: Aspose.PSD API .NET
description: Poznaj możliwości Aspose.PSD dla .NET dzięki naszemu przewodnikowi krok po kroku dotyczącemu wdrażania regulacji gamma. Bez wysiłku dostosuj jasność i kontrast obrazu.
type: docs
weight: 12
url: /pl/net/image-adjustment/gamma-adjustment/
---
## Wstęp

Witamy w tym kompleksowym przewodniku na temat wdrażania regulacji gamma w Aspose.PSD dla .NET! Regulacja gamma to kluczowa technika przetwarzania obrazu, która umożliwia precyzyjne dostrojenie jasności i kontrastu obrazu. W tym samouczku przeprowadzimy Cię przez proces, korzystając z potężnej biblioteki Aspose.PSD dla .NET.

## Warunki wstępne

Przed przystąpieniem do wdrożenia upewnij się, że spełnione są następujące wymagania wstępne:

-  Biblioteka Aspose.PSD dla .NET: Upewnij się, że masz zainstalowaną bibliotekę Aspose.PSD dla .NET. Możesz go pobrać[Tutaj](https://releases.aspose.com/psd/net/).

- .NET Framework: W tym samouczku założono, że masz podstawową wiedzę na temat programowania .NET i masz zainstalowany .NET Framework.

- Zintegrowane środowisko programistyczne (IDE): wybierz preferowane środowisko programistyczne .NET, takie jak Visual Studio.

## Importuj przestrzenie nazw

W projekcie .NET rozpocznij od zaimportowania przestrzeni nazw niezbędnych do pracy z Aspose.PSD:

```csharp
using Aspose.PSD.FileFormats.Tiff.Enums;
using Aspose.PSD.ImageOptions;
```

## Krok 1: Skonfiguruj swój projekt

Utwórz nowy projekt .NET w wybranym IDE. Pamiętaj, aby dodać odniesienia do biblioteki Aspose.PSD.

## Krok 2: Zdefiniuj katalog dokumentów

```csharp
string dataDir = "Your Document Directory";
```

## Krok 3: Załaduj obraz

```csharp
string sourceFile = dataDir + @"sample.psd";
using (var image = Image.Load(sourceFile))
{
    // W tym bloku zostaną wykonane dodatkowe kroki.
}
```

## Krok 4: Rzutuj na obraz rastrowy i dane z pamięci podręcznej

```csharp
RasterImage rasterImage = (RasterImage)image;
if (!rasterImage.IsCached)
{
    rasterImage.CacheData();
}
```

## Krok 5: Dostosuj gamma

```csharp
rasterImage.AdjustGamma(2.2f, 2.2f, 2.2f);
```

## Krok 6: Utwórz TiffOptions i zapisz

```csharp
string destName = dataDir + @"AdjustGamma_out.tiff";
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.BitsPerSample = new ushort[] { 8, 8, 8 };
tiffOptions.Photometric = TiffPhotometrics.Rgb;
rasterImage.Save(destName, tiffOptions);
```

## Wniosek

Gratulacje! Pomyślnie zaimplementowałeś regulację gamma przy użyciu Aspose.PSD dla .NET. Ta potężna biblioteka zapewnia solidne możliwości przetwarzania obrazów, co czyni ją cennym narzędziem dla programistów .NET.

## Często zadawane pytania

### P1: Gdzie mogę znaleźć dokumentację Aspose.PSD?

 Odpowiedź 1: Możesz zapoznać się z dokumentacją[Tutaj](https://reference.aspose.com/psd/net/).

### P2: Jak pobrać Aspose.PSD dla .NET?

 Odpowiedź 2: Możesz pobrać bibliotekę[Tutaj](https://releases.aspose.com/psd/net/).

### P3: Czy dostępny jest bezpłatny okres próbny?

 A3: Tak, możesz uzyskać bezpłatną wersję próbną[Tutaj](https://releases.aspose.com/).

### P4: Gdzie mogę uzyskać wsparcie dla Aspose.PSD?

 Odpowiedź 4: Możesz odwiedzić forum pomocy technicznej[Tutaj](https://forum.aspose.com/c/psd/34).

### P5: Czy potrzebuję licencji tymczasowej?

 Odpowiedź 5: W razie potrzeby możesz uzyskać licencję tymczasową[Tutaj](https://purchase.aspose.com/temporary-license/).