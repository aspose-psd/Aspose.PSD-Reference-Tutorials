---
title: Dostosowywanie krycia efektu cienia w Aspose.PSD dla .NET
linktitle: Dostosowywanie krycia efektu cienia
second_title: Aspose.PSD API .NET
description: Dowiedz się, jak dostosować krycie efektu cienia w Aspose.PSD dla .NET, korzystając z tego wszechstronnego samouczka.
type: docs
weight: 15
url: /pl/net/layer-effects/adjusting-shadow-effect-opacity/
---
## Wstęp

Witamy w naszym przewodniku krok po kroku dotyczącym dostosowywania krycia efektu cienia w Aspose.PSD dla .NET! W tym samouczku przeprowadzimy Cię przez proces wykorzystania właściwości Opacity elementu DropShadowEffect. Aspose.PSD dla .NET to potężna biblioteka, która pozwala na płynną pracę z plikami PSD w aplikacjach .NET.

## Warunki wstępne

Zanim przejdziemy do samouczka, upewnij się, że posiadasz następujące elementy:

-  Biblioteka Aspose.PSD dla .NET: Upewnij się, że masz zainstalowaną bibliotekę Aspose.PSD dla .NET w swoim projekcie. Możesz go pobrać[Tutaj](https://releases.aspose.com/psd/net/).

- Katalog dokumentów: skonfiguruj katalog dla wejściowego pliku PSD.

- Katalog wyjściowy: Utwórz katalog, w którym zostaną zapisane powstałe obrazy.

## Importuj przestrzenie nazw

W projekcie .NET pamiętaj o zaimportowaniu niezbędnych przestrzeni nazw:

```csharp
using System;
using System.IO;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers;
using Aspose.PSD.FileFormats.Psd.Layers.LayerEffects;
using Aspose.PSD.ImageOptions;
```

## Krok 1: Załaduj plik PSD

 Rozpocznij od załadowania pliku PSD za pomocą`Image.Load` metoda:

```csharp
string inputFile = Path.Combine(baseDir, "input.psd");
using (PsdImage psdImage = (PsdImage)Image.Load(inputFile, new LoadOptions()))
{
    // Tutaj znajduje się Twój kod do dalszego przetwarzania
}
```

## Krok 2: Uzyskaj dostęp do warstwy i dodaj efekt cienia

Pobierz żądaną warstwę z pliku PSD i dodaj efekt cienia:

```csharp
Layer workLayer = psdImage.Layers[1];
DropShadowEffect dropShadowEffect = workLayer.BlendingOptions.AddDropShadow();
dropShadowEffect.Distance = 0;
dropShadowEffect.Size = 8;
```

## Krok 3: Dostosuj krycie i zapisz obrazy

Teraz dostosuj właściwość krycia i zapisz obrazy z różnymi przezroczystościami:

```csharp
// Przykład z kryciem = 20
dropShadowEffect.Opacity = 20;
psdImage.Save(outputImage20, new PngOptions());

// Przykład z kryciem = 200
dropShadowEffect.Opacity = 200;
psdImage.Save(outputImage200, new PngOptions());
```

## Krok 4: Oczyść

Po zapisaniu obrazów wyczyść pliki tymczasowe:

```csharp
File.Delete(outputImage20);
File.Delete(outputImage200);
```

## Wniosek

Gratulacje! Pomyślnie dostosowałeś krycie efektu cienia w Aspose.PSD dla .NET. Ten samouczek zawiera prosty przewodnik dotyczący ulepszania obrazów PSD przy użyciu różnych stopni krycia cieni.

## Często zadawane pytania

### P1: Czy mogę zastosować ten samouczek do innych formatów obrazów?

O1: Nie, ten samouczek szczegółowo omawia dostosowywanie krycia efektu cienia w plikach PSD przy użyciu Aspose.PSD dla .NET.

### P2: Czy istnieją dodatkowe właściwości cienia, które można modyfikować?

O2: Tak, Aspose.PSD dla .NET oferuje różne właściwości dostrajania efektów cieni.

### P3: Jak mogę uzyskać tymczasową licencję na Aspose.PSD dla .NET?

 A3: Możesz uzyskać licencję tymczasową.[Tutaj](https://purchase.aspose.com/temporary-license/).

### P4: Czy Aspose.PSD dla .NET jest kompatybilny z .NET Core?

O4: Tak, Aspose.PSD dla .NET jest kompatybilny zarówno z .NET Framework, jak i .NET Core.

### P5: Gdzie mogę znaleźć wsparcie społeczności dla Aspose.PSD dla .NET?

 A5: Odwiedź[Fora Aspose.PSD](https://forum.aspose.com/c/psd/34) za wsparcie społeczności i dyskusje.