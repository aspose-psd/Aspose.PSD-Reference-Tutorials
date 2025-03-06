---
title: Tworzenie metadanych XMP w Aspose.PSD dla .NET
linktitle: Tworzenie metadanych XMP
second_title: Aspose.PSD API .NET
description: Poznaj tworzenie metadanych XMP w Aspose.PSD dla .NET. Popraw organizację obrazu dzięki płynnej manipulacji.
weight: 10
url: /pl/net/file-and-font-handling/create-xmp-metadata/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Tworzenie metadanych XMP w Aspose.PSD dla .NET

## Wstęp

dynamicznym świecie rozwoju .NET precyzyjne manipulowanie obrazami jest kluczowym aspektem wielu aplikacji. W tym samouczku omówiono tworzenie metadanych XMP w Aspose.PSD dla .NET, potężnej bibliotece, która upraszcza zadania przetwarzania obrazów. XMP (Extensible Metadata Platform) umożliwia osadzanie metadanych w plikach obrazów, ułatwiając sprawną organizację i wyszukiwanie informacji związanych z obrazami.

## Warunki wstępne

Zanim przejdziesz do samouczka, upewnij się, że spełniasz następujące wymagania wstępne:

-  Biblioteka Aspose.PSD dla .NET: Pobierz i zainstaluj bibliotekę z[Dokumentacja Aspose.PSD](https://reference.aspose.com/psd/net/).

- Środowisko programistyczne: skonfiguruj środowisko programistyczne .NET za pomocą programu Visual Studio lub preferowanego IDE.

- Podstawowa wiedza na temat platformy .NET: Zapoznaj się z podstawowymi koncepcjami platformy .NET, ponieważ w tym samouczku założono podstawową wiedzę na temat programowania platformy .NET.

## Importuj przestrzenie nazw

W swoim projekcie .NET uwzględnij niezbędne przestrzenie nazw, aby uzyskać dostęp do funkcjonalności Aspose.PSD:

```csharp
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.Xmp;
using Aspose.PSD.Xmp.Schemas.DublinCore;
using Aspose.PSD.Xmp.Schemas.Photoshop;
using System;
using System.IO;
```

Podzielmy teraz proces tworzenia metadanych XMP na serię kompleksowych kroków.

## Krok 1: Określ rozmiar obrazu i prostokąt

```csharp
// Ścieżka do katalogu dokumentów.
string dataDir = RunExamples.GetDataDir_DrawingAndFormattingImages();

//Określ rozmiar obrazu, definiując prostokąt
Rectangle rect = new Rectangle(0, 0, 100, 200);
```

## Krok 2: Utwórz nowy obraz

```csharp
// Utwórz zupełnie nowy obraz do celów przykładowych
using (var image = new PsdImage(rect.Width, rect.Height))
{
    // Tutaj znajduje się kod manipulacji obrazem...
}
```

## Krok 3: Utwórz nagłówek XMP i zwiastun XMP

```csharp
// Utwórz instancję nagłówka XMP
XmpHeaderPi xmpHeader = new XmpHeaderPi(Guid.NewGuid().ToString());

// Utwórz instancję klasy XMP-TrailerPi, XMPmeta, aby ustawić różne atrybuty
XmpTrailerPi xmpTrailer = new XmpTrailerPi(true);
XmpMeta xmpMeta = new XmpMeta();
```

## Krok 4: Ustaw atrybuty XMP

```csharp
// Ustaw atrybuty XMP, na przykład:
xmpMeta.AddAttribute("Author", "Mr Smith");
xmpMeta.AddAttribute("Description", "The fake metadata value");
```

## Krok 5: Utwórz opakowanie pakietów XMP

```csharp
// Utwórz instancję XmpPacketWrapper zawierającą wszystkie metadane
XmpPacketWrapper xmpData = new XmpPacketWrapper(xmpHeader, xmpTrailer, xmpMeta);
```

## Krok 6: Utwórz pakiet Photoshopa i ustaw atrybuty

```csharp
// Utwórz instancję pakietu Photoshop i ustaw atrybuty Photoshopa
PhotoshopPackage photoshopPackage = new PhotoshopPackage();
photoshopPackage.SetCity("London");
photoshopPackage.SetCountry("England");
photoshopPackage.SetColorMode(ColorMode.Rgb);
photoshopPackage.SetCreatedDate(DateTime.UtcNow);
```

## Krok 7: Dodaj pakiet Photoshop do metadanych XMP

```csharp
// Dodaj pakiet Photoshopa do metadanych XMP
xmpData.AddPackage(photoshopPackage);
```

## Krok 8: Utwórz pakiet DublinCore i ustaw atrybuty

```csharp
// Utwórz instancję pakietu DublinCore i ustaw atrybuty dublinCore
DublinCorePackage dublinCorePackage = new DublinCorePackage();
dublinCorePackage.SetAuthor("Mudassir Fayyaz");
dublinCorePackage.SetTitle("Confessions of a Man Insane Enough to Live With the Beasts");
dublinCorePackage.AddValue("dc:movie", "Barfly");
```

## Krok 9: Dodaj pakiet DublinCore do metadanych XMP

```csharp
// Dodaj pakiet dublinCore do metadanych XMP
xmpData.AddPackage(dublinCorePackage);
```

## Krok 10: Zaktualizuj metadane XMP i zapisz obraz

```csharp
using (var ms = new MemoryStream())
{
    // Zaktualizuj metadane XMP do obrazu i zapisz obraz na dysku lub w strumieniu pamięci
    image.XmpData = xmpData;
    image.Save(ms);
    image.Save(dataDir + "ee.psd");
    ms.Seek(0, System.IO.SeekOrigin.Begin);
}
```

## Krok 11: Załaduj obraz i przeczytaj metadane

```csharp
// Załaduj obraz ze strumienia pamięci lub z dysku, aby odczytać/pobrać metadane
using (var img = (PsdImage)Image.Load(ms))
{
    // Pobieranie metadanych XMP
    XmpPacketWrapper imgXmpData = img.XmpData;
    foreach (XmpPackage package in imgXmpData.Packages)
    {
        // Użyj danych pakietu...
    }
}
```

## Wniosek

Gratulacje! Pomyślnie utworzyłeś metadane XMP w Aspose.PSD dla .NET. Ta potężna funkcja zwiększa możliwości przetwarzania obrazu, umożliwiając wydajną organizację i wyszukiwanie ważnych informacji.

## Często zadawane pytania

### P1: Czy Aspose.PSD dla .NET jest kompatybilny ze wszystkimi formatami obrazów?

O1: Aspose.PSD koncentruje się głównie na formacie pliku PSD (Adobe Photoshop), ale obsługuje różne inne formaty.

### P2: Czy mogę manipulować istniejącymi metadanymi XMP przy użyciu Aspose.PSD dla .NET?

O2: Tak, Aspose.PSD umożliwia zarówno odczytywanie, jak i modyfikowanie istniejących metadanych XMP.

### P3: Czy istnieją jakieś ograniczenia dotyczące rozmiaru obrazu podczas korzystania z Aspose.PSD dla .NET?

O3: Aspose.PSD może obsługiwać obrazy o różnych rozmiarach, ale bardzo duże obrazy mogą wymagać dodatkowych rozważań.

### P4: Jak często jest aktualizowany Aspose.PSD dla .NET?

O4: Regularnie wydawane są aktualizacje zapewniające zgodność z najnowszymi wersjami platformy .NET i standardami branżowymi.

### P5: Czy istnieje forum społecznościowe dotyczące wsparcia Aspose.PSD?

 O: Tak, możesz znaleźć wsparcie i dyskusje na temat[Forum Aspose.PSD](https://forum.aspose.com/c/psd/34).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
