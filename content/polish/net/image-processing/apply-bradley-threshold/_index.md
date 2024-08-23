---
title: Stosowanie progu Bradleya w Aspose.PSD dla .NET
linktitle: Stosowanie progu Bradleya
second_title: Aspose.PSD API .NET
description: Ulepsz segmentację obrazu za pomocą Bradley Threshold w Aspose.PSD dla .NET. Przewodnik krok po kroku dotyczący skutecznej binaryzacji.
type: docs
weight: 15
url: /pl/net/image-processing/apply-bradley-threshold/
---
## Wstęp

Witamy w naszym obszernym samouczku na temat stosowania Bradley Threshold w Aspose.PSD dla .NET. Aspose.PSD dla .NET to potężna biblioteka, która umożliwia pracę z plikami Photoshopa w aplikacjach .NET. Bradley Thresholding to technika stosowana do binaryzacji obrazu, pomagająca skutecznie oddzielić obiekty od tła.

W tym samouczku przeprowadzimy Cię przez proces stosowania Bradley Threshold przy użyciu Aspose.PSD dla .NET. Zanim przejdziemy do kolejnych kroków, upewnij się, że masz spełnione niezbędne warunki wstępne.

## Warunki wstępne

Zanim zaczniesz, upewnij się, że masz następującą konfigurację:

-  Biblioteka Aspose.PSD dla .NET: Pobierz i zainstaluj bibliotekę z[Dokumentacja Aspose.PSD dla .NET](https://reference.aspose.com/psd/net/).
- Katalog dokumentów: Utwórz katalog do przechowywania źródłowego pliku PSD i wynikowego obrazu binarnego.

Teraz, gdy masz już przygotowane wymagania wstępne, przejdźmy do przewodnika krok po kroku.

## Importuj przestrzenie nazw

W projekcie .NET pamiętaj o zaimportowaniu wymaganych przestrzeni nazw, aby uzyskać dostęp do funkcjonalności Aspose.PSD:

```csharp
// Importuj przestrzenie nazw Aspose.PSD
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.ImageOptions;
```

## Krok 1: Załaduj zaszumiony obraz

Zdefiniuj ścieżkę do źródłowego pliku PSD i miejsce docelowe binarnego wyjścia:

```csharp
// Ścieżka do katalogu dokumentów.
string dataDir = "Your Document Directory";

string sourceFile = dataDir + @"sample.psd";
string destName = dataDir + @"binarized_out.png";
```

## Krok 2: Binaryzuj obraz za pomocą Bradley Threshold

Załaduj obraz PSD, określ wartość progową, zastosuj próg Bradleya i zapisz wynik jako obraz PNG:

```csharp
// Załaduj obraz
using (PsdImage image = (PsdImage)Image.Load(sourceFile))
{
    //Zdefiniuj wartość progową
    double threshold = 0.15;

    // Wywołaj metodę BinarizeBradley i przekaż wartość progową jako parametr
    image.BinarizeBradley(threshold);

    // Zapisz obraz wyjściowy
    image.Save(destName, new PngOptions());
}
```

## Wniosek

Gratulacje! Pomyślnie zastosowałeś Bradley Threshold w Aspose.PSD dla .NET. Technika ta jest nieoceniona przy poprawie segmentacji obrazu w różnych zastosowaniach.

Zachęcamy do zapoznania się z większą liczbą funkcji i funkcjonalności udostępnianych przez Aspose.PSD dla .NET w celu optymalizacji zadań przetwarzania obrazu.

## Często zadawane pytania

### P1: Czy mogę zastosować próg Bradley Threshold do dowolnego rodzaju obrazu?

Odpowiedź 1: Tak, metoda progowa Bradleya to wszechstronna technika odpowiednia dla różnych typów obrazów.

### P2: Gdzie mogę znaleźć dodatkową dokumentację Aspose.PSD?

 Odpowiedź 2: Patrz[dokumentacja](https://reference.aspose.com/psd/net/) aby uzyskać szczegółowe informacje na temat Aspose.PSD dla .NET.

### P3: Czy dostępny jest bezpłatny okres próbny?

 O3: Tak, możesz skorzystać z bezpłatnej wersji próbnej Aspose.PSD dla .NET[Tutaj](https://releases.aspose.com/).

### P4: Jak mogę uzyskać wsparcie dla Aspose.PSD?

 A4: Odwiedź[Forum Aspose.PSD](https://forum.aspose.com/c/psd/34) za wsparcie społeczności i dyskusje.

### P5: Gdzie mogę kupić licencję na Aspose.PSD?

 Odpowiedź 5: Możesz kupić licencję[Tutaj](https://purchase.aspose.com/buy).